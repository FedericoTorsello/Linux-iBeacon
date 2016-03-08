# Linux-iBeacon
========
This script make your GNU/Linux machine (PC or Raspberry Pi) in a true iBeacon!

"linux-iBeacon" script work on more disto Linux Debian-based (Raspbian, Ubuntu, etc) or Arch-based (Manjaro).

It's based on [piBeacon] (https://github.com/jacklund/piBeacon).

## Prerequisites
You'll need to download and install [BlueZ](http://www.bluez.org) version 5.7 or later and install it.

1. Install prerequisite packages

		$ sudo apt-get install libusb-dev libdbus-1-dev libglib2.0-dev libudev-dev libical-dev libreadline-dev

2. Download and install the latest BlueZ

		$ sudo wget www.kernel.org/pub/linux/bluetooth/bluez-5.x.tar.xz
		(go https://www.kernel.org/pub/linux/bluetooth/ to read the last version)
		$ sudo unxz bluez-5.x.tar.xz
		$ sudo tar xvf bluez-5.x.tar
		$ cd bluez-5.x

3. Configure and make BlueZ

		$ sudo ./configure --disable-systemd
		$ sudo make
		$ sudo make install
		
4. Download this git
		git clone https://github.com/FedericoTorsello/Linux-iBeacon.git
		
## Starting
	Example:
		$ sh ./linux-ibeacon -s 2
	(arg 2 in this example is the number of USB Bluetooth on your PC or Raspberry Pi)

## Blocking
	Example:
		$ sh ./linux-ibeacon -b 2
	(arg 2 in this example is the number of USB Bluetooth on your PC or Raspberry Pi)
