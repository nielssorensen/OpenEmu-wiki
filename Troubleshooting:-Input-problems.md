### Input not working?

**Note: OpenEmu running on non-Apple hardware aka "Hackintosh" is strictly unsupported.**

There are circumstances in which open applications, installed software or certain hardware usage can cause interference<sup>[*](#interference)</sup> with gamepad and keyboard input in OpenEmu. Please see each section below for details of possible problems and solutions.

<a name="interference">*</a> This is because OpenEmu handles input differently than most applications, due to our special nature of responding to both keyboard and HID events while a game is running. Keyboard events, especially, are handled at a lower level - not through Cocoa but through IOKit - so often times other applications running can cause interference.

### Applications

The following applications are commonly found to interfere with input and should be closed while using OpenEmu. This is an incomplete list so if you are experiencing issues beyond these, try closing all other open applications. If issues persist, try restarting your computer and then only launch OpenEmu.

* Google Chrome (HTML5 Gamepad API)
* DOSBox
* Terminal (Secure Keyboard Entry)
* iTerm2
* Keybase.io
* Webroot Antivirus (Secure Keyboard Entry)

### Keyboard and Gamepad modifier apps

Input modifier apps such as these are not compatible with OpenEmu, cause interference and should be closed or uninstalled.

* ControllerMate
* DarwiinRemote
* Enjoy2
* Enjoyable
* GamePad Companion
* Joystick Mapper
* Karabiner (KeyRemap4MacBook) and Karabiner-Elements
* SteelSeries Engine
* USB Overdrive  (disable the "Any Gaming, Any Application" option.)
* WJoy (unload kexts for WJoy via Terminal.app with the following command: `sudo kextunload -b com.alxn1.driver.wjoy`)

### Remote Desktop apps
Remote Desktop apps such as these are not compatible with OpenEmu and will not be able to receive input events.

* Splashtop
* Synergy
* TeamViewer

### Hardware

These are generally unsupported and you should plug in your device directly to your Mac if possible.

* Any non-HID compliant device (e.g. console-only Official Nintendo GameCube Controller Adapter for Wii U)
* Adapters
* USB Hub
