# Ubuntu 14 Nintendo Wii

This repository contains images of Ubuntu 14 for the Wii. Downloads are found to your right (on desktop).

# About The Project
Trying to bring newer versions of Ubuntu to the Wii has been a project of mine for the last few months. Many trial and errors.
This versions actually build somewhat off of [Wii-Linux-NGX](https://github.com/neagix/wii-linux-ngx)
But this version uses the same bootloader with a different kernel, a newer one. And it also boots Ubuntu 14 instead of Debian 8.

Kernel branch used in this is v4.20 from https://github.com/Wii-Linux/wii-linux-ngx which is forked from the original [NGX repo](https://github.com/neagix/wii-linux-ngx).

# TRY UBUNTU 16!
Ubuntu 14 is not getting releases anymore aside from a future USB mode. Please give it a try [here](https://github.com/Wiibuntu/Ubuntu-16.04-Wii)


# How to Install (Homebrew Needed!)
In the download section you will find a .img file. That file will two partitions: a fat32 partition and a ext4 partition. The fat32 partition will contain the Linux loader for the Homebrew Channel.

Just flash this image to an SD Card (2GB or more needed!)

*TO RUN OVER USB, YOU MUST RECOMPILE THE KERNEL!*
https://github.com/neagix/wii-linux-ngx#building-the-kernel 
(Or Wait For The USB Release)


# How To Boot
You will load up the homebrew channel to see its empty, thats normal. Simply press the home button and click "Launch BootMii"
That will instead load a bootloader known as Gumboot. More on Gumboot [here](https://neagix.github.io/gumboot/).
In order to select a different item in gumboot you MUST have a gamecube controller plugged in. But, thankfully it will auto boot in 30 seconds.

![alt text](https://github.com/Wiibuntu/Ubuntu14-Wii/blob/main/Screenshots/Screen%20Shot%202023-10-17%20at%205.50.29%20PM.png) ![alt text](https://github.com/Wiibuntu/Ubuntu14-Wii/blob/main/Screenshots/Screen%20Shot%202023-10-17%20at%205.50.53%20PM.png) 

Gumboots Options are a little different then shown (Image is for last version) But it will still boot to the Stable kernel by itself after 30 seconds.

# Login
user- ubuntu

pass- ubuntu

# Wi-Fi Config

Please download the "Whiite-ez-wifi-config" when you download the .img file and you will need to get that file over to your wii. If you cant get the file over to the Linux filesystem, you will have to do "sudo nano /etc/network/interfaces" and add your wifi informantion manually.

If wlan0 gets stuck on DOWN, this is an issue with wpasupplicant. Please downgrade to the .DEB provided in repo. This will allow you to connect to wifi and upgrade to a stable version of wpasupplicant.
(This is untested in version 2.0, as I now use a USB wifi adapter which works fine out of the box)

# Known Issues and Fixes

Going to be testing and using this a  lot until a newer kernel is built. I will post any issues I find below and how to fix them if possible.

-Fixed Boot Issues (v2.0)

![alt text](https://github.com/Wiibuntu/Ubuntu14-Wii/blob/main/Screenshots/Screen%20Shot%202023-10-17%20at%205.52.04%20PM.png) 

-libc6 package and others are now stable by default due to newer kernel. (v2.0)

# Contact
Contact me at wiibuntuhelp@gmail.com I will always try to help if I can and have the time to do so.

