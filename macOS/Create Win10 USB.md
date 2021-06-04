# Create Windows 10 Setup USB from Mac Terminal

### 1. Use the diskutil command to identify which drive your USB is mounted on

`diskutil list`

It will probably be something like  
`/dev/disk2`

### 2. Format your USB Drive to work with Windows

Next format your USB drive to Windows FAT32 format. This is a format that Windows 10 will recognize.
Note that you should replace the `disk2` with the name of the your drive if it wasn't `disk2`. (It may be `disk3` or `disk4`).

Run this command using the correct disk number for your USB:  
`diskutil eraseDisk MS-DOS "WIN10" GPT /dev/disk2`

Note that for some hardware, you may instead need to run this command, which uses the MBR format for partitioning instead of GPT.  
`diskutil eraseDisk MS-DOS "WIN10" MBR /dev/disk2`

### 3. Use `hdiutil` to mount the Windows 10 folder and prepare it for transfer.

You will need to check where your downloaded Windows 10 ISO file is and use that. But your file is probably located in your `~/Downloads` folder with a name of `Win10_1903_V1_English_x64.iso`.

`hdiutil mount ~/Downloads/Win10_1903_V1_English_x64.iso`

### 4. Copy the Windows 10 ISO over to your USB Drive

**Update April 2020:** One of the files in the Windows 10 ISO – install.wim – is now too large to copy over to a FAT-32 formatted USB drive. So I'll show you how to copy it over separately.

First run this command to copy over everything but that file:  
`rsync -vha --exclude=sources/install.wim /Volumes/CCCOMA_X64FRE_EN-US_DV9/* /Volumes/WIN10`

Then use Homebrew to install a tool called wimlib with this terminal command:  
`brew install wimlib`

Then go ahead and create the directory that you're going to write the files into:  
`mkdir /Volumes/WIN10/sources`

Then run this command:  
`wimlib-imagex split /Volumes/CCCOMA_X64FRE_EN-US_DV9/sources/install.wim /Volumes/WIN10/sources/install.swm 3800`

[Reference](https://www.freecodecamp.org/news/how-make-a-windows-10-usb-using-your-mac-build-a-bootable-iso-from-your-macs-terminal/)
