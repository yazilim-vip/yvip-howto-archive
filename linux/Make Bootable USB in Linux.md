Make Bootable USB in Linux

Linux dd ile usb iso oluşturmak

`sudo umount /dev/sdX`

`sudo dd if=/path/to/ubuntu.iso of=/dev/sdX bs=4M && sync`