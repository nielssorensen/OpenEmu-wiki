## Version Next

### Save State Manager
- Use array controller and improve core data fetching
- correctly show names of all 'special' save states, including quick save slots
- ~~accept dropped save states~~ [changes](https://github.com/OpenEmu/OpenEmu/compare/9b6d377eb4236e504c8dbe6731c5793764b15683...fcd5c9684ae68788dde0cb0243e863523ea3c76b)
- ~~allow drag of save state & screenshot files~~ [changes](https://github.com/OpenEmu/OpenEmu/compare/9b6d377eb4236e504c8dbe6731c5793764b15683...fcd5c9684ae68788dde0cb0243e863523ea3c76b)

### Save States
- rename all unused auto saves in a game to 'restored auto save'
- check for weird duplicates on first start of new version

### Screenshot / Videos
- ~~fix renaming screenshots~~ _seems to work already -cy_
- import screenshots without 100% match into 'Unknown' category
- ~~fix deleting screenshots~~ _seems to work already -cy_

### Yosemite
- ~~Fix HUDWindow title bar appearance (http://i.imgur.com/ikZWXCs.png)~~ 2d510a094e4028d6b72ffb25ab4acc28346a0987

### Misc
- ~~Tooltips not displaying in any view, _i checked tooltips in main window (like grid view button). those work, is this fixed? -cy_~~
    - ~~Nope, looks like titles in grid view still need tooltips when we hover over them~~
    - changes 0c568ff63adca5db72368311ea02edb6de767174
- ~~Fix grid view, click on a game a couple of times can launch it twice~~ ad93e3c6cde2b9465735fd7d6a2a076c6b4a5a57
- ~~Add info on cheats to save state plist (also advance state version in plist)~~ _not yet, moved to next release -cy_
- ~~Fix core data migration bug where updating 1.0.2 or earlier to 1.0.4 causes artwork images to be removed~~ [changes](https://github.com/OpenEmu/OpenEmu/commit/4841dbcb195ae1826f03029590b0029be0a320e6)

# Bugs and Crashes
- Import:
 - ~~Double clicking a ROM in Finder to import *sometimes* crashes OE https://gist.github.com/anonymous/bc5ab9d23ea67dd7863a~~ might be fixed by 335598662189
 - ~~Zipped ROMs that end up in the import issue resolver will not import (https://github.com/OpenEmu/OpenEmu/issues/1694)~~ 5fdad1e5b189dcb67d9272df93e1cb5e756a50d1
- UI:
 - App crash when launching a game. Happened with Nestopia at the time but can happen with any core (https://gist.github.com/anonymous/c6c040e9fe70ef2f1f0b & SNES9x: https://gist.github.com/anonymous/5ffddc76286eb98bbaff & GenesisPlusGX: https://gist.github.com/anonymous/25496fab9c6751bd6ef1 & https://gist.github.com/anonymous/7fee33ea62f179a06d61 & https://gist.github.com/anonymous/40a9b963ac547e28d227 )
 - ~~These seem to be related to import and cover downloading in the grid (https://gist.github.com/anonymous/906492c58d45a94ac120 & https://gist.github.com/anonymous/67d0529e006357fbb59a)~~
    - ~~can be reproduced by having at least one spinner visible and then resizing the window. after a few seconds console will be spammed with those messages (blocking the app) and you can't switch consoles or launch a game without heavy glitching. Also happens when spinner animation is disabled.~~ 90951ed63f9db68cfb60b37a1d954f74948f0a8f
 - INAppStoreWindow exception (https://gist.github.com/anonymous/a77996283181f43b3a44)
 - Another exception. Can't remember the exact details when it occurred but I could no longer right click on anything in the grid view (https://gist.github.com/anonymous/8478b6f2d3da018af53b)
 - (Rare?) Had this crash some times while launching the app (https://gist.github.com/anonymous/d239235e177d4813dfe9 & https://gist.github.com/anonymous/45307fefff5fdc6f67b6 & https://gist.github.com/anonymous/c0282c14dd7476fc5d43)
 - ~~(RARE?) Stuck context menus (https://github.com/OpenEmu/OpenEmu/issues/1639)
 _can't fix without more info or crash log -cy~~ Seems to be 10.7 and we no longer support it
 - ~~(Can't Replicate, Needs Info) Cmd+Q crashing? (https://github.com/OpenEmu/OpenEmu/issues/1734) wontfix until we get more info -cy~~ _probably fixed here https://github.com/OpenEmu/OpenEmu/compare/74c4dda7fd92...b5dc16a66e9d -cy_ 
 - ~~"Stop Emulation” not working; window closes but games still run (https://github.com/OpenEmu/OpenEmu/issues/1676)~~ 33acba127dc28c6caea18c1bcae774447899685e
 - ~~If you hit "Quit OpenEmu" more than once, multiple confirmation dialogs pop up (https://github.com/OpenEmu/OpenEmu/issues/1711)~~ 6db9e39e0b46f61a66005eb46b593d9803b2a587
 - ~~(RARE?) Crash while moving game window (https://github.com/OpenEmu/OpenEmu/issues/1692)~~ 2172d36e049576ccbe33fb7ef8443b94ebb087d5
 - ~~(RARE?) Crash when dragging game window between monitors (https://github.com/OpenEmu/OpenEmu/issues/1753)~~ 3a37cc2979f3b197b68a5601bf08a3e3080650c3
 - ~~(RARE?) HUD bar disappears when dragged to second monitor (https://github.com/OpenEmu/OpenEmu/issues/1647)~~ 8f51d3b56af05be78781acb1209c24d10542e328

# UI
- blank slate for:
 - screenshots (mentioning cmd + t shortcut?)
 - save states
- possibly in-game screenshot indicator (like save game 'notification')
- ~~check in-game save state notification~~ 6f082f03a3019f1385f308b0e44f5319fd9aab8c
- Alerts: Whenever you type into one of our modals, the keyboard presses will register for the both text field and emulator control. Should drop responder status whenever text field is in focus?
- Alerts: (related to above) Press ‘save hotkey’ twice makes two dialogs appear. To replicate, bind a 'special key' for 'Save' and press the button over and over.
- Popup menus: Are rounded corners for the top part of menu items missing in 10.10? I can't remember if they were ever there before :P
***

## Next Version (later…)
- Rewrite grid using OpenGL and CG renderers
 - image shadows can be drawn by using a pre-rendered 9 part image
 - use drawImage:inRect:fromRect:alpha:, drawText:inRect:withAttributes: & drawRect:withLineWidth: methods found in IKRenderer protocol
- Add info on cheats to save state plist (also advance state version in plist)
- manually implement drop & spinner animations

### Retrode (later…)
- Show Slot 1 / Slot 2 header
- Implement import action
- Implement import save file action, show dialog and remove autosave state so the save file is actually read from disk
- Read firmware version
- Check for updates on retrode.com, retrode abandoned = no more firmware updates?
- Alert user of updates, show install wizard