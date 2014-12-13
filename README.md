Setup
-----

Install the required packages to build the system.
	sudo apt-get install git build-essential ncurses-dev kpartx

Building
--------

	git clone --depth 1 git://github.com/NextThingCo/rpi-buildroot.git
	cd rpi-buildroot
	make stak_raspi_hwtest_defconfig
	make nconfig         # if you want to add packages or fiddle around with it
	                     # the Stak packages currently need to be enabled or they won't get included
	make                 # build (NOTICE: Don't use the **-j** switch, it's set to auto-detect)


Create SD Card IMG
------------------
	SD card image is created automagically as part of the build process. You can find the result
        at output/images/rpi-sdimg.img



