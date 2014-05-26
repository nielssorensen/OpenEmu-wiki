### three weeks?

***

### Core Data Rewirte
- Fix moving game library folder
- check save states
- check rom lookup (after import, initiated by context menu, on app launch)
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
- fix database debug actions

### Import issues
- deleting games that are scheduled for info sync causes a crash
- can't delete games from consoles anymore
- The black image appear while importing before cover art shows up.
- Sometimes when importing a new game, a different cover from the game next to it (or from completely other systems) briefly appear: http://cl.ly/1H2T163i0601
- Core data error after import: "OpenEmu[20546]: ERROR: ForceShrinkPersistentStore_NoLock -delete- We do not have a BLOB or TEXT column type.  Instead, we have 5." http://stackoverflow.com/questions/19140151/strange-new-ios-7-errors-receiver-from-db-forceshrinkpersistentstore-nolock suggests it might be cache related
- Sometimes game scanner gets stuck while importing a game and has the wrong count. This happened while importing a cuesheet game where it was successfully added into the library. Seems like importing enough games, especially ones with many binary tracks in the cuesheet will help trigger this easier. http://cl.ly/image/0p2a0l1B060l & http://cl.ly/image/0K2M3g0S3W3B
- TODO: Need to try a massive import and look for memory leaks
- Unrelated crash? This happened after I switched back to my normal Game Library after testing and launched the app: http://pastebin.com/qScHaGq6