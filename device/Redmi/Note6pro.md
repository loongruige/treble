# Xiaomi Redmi Note 6 Pro
| Device                  | Xiaomi Redmi Note 6 Pro                                     |
| ----------------------- | :---------------------------------------------------------- |
| SoC                     | Qualcomm SDM660 Snapdragon 636                              |
| CPU                     | 8x Qualcomm® Kryo™ 260 CPU                                  |
| GPU                     | Adreno 509                                                  |
| Memory                  | 4GB / 6GB RAM (LPDDR4X)                                     |
| Shipped Android version | 8.1.0                                                       |
| Storage                 | 64GB eMMC 5.1 flash storage                                 |
| MicroSD                 | Up to 256 GB                                                |
| Battery                 | Non-removable Li-Po 4000 mAh                                |
| Dimensions              | 157.9 x 76.4 x 8.3 mm                                       |
| Display                 | 2280 x 1080 (19:9), 6.26 inch                               |
| Rear camera 1           | 12 MP, f/1.9, 1/2.55", 1.4µm, dual pixel PDAF               |
| Rear camera 2           | 5 MP, f/2.2, 1.12µm, depth sensor                           |
| Front camera 1          | 20 MP, f/2.0, 0.9µm                                         |
| Front camera 2          | 2 MP, f/2.2, 1.75µm, depth sensor                           |

![Xiaomi Redmi Note 6 Pro](https://img.timesnownews.com/story/1544521578-Xiaomi_Redmi_Note_6_Pro_colours.jpg)

Device is ARM64 Aonly

UNIT IS WORN OUT, I WON'T BE A TESTER FOR IT

## GSI Flashing steps
```
fastboot flash system gsi.img
fastboot --disable-verity --disable-verification flash vbmeta vbmeta.img
fastboot reboot recovery
adb sideload Permissiver_v5.zip
```