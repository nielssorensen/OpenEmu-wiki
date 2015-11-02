## Version Next
- rename all unused auto saves in a game to 'restored auto save'
- import screenshots without 100% match into 'Unknown' category
- check for weird save state duplicates on first start of new version
- Use array controller and improve core data fetching in save state manager

### unordered
- setting second player's controls https://github.com/OpenEmu/OpenEmu/issues/1861, should have been fixed in https://github.com/OpenEmu/OpenEmu-SDK/commit/4415e6bc72e57d3af74860e1ff0e55f1bd7d3f95
- ~~review NSViewController+OEAdditions.m, NSColor+OEAdditions.m~~ ~~and OENonARCHacks.m to see if we still need "no ARC" hacks `-fno-objc-arc`~~ 4e57bc8565f44ec1a75ff6d05bbc51e9886193c2, 925df43afde59e9a72d6a7e64aad1e4173536397
 - https://github.com/OpenEmu/OpenEmu/commit/d55ea9e3868f118359420645ff72e83879d82576
 - https://github.com/OpenEmu/OpenEmu/commit/19a19445b0212fb61037234aea6314241c327be4
 - https://github.com/OpenEmu/OpenEmu/commit/35ff1f1c9e4a66162c0460608cae071773ebf271#diff-b2132583dd704be5d9832f2fc9ce274a

## Bugs and Crashes
 - App crash when launching a game. Happened with Nestopia at the time but can happen with any core (https://gist.github.com/anonymous/c6c040e9fe70ef2f1f0b & SNES9x: https://gist.github.com/anonymous/5ffddc76286eb98bbaff & GenesisPlusGX: https://gist.github.com/anonymous/25496fab9c6751bd6ef1 & https://gist.github.com/anonymous/7fee33ea62f179a06d61 & https://gist.github.com/anonymous/40a9b963ac547e28d227 )

### Probably wontfix
 - Another exception. Can't remember the exact details when it occurred but I could no longer right click on anything in the grid view (https://gist.github.com/anonymous/8478b6f2d3da018af53b)
 - (Rare?) Had this crash some times while launching the app (https://gist.github.com/anonymous/d239235e177d4813dfe9 & https://gist.github.com/anonymous/45307fefff5fdc6f67b6 & https://gist.github.com/anonymous/c0282c14dd7476fc5d43)

## UI change
- bug: query entered into searchbox doesn’t persist after game play but the results do. expected: search string should also persist in the box after game play.
- bug: during gameplay, titlebar cuts off the gameview http://i.imgur.com/laMOjtR.png
- bug: game scanner view doesn't pop up when there are import issues to resolve.
- bug: quit the app with one of the other categories selected, then relaunch and select the library, the sidebar is blank. also, quit the app with homebrew selected, relaunch and select the library (it will be blank) but also switch back to homebrew and then it will also be blank.
- crash: search field-related. steps to replicate: enter search in library mode, click another category like save states, click back to library category, enter in a search again (notice it won't actually filter and give a result), switch back to save states yet again, then switch back to library once more, enter a search, crash: https://gist.github.com/anonymous/0105333cd1c4e03eb42a
- crash: scary looking crash, possibly from exiting game in main window https://gist.github.com/anonymous/589a7429c31e1be3517f
- properly center blank slate content (subtract titlebar height)
- preferences window sometimes doesn't resize correctly (not sure why)
- preferences window doesn't finish animation when it's closed too early
- use one of those fancy special effects views in the sidebar
- restore selected sidebar item
- restore game collection view state (zoom, selection, view type, search)
- restore active overlay (aka screenshots, featured games, save states) and their respective states
- restore New Collection From Selection action https://github.com/OpenEmu/OpenEmu/blob/master/OpenEmu/OEGameCollectionViewController.m#L315-L321
- smoothen title bar changes
- fix 'resolve issues' button
- fix game scanner canceling
- ~~animate showing / hiding screenshots, featured games, save states~~ 91e4da8ebd944c3089da5c666c3bc4f8cd937156 && 0460901683a89d67848beecfa10dc2c3bdb2c4c8
- ~~fix grid view drop indicator (extends below titlebar)~~ 3c909cae210e1fe97d55278131210f4c21f2b121
- ~~fix sidebar drop indicator (also extends below titlebar)~~ _cannot replicate - clobber_
- ~~fix game scanner overlaying sidebar (users can't access collections while game scanner is active)~~ cf7313d74cf3b9f0c6b238b4713e2b1cb6136179
- ~~Possibly move list view into 'view options' menu or hide in something like http://i.stack.imgur.com/xfImA.png or http://i.imgur.com/EM4Pz1X.png~~ _looks like no longer necessary_
- ~~Move the +-button into the sidebar (or not maybe not)~~
- ~~Remove grid resizing slider~~ and ~~replace with using mouse gesture pinch to zoom/unzoom~~ _decided to shrink slider to match photos app - clobber_
- ~~restore toolbar after coming back from in-window gameplay~~
- ~~Remove grid / list ~~/ coverflow~~ buttons~~ _let's keep grid/list buttons - clobber_
- ~~possibly remove (or use less) grain in grid view~~
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
