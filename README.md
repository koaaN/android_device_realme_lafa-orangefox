# OrangeFox Recovery for Realme GT8 Pro (`lafa`)

Device tree for building OrangeFox Recovery on the Realme GT8 Pro.

## Status

Initial bring-up. Device functionality still needs to be tested and verified.

## How to build

### Clone and sync the source

```bash
mkdir -p ~/android/OrangeFox_14
cd ~/android/OrangeFox_14
git clone https://gitlab.com/OrangeFox/sync.git
cd sync
./orangefox_sync.sh --branch 14.1 --path ~/android/fox_14.1
```

### Clone the device tree

```bash
cd ~/android/fox_14.1/device
mkdir -p realme
cd realme
git clone https://github.com/koaaN/android_device_realme_lafa-orangefox -b R12 lafa
```

### Build

```bash
cd ~/android/fox_14.1
source build/envsetup.sh
lunch twrp_lafa-ap2a-eng
mka adbd recoveryimage
```
