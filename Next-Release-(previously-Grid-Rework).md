### three weeks?

***

### Image Rework
- use jpg as default (which compression factor?)
- don't generate thumbnails (atm new grid view does not support images at different sizes)
- migrate from old version
 - Delete thumbnails
 - Run background thread to convert pngs to jpg (save disk space, avoid hard drive as bottleneck for loading grid images)
 - save image format in core data so we keep track of which images to convert between launches

***

### Grid Rework
- caching layers properly
- fix layout
- implement spinner, file missing and drop indication layers
- ~~ratings~~
- ~~renaming items (field editor)~~
- drag and drop onto items (aka updating cover image)
- ~~selection of items without image~~
- animation (done but they have a 0.0s duration)
- ~~drag and drop (importing files/cover art/adding to collection)~~
- ~~rename~~
- improve missing artwork image (custom NSImage overriding drawInConetxt: so we can always draw without scaling?)
- grid scaling (always uses the same image for the grid, not the appropriately sized one; number needs to be the grid cell size) https://github.com/OpenEmu/OpenEmu/blob/NewGridView/OpenEmu/OEDBDataSourceAdditions.m#L122

***

### Misc
- Fix input issues :P
- can we keep track of battery saves?
- are OpenVGDB ids persistent? should we add them to the core data store?
- add default cover art aspect ratio to system plugins (localised)
