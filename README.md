# Z-Controller_mod

My variant of the Z-Controller by KOE, intended to be used with the firmware by fomonster (slightly adapted by me).

Original gerbers & CPLD/MCU programming files here: https://github.com/koe1234/Z-controller/tree/main

fomonster firmware here: https://github.com/fomonster/zcontroller

Redrawn from images before the gerbers were released. Prototyped in early 2024/late 2024.

Changes: 
- modernized SD card slot, since the original is hard to buy nowadays (search for "uxcell sd slot" - should be available on eBay, amazon, etc.), added solder jumper for different configurations of the pinout on the back
- added jumper to disable the PS/2 keyboard (thanks to black_cat - https://zx.clan.su/forum/8-170-1) to allow loading from tape
- added solder jumper for !IORQGE generation for the NemoIDE interface when using the fomonster firmware
- added solder jumper for "Power over IDE" when using "Disk on Module" HDDs
- modified pinout of the CPLD and minor changes to the MCU (both via firmware based on fomonster's github, no change to PCB in case you want to use the KOE firmware/KR1878VE1 MCU) for the "DualPIC Addon" since the fomonster firmware occasionally hangs when using mouse + keyboard at the same time
- designed "DualPIC Addon" daughterboard which plugs into DA1, DD2 and pins 3-10 on X7, which uses PIC16F628a MCUs, since KR1878VE1 ones are not easy to get and has fancy (optional) LEDs for mouse/keyboard activity
- added silkscreen layer according to documentation
- various PCB graffiti (Zilog logo, PCB Patch image, "Death to all fascists!" and adjusted credits)

Main layout is still being prototyped, DualPIC addon is done.
