
[GPHDT and GPTHS are supported ](https://github.com/ArduPilot/ardupilot/blob/master/libraries/AP_GPS/AP_GPS_NMEA.cpp#L378-L379)

in order to use it (in Simulation):

```
EK3_SRC1_YAW 2
GPS_TYPE 5
SIM_GPS_TYPE 5
```

Does it work with GPHDT alone? I don't think so. The GPS will not be considered "Healthy" in order for it to be consumed.


[autotest PR with GPS that provides GPHDT](https://github.com/ArduPilot/ardupilot/compare/master...Williangalvani:ardupilot:gps_yaw?expand=1)


To test it with BlueOS and Navigator:
```
SERIAL2_PROTOCOL to GPS
GPS_TYPE to NMEA

```
![[Pasted image 20231129111657.png]]