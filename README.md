# Linux tool for the Pictek Thunderbird mouse.
## About
Tool to adjust the LED color and mode of the Picktek Thunderbird mouse for Linux.
## DISCLAIMER
This program requires root unless you setup the following udev rule under /etc/udev/rules.d/50-Thunderbird.rules
```
SUBSYSTEMS=="usb", ATTRS{idVendor}=="258a", ATTRS{idProduct}=="1007", GROUP="plugdev", MODE="666"
```
## Usage
```
./thunderbird.py [OPTIONS] BRIGHTNESS
```
For example to set the led to solid blue:
```
./thunderbird.py --solid --profile 0 --rgb 0 0 255 9
```
or to set the led to neon:
```
./thunderbird.py -n 9
```
## Options
```
-n    Neon mode
-b    Breath mode
-s    Solid mode
```

## Requirements
* Python2.7 and up
* Pyusb
