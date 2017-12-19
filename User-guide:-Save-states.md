[Save states](http://en.wikipedia.org/wiki/Saved_game#Save_states) are 'snapshots' of a game's progress. Save states differ from the save functionality built into most games — because they are produced by the emulator itself, they carry none of the limitations that the game or console may otherwise impose. You can create any number of save states you like, as frequently as you like, and loading them will take you back to precisely where you were in the game when they were taken (even in the middle of a battle or cut scene).

You may use a game's built-in save mechanism instead of or in addition to save states, if you like. **IMPORTANT** —  Be aware that save state compatibility between updates is NOT a guarantee as they can break due to changes in an emulator core plugin.

### Automatic save states

OpenEmu automatically saves your progress as you play a game, so that you can always pick up where you left off without having to manually save. The next time you run the game, you will have the option of restarting from the automatic save state or not. (If you don't see this, you may have to [Reset warnings](https://github.com/OpenEmu/OpenEmu/wiki/User-guide:-Preferences:-Library#reset-all-dialog-warnings).)

### Quick Save State

The Quick Save State combines the ease of use of the automatic save state with the extra control afforded by manual save states. You can make use of it in-game via the *Save State* (⌘S) and *Load State* (⌘L) functions of the *Controls* menu, or via the *Quick Save* and *Quick Load* bindings under *Special Keys* in the *Controls* preferences. Once a Quick Save State has been created, you can also load from it via the HUD's disk menu.

### Manual save states

OpenEmu also features manual save states, like most other emulators.

#### Loading

To load from an existing save state, right-click a game in the library view and go to the *Play Save Games* menu. Here you will find all of the save states you've previously created (not including OE's automatic save state or the Quick Save State). Click on the desired save to load the game from that point.

You may also load a save state via the HUD's disk menu. Within the game window, move the mouse to produce the [HUD bar](#), and click the floppy disk icon near the centre. Clicking any of the saves in this menu (anything besides *Save Current Game*) will load from the corresponding state.

#### Saving

You must be running a game to save its state. Within the game window, move the mouse to produce the HUD bar, and click the floppy disk icon near the center. Inside this menu, you will see a *Save Current Game* option, as well as (if applicable) any previously created save states and the Quick Save State (see above).

To create a new save state, click on *Save Current Game*. A dialogue will appear where you can enter a custom name for the save (by default it is based on the date and time). Clicking *Save Game* will create the save, making it available in the HUD's disk menu as well as the *Play Save Games* menu in the Library view or Save States collection.

#### Deleting

You can delete a save state in the Save States collection by right-clicking on the desired state and selecting delete.

### Notes

Save states are generally limited to the core they were created with — if you change cores, your old save states will no longer work. However, if you try to load from a state saved on a different core, OE will automatically switch back to load it.
