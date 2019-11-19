# Tandy 1000 EX/HX 3-in-1 Expansion Board

This is a single expansion board designed for the Tandy 1000 EX and HX computers, to include the following upgrades:

* 640KB Base System Memory
* 96KB Upper Memory
* 16550-based DE9 Serial RS232 Port
* XT-IDE based CompactFlash "Hard Drive"

## Prerequisites

This board is for the Tandy 1000EX and 1000HX computers only.  It will not work in any other computer model as it is.
You must remove any expansion cards already in the computer, this is designed to be a single-board upgrade and has no provisions to allow for any other expansion cards.

## Installing

This board plugs into the Tandy PLUS interface, and takes up "Slot 2" on the rear of the computer.  Please be careful to align the PLUS bus connector before pushing down, to avoid bending pins on the computer.  Secure the backplate to the computer with two screws.
The IDE BIOS will automatically start and boot directly to the CF card on 1000EX machines.   1000HX loads a boot menu by default, and you will need to press F4 to load the IDE BIOS.  If you want to bypass the Tandy DOS ROM and boot menu, run "SETUPHX" and change the "Primary Start-up Device" to "DISK" and press F1 to save.

## Technical Details

This board has no configuration jumpers and is designed to be plug-and-play.  The only jumper is for write protecting the ROM.  Install the jumper to flash the XT-IDE BIOS, otherwise the jumper should be removed.

The board is hardwired with these memory locations/ports:
```
SRAM:  0x0000-0x5FFF, 0xC800-0xDFFF
UART:  0x3F8, IRQ 4
IDE:   0x300
ROM:   0xC000-0xC7FF
```

## Assembly Notes
All functions of the board are independent, and no parts are shared beyond power delivery.  If you do not want to use a specific function, you can safely omit any parts referenced with the function in the name (such as "232" for RS232).
The backplate for the CF card must have a hole created for the DE9 Serial connector.   I recommend not soldering down the DE9 Male connector until after the hole is made, and the CF adapter is mounted to the board.


## Bill of Materials
|Ref(s)        |Mouser Part Number  |Description                                                     
|--------------|--------------------|----------------------------------------------------------------
|BUS1          |710-61306421821     |2x31 2.54mm Header Socket (Cut off last two pins of 2x32 header)
|R1 through R3 |299-10K-RC          |10kOhm 1/8w Resistor
|C1 through C16|594-K104M15X7RF53L2 |0.1uF Multilayer Ceramic Capacitor, 2.5mm Lead Spacing
|CP1           |80-A750EK107M1CAAE18|100uF 16V Polymer Capacitor, 2.5mm Lead Spacing
|232-OSC1      |774-MXO45HS-3C-1.8  |1.8432Mhz 1/2-size Oscillator
|232-P2        |806-K22X-E9P-N-99   |DE9 Male Right Angle Connector   
|232-U6        |595-GD75232N        |GD75232N RS232 Driver
|232-U7, 232-U9|595-SN74HCT138N     |74LS138 3-to-8 Line Demux
|232-U8        |701-ST16C550IJ44-F  |16550/16C550 UART in PLCC-44 Package 
|232-U8 Socket |940-44-044-24-000000|PLCC-44 Through Hole Socket
|CF-J1         |n/a                 |2x20 2.54mm Header Socket, 11mm height.
|CF-J2         |200-CES10101TD      |1x2 2.54mm Header Socket
|CF-U1         |595-SN74HCT139N     |74LS129 Dual 2-to-4 Demux
|CF-U2, ROM-U4 |595-CD74HCT688E     |74LS688 8-bit Comparator
|CF-U3, RAM-U11|595-SN74HCT245N     |74LS245 Tri-state Bus Transciever
|RAM-U10       |913-AS6C4008-55PCN  |AS6C4008-55PCN 4mbit (512k x 8) Static RAM
|RAM-U10 Socket|649-DILB32P223TLF   |32-pin Wide DIP Socket
|RAM-U12       |595-SN74HCT00N      |74LS00 Quad NAND Gate
|RAM-U13       |595-SN74HCT32N      |74LS32 Quad OR Gate
|ROM-JP1       |855-M20-9990246     |1x2 2.52mm Header
|ROM-JP1 Jumper|806-SX1100-B        |2.54mm Jumper Shunt
|ROM-U5        |556-AT28C64B15PU    |28C64 64k x 8 EEPROM
|ROM-U5 Socket |649-DILB28P223TLF   |28-pin Wide DIP Socket


Note:	All 74LSxx series logic ICs can be substituted for ALS, ACT, F, or HCT .


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
* Adrian Black (https://www.youtube.com/user/craig1black/featured)
* Jacob Dorne of Monotech PCs (https://monotech.fwscart.com/)
* XTIDE Universal BIOS Team (http://www.xtideuniversalbios.org/)

## README TO-DO
* Assembly Instructions
* BIOS Flashing Instructions
