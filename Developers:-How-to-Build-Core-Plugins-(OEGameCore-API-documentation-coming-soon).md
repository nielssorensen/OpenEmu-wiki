## Getting Started
You will need the [latest Xcode](https://developer.apple.com/xcode/) to build OpenEmu.

Clone the [OpenEmu repo](https://github.com/OpenEmu/OpenEmu) on GitHub. Use the [GitHub for Mac](http://mac.github.com/) app if you're new to Git or don't want to use the command line.

Enable the debug preferences pane in OpenEmu with: `defaults write org.openemu.OpenEmu debug 1`

## About OpenEmu
The goal of OpenEmu is to be system agnostic so that plugins can be created to add support for new systems. One should be able to write a new plugin using only OpenEmuBase.framework and OpenEmuSystem.framework

OpenEmu can be described as three layers:

1. The **Application** handles audio and video output to the OS and input from HID devices. 
2. The **System Plugin** describes a system and provides an interface for cores to plug into.
3. The **Core Plugin** is the implementation of the emulator which then ties into a system plugin.

## System Plugins

### Overview
System Plugins describe a core system and contain:

* SystemController and SystemResponder classes
* Plugin name and system identifier
* Supported rom types (file suffixes)
* Button mapping defaults and settings
* Controller preference layouts, graphics and icons.

These settings are stored in property list (.plist) files.

## Core Plugins

### Overview
Core Plugins implement systems and contain:
...

### Structure of a Core Plugin
oecoreplugin, SystemResponderClient.h, GameCore.h, GameCore.mm ...

### How to build a Core Plugin
porting...

### How to use a Core Plugin
...