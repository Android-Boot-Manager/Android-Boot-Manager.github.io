# Android Boot Manager
## Welcome to Android Boot Manager page
Android Boot Manager is a new dualboot tool for Android. There were many of them before, such as: EFIDroid, MultiROM, Dualboot patcher, etc. Usually they reflashed boot dynamically for dualbooting. Some of them used one big hack like MultiROM's kexec-hardboot.

## How does Android Boot Manager work?
Android Boot Manager uses lk based bootloader flashed to boot partition for loading the device tree, kernel and ramdisk, and an android app with sh scripts and pre-compiled binary for easy rom management.In some rear cases (such as yggdrasil) Android Boot Manager's bootloader is flashed instead of stock.

## Current status
For now project is in pre-alpha stage. Actively developed.

## Devices 
For now this is developed for Motorola Moto G5 (cedric) and Volla Phone(yggdrasil), but a bit later I will create a porting guide.
