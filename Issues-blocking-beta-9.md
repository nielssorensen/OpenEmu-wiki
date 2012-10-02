### Grid view
Background dispatch queues were removed to fix the crashing but as a result we're back to slow/delayed scrolling. For the next beta test, we should at least fix the current upper left corner artifacts and the occasional empty view when switching libraries.

![Empty](http://f.cl.ly/items/1E0n2U340E0U1e171W1F/Screen%20Shot%202012-09-27%20at%205.40.16%20PM.png)

### Import scanning indicator
Since we ought to have this for 1.0, it will be helpful to have implemented for the next test to expose any issues that may come up.

![Importer](http://f.cl.ly/items/3V3y0q3I2Y0U1E0m1J0l/Screen%20Shot%202012-09-27%20at%209.39.23%20PM.png) &nbsp; ![Scanner](http://f.cl.ly/items/2u0o0A0i1i3K3u1p080C/Screen%20Shot%202012-09-27%20at%209.44.23%20PM.png)

### Setup assistant
We will want to implement gamepad setup as per [Issue #136](https://github.com/OpenEmu/OpenEmu/issues/136)

### Video hitching
Video code requires some optimization after the addition of the aspect ratio lookup. Currently some hitching/stuttering does occur.

### Unimplemented features
Context menu - 'Get Game Info From Archive.vg'
This is one of the few remaining features and we should decide how much of this needs to be implemented.
![Info](http://f.cl.ly/items/3V3v1X383A0i3q2R1x1e/OpenEmu%20-%20Grid%20View%20-%20Info%20Popover%20HUD%20Comparison.png.png)