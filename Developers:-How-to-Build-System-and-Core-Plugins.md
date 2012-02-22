## Getting Started
You will need the [latest Xcode](https://developer.apple.com/xcode/) (4.2 or greater) running on OS X 10.7 to build OpenEmu.

## About OpenEmu
The goal of OpenEmu is to be system agnostic so that plugins can be created to add support for new systems.

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

![System Plugins](http://i.imgur.com/vISr5.png)

### Structure of a System Plugin
Once compiled, system plugins take on the Product Name of the core they were built for if a target is set in the OpenEmu project. They are stored in ~/Library/Application Support/OpenEmu/Systems/

For example: Genesis.oesystemplugin, NES.oesystemplugin, SuperNES.oesystemplugin, etc.

![Systems](http://i.imgur.com/Pwehv.png)

![System Targets](http://i.imgur.com/VvVx9.png)

The contents of the system plugin bundle include the compiled SystemController and SystemResponder classes, the .plists and supporting files for controller preference graphics and icons.

### How to build a System Plugin
OpenEmu includes plugins for [several systems](https://github.com/OpenEmu/OpenEmu/wiki/Emulators). In this example, we will create a new system plugin for the TurboGrafx-16/PC Engine.

Our first step will be adding a new Target to the OpenEmu project. Choose the Bundle template under Framework & Library for Mac OS X and then give it a Product Name.

Once created, you will then have to add some custom OE-related values to the info plist. These will include, OEArchiveIDs, OEControlListKey, OEFileSuffixes, Principal Class, OESystemIcon, OESystemPluginName and OESystemIdentifier.

Since all plugins follow the same structure, we can duplicate a set from another system and then edit accordingly.

    NSString *OEPCEButtonNameTable[] =
    {
        @"OEPCEButton1",
        @"OEPCEButton2",
        @"OEPCEButtonUp",
        @"OEPCEButtonDown",
        @"OEPCEButtonLeft",
        @"OEPCEButtonRight",
        @"OEPCEButtonRun",
        @"OEPCEButtonSelect"
    };

### How to use a System Plugin
...


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