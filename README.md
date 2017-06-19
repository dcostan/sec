# Sec Development Environment
The Simplified Educational Computer is an immaginary microprocessor invented to teach students how the computer works. This program lets you to write and execute in an emulated environment the sec-assembler code.

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
