---
title: "Getting to Blinky"
date: 2019-02-15T19:23:03+05:30
draft: true
---

Blinky example is good way to test the setup. Following example will blink the Tang's onboard RGB LED.

Get blinky example code from github.com 

```
git clone https://github.com/Lichee-Pi/Tang_FPGA_Examples

```
{{% notice tip %}}
You will need [**git**](https://git-scm.com/) for above command to work.
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

Click on **Run** Icon to start compilation process.

![Start Compilation](/getting-started/Getting-to-Blinky/images/c.png "Start Compilation")

If compilation successful you will see the Console log as shown in picture below.

![Console log](/getting-started/Getting-to-Blinky/images/d.png "Console log")

## Download Bitstrean to Lichee Tang.

Plug in you Lichee Tang board to USB and click on **Download** icon to open Download Dialog. 

![Open Download box](/getting-started/Getting-to-Blinky/images/d1.jpg "Open Download box")

Make sure your device detacted by TD IDE. Add generated bitstream file by clicking on **Add** button.

![Open Bitstream](/getting-started/Getting-to-Blinky/images/e.png "Open Bitstream")

{{% notice tip %}}
If you can't see your device, try refreshing it by chicking on **Refresh** button.
{{% /notice %}}

Select the Bitstream file **Tang_FPGA_Examples/0.LED/prj/led.bit** in Open Dialog.

![Open Bitstream dialog](/getting-started/Getting-to-Blinky/images/f.png "Open Bitstream dialog")

Click on **Run** button to start Download process.

![start download](/getting-started/Getting-to-Blinky/images/g.png "start download")

{{% notice info %}}
Due to some unknown bug, JTAG work only with 400kbps or lower speed on Linux.
{{% /notice %}}

Wait for Download progress to reach 100%.

![Downlod progress](/getting-started/Getting-to-Blinky/images/h.png "Downlod progress")