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


## Built With

* [KiCAD EDA](http://www.kicad-pcb.org/)

## Authors

* **Rob Krenicki** - *Initial work* - [rkrenicki](https://github.com/rkrenicki)

## License

This project is licensed under the Creative Commons - Attribution - ShareAlike 3.0 License

## Attribution

This board was derrived from works by the following:
* Sergey Kiselev
* James Pearce
* Adrian Black
