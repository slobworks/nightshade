This is the SMD ISA version of the Nightshade CL-GD542x VGA card project. This board has been built by me and its operation verified (it works). 
It's got the usual Nightshade features:
- Dedicated regulator for the internal RAMDAC for improved video quality
- Four-layer PCB and hand-tuned return paths for (hopefully) reduced noise pickup
- Supports N-well CL-GD542x chips, starting from late revision CL-GD5422 all the way up to CL-GD5429 (though you may have to change strapping resistors as needed)
- Custom footprints with longer pads for the more difficult components, to ease hand assembly using a soldering iron
- Emphasis on implementation simplicity (added regulator aside) for reduced part count and effort needed to assemble the board
- Silkscreen decoration on opposite side of card drawn by me

Made in KiCAD 8.0something.
Also includes gerber files so you can try it out for yourself.

Bill of materials (all parts are Surface Mount Device / SMD unless indicated otherwise):
- 1x Cirrus Logic CL-GD542x graphic chip, PQFP-160
- 2x 424260-compatible FPM 256Kx16 DRAM chips rated at least 70ns, in SOJ-40 format (this might require you to cannibalize parts from other broken cards, or roll the dice on eBay)
- 1x 27C256 or compatible PROM/EPROM/flash ROM chip for BIOS, in DIP-28 format
- 1x 74HC244 in SSOP-20 format
- 1x LM334M in SOIC-8 format
- 1x 1N4148 or compatible diode in SOD-323 format
- 1x DSUB-15-HD connector (something akin to this: https://www.digikey.com/en/products/detail/assmann-wsw-components/A-HDF15A-KG-TAXB/1241905)
- A big bunch (order at least 25 for the best price break) of 0.22uF 0805/2012 metric ceramic caps of X5R or X7R type
- 3x 12pF 0805/2012 metric ceramic caps of C0G type
- 3x 75 ohm 0805/2012 metric resistors
- 3x 0805/2012 metric ferrite beads, rated for 20-50 ohms DCR @ 100MHz
- 5x 6.8K ohm 0805/2012 metric resistor
- 1x 15 ohm 0805/2012 metric resistor
- 1x 150 ohm 0805/2012 metric resistor
- 1x 100 ohm 0805/2012 metric resistor
