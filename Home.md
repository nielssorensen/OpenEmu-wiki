## New UI To Do List

### Priority
* Archive.VG API inclusion
    * <strike>Get releases and tosec from Archive.VG response</strike>
    * * Rename rome with tosec name
    * Add fetched info to database (in OEDBGame gameWithArchiveDictionary:inDatabase:)
    * <strike>Add support for session dependent api stuff</strike> _does not make it into version 1.0_
* <strike>Implement Screen Flow UI - https://github.com/mattball/MBCoverFlowView ? </strike>
* Cores Preference pane _no core details for now_
    * We want it!
    * Waiting for new designs
* Fix UI for pop out window title bar
* <strike>Fix Filters in preferences</strike>
* Fix OEMenu
    * Highlight menu item even if mouse was not released
    * <strike>Add menu separator</strike>
    * <strike>Correct sizing if menu has only 1 item</strike>
    * <strike>Move selection by Arrow-Keys</strike>
    * <strike>Add blinking + delay when an item is clicked</strike>
* Fix GridView
    * <strike>Shadow on top (when scrolling reaches end)</strike>
    * Multiple selection
    * Move selection by Arrow-Keys
    * Add drag and drop
    * <strike>Center title and ratings on items</strike>
    * Fix memory usage
    * Fix resize crash
* HUD controls bar
    * <strike>Create save games menu</strike>
    * <strike>Make "Save Current Game" work</strike>
    * <strike>"Done" Button</strike>
    * Add "stop fullscreen" button state
    * <strike>Set audio volume (individually for each game)</strike>
    * <strike>Show / hide with mouse movement</strike>
* MainMenu
    * enable/disable items
    * Manage "Last Played" menu
* <strike>Move About Window / Plugin Loading / HID Support away from OEGameDocument</strike>
* Rewrite OEDocument for new architecture

* Fix OESearchFieldCell (it loses its text attributes when pressing enter-key)
* <strike>Localization of console names/images (e.g. NES<->Famicom)</strike>
* Remember state of collections item (collapsed/expanded)
* Add functionality to Preferences -> Library Folder Change/Reset Buttons
* <strike>Available Libraries (using OESystemPlugin)</strike>

* Setup Assistant: 
* * Welcome to OpenEmu, get you started
* * Download cores
* * Set up your preferences, and bind controller info
* * Import some roms!

* Maybe setup assistant is video game themed, like you are building a character from an old RPG? I dunno. Just a lame idea. Blinky in a tux with an eye piece ? Who knows!

### Eventually
* Remove spurious linker and compiler warnings
* Remove ivars since we are now 64 bit clean

### Organization
* <strike>Put UI Mockups on Github.</strike>
* Organize code, remove unecessary files
* Replace copyright headers
* Agreed upon code guidelines?

## Emulators To Do List