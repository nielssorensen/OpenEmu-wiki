## Version 1.1

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
- Tooltips not displaying in any view, _i checked tooltips in main window (like grid view button). those work, is this fixed? -cy_
- ~~Fix grid view, click on a game a couple of times can launch it twice~~ ad93e3c6cde2b9465735fd7d6a2a076c6b4a5a57
- ~~Add info on cheats to save state plist (also advance state version in plist)~~ _not yet, moved to next release -cy_
- Fix core data migration bug where updating 1.0.2 or early to 1.0.4 causes artwork images to be removed

# Bugs and Crashes
- Import:
 - ~~Double clicking a ROM in Finder to import *sometimes* crashes OE https://gist.github.com/anonymous/bc5ab9d23ea67dd7863a~~ might be fixed by 335598662189
 - ~~Zipped ROMs that end up in the import issue resolver will not import (https://github.com/OpenEmu/OpenEmu/issues/1694)~~ 5fdad1e5b189dcb67d9272df93e1cb5e756a50d1
- UI:
 - ~~(RARE?) Stuck context menus (https://github.com/OpenEmu/OpenEmu/issues/1639)
 _can't fix without more info or crash log -cy
 - ~~(Can't Replicate, Needs Info) Cmd+Q crashing? (https://github.com/OpenEmu/OpenEmu/issues/1734) _wontfix until we get more info -cy_ ~~ _probably fixed here https://github.com/OpenEmu/OpenEmu/compare/74c4dda7fd92...b5dc16a66e9d -cy_ 
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

***

## Next Version (later…)
- Rewrite grid using OpenGL and CG renderers
 - image shadows can be drawn by using a pre-rendered 9 part image
 - use drawImage:inRect:fromRect:alpha:, drawText:inRect:withAttributes: & drawRect:withLineWidth: methods found in IKRenderer protocol
- Add info on cheats to save state plist (also advance state version in plist)
- manually implement drop & spinner animations

### Retrode (optional for next release)
- Show Slot 1 / Slot 2 header
- Implement import action
- Implement import save file action, show dialog and remove autosave state so the save file is actually read from disk
- Read firmware version
- Check for updates on retrode.com, retrode abandoned = no more firmware updates?
- Alert user of updates, show install wizard