Nightshade is a collection of attempts at making video cards based upon the Cirrus Logic CL-GD542x chipset. They're based on Cirrus Logic's reference schematics, but with a few added features to hopefully set it apart from your average CL-GD542x video card:
- Dedicated regulator for the internal RAMDAC for improved video quality
- Four-layer PCB and hand-tuned return paths for (hopefully) reduced noise pickup
- Supports N-well CL-GD542x chips, starting from late revision CL-GD5422 all the way up to CL-GD5429 (though you may have to change strapping resistors as needed)
- Judicious usage of resistor arrays and an emphasis on implementation simplicity (added regulator aside) for reduced part count and effort needed to assemble the board

Made in KiCAD 8.0something.
Also includes gerber files so you can try it out for yourself.
