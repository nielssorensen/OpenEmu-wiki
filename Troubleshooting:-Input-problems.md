### Input not working?

**Note: OpenEmu running on non-Apple hardware aka "Hackintosh" is strictly unsupported.**

There are circumstances in which open applications, installed software or certain hardware usage can cause interference with gamepad and keyboard input in OpenEmu. Please see each section below for details of possible problems and solutions.

### Applications

The following applications are commonly found to interfere with input and should be closed while using OpenEmu. This is an incomplete list so if you are experiencing issues beyond these, try closing all other open applications. If issues persist, try restarting your computer and then only launch OpenEmu.

* Google Chrome (HTML5 Gamepad API)
* DOSBox
* iTerm2
* Webroot Antivirus (Secure Keyboard Entry)

### Keyboard and Gamepad modifier apps

Input modifier apps such as these are not compatible with OpenEmu, cause interference and should be closed or uninstalled.

* ControllerMate
* DarwiinRemote
* Enjoy2
* Enjoyable
* GamePad Companion
* Joystick Mapper
* USB Overdrive  (disable the "Any Gaming, Any Application" option.)
* WJoy (unload kexts for WJoy via Terminal.app with the following command: `sudo kextunload -b com.alxn1.driver.wjoy`)

### Remote Desktop apps
Remote Desktop apps such as these are not compatible with OpenEmu and will not be able to receive input events.

* Splashtop
* TeamViewer

### Hardware

These are generally unsupported and you should plug in your device directly to your Mac if possible.

* Adapters
* USB Hub
