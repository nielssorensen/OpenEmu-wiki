### <s>Grid view</s>
<s>Background dispatch queues were removed to fix the crashing but as a result we're back to slow/delayed scrolling. For the next beta test, we should at least fix the current upper left corner artifacts, library spillover and the occasional empty view when switching libraries. It may also be worth exploring alternatives like [MUPhotoView](https://github.com/blakeseely/muphotoview).</s> Fixed in https://github.com/OpenEmu/OpenEmu/commit/e12d2f51e949fd16d3112bcc2857a602ad5b3593

![Spillover](http://f.cl.ly/items/3J3Q0h301a0S0N202g2f/Screen%20Shot%202012-10-02%20at%206.02.37%20PM.png)

![Empty](http://f.cl.ly/items/1E0n2U340E0U1e171W1F/Screen%20Shot%202012-09-27%20at%205.40.16%20PM.png)

### <s>Import scanning indicator</s>
<s>Since we ought to have this for 1.0, it will be helpful to have implemented for the next test to expose any issues that may come up.</s> Added in https://github.com/OpenEmu/OpenEmu/commit/0ab557a435a5d67c88a068e982472ef00924d69c

![Importer](http://f.cl.ly/items/3V3y0q3I2Y0U1E0m1J0l/Screen%20Shot%202012-09-27%20at%209.39.23%20PM.png) &nbsp; ![Scanner](http://f.cl.ly/items/2u0o0A0i1i3K3u1p080C/Screen%20Shot%202012-09-27%20at%209.44.23%20PM.png)

### Setup assistant
We will want to implement gamepad setup as per [Issue #136](https://github.com/OpenEmu/OpenEmu/issues/136)

### <s>Video hitching</s>
<s>Video code requires some optimization after the addition of the aspect ratio lookup. Currently some hitching/stuttering does occur.</s> Fixed in https://github.com/OpenEmu/OpenEmu/commit/98d0adc8a1ad20df38d422b884e9464bf545b5d2

### Unimplemented features
Context menu - 'Get Game Info From Archive.vg'
This is one of the few remaining features and we should decide how much of this needs to be implemented.
![Info](http://f.cl.ly/items/3V3v1X383A0i3q2R1x1e/OpenEmu%20-%20Grid%20View%20-%20Info%20Popover%20HUD%20Comparison.png.png)