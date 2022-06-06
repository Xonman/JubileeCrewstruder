# Crewstruder printhead
![Rendering of a Crewstruder](https://github.com/Xonman/JubileeCrewstruder/raw/main/images/Crewstruder%20v25%20cropped.png)
An afterburner-inspired printhead for the Jubilee3d Toolchanger.
The BMG tool for the Jubilee is a little utilitarian to look at. The Baby Bullet is a big step forward but when equipped with both 5015s is too wide to fit 5 tools.
This project is an effort to make a printhead which has good cooling from all angles, fits 5 tools and is at least a bit interesting to look at.

## Project goals
- Maximum width of 65mm to allow for 5 tools on a standard Jubilee frame
- Equal cooling from either side (or as close to as possible)
- Minimumise tool depth to avoid losing Y build volume
- Built-in cable management
- Space for a CAN toolboard (not a Duet3 1LC)
- Easy on the eyes

## Parts list
- 1x Dragon hotend (no groove-mount adapter)
- 1x 2510 hotend fan (a Slice Engineering Mosquito hotend fan works well)
- 1x Orbiter v2 extruder
- 1x Good quality 5015 blower fan (gdstime or Delta recommended)
- 1x heater to fit a Dragon hotend
- 1x thermister to fit a Dragon hotend
- 4x M2.5 8mm countersunk bolts
- 8x M3 10mm buttonhead bolts
- 3x M3 6mm countersunk bolts
- Jubilee tool mounting hardware (8mm threaded balls, tool wedge)
- 8x 4mm outer, 5mm long M3 heatset inserts (standard Jubilee BOM inserts _may_ fit)
- 42.2mm Bowden tube

## Printing instructions
Print 1 of each part with the following settings.

### Front plate
Orient face-down.
If you want a nice logo then use the Split Bodies to Parts feature to separate out the logo.
Use any material here, it doesn't cop any heat or mechanical load.
- 0.2mm layer height
- At least 3 walls
- Infill irrelevant (tested at 10%)
- Supports are not required if you have good bridges, otherwise supports should be placed by hand as per the below image
- Very high (like 100%) fan speed for the first 5.2mm (26 layers)

### Mid plate
Orient with the large void facing down.
PLA should work but PETG or any higher temp material would be better since the hotend is in close proximity.
- 0.2mm layer height
- At least 4 walls so the heatset inserts have some plastic to set into
- Infill as you like (tested at 10%)
- No supports are required

### Dragon mount
Orient with the flat side down.
PLA is fine here.
- 0.2mm layer height
- No supports required
- Ensure thin walls are enabled as the tips of this part get skinny
- Lots of cooling for the top

### Tool mounting plate
Orient with the flat side down, cutout for the tool wedge up.
Ideally a stiff material that doesn't suffer creep should be used. This part is blasted with the air coming off the hotend heatsink as well as under mechanical load. I've been using ASA successfully with no creep.
- 0.2mm layer height
- 100% infill - this part takes the pressure of the tool lock so needs to be strong
- No supports are required


## Assembly instructions
### Front plate assembly
- Take the 5015 blower and pop the front cover off it, and then throw it away. It won't fit after the next step.
- Using a hacksaw, Dremel, sander or any other abrasive force remove the screw mount wings and face clips from the 5015 so that you have a nice smooth circle (ish, it's not really a circle), and then test fit the fan to the front plate. If the fit is good, go ahead and run the cable down the cable management slot. The rear of the fan housing should roughly be flush with the back of the front plate.
- Using a long screw, small screwdriver or hex key punch out the hole bridge in the 3 mounting holes. These were used to make good quality holes during printing.
- Test-fit 3x M3 10mm bolts down the above holes. If they fit you can leave them there, otherwise gently embiggen these holes with a suitably sized drill bit.
- Test fit the 2510 hotend fan. It should slide in easily but not move around. Gently remove it after checking the fit.

### Dragon mount assembly
- Assemble the hotend with heater, thermistor and nozzle (only finger tight for now).
- Fit the Dragon to the mount with the long end of the heater facing away from the mount.
- Fix the Dragon in place with the 4x M2.5 bolts.
- The dragon should fit neatly into the recess in the top of the mount, and be held securely against the support at the bottom of the heatsink. You should not be able to easily move the hotend around at this point.

### Rear plate assembly
- Fit the 8mm thread balls to the 3 recessed holes in the rear of the plate, and tighten down with the 3x M3 6mm countersunk bolts. You might consider threadlocking these in place as they're hard to get at after assembly.
- Place the wedge plate into the wedge plate shaped recess with the cutout parallel to the bottom of the rear plate.
- Insert the 3x M3 12mm countersunk bolts through the 3 holes in the wedge.
- The above bolts will meet the Dragon mount soon, but do not assemble them yet or assembling the centre plate will be impossible.
- You should now have the Dragon secured firmly to the rear plate.

### Centre plate assembly
- Using the plate-set approach as per the Jubilee documentation fit the heatset inserts into the following holes:
- Place the 2510 hotend fan on the front of the plate, oriented so that it blows air into the centre plate. The fan wires _should_ line up with the wire management channel but are a very snug fit. Using something smooth and round-ish (like the shaft of a small screwdriver) gently coax them into place. Don't use anything sharp or the wires may be damaged.
- While ensuring the fan wires aren't crushed place the front plate over the fan and tighten down the front M3 bolts. They don't need to be gorilla-tight but there is lots of meat supporting them so no need to be gentle.
- Push the Dragon mount into the back of the centre plate so that the bottom of the plate lines up with the corresponding bottom of the centre plate.
- Run the heater wires up one channel and the thermistor wires up the other. Depending on your heater cartridge you may need to trim some of the silicone insulation. Ensure both wires are nestled neatly inside the channel and won't be crushed by the rear plate.
- Place the rear plate over the rear of the centre plate, ensuring the bolts going through the wedge align with the corresponding holes in the Dragon mount.
- Tighten down the rear plate to the centre plate using M3 12mm bolts using the holes on either side of the air outlets and above the top tool ball.
- Tighten down the bolts going through the wedge plate. The mount is now tightly sandwiched between centre and rear plates so don't go hercules on these as they're plastic threads.
- Carefully cut 42.2mm of Bowden tube, ensuring the cuts at either end are as square as possible. Inserting some spare filament while cutting will help avoid crushing the tube and causing un-square cuts. You might also want to chamfer the inside of one end, but be sure to remove any PTFE dust afterwards as this could clog your nozzle.
- Shove the Bowden tube down the hole on top of the centre plate. You should have a small amount still protruding which will fit into the bottom of the Orbiter.
- Place the Orbiter on top in the only orientation it fits and then tighten down with 2x M3 10mm bolts.



