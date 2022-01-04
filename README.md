# WinRT_Surface_to_LinuxOS
Steps taken to convert Windows RT Surface 2 Tablet to run Linux (Raspbian)

Windows RT Surface tablet is based on ARM architecture.  Booting into Linux via USB is just not possible.  So a specific bootloader is needed,  one provided on the OpenRT website. 


Source : [ OpenRT website ](https://openrt.gitbook.io/open-surfacert/surface-rt/linux/root-filesystem/distros/raspberry-pi-os) 

What follows are the steps taken to install Raspbian on the Windows RT Surface Tablet.  

1.  [Create a bootable Win95-FAT32 USB compatible with Surface Tablet](https://openrt.gitbook.io/open-surfacert/common/boot-sequence/uefi/fat32-isnt-fat32) .  
- Formating in linux as FAT32 is not exactly the filesystem type that the Surface tablet is used to.  So follow the linux steps to format it.

2.  Unzip then copy the files from [`Surface_RT_2_Jailbreak_USB_v1.3c.zip`](https://github.com/f-caro/WinRT_Surface_to_LinuxOS/blob/main/Surface_RT_2_Jailbreak_USB_v1.3c.zip)  to the bootable USB.   

- Then follow the instuctions on page [Jailbreak Guide](https://openrt.gitbook.io/open-surfacert/tools/surface-rt-and-surface-2-jailbreak-usb#troubleshooting)

- Make sure to install the "Yahallo INstall" step immediately after the "Golden Key Install".  Once the "Golden Key" step finishes, the tablet will restart.  Hold the Volume DOWN button, until it boots back into the BOOT MENU, then carry on with the install "Yahallo Install".  Otherwise you'll get a "Certficate not compatible Error".

3.  Create a new Bootable MicroSD, that will point to the Linux bootloaders -  
- Using the latest version of Raspbian is okay, since it is compiled for ARM32.  
- Use BALENA ETCHER, flash the MicroSD card with the raspbian ISO, 
- Then follow the steps to replace the important bootloaders.
