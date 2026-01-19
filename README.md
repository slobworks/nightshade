<img width="1403" height="728" alt="bleh" src="https://github.com/user-attachments/assets/0c628db1-54d8-4dc7-ab72-cddfd8dc2e94" />
<img width="1403" height="728" alt="bleh_back" src="https://github.com/user-attachments/assets/9e196e01-706c-42dd-a6d1-3cd77d7ebac0" />
This is, for all intents and purposes, a maxed-out version of the open-source, Nightshade CL-GD542x VGA card project. This board has been built by me and its operation verified (it works). 
It's got the usual Nightshade features:

- Dedicated regulator for the internal RAMDAC, and TL431+MMBT3904 IREF circuit, for improved video quality
- Four-layer PCB and hand-tuned return paths for (hopefully) reduced noise pickup
- Supports N-well CL-GD542x chips, starting from late revision CL-GD5422 all the way up to CL-GD5429 (though you may have to change strapping resistors as needed)
- Custom footprints with longer pads for the more difficult components, to ease hand assembly using a soldering iron
- Emphasis on implementation simplicity (added regulator aside) for reduced part count and effort needed to assemble the board
- Silkscreen decorations drawn by me

The Killer Tomato variant was basically intended as a mild satire of what the 'ideal' Cirrus ISA VGA card should be, but then it kind of spiralled out of control and became an actually viable product of its own. And it's scalable: if you don't want specific functionality (such as the second megabyte, serial EEPROM or Vesa Feature Connector), then simply don't fit them.

Made in KiCAD 9.x.
Also includes gerber files so you can try it out for yourself.

Bill of materials (all parts are Surface Mount Device / SMD unless indicated otherwise):
- 1x Cirrus Logic CL-GD542x graphic chip, PQFP-160
- 2x (1MB) or 4x (2MB) 424260-compatible FPM 256Kx16 DRAM chips rated at least 70ns, SOJ-40 (this might require you to cannibalize parts from other broken cards, or roll the dice on eBay)
- 1x DIP-28 socket (2 needed for 16-bit BIOS mode)
- 1x 27C256 or compatible PROM/EPROM/flash ROM chip for BIOS, DIP-28 (2 needed for 16-bit BIOS mode)
- 1x 74HCT244, SSOP-20 or TSSOP-20 (2 needed for 16-bit BIOS mode)
- 1x LM334M, SOIC-8
- 1x LF50 or 78M05 5V LDO regulator, DPAK (https://www.digikey.com/en/products/detail/stmicroelectronics/LF50CDT-TR/591636)
- 1x TL431DBZ, SOT-23-5
- (Optional) 1x NM93C46 or equivalent SOIC-8 serial EEPROM (you need the one with x16 mode support)
- 1x DSUB-15-HD right angle through hole VGA connector (something akin to this: https://www.digikey.com/en/products/detail/assmann-wsw-components/A-HDF15A-KG-TAXB/1241905)
- 24x 0.22uF 0805/2012 metric ceramic caps of X5R/X7R type (0.1uF will likely work too)
- 4x 10uF 16V+ 2012/3216 metric ceramic caps of X5R/X7R type (these work well: https://www.digikey.com/en/products/detail/samsung-electro-mechanics/CL31B106KAHNNNE/3887462)
- 1x 22~100uF 16V 5mm x 5.3mm (or equivalent) SMD electrolytic capacitor - the higher the uF value, the better the performance, up to a point
- 2x 2.2u 0805/2012 metric ceramic caps of X5R/X7R type (1uF will likely work too)
- 1x 0.01uF / 10nF 0805/2012 metric ceramic capacitor of X5R/X7R type
- 5x 47pF 0805/2012 metric ceramic caps of C0G type
- 2x 18pF 0805/2012 metric ceramic caps of C0G type
- 1x 10K ohm 0805/2012 metric resistor
- 6x 6.8K ohm 0805/2012 metric resistors
- 1x 1K ohm 0805/2012 metric resistor
- 1x 300 ohm 0805/2012 metric resistor
- 1x 100 ohm 0805/2012 metric resistor
- 5x 75 ohm 0805/2012 metric resistors
- 2x 47 ohm 0805/2012 metric resistors
- 3x 33 ohm 0805/2012 metric resistors
- 3x 16 ohm 0805/2012 metric resistors
- 3x 0.22~22 ohm @ 100MHz, 1210/3216 metric ferrite beads
