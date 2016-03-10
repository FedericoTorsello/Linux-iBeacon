# Linux-iBeacon

This script turns your GNU/Linux machine (PC or Raspberry Pi) in a true iBeacon!

This script work on more Linux distro Debian-based (Raspbian, Ubuntu, etc) or Arch-based (Manjaro).

It's based on [piBeacon] (https://github.com/jacklund/piBeacon).

# Prerequisites
You'll need to download and install [BlueZ](http://www.bluez.org) version 5.7 or later.

## For Debian system

1. Install prerequisite packages

		$ sudo apt-get install libusb-dev libdbus-1-dev libglib2.0-dev libudev-dev libical-dev libreadline-dev

2. Download and install the latest BlueZ

		$ sudo apt-get install bluez
		
		...or...
		
		$ cd ~ && sudo wget www.kernel.org/pub/linux/bluetooth/bluez-5.x.tar.xz
		(go https://www.kernel.org/pub/linux/bluetooth/ to read the last version)
		$ unxz bluez-5.x.tar.xz
		$ tar xvf bluez-5.x.tar
		$ cd bluez-5.x

3. Configure and make BlueZ

		$ ./configure --disable-systemd
		$ make
		$ sudo make install
		
4. Clone this git and change directory
		
		git clone https://github.com/FedericoTorsello/Linux-iBeacon.git
		cd Linux-iBeacon

## For Arch system

1. Check if Bluez's packages are installed on your system
		$ pacman -Ss bluez
		...or...
		$ yaourt -Ss bluez
		
2. Download and install the latest BlueZ

		$ sudo pacman -S bluez
		
		...or...
		
		$ yaourt -S bluez
		
		...or...
		
		$ cd ~ && wget www.kernel.org/pub/linux/bluetooth/bluez-5.x.tar.xz
		(go https://www.kernel.org/pub/linux/bluetooth/ to read the last version)
		$ unxz bluez-5.x.tar.xz
		$ tar xvf bluez-5.x.tar
		$ cd bluez-5.x

3. Configure and make BlueZ

		$ ./configure --disable-systemd
		$ make
		$ sudo make install
		
4. Clone this git and change directory
		
		git clone https://github.com/FedericoTorsello/Linux-iBeacon.git
		cd Linux-iBeacon
		
## Start

	Example:

		$ sudo sh linux-ibeacon -start 2
		
	(the param "2" in this example is the number of USB Bluetooth plugged in on your PC or Raspberry Pi)

## Stop

	Example:
	
		$ sudo sh linux-ibeacon -stop 3
		
	(the param "3" in this example is the number of USB Bluetooth plugged in on your PC or Raspberry Pi)

#Other

## Checking your Environment

		$ sudo hciconfig

	result like this:

		hci0:   Type: BR/EDR  Bus: USB
    		BD Address: 00:02:xx:DC:xx:4F  ACL MTU: 1021:8  SCO MTU: 64:1
    		UP RUNNING
    		RX bytes:1144 acl:0 sco:0 events:71 errors:0
    		TX bytes:1173 acl:0 sco:0 commands:71 errors:0
