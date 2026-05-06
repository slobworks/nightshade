<img width="1403" height="728" alt="bleh" src="https://github.com/user-attachments/assets/2d38e60e-668a-4ffd-a3fb-56545c47bddd" />
<img width="1403" height="728" alt="bleh_back" src="https://github.com/user-attachments/assets/8c4ee3c1-624e-43ec-99eb-0506bbc9097b" />
<b>Update!</b> I think I've neglected the mainline version long enough. Here's my attempt at bringing the mainline, non-satirical version up to parity with the satire. Incorporates a *lot* of changes as well as almost all the functionality of the "pro" version, except several things are marked as optional. Also incorporates too many bugfixes for me to count or keep track of.

This is the SMD ISA version of the open-source Nightshade CL-GD542x VGA card project. This board has been built by me and its operation verified (it works). 
It's got the usual Nightshade features:
- Dedicated regulator for the internal RAMDAC for improved video quality, using a part that is abundant and very inexpensive
- Four-layer PCB and hand-tuned return paths for (hopefully) reduced noise pickup
- Supports N-well CL-GD542x chips, starting from late revision CL-GD5422 all the way up to CL-GD5429 (though you may have to change strapping resistors as needed)
- Custom footprints with longer pads for the more difficult components, to ease hand assembly using a soldering iron
- Emphasis on implementation simplicity (added regulator aside) for reduced part count and effort needed to assemble the board
- Silkscreen decoration on opposite side of card drawn by me

Made in KiCAD 9.x.
Also includes gerber files so you can try it out for yourself.

Bill of materials (all parts are Surface Mount Device / SMD unless indicated otherwise):
- 1x Cirrus Logic CL-GD542x graphic chip, PQFP-160
- 2x (1MB) 424260-compatible FPM 256Kx16 DRAM chips rated at least 70ns, SOJ-40 (this might require you to cannibalize parts from other broken cards, or roll the dice on eBay)
- 1x DIP-28 through-hole socket (2 needed for 16-bit BIOS mode)
- 1x 27C256 or compatible PROM/EPROM/flash ROM chip for BIOS, DIP-28 (2 needed for 16-bit BIOS mode)
- 1x 14.31818MHz 5032 SMD crystal (https://www.digikey.com/en/products/detail/qst/QT532G-14-31818MBBK-T/26975047)
- 1x 74HCT244, SSOP-20 or TSSOP-20 (2 needed for 16-bit BIOS mode)
- 1x 78L05 5V LDO regulator, TO-92 (https://www.digikey.com/en/products/detail/diodes-incorporated/AS78L05Z-E1/4570493)
- 1x TL431DBZ, SOT-23-3 (https://www.digikey.com/en/products/detail/texas-instruments/TL431BQDBZR/714694)
- 1x MMBT3904 NPN small signal transistor, SOT-23-3  (https://www.digikey.com/en/products/detail/taiwan-semiconductor-corporation/MMBT3904H-RFG/26741367)
- (Optional) 1x NM93C46 or equivalent SOIC-8 serial EEPROM (you need the one with x16 mode support) - you WILL need to initialize the serial EEPROM with a valid image *before* assembling it onto the card. Please check the directory /seeprom to get a generic image with all sub-1280x1024 SVGA refresh rates set to 60 Hz. You will also need a BIOS image from an *ISA* GD542x card for the SEEPROM functionality to work; most generic 542x BIOSes were compiled for the VLB variants, which this functionality is disabled.
- 3x 2-pin, 2.54mm pitch male jumper connectors
- (Optional) 1x 2x13 pin, 2.52mm pitch male header for VESA Feature Connector
- 1x DSUB-15-HD right angle through hole VGA connector (something akin to this: https://www.digikey.com/en/products/detail/assmann-wsw-components/A-HDF15A-KG-TAXB/1241905)
- 25x 0.1uF 0805/2012 metric ceramic caps of X5R/X7R type (https://www.digikey.com/en/products/detail/samsung-electro-mechanics/CL21B104KACNNNC/3886757)
- 7x 10uF 16V+ 2012/3216 metric ceramic caps of X5R/X7R type (these work well: https://www.digikey.com/en/products/detail/samsung-electro-mechanics/CL31B106KAHNNNE/3887462)
- 1x 22~100uF 16V 5mm x 5.3mm (or equivalent) SMD electrolytic capacitor - the higher the uF value, the better the performance, up to a point
- 4x 2.2u 0805/2012 metric ceramic caps of X5R/X7R type (1uF will likely work too)
- 1x 0.01uF / 10nF 0805/2012 metric ceramic capacitor of X5R/X7R type
- 5x 47pF 0805/2012 metric ceramic caps of C0G type
- 2x 18pF 0805/2012 metric ceramic caps of C0G type
- 1x 10K ohm 0805/2012 metric resistor
- 6x 6.8K ohm 0805/2012 metric resistors
- 3x 1K ohm 0805/2012 metric resistor
- 1x 300 ohm 0805/2012 metric resistor
- 1x 100 ohm 0805/2012 metric resistor
- 5x 75 ohm 0805/2012 metric resistors
- 1x 47 ohm 0805/2012 metric resistor
- 6x 33 ohm 0805/2012 metric resistors
- 3x 16 ohm 0805/2012 metric resistors
- (Optional) 1x PTC resettable, 9V 200mA, 0805/2012 metric polyfuse (https://www.digikey.com/en/products/detail/littelfuse-inc/0805L020YR/1212820) - this is only needed if you want to supply +5V to pin 9 of the VGA connector
- 3x 0.22~22 ohm @ 100MHz, 1210/3216 metric ferrite beads
