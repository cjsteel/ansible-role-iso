
## Resources

* [](https://help.ubuntu.com/community/Installation/FromUSBStick#Boot_and_install)

## mkusb

mkusb - dd image of iso file to USB device safely

* high success rate.


https://launchpad.net/~mkusb/+archive/ubuntu/ppa

If you run standard Ubuntu, you need an extra instruction to get the repository Universe. (Kubuntu, Lubuntu ... Xubuntu have the repository Universe activated automatically.)

    sudo add-apt-repository universe  # only for standard Ubuntu

Otherwise the following three command lines are enough to install mkusb.

    sudo add-apt-repository ppa:mkusb/ppa  # and press Enter
    sudo apt-get update
    sudo apt-get install mkusb

View or download the quick start manual:

    http://phillw.net/isos/linux-tools/mkusb/mkUSB-quick-start-manual.pdf

## mkusb - wiki page

mkusb is described with more details at the following wiki page

    https://help.ubuntu.com/community/mkusb


