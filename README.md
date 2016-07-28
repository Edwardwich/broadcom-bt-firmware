# Broadcom Bluetooth firmware for Linux kernel

## Overview
This package intentended to provide firmware of Broadcom WIDCOMM® Bluetooth devices (including BCM20702, BCM20703, BCM43142 chipsets and other) for Linux kernel. This firmware comes from official driver package, which can be [downloaded here](http://www.broadcom.com/support/bluetooth).

## Detection and Installation

When you inserting Broadcom Bluetooth device you prefered Linux distribution may not load it properly:

```
Bluetooth: hci1: BCM: chip id 63
Bluetooth: hci1: BCM20702A
Bluetooth: hci1: BCM20702A1 (001.002.014) build 0000
bluetooth hci1: Direct firmware load for brcm/BCM20702A1-0b05-17cb.hcd failed with error -2
Bluetooth: hci1: BCM: Patch brcm/BCM20702A1-0b05-17cb.hcd not found
```

As you can see, you need `brcm/BCM20702A1-0b05-17cb.hcd` firmware.

Place required `.hcd` file to `/lib/firmware/brcm`. After inserting Broadcom Bluetooth device you will see that firmware successfully loaded:

```
Bluetooth: hci1: BCM: chip id 63
Bluetooth: hci1: BCM20702A
Bluetooth: hci1: BCM20702A1 (001.002.014) build 0000
Bluetooth: hci1: BCM20702A1 (001.002.014) build 1467
Bluetooth: hci1: Broadcom Bluetooth Device
```

Congratulations, now your bluetooth device successfully loaded. Now go to Bluez for futher configuration.

## Supported devices

See DEVICES.md file.