# PS3 FreeBSD ISO

This repository provides image files to help you run FreeBSD on your PlayStation 3. This is very exprimental project.

yes,almost trash as you excepted lol :)

## Getting Started
First, you'll need to mod an older PS3 model that's compatible with CFW. Check out [here](https://consolemods.org/wiki/PS3:Getting_Started) , I recommend EVILNAT.
Visit the [Releases page](https://github.com/LowPla3329/ps3-freebsd-iso/releases) to download the latest ISO and related files.

## Important Note
**First, you MUST install the storage initializer package, otherwise release-003 and newer releases will not boot!**
It can be downloaded from this release page.

## Guide
1. Resize the VFLASH from the OtherOS tools in the Custom Firmware menu.
2. then download dtbimage from this repository, place it in the root of your USB flash drive, and install Petitboot.
3. Boot OtherOS and exit to the terminal and enter the following command: Make sure the DVD is inserted at this point.
  ```
  # kexec -l /tmp/petitboot/mnt/sr0/boot/kernel/kernel
  ```
  After entering the command, press Ctrl+Alt+Del to restart the console.

4. After a while, the mountroot prompt will appear. Enter the following command to mount the root file system:
  ```
  mountroot> cd9660:iso9660/bsd
  ```
5. Yay! Enjoy BSD World!

## Contents

- `dtbImage.ps3.bin`: Petitboot Binary file.
- `PS3_FreeBSD_Storage_Initializer-v0.1.0_by_Low_Plankton_3329.pkg`: a small savefile that allows FreeBSD to access the PS3's HDD.
