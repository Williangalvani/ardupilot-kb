
### Chat with Tridge:

It is clearly visible in some logs:
![[Pasted image 20231106153034.png]]

We need to provide location for the ekf to be happy. Provide a parameter for backup location.

compass bug?
![[Pasted image 20231107205942.png]]

we need to deal with magnetic interference, tuning for all motors needs to me implemented

try decreasing the MAG NSE parameters, or gates


### Investigations:

MMC5883 driver has issues?

![[Pasted image 20231108111654.png]]

## The proposed solution

Create HOME_LAT and HOME_LON parameters in ArduSub.

[WIP](https://github.com/ArduPilot/ardupilot/compare/master...Williangalvani:ardupilot:default_origin?expand=1)

