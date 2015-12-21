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
- type select select in menus (eg console selection in controls settings) _not sure if this ever worked -cy_
- ~~for some reason it is impossible to deselect gambatte in setup assistant~~ _this was intentional to resolve some user headaches -clobber https://github.com/OpenEmu/OpenEmu/commit/002ede42aaf20f1590934cf9e1eb54ccbe9bc2ee_

## Bugs and Crashes
 - App crash when launching a game. Happened with Nestopia at the time but can happen with any core (https://gist.github.com/anonymous/c6c040e9fe70ef2f1f0b & SNES9x: https://gist.github.com/anonymous/5ffddc76286eb98bbaff & GenesisPlusGX: https://gist.github.com/anonymous/25496fab9c6751bd6ef1 & https://gist.github.com/anonymous/7fee33ea62f179a06d61 & https://gist.github.com/anonymous/40a9b963ac547e28d227 )

### Probably wontfix
 - Another exception. Can't remember the exact details when it occurred but I could no longer right click on anything in the grid view (https://gist.github.com/anonymous/8478b6f2d3da018af53b)
 - (Rare?) Had this crash some times while launching the app (https://gist.github.com/anonymous/d239235e177d4813dfe9 & https://gist.github.com/anonymous/45307fefff5fdc6f67b6 & https://gist.github.com/anonymous/c0282c14dd7476fc5d43)

## UI bugs
- fullscreen transition for games running in main window is not smooth
- resizing a running game window (main window or popout) can produce flickering garbage
- transition from Other Collections to Library has a slight 'pop' in the sidebar at the end of the animation *[It appears to be the NSVisualEffectView going from inactive state to active state.]*
- "Start Game" menu item is disabled in the main window and cannot be used to launch a game. It also enables while playing a game in the main window.

## UI changes
- restore game collection view state (zoom, selection, view type, search) *[Is this still accurate? These things seem to already be persisted.]*
- table views: use the standard look with Source List style + visual effect view? *[Is it conventional for non-source list table views to have a source list style and vibrancy? Would a table view with vibrancy sitting next to the sidebar with vibrancy be too much darned vibrancy? Also keep in mind that behind-window vibrancy and within-window vibrancy can't mix.]*

### Completed UI bugfixes/changes
- ~~Switching from the main library in list view to another category and back will cause controls in the library to be disabled and not persist the correct selected button state.~~ f0f4ac8edfaf342778ddb029f36a2ebe899dd56e and f75ce661df366d2b936cf09c2dc74fe37fa5d878
- ~~isSidebarVisible needs to be removed from OELibrarySplit view, since now that we don't support that people on 1.0.4 with their collapsed sidebar will also find their sidebar is collapse on 2.0 with no way to fix it~~ 141319844f10c8d712dbc6475e1cd20120ad49f0
- ~~Quitting main window gameplay after launching from a save state clears the save state selection after a delay.~~ c9629bf7faecac421383ff0a0da001a1b604a4e7
- ~~bug: In the gameplay popout window, going to fullscreen and then out of fullscreen causes the window title text to disappear.~~ db85b26824d49e77f7ee8a22aaf275e57eb7ef2d
- ~~bug: 'Recently Added' collection in the sidebar affected by a bug involving importDate: ZIMPORTDATE is null for a newly imported game on a clean library. Dates back to at least 1.0.4.~~ 8bb76685337daa3f8d0ec395243210d31e37b69f
- ~~bug: "clicking the list view column titles leaves untidy white lines" https://github.com/OpenEmu/OpenEmu/issues/2200~~ -0f5f64c
- ~~transition to the Homebrew collection has a longer delay than the rest of the collections. The usual crossfade animation occurs when the delay completes. The delay lasts the length of the transition duration, and setting the duration to 0 eliminates the delay (at the cost of eliminating the crossfade animation). The delay does not happen for the first transition to the homebrew collection.~~ 729a832 
- ~~bug: issue resolver is still glitching https://transfer.sh/xF3yV/screen-shot-2015-12-14-at-23.10.45.png~~ a9e11acb724c7ac643a7ca5ce8faa48dde8576ca
- ~~bug: konami code is broken~~ 3d67687061073d4f46c4479a6d027af69a7ac3ef
- ~~bug: the "hide" context menu action for hiding a library no longer works until the preferences window is shown. This is because the preferences window is now lazily loaded, and so there's nothing listening for OESidebarTogglesSystemNotification until OEPrefLibraryController gets initialized.~~ f7dade9e9a3dde3686c598f61f58bcfc56035059
- ~~bug: Launching a game in the library window from list mode and then exiting the game switches the library window to grid mode.~~ 5deb7b9970defe4a59ca612ec8abe9dd12c8c03e
- ~~bug: Importing a game in list mode switches the library window to grid mode.~~ 5deb7b9970defe4a59ca612ec8abe9dd12c8c03e
- ~~fix modal sheet positioning, probably to sit under the titlebar? https://transfer.sh/4ZRmf/screen-shot-2015-12-11-at-21.24.56.png~~ 223d714852af367201698377ca965cc426dd1701
- ~~preferences window sometimes doesn't resize correctly~~ b5fa707812f697e3dbe0a37cae0315575003c40c
- ~~preferences window doesn't finish animation when it's closed too early~~ b5fa707812f697e3dbe0a37cae0315575003c40c
- ~~bug: since the toolbar change to the preferences (a7dcd04ef2d213abefb5a0d49bc770655d6aef0c), only clicking the icon will change tabs instead of before where clicking the 'text' label would also work~~ b5fa707812f697e3dbe0a37cae0315575003c40c
- ~~OpenEmu's preference tab icons are 36x36, but NSToolbarItem uses HIG-specified icon size of 32x32, causing noticeable scaling. Before/after conversion to NSTabViewController: http://i.imgur.com/FWSyIJQ.png~~ d39d151699fad633363949d874a2c4035d0aab83
- ~~convert Prefs to NSTabViewController so it can manage the toolbar and the window automagically~~ b5fa707812f697e3dbe0a37cae0315575003c40c
- ~~search field flashing carat has a white line at the bottom. redraw issue?~~ c67c48c36b6ddb73c7ac909bfc196ce58d58da88
- ~~bug: after new gradient background view, resizing the main window doesn't look as 'smooth'~~ 2feeee90b621e56de4951fe8b3e91e270790bf2a
- ~~bug: after new gradient background view, double clicking the top titlebar doesn't 'expand' the window.~~ 876d38b41db3131380140ad6821e64c42975607e
- ~~reminder: all the .xib's have been changed so we will probably need to delete most localized ones. probably no time to update them all for localization and we don't want weird crashes.~~
- ~~restore selected sidebar item~~
- ~~maybe adjust space between grid cover and selector ring again? http://i.imgur.com/206lkMO.png~~ 953fd8c4fc972665de7596555a2c32159733369f
- ~~grid/list controls don't enable until after transitions when changing Collections and looks odd. remove the delay so they happen in response to the button click and not the animation.~~ 1f3c71da0f70f98bb8bc3231ade116e04f961864
- ~~titlebar needs a gradient to give some definition, otherwise too flat behind our themed controls~~ 1a7d78813b2faaa6e417174a026c7565394a1157
- ~~restore active overlay (aka screenshots, featured games, save states)~~ and their respective states
- ~~adjust space between grid cover and selector ring~~ 60d63e77db8c9046c2226e7bd6ef92230b4eba6c
- ~~adjust grid size slider hint image locations so it doesn't look weird on min / max size~~ d0d0a1c1fb1aef01540895b43cc6c502bfcfdfa0
- ~~ratings appear at twice the size when i move the main window from my retina screen to my standard resolution monitor: http://i.imgur.com/1aSptny.png~~ 21479c0a23228ade407b3b75249e6d77d5cd163b
- ~~properly center blank slate content (subtract titlebar height)~~ 6288391fa1d4af10ee868293ed419da12db58bb5
- ~~figure out way to more prominently display the 'CD guide' otherwise we're looking at annoying repeated questions and issues opened forever: http://i.imgur.com/Pom4Qib.png~~ 960c233f525003268665e64c75a33066c78c4809
- ~~bug: resolve issues 'link' doesn't load issue resolver view on second import. steps to replicate: import a game that will prompt the issue resolver, click the resolve issues link, select a system and apply. next, import another and try to click the resolve issues 'link' and the view will not load unless you first click anywhere other than the game scanner view.~~ 77d30fa3ed3abf1aa4bcacadcb8aa42287f9f874
- ~~bug: query entered into searchbox doesn’t persist after game play but the results do. expected: search string should also persist in the box after game play.~~ 5b1170462e44b3e626215d955f497135b40a867b
- ~~crash: search field-related. steps to replicate: enter search in library mode, click another category like save states, click back to library category, enter in a search again (notice it won't actually filter and give a result), switch back to save states yet again, then switch back to library once more, enter a search, crash: https://gist.github.com/anonymous/0105333cd1c4e03eb42a~~ 6d961c5a175dba934d67320ae9e5487f46e1d957
- ~~bug: if you switch to a different category from library and switch back, then import a game that will prompt the issue resolver, the issue resolver view will be empty unless you resize the window https://i.imgur.com/TsVBcsO.png~~ 0e37dab2ca773a88edb6498f0cf2f0f8cd059ca7
- ~~crash: quitting the application (Command+Q) while running a game in the main window: https://gist.github.com/anonymous/26e972f6322087ebe7c5~~ e2299750d32e4c3b91c6d7cf043a0f673a95ca4e
- ~~restore New Collection From Selection action https://github.com/OpenEmu/OpenEmu/blob/master/OpenEmu/OEGameCollectionViewController.m#L315-L321~~ 8f96c1b3b786dc99fb28d9e92125e9fb56eac043
- ~~fix 'resolve issues' button~~ ea1da7ee2c8f38c645ce80851c2a3e8745bce934
- ~~fix game scanner canceling~~ ed6b3fb0e6c6907bc525a87ff88fc5b92dbccee4
- ~~bug: during gameplay, titlebar cuts off the gameview http://i.imgur.com/laMOjtR.png~~ 8727c7ef7610d6c83e2415356c1f42b7fa9d9409
- ~~bug: quit the app with one of the other categories selected, then relaunch and select the library, the sidebar is blank. also, quit the app with homebrew selected, relaunch and select the library (it will be blank) but also switch back to homebrew and then it will also be blank.~~ 6b68879224f0fd89beda8e19a3c7895b6878bd9e
- ~~bug: if you have scrollbars and translucency on, the scollbar persists briefly during transition from library to another category.~~ 457728470ad64b48fc23fe9eaed9169f22f9a511
- ~~bug: scrollbars look wide instead of thin when system translucency is on http://i.imgur.com/ETZhyok.png~~ 457728470ad64b48fc23fe9eaed9169f22f9a511
- ~~bug: game scanner view doesn't pop up when there are import issues to resolve.~~ 09dfe478e58e00c5e099bb9c6b98a4f2346d8f34
- ~~crash: happens when exiting a game in the main window. steps to reproduce: load a game, quit the game, load it again, quit it again and you should eventually get the crash: https://gist.github.com/anonymous/d5eb58b3649121cdc382 & https://gist.github.com/anonymous/da02a16b906f5a1f0b5a - robotoad able to replicate. Crash is related to autolayout with the solution being to disable autolayout for OELibraryGamesViewController.xib and manually layout the game scanner view.~~ 6cd03fb6d22b20f42a955855e32ed1f976b27fd1
- ~~use one of those fancy special effects views in the sidebar~~ b5072f2d90a75bc531e019c50dfb131c2369bb7c
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
- ~~smoothen title bar changes~~ f1047c0bb19c4883e5eca44e55412c8f07faf4ad
- ~~disable all titlebar view controls while in the issue resolver view, otherwise it can break while switching categories~~ 3772aaac81438ca67ed6a13ff47ef9cc00d8e6cd

## Next Version (later…)
- Rewrite grid using OpenGL and CG renderers
 - image shadows can be drawn by using a pre-rendered 9 part image
 - use drawImage:inRect:fromRect:alpha:, drawText:inRect:withAttributes: & drawRect:withLineWidth: methods found in IKRenderer protocol
- Add info on cheats to save state plist (also advance state version in plist)
- manually implement drop & spinner animations