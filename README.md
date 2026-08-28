# PIXIS-CODE
Drivers and Utilities for the PIXIS Project

Download the drivers for Landscape (st7789vl.bin) and Portrait (st7789vp.bin) screen orientation and copy them to your /usr/lib/firmware directory. If you are using an OS other than Raspberry Pi Debian then copy the driver into the appropriate directory. 

Follow the instructions in LCDconfigs.txt to edit your config.txt file. They will tell you to add these lines in config.txt under the [all] section  

#For st7789vl Landscape 2.8inch Waveshare SKU 27579 use

dtoverlay=mipi-dbi-spi,speed=48000000
dtparam=compatible=st7789vl\0panel-mipi-dbi-spi
dtparam=width=320,height=240,width-mm=59,height-mm=44
dtparam=reset-gpio=27,dc-gpio=25,backlight-gpio=18

#For st7789vp Portrait 2.8inch Waveshare SKU 27579 use

dtoverlay=mipi-dbi-spi,speed=48000000
dtparam=compatible=st7789vp\0panel-mipi-dbi-spi
dtparam=width=240,height=320,width-mm=44,height-mm=59
dtparam=reset-gpio=27,dc-gpio=25,backlight-gpio=18

Comment out the Portrait lines if using Landscape or comment out the Landscape lines if using Portrait.

The .txt files are guides you may edit to help you create new binaries should you wish to work with LCDs other than the Waveshare 2.8 inch SKU 27579. Please use at your own risk.

Thanks to Isaac and Kieran at Ideas On Board and Linuxembedded for providing these files.
