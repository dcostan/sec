# Sec Development Environment
The Simplified Educational Computer is an immaginary microprocessor invented to teach students how the computer works. This program lets you to write and execute in an emulated environment the sec-assembler code.

## Installing from source package (linux)
This program is distributed as binary for amd64 architectures via the .run file, but if you want this program to run on other architectures you need to build it.
* Download and extract the .tar.gz file
* Enter on the **interpreter** directory
* Run ``make`` and ``sudo make install``
* Return back and enter on the **ide** directory
* Run ``qmake -qt=5``
* Run ``make`` and ``sudo make install``
* Open the application with ``secide`` command or from the dash

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
