
### Chat with Tridge:

It is clearly visible in some logs:
![[Pasted image 20231106153034.png]]

We need to provide location for the EKF to be happy. Provide a parameter for backup location.

![[Pasted image 20231107205942.png]]

We need to deal with magnetic interference, tuning for all motors needs to me implemented

We can try decreasing the MAG NSE parameters, or gates, to rely heavier on compass than Gyros
## The proposed solution

Create HOME_LAT and HOME_LON parameters in ArduSub.

[WIP branch](https://github.com/ArduPilot/ardupilot/compare/master...Williangalvani:ardupilot:default_origin?expand=1)


## New solution:
[allow estimating earth frame fields with no gps](https://github.com/ArduPilot/ardupilot/compare/master...Williangalvani:ardupilot:allow_mag_estimation?expand=1)

https://github.com/ArduPilot/ardupilot/compare/master...Williangalvani:ardupilot:sub-sideways?expand=1

These are apparently already use in AP_Beacon.

this is apparently easily doable with a script, which should help diagnosing



from devcall:

line 669 or NAVEKF control

check logs, look if z gyro bias is updating

this is on old drifting logs


make an autotest. disable gps test
add z gyro bias 



other notes:
  - WMM is only populated if Compass Scale is set (full gps-enabled calibration)
  - WMM is only populated if AUTO_DEC is on
  - let's try INS_GYR_CAL set to 0 (NEVER)




Debbugin session started at june 10th:

let's keep track of my train of toughts.
	- I made a test for GBIAS and GBIAS estimation. works fine in SITL
	- GBIAS_P_NSE is limited in code to 0.5
	- 
