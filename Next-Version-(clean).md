## Version Next
- rename all unused auto saves in a game to 'restored auto save'
- import screenshots without 100% match into 'Unknown' category
- check for weird save state duplicates on first start of new version
- Use array controller and improve core data fetching in save state manager

### unordered
- setting second player's controls https://github.com/OpenEmu/OpenEmu/issues/1861, should have been fixed in https://github.com/OpenEmu/OpenEmu-SDK/commit/4415e6bc72e57d3af74860e1ff0e55f1bd7d3f95
- review NSViewController+OEAdditions.m, NSColor+OEAdditions.m ~~and OENonARCHacks.m to see if we still need "no ARC" hacks `-fno-objc-arc`~~ second part done in 925df43afde59e9a72d6a7e64aad1e4173536397
 - https://github.com/OpenEmu/OpenEmu/commit/d55ea9e3868f118359420645ff72e83879d82576
 - https://github.com/OpenEmu/OpenEmu/commit/19a19445b0212fb61037234aea6314241c327be4
 - https://github.com/OpenEmu/OpenEmu/commit/35ff1f1c9e4a66162c0460608cae071773ebf271#diff-b2132583dd704be5d9832f2fc9ce274a

## Bugs and Crashes
 - App crash when launching a game. Happened with Nestopia at the time but can happen with any core (https://gist.github.com/anonymous/c6c040e9fe70ef2f1f0b & SNES9x: https://gist.github.com/anonymous/5ffddc76286eb98bbaff & GenesisPlusGX: https://gist.github.com/anonymous/25496fab9c6751bd6ef1 & https://gist.github.com/anonymous/7fee33ea62f179a06d61 & https://gist.github.com/anonymous/40a9b963ac547e28d227 )
 - INAppStoreWindow exception (actually just a warning) (https://gist.github.com/anonymous/a77996283181f43b3a44)

### Probably wontfix
 - Another exception. Can't remember the exact details when it occurred but I could no longer right click on anything in the grid view (https://gist.github.com/anonymous/8478b6f2d3da018af53b)
 - (Rare?) Had this crash some times while launching the app (https://gist.github.com/anonymous/d239235e177d4813dfe9 & https://gist.github.com/anonymous/45307fefff5fdc6f67b6 & https://gist.github.com/anonymous/c0282c14dd7476fc5d43)

## UI change
- preferences window sometimes doesn't resize correctly (not sure why)
- preferences window doesn't finish animation when it's closed too early
- Move the +-button into the sidebar (or not maybe not)
- Possibly move list view into 'view options' menu or hide in something like http://i.stack.imgur.com/xfImA.png or http://i.imgur.com/EM4Pz1X.png
- use one of those fancy special effects views in the sidebar
- possibly remove (or use less) grain in grid view
- restore selected sidebar item
- restore game collection view state (zoom, selection, view type, search)
- restore active overlay (aka screenshots, featured games, save states) and their respective states
- Remove grid resizing slider and ~~replace with using mouse gesture pinch to zoom/unzoom~~
- smoothen title bar changes
- restore toolbar after coming back from in-window gameplay
- animate showing / hiding screenshots, featured games, save states
- Remove grid / list ~~/ coverflow~~ buttons
- ~~Remove 'Media' library subsection from sidebar~~
- ~~Move former 'Media' library to their own category selector buttons in the top bar above the sidebar, like new iTunes http://i.imgur.com/i3PE7xY.png~~
- ~~probably want the title of the game playing in the new toolbar~~
- ~~show title bar during gameplay (and setup assistant?)~~
- ~~hide toolbar during fullscreen game play~~
- ~~Remove bottom bar and replace with top bar in the style of the new iTunes (think NSTitleBarAccessoryViewController)~~
- ~~Move search to the new top bar~~
- ~~possibly remove accessory view during gameplay~~
- ~~remove lower inset shadow in grid view~~
- ~~use WAYWindow for preferences (not sure if needed or can / should be done using titlebar accessory view)~~ _using WAYWindow was not necessary  -cy_
- ~~fix sidebar button~~
- ~~disable toolbar during setup assistant / game play~~ _hidden instead  -cy_
- ~~disable toolbar editing~~
- ~~sidebar button position while in fullscreen~~

## Next Version (later…)
- Rewrite grid using OpenGL and CG renderers
 - image shadows can be drawn by using a pre-rendered 9 part image
 - use drawImage:inRect:fromRect:alpha:, drawText:inRect:withAttributes: & drawRect:withLineWidth: methods found in IKRenderer protocol
- Add info on cheats to save state plist (also advance state version in plist)
- manually implement drop & spinner animations

## Retrode (later…)
- Show Slot 1 / Slot 2 header
- Implement import action
- Implement import save file action, show dialog and remove autosave state so the save file is actually read from disk
- Read firmware version
- Check for updates on retrode.com, retrode abandoned = no more firmware updates?
- Alert user of updates, show install wizard