# Readme

This example configuration is for a 3KU (2017) with a printable bed diameter of 200mm and a height of 280mm. It also has the auto bed leveling probe (BLTOUCH) and the heated bed activated.

These configurations activate many of the new advanced features of the Marlin firmware:

 * Auto Calibration
 * Auto Bed Leveling
 * Pause & Filament Change

**Important**: Before doing anything else after updating the firmware, go to `Configuration > Advanced Settings > Initialize EEPROM` to get rid of old configurations.

Then you should execute `Configuration > Delta Calibration > Set Delta Height` and also run `Configuration > Delta Configuration > Probe Z-offset` to verify the Probe offset.

After that you should connect the Z-Probe and start `Configuration > Delta Calibration > Auto Calibration`. When it's done don't forget to also do `Configuration > Delta Calibration > Store Settings` to make it permanent.

You should also do a `Motion > Bed Leveling > Level bed` followed by `Store Settings` to ensure a perfect leveling.

Please do a manual paper test (moving the nozzle slowly down to Z0 and checking with a piece of paper). If it's not perfect, use `Configuration > Advanced Settings > Probe Z Offset` to correct the difference and execute the calibration again.

## Configuration
You might need (or want) to edit at least the following settings in `Configuration.h`:
* `MANUAL_Z_HOME_POS` - The available height of your printing space. Auto Bed Leveling makes it less important to have the exact value.
* `DELTA_PRINTABLE_RADIUS` - The printable radius is how far from the center the nozzle can reach.
* `DEFAULT_AXIS_STEPS_PER_UNIT` - Steps-per-millimeter for the delta steppers, and for the extruder [to optimize the amount of filament flow](http://zennmaster.com/makingstuff/reprap-101-calibrating-your-extruder-part-1-e-steps).

### Fine tuning
* Increase `DELTA_RADIUS` if the model comes out convex (with a bulge in the middle)
* Increase `DELTA_DIAGONAL_ROD` if the model comes out larger than expected

## Join us
Tune in to our 3KU Owners Club on Discord, https://discord.com/channels/513703242929274880/513703242929274882