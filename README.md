# rpi-overlays

## Usage

1. Compile the dts into a Device Tree Overlay blob: `dtc -W no-unit_address_vs_reg -@ -I dts -O dtb -o wave144.dtbo wave144.dts`
2. Move it where it belongs `sudo cp wave144.dtbo /boot/overlays`
3. Modify `/boot/config.txt` to add `dtoverlay=wave144` at end
4. Optionally add `fbcon=map:10` to `/boot/cmdline.txt`

## Issue

The Waveshare 1.44" 128x128 display's origin is not at (0, 0). Two rows at the top and one column at the left of the display are missing.



