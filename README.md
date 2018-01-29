# resin-scripts
Scripts with tricks with Resin.io on a Raspberry-Pi3 


### startscan
This is a shell script to call a python script that executes a BLE scan using the bluetooth stack.

The "wait for modem" trick is a workaround to get the modem to connect - it won't connect on boot if the BLE scanner script starts too early. 

Note: on pre-ResinOS 2.9.6 versions I needed to use another trick to attach the bluetooth interface:

```
 /usr/bin/hciattach /dev/ttyAMA0 bcm43xx 921600 noflow -
```

But this is not necessary anymore. (Tested with ResinOS 2.9.6 on RaspberryPi 3).

