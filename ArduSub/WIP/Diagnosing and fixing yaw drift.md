
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
