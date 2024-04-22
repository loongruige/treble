# General Mobile GM 22 Plus

| Device                  | General Mobile GM 22 Plus                                   |
| ----------------------- | :---------------------------------------------------------- |
| Chipset                 | MediaTek Helio G80 (MT6768/CU)                              |                                 
| Memory                  | 4GB                                                         |
| Shipped Android version | 11.0                                                        |
| Storage                 | 128GB flash storage                                         |
| MicroSD                 | Up to 512 GB                                                |
| Battery                 | Non-removable Li-on 6000 mAh                                |
| Dimensions              | 168.65mm x 76.5mm x 9.08mm                                  |
| Display                 | 6.78 inch 1080x2460 IPS LCD                                 |
| Rear camera 1           | 48 MP                                                       |
| Rear camera 2           | 5 MP                                                        |
| Rear camera 3           | 2 MP                                                        |
| Front camera            | 8 MP                                                        |

Device is ARM64 A/B, recovery as boot

I won't be able to test this device, since I've lent it to someone. DSU testing is probable

## GSI flashing steps
```
fastboot flash system_a gsi.img
fastboot --disable-verity --disable-verification flash vbmeta_a vbmeta_a.img
fastboot --disable-verity --disable-verification flash vbmeta_b vbmeta_b.img
```

## Tested GSI
Flyme 13 SIM won't work

DerpFest 14 Fingerprint won't work

Pixel Experience 13 Fingerprint won't work



