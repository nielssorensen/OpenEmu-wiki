[Save states](http://en.wikipedia.org/wiki/Saved_game#Save_states) are 'snapshots' of a game's progress. Save states differ from the save functionality built into most games — because they are produced by the emulator itself, they carry none of the limitations that the game or console may otherwise impose. You can create any number of save states you like, as frequently as you like, and loading them will take you back to precisely where you were in the game when they were taken (even in the middle of a battle or cut scene).

You may use a game's built-in save mechanism instead of or in addition to save states, if you like.

### Automatic save states

OpenEmu automatically saves your progress as you play a game, so that you can always pick up where you left off without having to manually save. The next time you run the game, you will have the option of restarting from the automatic save state or not. (If you don't see this, you may have to [Reset warnings](#).)

![Auto-save continue prompt](https://raw.github.com/okdana/OpenEmu-documentation/master/assets/img/user%20guide/Auto-save%20continue%20prompt.png)

Automatic save states are written to the following location in the file system:

~/Library/Application Support/OpenEmu/Save States/`<console>`/`<game>`/Auto Save.oesavestate

As of version 1.0, the following limitations exist with this feature:

1. The automatic save state does not appear in the [library view](#) context menu's list of save states (although it does increment the number in the Save Games column).
2. There is no way to delete the automatic save state from within the application.
3. The only options for loading from the automatic save state are to never do so, to always do so, or to always prompt. If you tell the dialogue that you never want to load from it, you will not be able to load from it manually, either, unless you [Reset warnings](#).

### Quick Save State

The Quick Save State combines the ease of use of the automatic save state with the extra control afforded by manual save states. You can make use of it in-game via the *Save State* (⌘S) and *Load State* (⌘L) functions of the *Controls* menu, or via the *Quick Save* and *Quick Load* bindings under *Special Keys* in the *Controls* preferences. Once a Quick Save State has been created, you can also load from it via the [HUD](#)'s disk menu (see below).

As with manual save states, you can delete the Quick Save State from within the application (see below).

Quick Save States are written to the following location in the file system:

~/Library/Application Support/OpenEmu/Save States/`<console>`/`<game>`/Quick Save.oesavestate

As of version 1.0, the following limitations exist with this feature:

1. The Quick Save State does not appear in the library view context menu's list of save states (although it does increment the number in the Save Games column). It does appear in the HUD's disk menu.

### Manual save states

OpenEmu also features manual save states, like most other emulators.

Manual save states are written to the following location in the file system:

~/Library/Application Support/OpenEmu/Save States/`<console>`/`<game>`/`<save name>`.oesavestate

As of version 1.0, the following limitations exist with this feature:

1. It is not possible to over-write an existing manual save state — you can only delete saves and create new ones.

#### Loading

To load from an existing save state, right-click a game in the library view and go to the *Play Save Games* menu. Here you will find all of the save states you've previously created (not including OE's automatic save state or the Quick Save State). Click on the desired save to load the game from that point.

You may also load a save state via the HUD's disk menu. Within the game window, move the mouse to produce the [HUD bar](#), and click the floppy disk icon near the centre. Clicking any of the saves in this menu (anything besides *Save Current Game*) will load from the corresponding state.

![HUD save menu](https://raw.github.com/okdana/OpenEmu-documentation/master/assets/img/user%20guide/HUD%20-%20saves%20-%20my%20save%202%20%28no%20game%29.png)

#### Saving

You must be running a game to save its state. Within the game window, move the mouse to produce the HUD bar, and click the floppy disk icon near the centre. Inside this menu, you will see a *Save Current Game* option, as well as (if applicable) any previously created save states and the Quick Save State (see above).

To create a new save state, click on *Save Current Game*. A dialogue will appear where you can enter a custom name for the save (by default it is based on the date and time). Clicking *Save Game* will create the save, making it available in the HUD's disk menu as well as the *Play Save Games* menu in the [library view](#).

![Save Current Game dialogue](https://raw.github.com/okdana/OpenEmu-documentation/master/assets/img/user%20guide/Save%20Current%20Game%20dialogue.png)

#### Deleting

You can delete a manual save state (or a Quick Save State) from the Save States library by right-clicking on the desired state and selecting delete.

![HUD disk menu](https://raw.github.com/okdana/OpenEmu-documentation/master/assets/img/user%20guide/HUD%20-%20saves%20-%20delete%20my%20save%202%20%28no%20game%29.png)

### Notes and limitations

Save states are generally limited to the [core](#) they were created with — if you change cores, your old save states will no longer work. However, if you try to load from a state saved on a different core, OE will automatically switch back to load it.

OpenEmu save states are saved as [bundles](http://en.wikipedia.org/wiki/Application_bundle) with an extension of `.oesavestate`. Each bundle contains three files:

1. `Info.plist` — An [XML plist](http://en.wikipedia.org/wiki/Plist) file containing various meta-data, such as the save name, a time stamp, a hash of the ROM file, the OE version number, the [core](#) which produced the save state, and the version number of the core.

2. `ScreenShot` — An 8-bit [PNG](http://en.wikipedia.org/wiki/Portable_Network_Graphics) file containing a screenshot representing the saved game state.

3. `State` — The actual state file, as provided by the core.