## Version 1.0.5 / 1.1

### Features
- Featured Games
- BIOS preferences

## Version 1.0.4
### Save State Manager
- Use array controller and improve core data fetching
- correctly show names of all 'special' save states, including quick save slots
- accept dropped save states
- allow drag of save state & screenshot files

### Save States
- rename all unused auto saves in a game to 'restored auto save'
- check for weird duplicates on first start of new version

### Screenshot / Videos
- fix renaming screenshots
- import screenshots without 100% match into 'Unknown' category
- fix deleting screenshots

### Yosemite
- Fix HUDWindow title bar appearance (http://i.imgur.com/ikZWXCs.png)

### Misc
- Tooltips not displaying in any view
- Fix grid view, click on a game a couple of times can launch it twice
- Add info on cheats to save state plist (also advance state version in plist)
 - manually implement drop & spinner animations

# UI
- blank slate for:
 - screenshots (mentioning cmd + t shortcut?)
 - save states
- possibly in-game screenshot indicator (like save game 'notification')

## Next Version (later…)
- Rewrite grid using OpenGL and CG renderers
 - image shadows can be drawn by using a pre-rendered 9 part image
 - use drawImage:inRect:fromRect:alpha:, drawText:inRect:withAttributes: & drawRect:withLineWidth: methods found in IKRenderer protocol

### Retrode (optional for next release)
- Show Slot 1 / Slot 2 header
- Implement import action
- Implement import save file action, show dialog and remove autosave state so the save file is actually read from disk
- Read firmware version
- Check for updates on retrode.com, retrode abandoned = no more firmware updates?
- Alert user of updates, show install wizard