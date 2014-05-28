### three weeks?

***

### Core Data Rewirte
- check how openvgdb lookup behaves when no internet connection is available
- see if reloading collection view can be optimised (right now we reload on every main context save)

***

### Misc
- Fix input issues :P
- can we keep track of battery saves?
- fix database debug actions

### Import issues
- ~~deleting games that are scheduled for info sync causes a crash~~ _fixed in 71a733493449cc987329274664dda2623a217ed9 -cy_
- The black image appear while importing before cover art shows up. 
        _wontfix, we'll have to rewrite grid drawing code using OpenGL and at least draw images and image shadows ourselves -cy_
- Sometimes when importing a new game, a different cover from the game next to it (or from completely other systems) briefly appear: http://cl.ly/1H2T163i0601 _haven't seen this in a while, still an issue? -c_
- Core data error after import: "OpenEmu[20546]: ERROR: ForceShrinkPersistentStore_NoLock -delete- We do not have a BLOB or TEXT column type.  Instead, we have 5." http://stackoverflow.com/questions/19140151/strange-new-ios-7-errors-receiver-from-db-forceshrinkpersistentstore-nolock suggests it might be cache related
- TODO: Need to try a massive import and look for memory leaks
- Unrelated crash? This happened after I switched back to my normal Game Library after testing and launched the app: http://pastebin.com/qScHaGq6