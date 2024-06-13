
You need to switch to BlueOS master version in order to do some of these things.



## Install Python 3.12.2

ADD IT TO PATH!

python3 -m pip install --upgrade pygpsclient
pygpsclient

## SWitch the boat to a BlueOS version newer than 1.2.2


## Set some parameters:

GPS_AUTOCONFIG to 0

REMOVE SERIAL5 from autopilot serial ports

use screen to find the gps baudrate

setup a new bridge as server, on ttyAMA3 (SERIAL5) 




Notes: UPDATING from 1.1 to master and bridges would not work.

