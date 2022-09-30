<!--
 Copyright (c) 2022 Innodisk crop.
 
 This software is released under the MIT License.
 https://opensource.org/licenses/MIT
-->
# Table of Contents
- [Table of Contents](#table-of-contents)
- [What you will need](#what-you-will-need)
  - [Hardware](#hardware)
  - [Software](#software)
- [Setting up the SD Card Image](#setting-up-the-sd-card-image)
- [Connect your X261](#connect-your-x261)
- [Booting your X261](#booting-your-x261)
- [Next Steps](#next-steps)

# What you will need
## Hardware
- X261-SOM Board  
![X261-som-board](fig/X261-som-board.png)  
- X261-Carrier Board
![X261-carrier-board-all](fig/X261-carrier-board-all.png) 
- (optional) A Debug Board: You can use it to communicate with the host through uart
![debug-board](fig/debug-board.jpg)
- A Power Supply
![power-supply](fig/power.png)
- A MicroSD Card: Please prepare a microSD card of 16GB or more  
![microsd-card](fig/microsd-card.jpg)
## Software
- OS Image(Ubuntu), you can contact james_chen@innodisk.com, then you can refer to the "Setting up the SD Card Image" section for first boot.

# Setting up the SD Card Image
You will need a computer to prepare the system for use on X261. Here we will introduce writing the system to the microSD card, and then no matter whether the operating system you are using is Windows or Linux, you can use the following flow normally.
1. Download the `X261 WIC Image`(please contact james_chen@innodisk.com) to your computer.
2. Flash the image file to the microSD card according to the following instructions:
   1. Download and launch [Etcher](https://www.balena.io/etcher/).
   2. Select the image file to use(If you don't have any WIC Image, you can download it [here](fig/balena-01.png)).  
   ![balena-01](fig/balena-01.png)
   1. Please insert the microSD card into your computer, then select the microSD Card to use.  
   ![balena-03](fig/balena-03.png)  
   1. After clicking “Flash!”, it will take about 10-20 minutes.  
   ![balena-05](fig/balena-05.png)  
   1. Done!  
   ![balena-06](fig/balena-06.png)  
   1. Finally, please safely remove your SD card.  
# Connect your X261  
1. Insert the microSD card containing the X261 image in the microSD card slot.  
![connect-01](fig/connect-01.png)  
2. (optional) If you want to transfer x261 information via uart, please use debug board.  
![connect-02](fig/connect-02.png)  
3. (optional) If you want to display X261 information through the screen, please plug in the HDMI cable.  
![connect-03](fig/connect-03.png)  
4. Finally, system boot immediately after plugging in the Power Supply.  
![connect-04](fig/connect-04.png)   
# Booting your X261
Please refer to [Xilinx Website](https://www.xilinx.com/products/som/kria/kv260-vision-starter-kit/kv260-getting-started/booting-your-starter-kit.html)
# Next Steps
After booting into the system successfully, you can refer to [this](../1.Hardware/hardware.md) for more detail. Or you can run some of the examples we provide on the X261:
- [dpu-sc](../2.Software/dpu-sc.md): dpu-sc is a sample code that uses DPU instead of GPU for AI inference.
- [stesting-sc](../2.Software/stesting-sc.md): stesting-sc provide the board IO self testing, some of the io test required jigs.
- [VVAS](../2.Software/VVAS.md): VVAS(Vitis Video Analytics SDK) contains plugin developed by xilinx based on gstreamer. It can use hardware IP to accelerate image processing and AI inference in gstreamer.