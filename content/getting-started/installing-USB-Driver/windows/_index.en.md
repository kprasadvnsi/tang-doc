---
title: "Install TD driver on Windows"
date: 2019-02-15T19:21:19+05:30
draft: false
---

## Check for default windows driver

Insert Tang Primer into your computer and open Device Manager to see the information. Make sure USB VID:PID is `0547:1002`.

![device manager](/getting-started/installing-USB-Driver/windows/images/no_driver.png "Check for default windows driver.")

## Install drivers

Double click on `WinUsb Device` to select update driver

![update driver 1](/getting-started/installing-USB-Driver/windows/images/update_driver1.png "Update driver step 1")

![update driver 2](/getting-started/installing-USB-Driver/windows/images/update_driver2.png "Update driver step 2")

Browse the folder and select the driver directory under the `TD installation directory`. Click OK to start the installation.

![Choose driver folder](/getting-started/installing-USB-Driver/windows/images/choosefolder.png "Choose driver folder")

The installation is successful and can be seen in the device manager.

![Install success](/getting-started/installing-USB-Driver/windows/images/installsuccess.png "Install success")

## Check if device detacted by Tang Dynasty IDE

Click on Download buttion as shown in following image.

![TD GUI Mode](/getting-started/installing-USB-Driver/linux/images/87078310026779781.jpg "Tang Dynasty SDK in GUI Mode.")

Plugin Tang Primer into your computer and hit Refresh buttion on Download Dialog box.

![TD Download Dialog](/getting-started/installing-USB-Driver/linux/images/1823555291194601.jpg "Bitstream Download Dialog")

Congratulations, you have setup the TD driver on Windows.
