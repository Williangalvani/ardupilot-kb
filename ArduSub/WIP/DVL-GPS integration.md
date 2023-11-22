
Clydes suggested params don't seem to work well with no gps:
https://github.com/bluerobotics/BlueOS-Water-Linked-DVL/issues/35#issue-1938971715


This script seems to work, needs some more testing and validation. I'll try it in open water soon.

```
-- This scripts handles switching between surface GPS and DVL.
-- It creates a parameter DVL_GPS_THR, which is the maximum gps_speed_accuracy
-- we accept from the GPS to use it as a source.
-- As soon as the GPS accuracy is above that value, we switch back to using the DVL
-- As the DVL is much noisier than the DVL, our positioning error is that of the GPS position
-- plus the eventual DVL drift
-- Tested on Sub 4.5-dev as of Nov 22 2023

local PARAM_TABLE_KEY = 90
local PARAM_TABLE_PREFIX = 'DVL_'

gcs:send_text(3, "Starting DVL/GPS integration")

-- bind a parameter to a variable
function bind_param(name)
   local p = Parameter()
   assert(p:init(name), string.format('could not find %s parameter', name))
   return p
end

-- add a parameter and bind it to a variable
function bind_add_param(name, idx, default_value)
   assert(param:add_param(PARAM_TABLE_KEY, idx, name, default_value), string.format('could not add param %s', name))
   return bind_param(PARAM_TABLE_PREFIX .. name)
end

assert(param:add_table(PARAM_TABLE_KEY, PARAM_TABLE_PREFIX, 32), 'could not add param table')

local gps_threshold = bind_add_param('GPS_THR', 1, 0.5)

-- Setup ekf sources
local ek3_src1_posxy = bind_param('EK3_SRC1_POSXY')
local ek3_src1_velxy = bind_param('EK3_SRC1_VELXY')
local ek3_src1_posz = bind_param('EK3_SRC1_POSZ')
local ek3_src1_velz = bind_param('EK3_SRC1_VELZ')

-- TODO: do not change this, just alert the user
ek3_src1_posxy:set(6)
ek3_src1_velxy:set(6)
ek3_src1_posz:set(1)
ek3_src1_velz:set(0)

local ek3_src2_posxy = bind_param('EK3_SRC2_POSXY')
local ek3_src2_velxy = bind_param('EK3_SRC2_VELXY')
local ek3_src2_posz = bind_param('EK3_SRC2_POSZ')
local ek3_src2_velz = bind_param('EK3_SRC2_VELZ')

-- TODO: do not change this, just alert the user
ek3_src2_posxy:set(3)
ek3_src2_velxy:set(6) -- not 100% sure of this one
ek3_src2_posz:set(1)
ek3_src2_velz:set(0)

local options = bind_param('EK3_SRC_OPTIONS')
options:set(0)


-- the main update function
function update()
  local gps_speed_accuracy = gps:speed_accuracy(gps:primary_sensor())
  if gps_speed_accuracy == nil then
    gcs:send_named_float('GpsSpeed', 10000)
    return update, 100
  else
    gcs:send_named_float('GpsSpeed', gps_speed_accuracy)
  end
  local wanted_source = 0
  if gps_speed_accuracy < gps_threshold:get() then
    wanted_source = 1
    if not ahrs:get_origin() then
        ahrs:set_origin(ahrs:get_location())
    end
  else
    wanted_source = 0
  end
  if ahrs:get_posvelyaw_source_set() ~= wanted_source then
    ahrs:set_posvelyaw_source_set(wanted_source)
  end
  gcs:send_named_float('EkfSource', ahrs:get_posvelyaw_source_set())
  return update, 100
end

return update()
```

### NEXT:

 - [ ] Improve the SITL GPS so it can properly simulate being underwater
 - [ ] Write an autotest test for this script/feature