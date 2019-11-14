# Tandy 1000 EX/HX 3-in-1 Expansion Board

This is a single expansion board designed for the Tandy 1000 EX and HX computers, to include the following upgrades:

```
640KB Base System Memory
96KB Upper Memory
16550-based RS232 Serial RS232 Port
XT-IDE based Compact Flash "Hard Drive"
```

## TO-DO
* BOM
* Assembly Instructions
* BIOS Flashing Instructions

## Getting Started

### Prerequisites

This board is for the Tandy 1000EX and 1000HX computers only.  It will not work in any other computer model as it is.
You must remove any expansion cards already in the computer, this is designed to be a single-board upgrade and has no provisions to allow for any other expansion cards.

### Installing

This board plugs into the Tandy PLUS interface, and takes up "Slot 2" on the rear of the computer.  Please be careful to align the PLUS bus completely, to avoid bending pins on the computer.


## Technical Details

This board is jumperless and is designed to be plug-and-play.   The board is hardwired with these memory locations/ports:
```
SRAM:  0x0000-0x5FFF, 0xC800-0xDFFF
UART:  0x3F8, IRQ 4
IDE:   0x300
ROM:   0xC000-0xC7FF
```

## Bill of Materials
```
---------------------------------------
Ref(s)            Value
-------------------------------------------
BUS1              2x31 2.54mm Header Socket
R1 through R3     10kOhm 1/8w Resistor
C1 through C16    0.1uF Multilayer Ceramic Capacitor, 2.5mm Lead Spacing
CP1               10-100uF 10-25V Electrolytic or Polymer Capacitor, 2.5mm Lead Spacing
232-P2            DE9 Male Right Angle Connector   
232-U6            GD75232N RS232 Driver
232-U7, 232-U9    74ACT138 3-to-8 Line Demux
232-U8            16550/16C550 UART in PLCC-44 Package 
232-U8 Socket     PLCC-44 Through Hole Socket
CF-J1             2x20 2.54mm Header Socket, 11mm height.
CF-J2             1x2 2.54mm Header Socket
CF-U1             74LS129 Dual 2-to-4 Demux
CF-U2, ROM-U4     74LS688 8-bit Comparator
CF-U3, RAM-U11    74LS245 Tri-state Bus Transciever
RAM-U10           AS6C4008-55PCN 4mbit (512k x 8) Static RAM
RAM-U10 Socket    32-pin Wide DIP Socket
RAM-U12           74LS00 Quad NAND Gate
RAM-U13           74LS32 Quad OR Gate
ROM-U5            28C64 64k x 8 EEPROM
ROM-U5 Socket     28-pin Wide DIP Socket


Note:	All 74xx series logic ICs can be substituted for LS, ALS, ACT, F, or HCT .
```


## Built With

* [KiCAD EDA](http://www.kicad-pcb.org/)

## Authors

* **Rob Krenicki** - [rkrenicki](https://github.com/rkrenicki)

## License

This project is licensed under the Creative Commons - Attribution - ShareAlike 3.0 License

## Attribution

This board was derrived from works by, and contains sofware writen by the following:
* Sergey Kiselev (http://www.malinov.com/Home/sergeys-projects)
* James Pearce (https://www.lo-tech.co.uk/)
* Adrian Black
* Jacob Dorne of Monotech PCs (https://monotech.fwscart.com/)
* XTIDE Universal BIOS Team (http://www.xtideuniversalbios.org/)
