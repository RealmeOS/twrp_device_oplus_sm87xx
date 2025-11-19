# TWRP device tree for Realme GT7 Pro

Realme GT7 Pro (codenamed _"RMX5010"_) is a high-end smartphone from Realme.

## Build it yourself?

```
mkdir twrp && cd twrp
repo init --depth=1 -u https://github.com/TWRP-Test/platform_manifest_twrp_aosp -b twrp-14.1
repo sync -j8
git clone --depth=1 https://github.com/RealmeOS/twrp_device_oplus_sm87xx device/realme/rmx5010 -b twrp-14
```

```
export ALLOW_MISSING_DEPENDENCIES=true
source build/envsetup.sh
lunch twrp_rmx5010-ap2a-eng
make recoveryimage
```


If there is no error, recovery.img will be found in out/target/product/rmx5010/recovery.img  
**NOTE**  
Using Github Actions to build TWRP-14 branch may fail because of the large source


## Features
Works:
- [X] ADB
- [X] Display
- [X] Decryption
- [X] Fasbootd
- [X] Flashing
- [X] MTP
- [X] Sideload
- [X] USB OTG
- [X] Vibrator
- [X] Mount /data

## To use it:

```
fastboot flash recovery recovery.img
```
