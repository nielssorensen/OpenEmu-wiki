## Version 1.0.4 / 1.1

### Save State Manager
- ~~Disable group selection~~ ba6fabe6110ef24ead8e76c9208fdc6c3b36f4f8
- Add 'Launch Save State' menu item
- Add warning before deleting save states
- Implement search (search game title, state names & state user description)
- Use array controller and improve core data fetching
- Add warning before renaming 'special' save states 
- ~~Fix subtitle font size~~ 8c1a9f8e4360a507bbb99349dec4606733ed1888
- ~~Change subtitle date display to a prettier format~~ 03807ae6d73fd4cf38726a2299cb7112e6590bba

### Screenshot / Videos
- Implement video & audio capture
- Modify core data model to include screenshots and videos
- Scan screenshots directory on first launch and add them to the library

### Yosemite
- Inspect grid glitches & fix them :P
- INAppstoreWindow crashes because of a custom theme frame, maybe they'll fix this
- Button cells with borders do not honour attributed string titles, can be fixed by drawing button titles ourselves, or maybe we just wait for the next dp

### Misc
- Add info on cheats to save state plist (also advance state version in plist)