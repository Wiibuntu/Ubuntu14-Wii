# Ubuntu 14 Nintendo Wii



This repository contains images of Ubuntu 14 for the Wii. Downloads are found to your right (on desktop).

# About The Project
Trying to bring newer versions of Ubuntu to the Wii has been a project of mine for the last few months. Many trial and errors.
This versions actually build somewhat off of [Wii-Linux-NGX](https://github.com/neagix/wii-linux-ngx)
But this version uses the same bootloader with a different kernel, a newer one. And it also boots Ubuntu 14 instead of Debian 8.

Kernel branch used was "Stable 3x". Originally used the "rebased-v3" Kernel but things where broken.

# How to Install (Homebrew Needed!)
In the download section you will find a .img file. That file will two partitions: a fat32 partition and a ext4 partition. The fat32 partition will contain the Linux loader for the Homebrew Channel.

Just flash this image to an SD Card (2GB or more needed!)

*TO RUN OVER USB, YOU MUST RECOMPILE THE KERNEL!*
https://github.com/neagix/wii-linux-ngx#building-the-kernel 

(Baedit does not work)


# How To Boot
You will load up the homebrew channel to see its empty, thats normal. Simply press the home button and click "Launch BootMii"
That will instead load a bootloader known as Gumboot. More on Gumboot [here](https://neagix.github.io/gumboot/).
In order to select a different item in gumboot you MUST have a gamecube controller plugged in. But, thankfully it will auto boot in 30 seconds.

![alt text](https://github.com/Wiibuntu/Ubuntu14-Wii/blob/main/Screenshots/Screen%20Shot%202023-10-17%20at%205.50.29%20PM.png) ![alt text](https://github.com/Wiibuntu/Ubuntu14-Wii/blob/main/Screenshots/Screen%20Shot%202023-10-17%20at%205.50.53%20PM.png) 

Gumboots Options are a little different then shown (Image is for last version) But it will still boot to the Stable kernel by itself after 30 seconds.

You will see an errors have been found at / dialog, im no pro, so I did most likely mess something up, but press I on a keyboard to ignore this and continue to boot.

![alt text](https://github.com/Wiibuntu/Ubuntu14-Wii/blob/main/Screenshots/Screen%20Shot%202023-10-17%20at%205.52.04%20PM.png) ![alt text](https://github.com/Wiibuntu/Ubuntu14-Wii/blob/main/Screenshots/Screen%20Shot%202023-10-17%20at%205.52.19%20PM.png)

# Login
user- ubuntu

pass- ubuntu

# Wi-Fi Config

Please download the "Whiite-ez-wifi-config" when you download the .img file and you will need to get that file over to your wii. If you cant get the file over to the Linux filesystem, you will have to do "sudo nano /etc/network/interfaces" and add your wifi informantion manually.

# Known Issues and Fixes

Going to be testing and using this a  lot until a newer kernel is built. I will post any issues I find below and how to fix them if possible.


-libc6 package is an unstable version, In order to properly install and upgrade things you MUST downgrade libc6 with aptitude to version 2.19-0ubuntu6.

-More packages happen to be unstable, thankfully aptitude can help you solve that problem and downgrade them (even in batches) just keep requesting a new solution until one includes downgrading the packages causing problems.

