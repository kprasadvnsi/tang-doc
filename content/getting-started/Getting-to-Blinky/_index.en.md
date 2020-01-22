---
title: "Getting to Blinky"
date: 2019-02-15T19:23:03+05:30
draft: false
---

The Blinky example is good way to test the setup. The following example will blink the Tang Primer's onboard RGB LED.

Get the blinky example code from github.com 

```
git clone https://github.com/Lichee-Pi/Tang_FPGA_Examples

```
{{% notice tip %}}
You will need [**git**](https://git-scm.com/) for the above command to work.
{{% /notice %}}

Run TD IDE in GUI mode

```
$ td -gui
```

## Open the Blinky example.

In the Menubar goto **Project -> Open Project** or use the shortcut key **Ctrl+Alt+O**.

![Open project](/getting-started/Getting-to-Blinky/images/a.png "Open project")

Select the Project file **Tang_FPGA_Examples/0.LED/prj/led.al** in Open Dialog.

![Open project dialog](/getting-started/Getting-to-Blinky/images/b.png "Open project dialog")

## Generate the Bitstream file.

Click on the **Run** icon to start the compilation process.

![Start Compilation](/getting-started/Getting-to-Blinky/images/c.png "Start Compilation")

If the compilation is successful you will see the Console log as shown in picture below.

![Console log](/getting-started/Getting-to-Blinky/images/d.png "Console log")

## Download Bitstrean to Tang Primer.

Plug in your Tang Primer board to USB and click on **Download** icon to open the Download dialog. 

![Open Download box](/getting-started/Getting-to-Blinky/images/d1.jpg "Open Download box")

Make sure your device detacted by TD IDE. Add generated bitstream file by clicking on **Add** button.

![Open Bitstream](/getting-started/Getting-to-Blinky/images/e.png "Open Bitstream")

{{% notice tip %}}
If you can't see your device, try refreshing it by clicking on the **Refresh** button.
{{% /notice %}}

Select the Bitstream file **Tang_FPGA_Examples/0.LED/prj/led.bit** in the Downloading & Programming dialog, then click the **Open** button. (You may also double-click on **led.bit** to automatically open it.)

![Open Bitstream dialog](/getting-started/Getting-to-Blinky/images/f.png "Open Bitstream dialog")

Click on the **Run** button to start the download process.

![Start download](/getting-started/Getting-to-Blinky/images/g.png "Start download")

{{% notice info %}}
Due to some unknown bug, JTAG only works with 400kbps or lower speed on Linux.
{{% /notice %}}

Wait for Download progress to reach 100%.

![Download progress](/getting-started/Getting-to-Blinky/images/h.png "Download progress")
