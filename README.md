![front](https://github.com/user-attachments/assets/7549e81b-25af-42e6-b017-eb23f1c58a5b)
![back](https://github.com/user-attachments/assets/0670de9a-8a0f-4417-bb97-4d286bad9976)
This is the SMD ISA version of the open-source Nightshade CL-GD542x VGA card project. This board has been built by me and its operation verified (it works). 
It's got the usual Nightshade features:
- Dedicated regulator for the internal RAMDAC for improved video quality
- Four-layer PCB and hand-tuned return paths for (hopefully) reduced noise pickup
- Supports N-well CL-GD542x chips, starting from late revision CL-GD5422 all the way up to CL-GD5429 (though you may have to change strapping resistors as needed)
- Custom footprints with longer pads for the more difficult components, to ease hand assembly using a soldering iron
- Emphasis on implementation simplicity (added regulator aside) for reduced part count and effort needed to assemble the board
- Silkscreen decoration on opposite side of card drawn by me

Made in KiCAD 9.x.
Also includes gerber files so you can try it out for yourself.

Bill of materials (all parts are Surface Mount Device / SMD unless indicated otherwise):
- 1x Cirrus Logic CL-GD542x graphic chip, PQFP-160
- 2x 424260-compatible FPM 256Kx16 DRAM chips rated at least 70ns, SOJ-40 (this might require you to cannibalize parts from other broken cards, or roll the dice on eBay)
- 1x 27C256 or compatible PROM/EPROM/flash ROM chip for BIOS, DIP-28
- 1x 74LS244/74HCT244, SSOP-20 
- 1x LM334M, SOIC-8
- 1x LDK320AM50R 5V LDO regulator, SOT-23-5 (https://www.digikey.com/en/products/detail/stmicroelectronics/LDK320AM50R/6192780)
- 1x 1N4148 or compatible diode, SOD-323
- 1x DSUB-15-HD right angle through hole VGA connector (something akin to this: https://www.digikey.com/en/products/detail/assmann-wsw-components/A-HDF15A-KG-TAXB/1241905)
- 20x 0.22uF 0805/2012 metric ceramic caps of X5R/X7R type
- 4x 10uF 16V+ 2012/3216 metric ceramic caps of X5R/X7R type (these work well: https://www.digikey.com/en/products/detail/samsung-electro-mechanics/CL31B106KAHNNNE/3887462)
- 2x 2.2u 0805/2012 metric ceramic caps of X5R/X7R type
- 1x 0.01uF / 10nF 0805/2012 metric ceramic capacitor of X5R/X7R type
- (Optional) 2x 100pF 0805/2012 metric ceramic capacitor of C0G type (if needed)
- 2x 47pF 0805/2012 metric ceramic caps of C0G type
- 2x 18pF 0805/2012 metric ceramic caps of C0G type
- 3x 12pF 0805/2012 metric ceramic caps of C0G type
- 1x 10K ohm 0805/2012 metric resistor
- 5x 6.8K ohm 0805/2012 metric resistor
- 1x 150 ohm 0805/2012 metric resistor
- 1x 100 ohm 0805/2012 metric resistor
- 5x 75 ohm 0805/2012 metric resistors
- 2x 47 ohm 0805/2012 metric resistors
- 3x 33 ohm 0805/2012 metric resistors
- 1x 15 ohm 0805/2012 metric resistor
- 1x 0 ohm 0805/2012 metric resistor (to enable 0 waitstate mode; depending on BIOS this may not be needed)
- 3x 0805/2012 metric ferrite beads, rated for 20-50 ohms DCR @ 100MHz
- 1x 14.31818MHz 2-pin SMD crystal, 5032 
- (Optional) 1x 2.54mm pitch 2-pin through hole header (to enable IRQ 9 if needed)
- 1x Keystone 9200-1 I/O bracket (https://www.digikey.com/en/products/detail/keystone-electronics/9200-1/317282)
