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
...
.oesystemplugin
1(classes)
2(supporting files, plists)

### How to build a System Plugin
OpenEmu includes plugins for [several systems](https://github.com/OpenEmu/OpenEmu/wiki/Emulators). In this example, we will create a new system plugin for the TurboGrafx-16/PC Engine.



### How to use a System Plugin
...


## Core Plugins

### Overview
Core Plugins implement systems and contain:
...

### Structure of a Core Plugin
...

### How to build a Core Plugin
porting...

### How to use a Core Plugin
...