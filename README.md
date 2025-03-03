# HP Pro c640 Chromebook (Dratini) Linux
This repository contains some useful information and files for running Linux Desktop on the HP Pro c640 Chromebook (Dratini).

Information updated: 2025/03/01. Let me know if you find any outdated information.

## Hardware
- Based on Intel Comet Lake-U platform, Board "hatch", codename "dratini".
- Intel Core i3-10110U/i5-10310U/i7-10610U(/Pentium Gold 6405U? Not sure)
- 8GB/16GB LPDDR4
- 64G/128G eMMC (M.2 NVMe slot can be added by DIY, ask expert if you want this)
- 1366x768(TN)/1920x1080(IPS) 14" Display (with optional touch)

(Note: they're from internet so may be inaccurate, any correction is welcome)

## Firmware
Currently, this machine has NO RW_LEGACY firmware available, so if you want to install a custom OS, you may have to flash the full UEFI firmware.

*Although not recommended, technically booting mainline Linux may be possible with the stock firmware(which is based on depthcharge), but I've not tested it. If you succeed, please let me know.*

You can find custom coreboot firmware made by MrChromeBox [here](https://mrchromebox.tech/). Follow their instructions to flash the firmware.

## Installation
After flashing the firmware, you can install any your favorite Linux distribution as usual.
These are the hardware that is likely to work:
- It boots: It should at least boots and basically works.
- Network: They're usual Intel Wireless card, so they should work out of the box.
- Touchpad: Should work out of the box.
- Touchscreen: Most of the time it should works, but it may not be supported by Debian 12 Stable. Consider using Debian Testing (or playing with the kernel. if you succeed, please let me know).
- SD Card Reader: Should work out of the box. However you can not use it as a boot device(initramfs can not find the root device). As always, If you succeed, please let me know.

These are the hardware that may need some extra work:
### Audio
As many other Chromebooks, audio does not work out of the box.
Run this script: https://github.com/WeirdTreeThing/chromebook-linux-audio
and it should work after reboot.

### Keyboard
It has a common Chromebook keyboard layout, so you may need to remap some keys.
I recommend using `keyd` for this purpose. You can use my config file (keyd.conf) as a reference. I've followed ChromeOS's default keymap as much as possible, so you can just use it as is. Of course, you can modify it as you like.

### Other OSs
Windows can also be installed, with some extra work and some other bugs. You can find more informations in CoolStar's website currently, and more information may be available in the future.

## Contact
Feel free to open issues if you have any questions or find any bugs. I'll try to help you as much as possible.
