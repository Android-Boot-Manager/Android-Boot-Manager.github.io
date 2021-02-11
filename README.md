# Android Boot Manager
## Welcome to our Website!
Android Boot Manager is a new dualboot tool for Android.
There were many of them before, such as: EFIDroid, MultiROM, Dualboot Patcher, etc.
Usually they reflashed boot dynamically for dualbooting.
Some of them used one big hack like MultiROM's kexec-hardboot.

## How does ABM work?
It uses an App for Android to manage & install ABM and ROMs.
It also needs an bootloader, we call ours DroidBoot.
We have 3 variants:

### 1st-stage bootloader (lk, systemd-boot or UEFI app)
This is the best solution because it does booting exactly where it's supposed to be done: in the Bootloader.
This solution however also requires the most porting work as it needs to be rewritten for each device individually.

### 2nd-stage bootloader (lk2nd)
This is an good solution:
- It uses an bootloader software designed for booting the Linux kernel
- It doesn't need to reboot twice to start an OS, unlike the third solution.
But it has a few disadvantages:
- The 2nd-stage bootloader is in the boot partition. This means it gets overwritten very often.
- This is only possible with older (non-UEFI) qualcomms for now.

### The no bootloader workaround ramdisk (no-bootloader-workaround-rd)
This is the worst solution:
- This needs to reboot twice when booting an OS (first to the menu, then to the OS)
- It reflashes boot. This is slow.
- It still lives in the boot image so it's getting easily overwritten.
Though it also has a few advantages:
- It's way easier to port
- It supports touchscreen

## How can I use it?
Currently, only the Volla Phone is ready to use.
You probably want to join our group on Telegram: https://t.me/andbootmgr.
An proper guide will be created soon.

## How can I port it?
Currently, your best bet is our Telegram group: https://t.me/andbootmgr

## Current status
This project is in the beta status. All devices except the Volla Phone are in the pre-alpha status.
