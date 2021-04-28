# EDK2 for UEFI Firmware for Motorola One Action and Motorola One Vision
Based on port Linux-On-Sdm6Series for Asus Zenfone Max Pro M1 (X00TD) (https://github.com/Linux-On-Sdm6Series/edk2-X00TD/).

## Status

What works:
- Display
- UEFI Shell

What does not work:
- Clocks
- eMMC (SdccDxe requires Clocks)
...

## Building
Tested on Ubuntu 18.04.

First, clone EDK2.

```
cd ..
git clone https://github.com/tianocore/edk2.git --recursive
git clone https://github.com/tianocore/edk2-platforms.git
```

You should have all three directories side by side.

Next, install dependencies:

18.04:

```
sudo apt install build-essential uuid-dev iasl git nasm python3-distutils gcc-aarch64-linux-gnu abootimg
```

Also see [EDK2 website](https://github.com/tianocore/tianocore.github.io/wiki/Using-EDK-II-with-Native-GCC#Install_required_software_from_apt)

Finally, ./build.sh.

Then `fastboot flash boot uefi.img`.

# Credits

This is based on Linux-On-Sdm6Series [X00TD port](https://github.com/Linux-On-Sdm6Series/edk2-X00TD/).  
SimpleFbDxe screen driver is from imbushuo's [Lumia950XLPkg](https://github.com/WOA-Project/Lumia950XLPkg).  
Special thanks to @lemon1ice and @imbushuo for guidance.
