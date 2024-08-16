<!--
 Copyright (c) 2022 Innodisk crop.
 
 This software is released under the MIT License.
 https://opensource.org/licenses/MIT
-->
# TOC
- [Summary](#summary)
- [What you will need](#what-you-will-need)
  - [Hardware](#hardware)
  - [Software](#software)
- [Connect your X261](#connect-your-x261)
- [Booting your X261](#booting-your-x261)
- [Next Steps](#next-steps)

# Summary
Innodisk's FPGA product line currently has two versions: EXMU-X261 and EXOU-X261. The EXMU-X261 is a board-level product developed based on AMD Xilinx Kria K26 SOM, which includes the K26 SOM and a dedicated carrier board. The EXOU-X261 is a system product based on the EXMU-X261, with an optimized thermal solution and enclosure. Please refer to the table below for more details.

Model |	P/N | Description | Packing List
--- | --- | --- | ---
EXMU-X261 | EXMU-X261-00A1-C1 | FPGA Machine Vision Solution Kit, 0~70°C | AMD Kria K26-C SOM x1 <br/>EXMU-X261 Carrier Board x1Debug Board x1 <br/>Custom USB Type C to Type C Cable x1USB Type A to Micro USB Cable x1 <br/>Heatsink with Fan x1
EXMU-X261	| EXMU-X261-00A1-W1	| FPGA Machine Vision Solution Kit, -40~85°C | AMD Kria K26-I SOM x1 <br/>EXMU-X261 Carrier Board x1Debug Board x1 <br/>Custom USB Type C to Type C Cable x1 <br/>USB Type A to Micro USB Cable x1 <br/>Heatsink with Fan x1
EXOU-X261	| EXOU-X261-00A1-S1 | FPGA Machine Vision Box, 0~50°C | AMD Kria K26-C SOM x1 <br/>EXOU-X261 Machine Vision Box x1 <br/>Debug Board x1 <br/>Custom USB Type C to Type C Cable x1 <br/>USB Type A to Micro USB Cable x1 <br/>60W Power Adapter x1US Power Cord x1
EXOU-X261	| EXOU-X261-00A1-E1 | FPGA Machine Vision Box, -30~70°C | AMD Kria K26-I SOM x1 <br/>EXOU-X261 Machine Vision Box x1 <br/>Debug Board x1 <br/>Custom USB Type C to Type C Cable x1 <br/>USB Type A to Micro USB Cable x1 <br/>60W Power Adapter x1US Power Cord x1

# What you will need
## Hardware
- EXMU-X261.
![x261-io](fig/x261-io.png)

- Or EXOU-X261.
![SBC](fig/SBC.png) 

- A Debug Board: You can use it to communicate with the host through UART.
![debug-board](fig/debug-board.jpg)
- A Power Supply: Please prepare a power adapter of at least 12V 3A or higher

## Software
**Our FPGA device has preloaded an image in eMMC during manufacturing.** Once you have access to the platform, you can start using it right away.

By default, the boot sequence is set to boot from the SD card then eMMC. Therefore, if no SD card is inserted, the device will automatically boot into the system stored in the eMMC. If needed to change the boot sequence, please refer to the [chboot tool](../2.Software/utilities-intro.md#chboot).

# Connect your FPGA device
1. You can use the FPGA device in two ways. First, similar to operating a PC, you can connect a keyboard, mouse, and a monitor via an HDMI cable. Alternatively, you can connect the FPGA device to your main system using the debug board included with the FPGA product and communicate with the FPGA device through a terminal.
![connect-x261](fig/connect-x261.png)
  > With debug board, will need to install the [FTDI driver](../4.FAQ/FAQ.md#driver-of-debug-board) on the host. The UART's bitrate of 115200 and settings of 8 data bits, no parity, 1 stop bit, and no flow control.

2. Please first connect the keyboard, mouse, HDMI cable, and debug board (if needed). Finally, connect the power adapter, and the FPGA device will automatically power on and boot into the OS.
![connect-dc](fig/connect-dc.png)

> If you use EXOUX-261, the Connecting diagram as following.
![connect-sbc](fig/SBC-connect.png)

# Boot up the system
1. After the system boots into the OS, you will see a prompt asking the user to enter a username. Please enter the default username: **petalinux**
2. Next, will see a prompt to enter a **new password**. Please set a new password, and be sure to store it for future use. If you need to change the password, please refer the [How to reset the password?](../4.FAQ/FAQ.md#how-to-reset-the-device-password)

> Refer to [check-system](./check-system.md) topic to check the system status.


# Next Steps
Next, you can operate the system just like any other embedded Linux, or refer to the [PetaLinux tool](https://www.xilinx.com/products/design-tools/embedded-software/petalinux-sdk.html#tools) or [hardware configuration](../1.Hardware/hardware.md) for more details. If you want to quickly run some demos, you can download the following images, flash them to an SD card, and run various demo examples on the FPGA device.
- [pre-build-image](../0.Getting-Started/pre-build-image.md): use pre-built image to intuitively experience the potency of employing AI solutions on the platform.
- [dpu-sc](../2.Software/dpu-sc.md): dpu-sc is a sample code that uses DPU instead of GPU for AI inference.
- [stesting-sc](../2.Software/stesting-sc.md): stesting-sc provide the board IO self testing, some of the io test required jigs.