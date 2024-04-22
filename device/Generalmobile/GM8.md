# General Mobile GM 8 (d)

============================================================
Basic   | Spec Sheet
-------:|:-------------------------
CPU     | Quad-core 1.4 GHz ARM Cortex-A53
CHIPSET | Qualcomm Snapdragon 435 MSM8940
GPU     | Adreno 505
Memory  | 3/4 GB
Shipped Android Version | 8.0
Storage | 32/64 GB
MicroSD | Up to 128 GB
Battery | 3075 mAh (non-removable)
Display | 720 x 1440 pixels, 5.7"
Rear Camera  | 13.0 MP Dual-Flash
Front Camera | 13.0 MP
Release Date | Feb 2018

![GM8](https://assets.generalmobile.com/images/gm8/galeri/02.jpg "GM8")

Device is ARM64 Legacy A/B

FLASHING S STOCK QFIL TO D FOR UNBRICK WILL WORK, FASTBOOT FLASH D ROM TO GET DUAL (haven't tested dual rom after single qfil, may damage 2nd IMEI)

## GSI flashing steps
```
fastboot flash system gsi.img 
fastboot --disable-verity --disable-verification flash boot boot.img
fastboot -w reboot
```
Unconfirmed

## System partition resizing

```
adb reboot recovery
adb push parted /sbin
adb shell
chmod +x /sbin/parted
parted
p
rm 25
rm 26
mkpart system_a ext4 606 5437.5
mkpart system_b ext4 5437 7049
name 25 system_a
name 26 system_b
quit
```
Doesn't work, you system_a and system_b probably has to be the same size
TODO: remove all partitions until system, then remove system, resize system to be 5gb each, recreate all other partition with offset, remove remaining from userdata

## Custom recovery
```
adb reboot bootloader
fastboot flash boot twrp
```
After this is done, hold vol- and power, then hold vol+ and powers release power when logo