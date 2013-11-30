aosp_device_zopo_zp990
======================

Device folder for ZP990 (MTK6589T)

Warning !
-------

**Don't flash rom compiled with this folder this is only an example**


This is a base for the device folder for ZP990 (Zopo device based on MTK6589T processor).

The device folder structure is enought generic to be adapt to all devices, of course the overlay, packages and prebuilds subfolders are specifi for ZP990

At moment (11/2013) there aren't the source code for kernel, so the directive TARGET_NO_KERNEL and TARGET_NO_BOOTLOADER in BoardConfig.mk are set to true.



