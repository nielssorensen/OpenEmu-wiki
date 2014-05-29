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
- ~~Feature request :P - Can we force update all Cores after OE upgrades and relaunches? Since the change of moving options/bios stuff into the Cores, users will need the latest ones now~~ _1216ab4a910d86e57e8a5583a607ac810e9cd080 & 6a469b3ad5e23ce4c8d2c0dbb2c98c85e58d738d_

### Library/Gridview issues
- ~~Tooltips not appearing when hovering over game titles.~~ _51fdb679e6711fb00139035409cff566c36d1f17_
- ~~"Add Cover Art From File" doesn't work.~~ _8f72190e470425b7dd3c3ecf1d860db36471b904_ 
- ~~Have a game selected in a library and hit 'add to collections > blah whatever collection', it'll get added fine, but if i go to that new collection the game will still be highlighted and if i hit 'delete' the game won't delete. For it to delete, i'll first have to deselect it and then delete it again.~~ _7bf97b189adb8401fa1774eff74f7af298750bd9_
- ~~In an empty library, the "Core Provided By ..." text only allows for showing 2 Cores whereas for NES we actually have 3 (FCEU, Higan, Nestopia). Maybe room for a max of 3 is enough http://cl.ly/image/2E0U2w2i1S1r~~ _168b10e45b80b2c3cbfae22f90886902fe191cdd_
- After import, during lookup phase, CPU use is very high. Dunno if normal or not though.

### Import issues
- ~~deleting games that are scheduled for info sync causes a crash~~ _fixed in 71a733493449cc987329274664dda2623a217ed9 -cy_
- The black image appear while importing before cover art shows up. 
        _wontfix, we'll have to rewrite grid drawing code using OpenGL and at least draw images and image shadows ourselves -cy_
- ~~If i hit "don't import" while in the issue resolver for a game, the game scanner dialog will still appear http://cl.ly/image/093e2a1p2O23 and stick there~~_5e4da16ed6a2929b453fda20bfd0e19ee5d0bdda_
- Core data error after import: "OpenEmu[20546]: ERROR: ForceShrinkPersistentStore_NoLock -delete- We do not have a BLOB or TEXT column type.  Instead, we have 5." http://stackoverflow.com/questions/19140151/strange-new-ios-7-errors-receiver-from-db-forceshrinkpersistentstore-nolock suggests it might be cache related
- TODO: Need to try a massive import and look for memory leaks
- Unrelated crash? This happened after I switched back to my normal Game Library after testing and launched the app: http://pastebin.com/qScHaGq6