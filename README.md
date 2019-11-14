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
Ref(s)		Value
-------------------------------------------
U1		AT28C64B DIP-28 (EEPROM)
U2-U3		74HCT688 SOIC-20 7.52mm
U4		74HCT32 SOIC-14
U5		74HCT04 SOIC-14
SW1-SW2		SPDT Slide Switch, right angle (CnK OS102011MA1QN1)
SW3-SW4		3-position DIP Switch (Piano, 2.54mm) (Best to get two colours; piano style is optional)
RN1-RN3		10K x 4 Isolated Resistor Array - 4x1206 SMD
RN4		1K x 4 Isolated Resistor Array - 4x1206 SMD
R1		5.6K 0805 SMD Resistor
D1		3mm LED
P1		3M N7E50-7516TS0884 CF Card Socket
C1-C6		10 - 100nF  0805 SMD Capacitor
C7-C8		10uF 0805 SMD Capacitor
SOCKET		28-pin IC Socket (wide type) (for EEPROM)

Note:	All 7400 series logic ICs can be substituted for LS, ALS, ACT, F, or HCT equivalents.
	74*688 and 74*521 are identical ICs. Locally, Texas Instruments 74F521 is cheapest for some reason so I use those.
	PCB can be adjusted for more common CF card types; I just had a bunch of these to use.
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
