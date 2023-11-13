
[available on master](https://github.com/ArduPilot/mavlink/blob/dccd8555cd601467dc793ea9abf85caa63c0a9e8/message_definitions/v1.0/common.xml#L5579)

can it be used with no actual coordinates? [Nope, coordinates are always consumed](https://github.com/ArduPilot/ardupilot/blob/master/libraries/AP_GPS/AP_GPS_MAV.cpp#L64-L66)
