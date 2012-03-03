### New UI To Do List

### Priority
* Archive.VG API inclusion
    * <strike>Get releases and tosec from Archive.VG response</strike>
    * * Rename rom files with tosec name
    * Add fetched info to database (in OEDBGame gameWithArchiveDictionary:inDatabase:)
    * <strike>Add support for session dependent api stuff</strike> _does not make it into version 1.0_
* Library
    * Allow for deletion/removal of Games from the library.
* Fix OEMenu
    * <strike>Highlight menu item even if mouse was not released</strike>
    * <strike>Add menu separator</strike>
    * <strike>Correct sizing if menu has only 1 item</strike>
    * <strike>Move selection by Arrow-Keys</strike>
    * <strike>Add blinking + delay when an item is clicked</strike>
    * make scrollable
    * <strike>allow max size</strike>
    * <strike>rethink positioning</strike>
* Fix GridView
    * <strike>Shadow on top (when scrolling reaches end)</strike>
    * <strike>Multiple selection</strike>
    * <strike>Move selection by Arrow-Keys</strike>
    * <strike>Scroll when selection reaches end and arrow key is pressed</strike>
    * Add drag and drop &mdash; drag game to collection
    * <strike>Center title and ratings on items</strike>
    * <strike>Fix memory usage</strike>
    * <strike>Fix resize crash</strick>
    * truncate collection name in view if collection is empty
    * context menu
* HUD controls bar
    * <strike>Create save games menu</strike>
    * <strike>Make "Save Current Game" work</strike>
    * <strike>"Done" Button</strike>
    * Add "stop fullscreen" button state
    * <strike>Set audio volume (individually for each game)</strike>
    * <strike>Show / hide with mouse movement</strike>
    * Fix bug where play/pause button is in incorrect state after saving a game
    * <strike>keep from fading out while a menu is open</strike>
* MainMenu
    * <strike>enable/disable items</strike>
    * Manage "Last Played" menu
* Input Preferences
    * <strike>Rethink grouping of buttons</strike>
* Cores Preference pane _no core details for now_
    * <strike>Waiting for new designs</strike>
    * Install Cores after download

* ### General Stuff
* <strike>Implement Screen Flow UI - https://github.com/mattball/MBCoverFlowView ? </strike>
* give Game Window pop out a hud look
* flip text shadow of blue hud button
* <strike>Fix Filters in preferences</strike>
* <strike>Move About Window / Plugin Loading / HID Support away from OEGameDocument</strike>
* <strike>Rewrite OEDocument for new architecture</strike>
* Fix OESearchFieldCell (loses text attributes after enter-key was pressed)
* <strike>Localization of console names/images (e.g. NES<->Famicom)</strike>
* Remember state of collections item (collapsed/expanded)
* Add functionality to Preferences -> Library Folder Change/Reset Buttons
* <strike>Available Libraries (using OESystemPlugin)</strike>
* rewrite main library split view and correctly remember/restore last sidebar width

* Setup Assistant: 
    * <strike>Intro Video</strike>
    * <strike>Welcome to OpenEmu</strike>
    * <strike>Core Installation</strike>
    * <strike>Game Scanner</strike>
    *    * Additional Sources
    * <strike>Game Pad Setup</strike>
    *    * <strike>Button Detection</strike>
    * <strike>Let's Go</strike>

### Eventually
* <strike>Remove spurious linker and compiler warnings</strike>
* Remove ivars since we are now 64 bit clean

### Organization
* <strike>Put UI Mockups on Github.</strike>
* Organize code, remove unecessary files
* Replace copyright headers
* <strike>Agreed upon code guidelines?</strike> [Style Guide](https://github.com/OpenEmu/OpenEmu/wiki/Style-Guide)

## Emulators To Do List