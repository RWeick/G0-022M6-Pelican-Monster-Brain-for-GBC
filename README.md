# G0-022M6-Pelican-Monster-Brain-for-GBC
The schematics, PCB, and flash dumps of three versions of the GBC Pelican Monster Brain.

Version 1.1 is for Pokemon Red and Blue, and comes in a case with a blue BrainBoy sticker/logo.
Version 2.0 is for Pokemon Gold and Silver, and comes in a case with a gold BrainBoy sticker/logo.
Version 3.6 is for every Gameboy Pokemon edition, and comes in a case with a purple Monster Brain sticker/logo.

All components labeled "Unknown" in the schematic were not present on the commercial PCB. This PCB is used for both the Monster Brain and the Codebreaker, and the missing components are present when this board is used in a Codebreaker.

The CPLD is the same between all devices.

The Colorizer button PCB wires solder to the inner two pads of the 4 at the rear top edge of the PCB.

Jumper configuration for normal operation: 

- J1: Pads 2 and 3 are shorted.
- J2: Open.
- J3: Shorted.
- J4: Shorted.

The CPLD functions I've been able to deduce are as follows:

A read must be performed at address 0x100 in order to enable address banking in the CPLD.

The write address to change banks is 0xA000.

The full rom is available from 0x2000 to 0x3FFF by switching either 32 or 64 banks depending on the device. The blue label Brainboy has 64 banks, and the rest of the devices use 32 banks due to smaller eeproms. The maximum known EEPROM size included with an off the shelf device is 512 KB.

PCB Thickness: 0.8 mm

![image](https://github.com/RWeick/G0-022M6-Pelican-Monster-Brain-for-GBC/blob/main/MonsterBrain.png)
![image](https://github.com/RWeick/G0-022M6-Pelican-Monster-Brain-for-GBC/blob/main/ButtonBoard.png)
