# PS3 FreeBSD ISO

This repository provides image files to help you run FreeBSD on your PlayStation 3. This is very exprimental project.

yes,almost trash as you excepted lol :)

## Getting Started
First, you'll need to mod an older PS3 model that's compatible with CFW. Check out [here](https://consolemods.org/wiki/PS3:Getting_Started) , I recommend EVILNAT.
Visit the [Releases page](https://github.com/LowPla3329/ps3-freebsd-iso/releases) to download the latest ISO and related files.

## Important Note
**First, you MUST install the storage initializer package, otherwise release-003 and newer releases will not boot!**
It can be downloaded from this release page.
If the FreeBSD environment is broken(or if you executed rm -rf / lol), delete the FreeBSD save file from the XMB game data utility.

## Guide
1. Resize the VFLASH from the OtherOS tools in the Custom Firmware menu.
2. then download dtbimage from this repository, place it in the root of your USB flash drive, and install Petitboot.
3. You need a DVD-R or RW. ImgBurn is the recommended burning software. burn ISO image to DVD. CD will also works on some builds.
4. Boot OtherOS and exit to the terminal and enter the following command: Make sure the DVD is inserted at this point.
```
# kexec -l /tmp/petitboot/mnt/sr0/boot/kernel/kernel
```
After entering the command, press Ctrl+Alt+Del to restart the console.
5. After a while, the mountroot prompt will appear. Enter the following command to mount the root file system:
  ```
  mountroot> cd9660:iso9660/bsd
  ```
6. Yay! Enjoy BSD World!

## Contents

- `dtbImage.ps3.bin`: Petitboot Binary file.
- `PS3_FreeBSD_Storage_Initializer-v0.1.0_by_Low_Plankton_3329.pkg`: a small savefile that allows FreeBSD to access the PS3's HDD.

## Restrictions
- Only works on a single core, so 7/8 of PS3 powers are wasted.
- 100MB of free RAM.
- No wifi/bluetooth.
- Only support 1920x1080 display.
- The mouse has big glitches.
