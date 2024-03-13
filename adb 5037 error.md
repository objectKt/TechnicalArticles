```
user@BEANZCAR release % lsof -i tcp:5037
COMMAND  PID  USER   FD   TYPE             DEVICE SIZE/OFF NODE NAME
adb     3772 user    9u  IPv4 0x9dae8b23ec644fe7      0t0  TCP localhost:5037 (LISTEN)
user@BEANZCAR release % kill 3772
user@BEANZCAR release % lsof -i tcp:5037
user@BEANZCAR release % adb devices
* daemon not running; starting now at tcp:5037
* daemon started successfully
List of devices attached

user@BEANZCAR release % adb connect 192.168.8.21
already connected to 192.168.8.21:5555
user@BEANZCAR release % 
```
