Using the guide below, we will try and walk you through the steps required to download and compile the OpenEmu application from source. You will need a Macintosh computer running OS X 10.9 or greater. We recommend updating to the latest version and ensuring all software is up to date.

If you have used earlier OpenEmu versions, please see [Cleaning Up Previous Versions](https://github.com/OpenEmu/OpenEmu/wiki/Compiling-From-Source-Guide#cleaning-up-previous-versions) at the bottom **before** compiling OpenEmu.

##Command Line Install Guide (Advanced users)
Not afraid of the command line? Follow this guide if you already have Xcode and Command Line Tools and want to clone and compile via terminal. Otherwise, please follow the [GUI Install Guide](https://github.com/OpenEmu/OpenEmu/wiki/Compiling-From-Source-Guide#gui-install-guide-easy-mode).

Alternatively, you can easily install the necessary Command Line Tools by following [this guide](http://www.computersnyou.com/2025/). Xcode is still necessary for successful compilation.

### SSH Keys
Please follow [this guide] (https://help.github.com/articles/generating-ssh-keys) to setup secure authentication with GitHub's servers otherwise you may receive an error similar to this one:
```
Cloning into 'BSNES'...
Permission denied (publickey).
fatal: Could not read from remote repository.

Please make sure you have the correct access rights and the repository exists.
Clone of 'git@github.com:OpenEmu/BSNES-Core.git' into submodule path 'BSNES' failed
```
### Cloning
```
git clone --recursive https://github.com/OpenEmu/OpenEmu.git
cd OpenEmu
xcodebuild -workspace OpenEmu.xcworkspace -scheme "Build All" -configuration Release
```
The compiled OpenEmu.app binary is located in the default DerivedData path, `~/Library/Developer/Xcode/DerivedData` within a generated `OpenEmu-...` folder and then inside `Build/Products/Release`

To get the experimental build, which includes extra work-in-progress cores, change `"Build All"` to `"Build All + Experimental"`

##GUI Install Guide (Easy mode)
###Step 1

Download and install the latest copy of XCode, which is free software provided by Apple, from the Mac App Store at <https://itunes.apple.com/gb/app/xcode/id497799835>. At the time of writing, Xcode is a hefty download weighing in at 1.7GB. Download it, and while waiting for it to download, grab a coffee or watch some TV.

![XCode on The Mac App Store](http://i.imgur.com/1w9V4no.png)

###Step 2

**Warning: Do not download the ZIP! It will not work!**

With Xcode downloaded and installed on your computer, we now need to clone the source code for OpenEmu. 
Install Github for Mac from <http://mac.github.com/> and create a Github account. Then, navigate to the OpenEmu repo at <https://github.com/OpenEmu/OpenEmu> and click "Clone in Desktop".

![Clone Panel](http://i.imgur.com/ePKEDcp.png)
![Clone Button](http://i.imgur.com/d3mwhwW.png)
<br />
![Clone in Github for Mac](http://i.imgur.com/I6ObkRI.png)

**Note for advanced users:**
If you cloned OpenEmu from the command line you also need to initialize the submodules with: 
````
git submodule update --recursive --init
````

###Step 3

Once Github for Mac has finished cloning, browse to the 'OpenEmu' folder it cloned to.

![Browse to the OpenEmu Folder](http://i.imgur.com/Vu815wF.png)

###Step 4

Open the 'OpenEmu' folder and browse through the files until you find the XCode project file called 'OpenEmu.xcworkspace'. Double click this file and it should open in Xcode.

![OpenEmu Folder](http://i.imgur.com/pjtLaN7.png)

###Step 5

With Xcode open, you will see a lot of files and 'cores' that make up the OpenEmu application in the left sidebar. At the top of the application, you will see a lot of buttons. You need to click on the long bar to the right of the 'Stop' button and select the correct 'Scheme'.

![The Scheme Bar](http://i.imgur.com/64qjZJU.png)

Click on the left-most portion of this bar, and be sure to scroll through the popover and select 'Build All' > 'My Mac 64 Bit'...

![Selecting The Correct Scheme](http://i.imgur.com/nnlLkfu.png)

###Step 6

With the correct scheme selected in Step 5, you are now ready to compile the application. To do so, either press ⇧⌘I or click on 'Product' > 'Build For' > 'Profiling' in the menu bar. This makes sure that you get a release build that makes use of optimizations.

![Build for Profiling](http://f.cl.ly/items/1Z3G1G3X3E332Q0f0Q3T/profiling.png)

###Step 7

OpenEmu and all of its cores will now begin compiling. This process should take around 5 minutes to complete.

![OpenEmu Compiling - Status](http://i.imgur.com/j2LIMTg.png)

###Step 8

Once XCode has compiled OpenEmu, simply search for OpenEmu.app in Finder, right-click on it and select 'Open Enclosing Folder'.

![Select 'Open Enclosing Folder'](http://i.imgur.com/tgI8f6k.png)

This should show you the application inside the 'Release' folder.

![OpenEmu.app Inside the 'Release' Folder](http://i.imgur.com/mJAl02C.png)

You can, of course launch the application directly from this folder. Or, if you want it to be easier to find next time, you can move it over to your applications folder!

###Step 9

From here, you can begin adding and playing your favorite games and using the application as normal (assuming that the source code you downloaded is in a usable state!)

![OpenEmu: All Fresh & New](http://i.imgur.com/GrsCjf5.png)

## Cleaning Up Previous Versions

If you have installed or used earlier versions of OpenEmu, some things have changed that require manual cleanup to ensure proper functionality of OpenEmu 1.0.

### A) Remove older core and system plugins.

Navigate to your ~/Library/Application Support/OpenEmu/Cores/ folder and delete it.

Navigate to your ~/Library/Application Support/OpenEmu/Systems/ folder and delete it (If applicable. This is old and not everyone has this folder).

### B) Remove older key bindings.

Navigate to your ~/Library/Application Support/OpenEmu/Bindings Configurations/ folder and delete it.

### C) Remove older preferences

Run the following command in Terminal.app: `defaults delete org.openemu.OpenEmu`

### D) Proceed to Step 1 to compile OpenEmu.