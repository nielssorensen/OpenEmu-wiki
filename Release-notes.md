#### 1.0.1 — 2014-01-03

**Features**
* Added debug options to take screenshots at native size and without aspect ratio correction. (12a8195, 126f396)
* Added a *Restart System* menu item. (cb5e05e)

**Enhancements**
* Added `.sgb` to supported extensions for Game Boy ROMs. (5755357)
* Implemented detection for PC Engine CD-ROM games. (7167a96)
* Improved the behaviour of the search bar. (3c17840, 0503fd4)
* Improved cover art and meta-data look-up behaviour. (ad38c71, 99d099f, f896aa7, 8148564)
* Added a Help menu. (4a357b8, 639203a)
* Various other minor enhancements.

**Fixes**
* Corrected an issue which could cause an erroneous path to be returned when resetting the library folder location. (af00cbd)
* Corrected an issue with archive handling which could cause problems when importing Mega Drive and arcade ROMs. (aae80b9)
* Corrected an issue which could prevent the import of folders whose names contain a dot. (c713afa)
* Corrected an issue which could prevent the editing of control bindings after the Preferences window has been closed. (8e1b973)
* Corrected an issue which could cause the application to crash upon deleting a game from a Smart Collection. (0d84eab)
* Corrected an issue which could cause crashing on OS X 10.7. (153fb71)
* Corrected an issue which prevented the *Quit Emulation* menu item from working in pop-out mode. (a7bcdd5)
* Corrected issues which could cause the application to crash when importing/scanning a large number of games. (b6dc687, 99d099f, b088f6e)
* Corrected an issue which could prevent access to the *Special Keys* control bindings on OS X 10.7. (4e59b67)
* Corrected an issue which could cause loss of the current battery save when quitting the application. (2b8462e)
* Various other minor fixes.

**Other**
* Removed RetroUSB controller auto-mapping (for now) to prevent conflicts with different controllers which all share the same hardware IDs. (738c90b)

#### 1.0 — 2013-12-23

* Initial public release.