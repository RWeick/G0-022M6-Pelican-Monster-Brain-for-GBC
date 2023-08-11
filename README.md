# G0-022M6-Pelican-Monster-Brain-for-GBC
The schematics, PCB, and flash dumps of three versions of the GBC Pelican Monster Brain.

Version 1.1 is for Pokemon Red and Blue, and comes in a case with a blue BrainBoy sticker/logo.
Version 2.0 is for Pokemon Gold and Silver, and comes in a case with a gold BrainBoy sticker/logo.
Version 3.6 is for every Gameboy Pokemon edition, and comes in a case with a purple Monster Brain sticker/logo.

All components labeled "Unknown" in the schematic were not present on the commercial PCB. This PCB is used for both the Monster Brain and the Codebreaker, and the missing components are present when this board is used in a Codebreaker.

The Colorizer button PCB wires solder to the inner two pads of the 4 at the rear top edge of the PCB.

Jumper configuration for normal operation: 

- J1: Pads 2 and 3 are shorted.
- J2: Open.
- J3: Shorted.
- J4: Shorted.

The CPLD functions I've been able to deduce are as follows:

The bank write address to change banks is 0xA000.

The full rom is available from 0x4000 to 0x5FFF by switching either 32 or 64 banks depending on the device. The blue label Brainboy has 64 banks, and the rest of the devices use 32 banks due to smaller eeproms.

To enable access to the full rom, dummy reads must be performed to mirror the initial boot reads for the logo, as well as reading 8 KB from 0x0 to 0x1FFF and 8 KB from 0x2000 to 0x3FFF using bank switching. 

It is likely that not all of these reads are necessary, but I have not yet determined which specific reads in those ranges are the actual triggers.

PCB Thickness: 0.8 mm

![image](https://github.com/RWeick/G0-022M6-Pelican-Monster-Brain-for-GBC/blob/main/MonsterBrain.png)
![image](https://github.com/RWeick/G0-022M6-Pelican-Monster-Brain-for-GBC/blob/main/ButtonBoard.png)
