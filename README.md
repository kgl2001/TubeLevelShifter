# Tube Level Shifter for use with BBC Micro and Master 128 computers.

This project allows a Raspberry Pi to be connected to the Tube port on the BBC Micro and Master 128 computers. With the [PiTubeDirect](https://github.com/hoglet67/PiTubeDirect/wiki) software loaded onto the Pi, the following list of co-processors can be emulated:

```
 n   Processor - *FX 151,230,n
 0   65C02 (fast)
 1   65C02 (3MHz)
 2   65C102 (fast)
 3   65C102 (4MHz)
 4   Z80 (1.21)
 5   Z80 (2.00)
 6   Z80 (2.2c)
 7   Z80 (2.30)
 8   80186
 9   MC6809
11   PDP-11
12   ARM2
13   32016
14   Disable
15   ARM Native
16   LIB65C02 64K
17   LIB65C02 256K Turbo
18   65C816 (Dossy)
19   65C816 (ReCo)
20   OPC5LS
21   OPC6
22   OPC7
23   RISC-V
24 * 65C02 (JIT)
28   Ferranti F100-L
```

Most Pi models are compatible with PiTubeDirect. The smaller PiZero, PiZeroW or PiZero2W and level shifter can sit under a Beeb or Master.

The larger Pi1, Pi2, Pi3A/B & Pi4 models are also supported via a cable as they won't fit under the computer.

The latest PiTubeDirect software can be downloaded from the following site:

https://github.com/hoglet67/PiTubeDirect/releases

Some general notes:

* The source files are to be used with KiCAD v9.0.0 or later.
* The gerber files have been optimised for fabrication by JLCPCB. In particular, there is a 8mmx8mm silkscreen box on the rear of the PCB. This is to allow a 2D barcode, with unique serial number to be printed on the PCB.
* If you want the barcode to be added, then make sure to select this option in the 'Mark on PCB' field, and make sure to select 'Specify position' in the '2D Barcode Position' field, otherwise you will end up with a white 8mm x 8mm box printed on your PCB and a 8mm x 8mm barcode printed at a position of JLCPCBs choosing. Thrust me on this!
* If you don't want the barcode added, then remove the 8mm x 8mm box from the silkscreen layer and regenerate the gerbers. Otherwise you will end up with a white 8mm x 8mm box printed on your PCB.
* A combined CPL / BOM file is included in the gerber directory. Again, this is for use with JLCPCB, if you want to use their PCBA (PCB Assembly) to solder on all the SMD parts.
* You will need to source suitable 40 pin right angle and 40 pin straight through sockets, and solder these onto the PCB. The Raspberry Pi will connect to the 40 pin straight through socket and the level shifter will plug into the tube port via the 40 pin right angle socket.
* Be aware that it is possible to misalign the 40 pin right angle socket both vertically and horizontally when plugging it into the tube port so take care to ensure it is aligned correctly.
* The pins on the tube port connector may be tarnished if the header has not been used for many years. This can cause unreliable operation. This can usually be fixed with repeated removal and re-insertion of the level shifter into the header.
* Do not use a ribbon cable to connect the Raspberry Pi to the level shifter. Instead, the Raspberry Pi should be plugged directly into the level shifter.
* The level shifter can be plugged directly into the tube port in the well underneath the keyboard, or it can be attached to the tube port via a 40 way male / female ribbon cable.
* There is limited space in the well underneath the Master, so the the level shifter should initially be inserted at an angle and then straightened out as the level shifter is pushed home into the tube port.
* Due to the limited space underneath the Master, a compromise had to be made on the overall size of the level shifter board. Therefore, when fitting the level shifter into the Model B it may not be possible to push the level shifter fully into the tube port socket, otherwise the front face of the Pi will clash with part of the computer case.
* An optional power header can be attached to the level shifter. This header can then be used to power the Pi1MHz level shifter and assocaited Raspberry Pi, if attached to the 1MHz bus. The 5v supply is protected by a 500mA Poylfuse.
* If the level shifter is connected to the tube port via a ribbon cable then the simplest way to power the level shifter and Raspberry Pi is via a standard Raspberry Pi power supply connected to the Raspberry Pi. This will also power the level shifter. In this case, jumper J1 should be removed to prevent the Raspberry Pi supply from powering the main computer.

## Developer

The 1MHz level shifter board is developed and maintained by Ken Lowe.
    
## Hardware License (Creative Commons BY-SA 4.0)

Please see the following link for details: https://creativecommons.org/licenses/by-sa/4.0/

You are free to:

Share - copy and redistribute the material in any medium or format
Adapt - remix, transform, and build upon the material
for any purpose, even commercially.

This license is acceptable for Free Cultural Works.

The licensor cannot revoke these freedoms as long as you follow the license terms.

Under the following terms:

Attribution - You must give appropriate credit, provide a link to the license, and indicate if changes were made. You may do so in any reasonable manner, but not in any way that suggests the licensor endorses you or your use.

ShareAlike - If you remix, transform, or build upon the material, you must distribute your contributions under the same license as the original.

No additional restrictions - You may not apply legal terms or technological measures that legally restrict others from doing anything the license permits.
