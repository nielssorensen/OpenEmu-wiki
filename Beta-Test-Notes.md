## Welcome to the OpenEmu 1.0 Beta 10

# Requirements:

Mac OS X 10.7 or greater

# Setup

1. If you've run OpenEmu before, please remove folders in ~/Library/Application Support/OpenEmu and /Library/Application Support/OpenEmu as well as plists related to OpenEmu in ~/Library/Preferences. Note that removing ~/Library/Application Support/OpenEmu removes all ROM files that were automatically copied by OpenEmu when importing ROMs, so make a backup in case you don’t have those ROM files stored somewhere else.
2. Copy the App to your Applications folder.
3. Launch OpenEmu, and let the setup assistant run, optionally importing roms. Note that OpenEmu copies ROM files to its internal library folder in ~/Library/Application Support/OpenEmu/ by default.

**Additionally you can run this Apple Script to automate the process https://raw.github.com/OpenEmu/OpenEmu/master/Scripts/OpenEmuWiper.applescript (save page as and run)**

# Game Controllers

Any generic HID compliant USB or Bluetooth game controller should work with OpenEmu out of the box.

OpenEmu now automatically maps controls for the following recognized devices in our database:
* Xbox 360 and 3rd party controllers (driver required)
* PlayStation 3
* Logitech series (Dual Action, Rumblepad 2, Gamepad F310/F510/F710)
* Gravis GamePad Pro
* RetroUSB SNES RetroPort and RetroPad
* Sega Saturn USB
* PS3 Neo Geo Pad USB
* Retrode (SNES)
* Retrolink SNES
* Retrolink N64
* N64 Adaptoid
* Nintendo Wiimote
* Nintendo Wii U Pro

**If using an Xbox 360 compatible controller, please install the latest driver found at http://tattiebogle.net/index.php/ProjectRoot/Xbox360Controller/OsxDriver.**

**If using a Wiimote or Wii U Pro controller, please go to the Controller preferences, select "Add a Wiimote" from the Input box and follow the pairing directions.**

Additionally, you can use [Joypad Connect](http://getjoypad.com/legacy/) to connect your iPhone as a controller.

# Known Issues

Single file compressed ROMs are supported, but not files with multiple ROMs.

Please be aware that not all imported ROMs may have artwork associated with them on [Archive.vg](http://archive.vg). An internet connection is required to download emulator cores, artwork and game metadata.

# Other major known issues in this release:

* Trying to re-map a button in controller prefs doesn't work - [Issue #556](https://github.com/OpenEmu/OpenEmu/issues/556) **Now fixed in main repo**
* Discontinued the Quartz Composer plugins originally included in earlier betas. Please know that currently they are discontinued to focus on the main app. We hope to return to their development in the future. In the meantime, we hope that the inclusion of [Syphon](http://syphon.v002.info/) is sufficient.
* NeoGeo Pocket missing a controller graphic

# Reporting Bugs

To report bugs, please see: https://github.com/openEmu/OpenEmu/issues. Please refrain from reporting duplicate bugs, but feel free to comment on existing issues if you can duplicate a bug or add new information. Even a note that it is repeatable is useful.

Please keep in mind, some Game Cores and ROMs may have their own unique bugs. If possible, determine if a bug is specific to a core, to a ROM, or globally to OpenEmu. Please indicate which of the above behaviours is specific to the bug you are reporting.

Thank you for participating in the beta. We hope to make 1.0 a ground-breaking release for gaming on the Mac. With your input and help, we can move closer to a solid release.