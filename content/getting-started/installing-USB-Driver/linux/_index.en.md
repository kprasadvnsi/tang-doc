---
title: "Install TD driver on Linux"
date: 2019-02-15T19:21:27+05:30
draft: false
---

## Check for default linux driver

Insert Tang Primer into your computer and execute lsusb to see the information. Make sure USB VID:PID is `0547:1002` as shown in image below.

![lsusb](/getting-started/installing-USB-Driver/linux/images/237929105611360081.jpg "Check for default linux driver.")

## Create a new udev rule file

Set udev rules to enable Tang Primer to be accessed by the plugdev group

Execute the following command in terminal to create a new udev rules file.

```
sudo nano /etc/udev/rules.d/91-anlogic-jtag.rules
```
Copy the following code into text editor and save it, as shown in following image.

```toml
SUBSYSTEMS=="usb", ATTRS{idVendor}=="0547", ATTRS{idProduct}=="1002", \
  GROUP="plugdev", \
  MODE="0660"
```
![udev edit](/getting-started/installing-USB-Driver/linux/images/572316008299057820.jpg "Create a new udev rule file.")

Execute the following command in terminal to restart the udev service.

```
sudo service udev restart
```

## Check if device detected by Tang Dynasty IDE

Go to `<TD installation directory>/bin/` and execute the following command to open TD IDE in GUI mode.

```
./td -gui
```
Click on Download buttion as shown in following image.

![TD GUI Mode](/getting-started/installing-USB-Driver/linux/images/87078310026779781.jpg "Tang Dynasty SDK in GUI Mode.")

Plugin Tang Primer into your computer and hit Refresh buttion on Download Dialog box.

![TD Download Dialog](/getting-started/installing-USB-Driver/linux/images/1823555291194601.jpg "Bitstream Download Dialog")

{{% notice info %}}
Due to some unknown bug, JTAG work only with 400kbps or lower speed.
{{% /notice %}}

Congratulations, you have setup the TD driver on Linux.
