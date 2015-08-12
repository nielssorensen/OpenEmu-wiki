## Version Next
- rename all unused auto saves in a game to 'restored auto save'
- import screenshots without 100% match into 'Unknown' category
- check for weird save state duplicates on first start of new version
- blank slate for screenshots (mentioning cmd + t shortcut?)
- blank slate for save states
- Use array controller and improve core data fetching in save state manager

### unordered
- fix pt and es localizations https://github.com/OpenEmu/OpenEmu/issues/1963
- setting second player's controls https://github.com/OpenEmu/OpenEmu/issues/1861, should have been fixed in https://github.com/OpenEmu/OpenEmu-SDK/commit/4415e6bc72e57d3af74860e1ff0e55f1bd7d3f95
- blank slate for cd based games mentioning / linking to new guide

## Bugs and Crashes
 - App crash when launching a game. Happened with Nestopia at the time but can happen with any core (https://gist.github.com/anonymous/c6c040e9fe70ef2f1f0b & SNES9x: https://gist.github.com/anonymous/5ffddc76286eb98bbaff & GenesisPlusGX: https://gist.github.com/anonymous/25496fab9c6751bd6ef1 & https://gist.github.com/anonymous/7fee33ea62f179a06d61 & https://gist.github.com/anonymous/40a9b963ac547e28d227 )
 - INAppStoreWindow exception (actually just a warning) (https://gist.github.com/anonymous/a77996283181f43b3a44)

### Probably wontfix
 - Another exception. Can't remember the exact details when it occurred but I could no longer right click on anything in the grid view (https://gist.github.com/anonymous/8478b6f2d3da018af53b)
 - (Rare?) Had this crash some times while launching the app (https://gist.github.com/anonymous/d239235e177d4813dfe9 & https://gist.github.com/anonymous/45307fefff5fdc6f67b6 & https://gist.github.com/anonymous/c0282c14dd7476fc5d43)

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