## Welcome to the OpenEmu 1.0 Beta 9

# Requirements:

Mac OS X 10.7 or greater

# Setup

1. If you've run OpenEmu before, please remove folders in ~/Library/Application Support/OpenEmu and /Library/Application Support/OpenEmu as well as plists related to OpenEmu in ~/Library/Preferences. Note that removing ~/Library/Application Support/OpenEmu removes all ROM files that were automatically copied by OpenEmu when importing ROMs, so make a backup in case you don’t have those ROM files stored somewhere else.
2. Copy the App to your Applications folder.
3. Launch OpenEmu, and let the setup assistant run, optionally importing roms. Note that OpenEmu copies ROM files to its internal library folder in ~/Library/Application Support/OpenEmu/ by default.

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

**If using an Xbox 360 compatible controller, please install the latest driver found at http://tattiebogle.net/index.php/ProjectRoot/Xbox360Controller/OsxDriver.**

# Known Issues

Please be aware that currently OpenEmu does not support compressed ROM files, and that not all imported ROMs may have artwork associated with them on archive.vg. An internet connection is required to download emulator cores, artwork and game metadata.

# Other major known issues in this release:

* Graphics - Framerate slowdown on the 9600M GT - seems to only be an issue with this GPU (issue 316).
* Input - multiple controllers/players. When using multiple controllers, there is currently no way to switch which controller belongs to which player (issue 334).
* ROMs with the .bin extension are not supported. If they are for Sega Genesis/Mega Drive, simply rename to .smd or .gen. (issue 139).
* Compressed ROMs are not currently supported (issue 103).
* Discontinued the Quartz Composer plugins originally included in earlier betas. Please know that currently they are discontinued to focus on the main app. We hope to return to their development in the future. In the meantime, we hope that the inclusion of Syphon is sufficient.

# Reporting Bugs

To report bugs, please see: https://github.com/openEmu/OpenEmu/issues. Please refrain from reporting duplicate bugs, but feel free to comment on existing issues if you can duplicate a bug or add new information. Even a note that it is repeatable is useful.

Please keep in mind, some Game Cores and ROMs may have their own unique bugs. If possible, determine if a bug is specific to a core, to a ROM, or globally to OpenEmu. Please indicate which of the above behaviours is specific to the bug you are reporting.

Thank you for participating in the beta. We hope to make 1.0 a ground-breaking release for gaming on the Mac. With your input and help, we can move closer to a solid release.