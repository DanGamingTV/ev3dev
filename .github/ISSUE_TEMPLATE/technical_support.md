---
name: Technical Support
about: I need techical support for ev3dev because something is not working right
title: 'Cannot connect to Wi-Fi with Edimax EW-7811Un'
labels: question
assignees: ''

---

**What are you trying to do?**

I am trying to connect to my home wifi network.

**What did you expect to happen**

The EV3 should have connected to my Wi-Fi network through the plugged in Wi-Fi dongle.

**What actually happened**

The program didn't connect at all.
I tried connecting through the EV3 brick directly, and I get an error along the lines of "GDBus.error:net.connman..."

**Source Code**

Here is the program I am trying to run.

```
robot@ev3dev:~$ connmanctl
Error getting VPN connections: The name net.connman.vpn was not provided by any connmanctl> enable wifi
Error wifi: Already enabled
connmanctl> scan wifi
Scan completed for wifi
connmanctl> services
*AO Wired                gadget_2216535bcfa7_usb
    (my wifi network)            wifi_thing_managed_psk
connmanctl> agent on
Agent registered
connmanctl> connect wifi_thing_managed_psk
Agent RequestInput wifi_thing_managed_psk
  Passphrase = [ Type=psk, Requirement=mandatory ]
Passphrase? **********
(nothing happens for a long time)
connmanctl> connect wifi_thing_managed_psk
Error /net/connman/service/wifi_thing_managed_psk: In progress
Error /net/connman/service/wifi_thing_managed_psk: Did not receive a reply. Possible causes include: the remote application did not send a reply, the message bus security policy blocked the reply, the reply timeout expired, or the network connection was broken.
```

**Desktop (please complete the following information):**
 - OS and version: [Windows 10 1909]
 - Connection Type: [USB]
 - Software: [PuTTY]

**Robot (please complete the following information):**
 - Device: [EV3]
 - Versions: [Linux ev3dev 4.14.117-ev3dev-2.3.5-ev3 #1 PREEMPT Sat Mar 7 12:54:39 CST 2020 armv5tejl]

```
Image file:         ev3dev-stretch-ev3-generic-2020-04-10
Kernel version:     4.14.117-ev3dev-2.3.5-ev3
Brickman:           0.10.3
BogoMIPS:           148.88
Bluetooth:
Board:              board0
BOARD_INFO_HW_REV=7
BOARD_INFO_MODEL=LEGO MINDSTORMS EV3
BOARD_INFO_ROM_REV=6
BOARD_INFO_SERIAL_NUM=0016535BCFA7
BOARD_INFO_TYPE=main
```


**Background Information**
<!-- Explaining the bigger picture helps give context to the problem -->

I am trying to ... because I want to build a robot that ...
