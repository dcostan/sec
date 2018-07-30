# Sec Development Environment
The Simplified Educational Computer is an immaginary microprocessor invented to teach students how the computer works. This program lets you to write and execute in an emulated environment the sec-assembler code.

## Installing from source package
This program is distributed as binary for amd64 architectures via the .run file, but if you want this program to run on other architectures you need to build it. These instructions are for linux, but the source tarball can be used also for windows.
* Download and extract the .tar.gz file
* Enter on the **interpreter** directory
* Run ``make`` and ``sudo make install``
* Return back and enter on the **ide** directory
* Run ``qmake -qt=5``
* Run ``make`` and ``sudo make install``
* Open the application with ``secide`` command or from the dash

## Binary for old linux distros
The latest binary is based on Qt 5.11 and requires a version of GLibC equal or higher than 2.25. Ancient linux distros, like Ubuntu 16.04, are based on an older GLibC version and so you need to install a previous version of the Sec IDE package
*[SecInstaller_x86.run (old)](https://github.com/dcostan/sec/raw/53aec13261d40f423223d1ce23dee651095fd9c7/SecInstaller_x64.run)

## Example
This is an example program that calculates the moltiplication between 4 and 7:
```assembly
0000 ENT,0,0000
0001 STA,0,0100
0002 STA,0,0101
0003 ENT,0,0001
0004 STA,0,0102
0005 ENT,0,0004
0006 STA,0,0200
0007 ENT,0,0007
0010 STA,0,0201
0011 LDA,0,0100
0012 ADD,0,0200
0013 STA,0,0100
0014 LDA,0,0101
0015 ADD,0,0102
0016 STA,0,0101
0017 SUB,0,0201
0020 JZA,0,0030
0021 JMP,0,0011
0030 LDA,0,0100
0031 HLT
```
