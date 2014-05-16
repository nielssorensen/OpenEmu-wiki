### three weeks?

***

### Image Rework
- ~~use jpg as default (which compression factor?)~~
- ~~don't generate thumbnails (atm new grid view does not support images at different sizes)~~
- ~~migrate from old version~~
 - ~~Delete thumbnails~~
 - ~~Run background thread to convert pngs to jpg (save disk space, avoid hard drive as bottleneck for loading grid images)~~
 - ~~save image format in core data so we keep track of which images to convert between launches~~
 - ~~Add indicator for migration progress~~
 - ~~Improve behaviour when migration fails for an image (usually caused by missing artwork file, remove box image, schedule for syncing if automatic lookup is enabled)~~
 
***

### Grid Rework
- ~~Fix drag~~
- ~~Fix drop (highlight & don't accept images on whole view)~~
- ~~Improve layout (http://imgur.com/a/QNQBM, new grid at bottom)~~
- Try to avoid black images

***

### Core Data Rewirte
- Fix moving game library folder
- check save states
- check rom lookup (after import, initiated by context menu, on app launch)
- reduce core data saves
 - ~~OpenVGDB sync could save every 5 seconds or after x items~~
 - same for importer
- check how openvgdb lookup behaves when no internet connection is available
- see if reloading collection view can be optimised (right now we reload on every main context save)
- Test Importer
 - ~~Single roms~~
 - ~~Directories~~
 - ~~Large data set~~
 - ~~Lookup~~
 - Copy / organize
 - Archived roms
 - Multi-rom archives
 - arcade (multi-file archive, single rom)
 - cd based systems (bin / cue), especially issue resolving
- don't hide game scanner with active import issues

***

### Misc
- Fix input issues :P
- can we keep track of battery saves?
- ~~are OpenVGDB ids persistent? should we add them to the core data store?~~
- ~~add default cover art aspect ratio to system plugins (localised)~~
- add support for multi-rom archives (is the stuff in multi-rom-archives branch working?)
 - ~~import~~
 - ~~deletion~~
 - ~~launching~~
 - ~~lookup~~
 - ~~migration~~, not tested, but should be fine
 - ~~move library~~
 - ~~save state directories~~
- ~~Fix coredata deadlock on quit (caused by saving child contexts when app terminates, temporarily fixed by ignoring changes in child contexts)~~
- ~~rewrite secrets pane (tableview based)~~
- fix database debug actions
- ~~improve warning when a core is missing (also don't show that warning if core download was cancelled)~~

### Import issues
- The black image appear while importing before cover art shows up.
- Sometimes when importing a new game, a different cover from the game next to it (or from completely other systems) briefly appear: http://cl.ly/1H2T163i0601
- Sometimes when importing a new game, a weird animation happens: http://cl.ly/1S2q0P243y3K
- Importing games that need cuesheets: cue gets copied to the game library folder but not the binaries inside and the game doesn't appear in the library.
- Arcade ROMs (MAME) won't properly import because of the multiple files. They get extracted and end up in other libraries. Tested with dkong.zip where its contents are recognized as Atari 2600.
- Double click a ROM to import into OE. "Your game finished importing, do you want to play it now?" pops up, hit Yes and OE crashes: http://pastebin.com/p2JiJpRt
- "World/multi-region" ROMs no longer display any covers. Before it accurately grabbed the correct cover based on your locale. Tested with Sonic & Knuckles (World).md MD5 checksum 4ea493ea4e9f6c9ebfccbdb15110367e
- TODO: Need to try a massive import and look for memory leaks
- Unrelated crash? This happened after I switched back to my normal Game Library after testing and launched the app: http://pastebin.com/qScHaGq6
