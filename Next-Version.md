## Version 1.0.4 / 1.1

### Save State Manager
- ~~Disable group selection~~ ba6fabe6110ef24ead8e76c9208fdc6c3b36f4f8
- ~~Add 'Launch Save State' menu item~~
- ~~Add warning before deleting save states~~ 8491a86aa82bf3c35e4c5fdc77c17dd131d20488 might wanna show game title in the warnings as well (especially for quick / auto saves)
- Implement search (search game title, state names & state user description)
- Use array controller and improve core data fetching
- ~~Add warning before renaming 'special' save states~~ aa32e469cfc1223bcab12d7a60a06d7c473acdab rephrase
- ~~Fix subtitle font size~~ 8c1a9f8e4360a507bbb99349dec4606733ed1888
- ~~Change subtitle date display to a prettier format~~ 03807ae6d73fd4cf38726a2299cb7112e6590bba
- correctly show names of all 'special' save states, including quick save slots

### Save States
- Use relative paths
- handle case-sensitive paths correctly
- rename all unused auto saves in a game to 'restored auto save'

### Screenshot / Videos
- ~~Implement video & audio capture~~ - Talked to vade in IRC, it seems best if we leave audio/video capture to another app, like obs-studio (once its rewrite is finished http://www.michaelevans.org/blog/2014/06/07/building-obs-studio-for-os-x/). Better to leave this to apps that handle AV capture properly than trying to do it ourselves. With OBS, users will be able to stream to whatever site they want too.
- Modify core data model to include screenshots ~~and videos~~
- Scan screenshots directory on first launch and add them to the library

### Yosemite
- Fix grid glitches, they seem to be caused by calling setFrame: on CALayers in -layerForType: method, not caused by use of private api as far as i can tell 
- INAppstoreWindow crashes because of a custom theme frame, maybe they'll fix this
- Button cells with borders do not honour attributed string titles, can be fixed by drawing button titles ourselves, or maybe we just wait for the next dp
- Update Sparkle.framework. Our version in use appears to be 4 years old and the developer has ceased maintaining it (https://github.com/andymatuschak/Sparkle/). Updating to the final release may fix 10.10 support, or we can check out a fork that appears to be active (https://github.com/pornel/Sparkle). Have to make sure that newer Sparkle versions still allow us to distribute updates without the need of code signing. Currently we are allowed to bypass code signing because we distribute updates over SSL.

### Misc
- Fix grid view, click on a game a couple of times can launch it twice
- Add info on cheats to save state plist (also advance state version in plist)
- Rewrite grid using OpenGL and CG renderers
 - image shadows can be drawn by using a pre-rendered 9 part image
 - use drawImage:inRect:fromRect:alpha:, drawText:inRect:withAttributes: & drawRect:withLineWidth: methods found in IKRenderer protocol
 - manually implement drop & spinner animations
 - fixes 10.10 grid glitches

### Retrode (optional for next release)
- Show Slot 1 / Slot 2 header
- Implement import action
- Implement import save file action, show dialog and remove autosave state so the save file is actually read from disk
- Read firmware version
- Check for updates on retrode.com, retrode abandoned = no more firmware updates?
- Alert user of updates, show install wizard