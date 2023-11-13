
Clydes suggested params don't seem to work well with no gps:
https://github.com/bluerobotics/BlueOS-Water-Linked-DVL/issues/35#issue-1938971715


This script seems to work. but the EKF is ALWAYS consuming the gps.

```

local PARAM_TABLE_KEY = 120
local PARAM_TABLE_PREFIX = 'DVL_'

local GPS_THRESHOLD = 0.5

local ek3_src1_posxy = param:get('EK3_SRC1_POSXY')
local ek3_src1_velxy = param:get('EK3_SRC1_VELXY')
local ek3_src1_posz = param:get('EK3_SRC1_POSZ')
local ek3_src1_velz = param:get('EK3_SRC1_VELZ')

-- TODO: do not change this, just alert the user
ek3_src1_posxy = 6
ek3_src1_velxy = 6
ek3_src1_posz = 1
ek3_src1_velz = 0

local ek3_src2_posxy = param:get('EK3_SRC1_POSXY')
local ek3_src2_velxy = param:get('EK3_SRC1_VELXY')
local ek3_src2_posz = param:get('EK3_SRC1_POSZ')
local ek3_src2_velz = param:get('EK3_SRC1_VELZ')

-- TODO: do not change this, just alert the user
ek3_src2_posxy = 3
ek3_src2_velxy = 3
ek3_src2_posz = 1
ek3_src2_velz = 0



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
  if gps_speed_accuracy < GPS_THRESHOLD then
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