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

![Add Target](http://i.imgur.com/MZDnp.png) ![Bundle](http://i.imgur.com/DIhbR.png)

A folder with the Product Name you chose will be generated with some files. This should be moved into the System Plugins group.

Once created, you will then have to add some custom OE-related values to the [Product Name]-Info.plist. These will include, OEArchiveIDs, OEControlListKey, OEFileSuffixes, Principal Class, OESystemIcon, OESystemPluginName and OESystemIdentifier. Since all system plugins follow the same structure, **please view a plist of another plugin for guidance on what values to fill in.**

Once finished, you will have a [Product Name]-Info.plist that looks like this:

![Info](http://i.imgur.com/6q0fe.png)

Next go to the Build Phases tab for your new system plugin and add OpenEmuSystem for Target Dependencies and OpenEmuSystem.framework under Link Binary With Libraries.

![Build Phases](http://i.imgur.com/FV0iI.png)

In the Build Settings tab under Packaging, change the Wrapper Extension to **oesystemplugin**

![Build Settings](http://i.imgur.com/ZZwJn.png)

Finally, edit the Build SystemPlugins target. Under the Build Phases tab, add the new system plugin for Target Dependencies and Copy Files. This will tell the scheme to build the new **.oesystemplugin** when you compile OpenEmu.

![Build SystemPlugins](http://i.imgur.com/HqnWO.png)

While some files will be auto-generated, SystemController and SystemResponder classes and headers still need to be created.
These classes are similar in all systems so we can duplicate a set from another system and then edit accordingly.

**The following 5 class and header files must be created for a new system plugin:**

* OE[SystemName]SystemController.m and .h
* OE[SystemName]SystemResponder.m and .h
* OE[SystemName]SystemResponderClient.h

For our TurboGrafx-16/PC Engine example:

SystemController header

    /* OEPCESystemController.h */
    #import <Cocoa/Cocoa.h>
    #import <OpenEmuSystem/OpenEmuSystem.h>

    @interface OEPCEController : OESystemController

    @end

SystemController class

    /* OEPCESystemController.m */
	#import "OEPCESystemController.h"
	#import "OEPCESystemResponder.h"
	#import "OEPCESystemResponderClient.h"

	@implementation OEPCESystemController

	- (NSUInteger)numberOfPlayers;
	{
    	return 1;
	}

	- (Class)responderClass;
	{
    	return [OEPCESystemResponder class];
	}

	- (NSArray *)genericSettingNames;
	{
    	return [super genericSettingNames];
	}

	- (NSArray *)genericControlNames;
	{
    	return [NSArray arrayWithObjects:OEPCEButtonNameTable count:OEPCEButtonCount];
	}

	- (NSDictionary *)defaultControls
	{
    	NSDictionary *controls = [NSDictionary dictionaryWithObjectsAndKeys:
                              	[NSNumber numberWithUnsignedInt:kHIDUsage_KeyboardUpArrow]   , @"OEPCEButtonUp[1]"    ,
                              	[NSNumber numberWithUnsignedInt:kHIDUsage_KeyboardDownArrow] , @"OEPCEButtonDown[1]"  ,
                              	[NSNumber numberWithUnsignedInt:kHIDUsage_KeyboardLeftArrow] , @"OEPCEButtonLeft[1]"  ,
                              	[NSNumber numberWithUnsignedInt:kHIDUsage_KeyboardRightArrow], @"OEPCEButtonRight[1]" ,
                              	[NSNumber numberWithUnsignedInt:kHIDUsage_KeyboardA]         , @"OEPCEButton1[1]"     ,
                              	[NSNumber numberWithUnsignedInt:kHIDUsage_KeyboardS]         , @"OEPCEButton2[1]"     ,
                              	[NSNumber numberWithUnsignedInt:kHIDUsage_KeyboardSpacebar]  , @"OEPCEButtonRun[1]" ,
                              	[NSNumber numberWithUnsignedInt:kHIDUsage_KeyboardEscape]    , @"OEPCEButtonSelect[1]",
                              	nil];
		return controls;
	}

	- (NSUInteger)playerNumberInKey:(NSString *)keyName getKeyIndex:(NSUInteger *)idx{
		if(idx!=NULL) *idx = [[self genericControlNames] indexOfObject:keyName];
	
		return 1;
	}

	@end

SystemResponder header

    /* OEPCESystemResponder.h */
	#import <Cocoa/Cocoa.h>
	#import <OpenEmuSystem/OpenEmuSystem.h>

	@protocol OEPCESystemResponderClient;

	extern NSString *OEPCEButtonNameTable[];

	@interface OEPCESystemResponder : OEBasicSystemResponder

	@property(nonatomic, weak) id<OEPCESystemResponderClient> client;

	@end

SystemResponder class

    /* OEPCESystemResponder.m */
	#import "OEPCESystemResponder.h"
	#import "OEPCESystemResponderClient.h"

	NSString *OEPCEButtonNameTable[] =
	{
    	@"OEPCEButton1[@]",
    	@"OEPCEButton2[@]",
    	@"OEPCEButtonUp[@]",
    	@"OEPCEButtonDown[@]",
    	@"OEPCEButtonLeft[@]",
    	@"OEPCEButtonRight[@]",
    	@"OEPCEButtonRun[@]",
    	@"OEPCEButtonSelect[@]"
	};

	@implementation OEPCESystemResponder
	@dynamic client;

	+ (Protocol *)gameSystemResponderClientProtocol;
	{
    	return @protocol(OEPCESystemResponderClient);
	}

	- (OEEmulatorKey)emulatorKeyForKeyIndex:(NSUInteger)index player:(NSUInteger)thePlayer
	{
    	return OEMakeEmulatorKey(0, index);
	}

	- (void)pressEmulatorKey:(OEEmulatorKey)aKey
	{
    	[[self client] didPushPCEButton:(OEPCEButton)aKey.key];
	}

	- (void)releaseEmulatorKey:(OEEmulatorKey)aKey
	{
    	[[self client] didReleasePCEButton:(OEPCEButton)aKey.key];
	}

	@end

SystemResponderClient header

    /* OEPCESystemResponderClient.h */
	#import <Foundation/Foundation.h>

	@protocol OESystemResponderClient;

	typedef enum _OEPCEButton
	{
    	OEPCEButton1,
    	OEPCEButton2,
    	OEPCEButtonUp,
    	OEPCEButtonDown,
    	OEPCEButtonLeft,
    	OEPCEButtonRight,
    	OEPCEButtonRun,
    	OEPCEButtonSelect,
    	OEPCEButtonCount,
	} OEPCEButton;

	@protocol OEPCESystemResponderClient <OESystemResponderClient, NSObject>

	- (void)didPushPCEButton:(OEPCEButton)button;
	- (void)didReleasePCEButton:(OEPCEButton)button;

	@end

Supporting Files:
...

![Supporting Files](http://i.imgur.com/9BOzd.png)

Our end result with be a new system plugin in the UI and controller in the Preferences.

![Controller](http://i.imgur.com/XPTUS.png) &nbsp; ![Controller](http://i.imgur.com/nseV4.png)

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