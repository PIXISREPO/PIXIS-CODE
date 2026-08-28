# PIXIS-CODE
Drivers and Utilities for the PIXIS Project

Select the appropriate driver for Landscape (st7789vl.bin) or Portrait (st7789vp.bin) screen orientation and place the LCD binary driver in your /usr/lib/firmware directory. If you are using an OS other than Raspberry Pi Debian then copy the driver into the appropriate directory. 

Follow the instructions in LCDconfigs.txt to edit your config.txt file. Add these lines under the [all] section  

#For st7789vl Landscape 2.8inch Waveshare SKU 27579 use
dtoverlay=mipi-dbi-spi,speed=48000000
dtparam=compatible=st7789vl\0panel-mipi-dbi-spi
dtparam=width=320,height=240,width-mm=59,height-mm=44
dtparam=reset-gpio=27,dc-gpio=25,backlight-gpio=18

The .txt files are guides you may edit to help you create new binaries should you wish to work with LCDs other than the Waveshare 2.8 inch SKU 27579. Please use at your own risk.

Thanks to Isaac and Kieran at Ideas On Board and Linuxembedded for providing these files.
