# Ubuntu 14 Nintendo Wii



This repository contains images of Ubuntu 14 for the Wii. Downloads are found to your right (on desktop).

# About The Project
Trying to bring newer versions of Ubuntu to the Wii has been a project of mine for the last few months. Many trial and errors.
This versions actually build somewhat off of [Wii-Linux-NGX](https://github.com/neagix/wii-linux-ngx)
But this version uses the same bootloader with a different kernel, a newer one. And it also boots Ubuntu 14 instead of Debian 8.
Kernel branch used was "stable-v3.14.19". Originally used the Rebased Kernel but things where broken.

# How to Install (Homebrew Needed!)
In the download section you will find a .img.gz file. That file will contain a .img file with two partitions: a fat32 partition and a ext4 partition. The fat32 partition will contain the Linux loader for the Homebrew Channel.

Just flash this image to an SD Card (16gb or more needed!)

*TO RUN OVER USB, YOU MUST RECOMPILE THE KERNEL!*
https://github.com/neagix/wii-linux-ngx#building-the-kernel


# How To Boot
You will load up the homebrew channel to see its empty, thats normal. Simply press the home button and click "Launch BootMii"
That will instead load a bootloader known as Gumboot. More on Gumboot in sources below.
In order to select a different item in gumboot you MUST have a gamecube controller plugged in. But, thankfully it will auto boot in 30 seconds.

You will see an errors have been found at / dialog, obviously im no pro, so I did most likely messed something up, but Press I on a keyboard to ignore this and continue to boot.
