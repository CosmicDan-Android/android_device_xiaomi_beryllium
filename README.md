# android_device_xiaomi_beryllium
For building TWRP for PocoPhone F1

TWRP device tree for PocoPhone F1




PocoPhone F1 was announced and released on 22th of august 2018.

## Device specifications

| Device       | PocoPhone F1                                    |
| -----------: | :---------------------------------------------- |
| SoC          | Qualcomm SDM845 Snapdragon 845                  |
| CPU          | 8x Qualcomm® Kryo™ 385 up to 2.8GHz             |
| GPU          | Adreno 630                                      |
| Memory       | 6GB / 8GM RAM (LPDDR4X)                         |
| Shipped Android version | 8.1                                  |
| Storage      | 64GB / 128GB UFS 2.1 flash storage              |
| Battery      |  Non-removable Li-Po 4000 mAh                   |
| Dimensions   |  155.5 x 75.3 x 8.8 mm                          |
| Display      | 2246x1080 (18:9), 6.18  inch                    |
| Rear camera 1 | 12 MP, f/1.9, 1/2.55", 1.4µm,                  |
| Rear camera 2 | 5 MP, f/2.0, 1.12µm                            |
| Front camera | 20 MP, f/2.0, 0.9µm 1080p 30 fps video  |

## Device picture

![Pocophone F1](https://cdn2.gsmarena.com/vv/pics/xiaomi/xiaomi-pocophone-f1-2.jpg)

## Features

Works:

- ADB
- MTP
- Screen brightness settings
- Now UI is very smooth (thanks to TWRP fix 16d831bee5a660f5ac6da0d8fff2b3ec4697d663)
- Vibration on touch (see https://gerrit.omnirom.org/#/c/android_bootable_recovery/+/31021/)
- Correct screenshot color (see https://gerrit.omnirom.org/#/c/android_bootable_recovery/+/31042/)

Dont work:
- Decryption of data
- Short freeze when connected to pc 

Finally execute these:

```
export ALLOW_MISSING_DEPENDENCIES=true
. build/envsetup.sh
lunch omni_beryllium-eng 
LC_ALL=C 
mka recoveryimage
```
