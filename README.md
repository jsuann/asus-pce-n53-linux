# Asus PCE-N53 linux driver for kernel 3.x

Forked from [here](https://github.com/mareksuscak/asus-pce-n53-linux) with a patch for 4.15 kernel and other additional fixes. Tested on Void Linux.

## Important Note

[5 GHz isn't working by default](https://github.com/mareksuscak/asus-pce-n53-linux/issues/2) with this patched driver as of 4.2.0-17-generic kernel. There's a manual fix provided in the link but no patch as of yet.

## How to Install

Instructions for Ubuntu/Debian/etc:

```
$ sudo apt-get update
$ sudo apt-get upgrade -y
$ sudo apt-get install build-essential linux-headers-generic linux-headers-$(uname -r) -y
$ cd ~
$ git clone https://github.com/jsuann/asus-pce-n53-linux.git
$ cd asus-pce-n53-linux
$ make
$ sudo make install
$ sudo modprobe rt5592sta
```

If everything worked well you should be able to configure the network card & connect to a Wireless network.
