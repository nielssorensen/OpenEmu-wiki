### three weeks?

***

### Image Rework
- ~~use jpg as default (which compression factor?)~~
- ~~don't generate thumbnails (atm new grid view does not support images at different sizes)~~
- ~~migrate from old version~~
 - ~~Delete thumbnails~~
 - ~~Run background thread to convert pngs to jpg (save disk space, avoid hard drive as bottleneck for loading grid images)~~
 - ~~save image format in core data so we keep track of which images to convert between launches~~
 - Add indicator for migration progress

***

### Grid Rework
- Fix drag
- Fix drop (highlight & don't accept images on whole view)
- Improve layout (http://imgur.com/a/QNQBM, new grid at bottom)

***

### Misc
- Fix input issues :P
- can we keep track of battery saves?
- ~~are OpenVGDB ids persistent? should we add them to the core data store?~~
- ~~add default cover art aspect ratio to system plugins (localised)~~
- add support for multi-rom archives (is the stuff in multi-rom-archives branch working?)