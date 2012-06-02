## Welcome to the OpenEmu 1.0 Beta 8

# Requirements:

Mac OS X 10.7

# Setup

1. If you've run OpenEmu before, please remove folders in ~/Library/Application Support/OpenEmu and /Library/Application Support/OpenEmu as well as plists related to OpenEmu in ~/Library/Preferences.
2. Copy the App to your Applications folder.
3. Launch OpenEmu, and let the setup assistant run, optionally importing roms and setting up your gamepad.

# Game Controllers

Any generic HID compliant USB or Bluetooth game controller should work with OpenEmu out of the box. Wii Remote and Wii Classic Controllers, wired XBox 360 controllers, and Playstation 3 controllers are natively supported. Be sure to pair your wireless controllers (and unpair them from other devices) before using with OpenEmu. Wii Remotes can be paired by holding buttons 1 and 2 simultaneously while in the Controls preferences. If using the XBox 360 controller, please install the latest driver for 10.7 found at http://tattiebogle.net/index.php/ProjectRoot/Xbox360Controller/OsxDriver.

# Known Issues

Please be aware that currently OpenEmu does not support compressed ROM files, and that not all imported ROMs may have artwork associated with them on archive.vg. An internet connection is required to download artwork and game metadata. Additionally, game library organization (found in preferences) is currently non-functioning. 

# Other major known issues in this release:

* Setup Assistant: Game Pad setup does not properly set preferences for the Game Cores (issue 136).
* ROMs with the .bin extension are not supported. If they are for Sega Genesis/Mega Drive, simply rename to .smd or .gen. (issue 139).
* If you have opted in to the Setup Assistant's automatic ROM importing, there is currently no indication that game importing is happening in the background. Similarly, when dragging many ROMs into the Library, there is no indication of background importing (issue 137).
* Compressed ROMs are not currently supported (issue 103).
* You may have to remap your controls from time to time. This can be caused by reconnecting controllers, waking up from sleep or rebooting (issue 118).
* "Organize Game Library" preference is currently non-functional (issue 138).
* On some ATI cards, QTZ based filters have inverted colors (issue 142).
* Discontinued the Quartz Composer plugins originally included in earlier betas. Please know that currently they are discontinued to focus on the main app. We hope to return to their development in the future. In the meantime, we hope that the inclusion of Syphon is sufficient.

# Reporting Bugs

To report bugs, please see: https://github.com/openEmu/OpenEmu/issues. Please refrain from reporting duplicate bugs, but feel free to comment on existing issues if you can duplicate a bug or add new information. Even a note that it is repeatable is useful.

Please keep in mind, some Game Cores and ROMs may have their own unique bugs. If possible, determine if a bug is specific to a core, to a ROM, or globally to OpenEmu. Please indicate which of the above behaviours is specific to the bug you are reporting.

Thank you for participating in the beta. We hope to make 1.0 a ground-breaking release for gaming on the Mac. With your input and help, we can move closer to a solid release.
