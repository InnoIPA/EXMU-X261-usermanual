<!--
 Copyright (c) 2023 innodisk Crop.
 
 This software is released under the MIT License.
 https://opensource.org/licenses/MIT
-->

# TOC
- [TOC](#toc)
- [Overview](#overview)
- [Choverlay](#choverlay)
- [Chboot](#chboot)

# Overview
This page introduce the simple utilities on EXMU-X261 that enhance the user expericence. 


# Choverlay
- Choverlay is a simple utility that based on shell script, it can change the default loadapp of during the boot process.
- Help:
    ```bash
    xilinx-k26-som-20221:/home/petalinux$ sudo choverlay 
    [CHOVERLAY] No arguments supplied, following overlays are currently avalible.

            app-x261-aibox
            app-x261-bsp
    ```
- Usage:
    ```bash
    sudo choverlay <name-of-overlay-app>
    ```
- Result:
![choverlay](fig/choverlay.png)
# Chboot
- Chboot is a simple utility that based on shell script, it can change the default boot partition between external SDcard and EMMC which on som board.
- Help:
    ```bash
    xilinx-k26-som-20221:~$ sudo chboot                              
    [CHBOOT] Current bootcmd :
    bootcmd=setenv boot_targets mmc1 && run distro_bootcmd; setenv boot_targets mmc0 && run distro_bootcmd
    [CHBOOT] Help function of chboot.
    chboot is a simple tool to change the boot partition by setting the u-boot varible.
    Following arguments are avalible.
    /usr/bin/chboot sdcard
    /usr/bin/chboot emmc
    /usr/bin/chboot sdcard emmc
    /usr/bin/chboot emmc sdcard
    ```
- Usage:  
    Change boot partition into EMMC, if failed boot from SDcard.
    ```bash
    sudo choverlay emmc sdcard
    ```
- Result:
![chboot](fig/chboot.png)
