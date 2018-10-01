Using the guide below, we will try and walk you through the steps required to download and compile the OpenEmu application from source. You will need a Mac running the latest stable version of [Xcode](https://itunes.apple.com/us/app/xcode/id497799835?mt=12).

If you have used earlier OpenEmu versions, please see [Cleaning Up Previous Versions](https://github.com/OpenEmu/OpenEmu/wiki/Compiling-From-Source-Guide#cleaning-up-previous-versions) at the bottom **before** compiling OpenEmu.

## Command Line Install Guide (Advanced users)
Not afraid of the command line? Follow this guide if you already have Xcode or Command Line Tools and want to clone and compile via terminal. Otherwise, please follow the [Visual Install Guide](https://github.com/OpenEmu/OpenEmu/wiki/Compiling-From-Source-Guide#visual-install-guide-easy-mode).

Alternatively, you can easily install the necessary Command Line Tools by following [this guide](http://www.computersnyou.com/2025/). Xcode is still necessary for successful compilation.

### SSH Keys
Please follow [this guide](https://help.github.com/articles/generating-ssh-keys) to setup secure authentication with GitHub's servers otherwise you may receive an error similar to this one:
```
Cloning into 'BSNES'...
Permission denied (publickey).
fatal: Could not read from remote repository.

Please make sure you have the correct access rights and the repository exists.
Clone of 'git@github.com:OpenEmu/BSNES-Core.git' into submodule path 'BSNES' failed
```

Alternatively you can force git to use HTTPS when talking to GitHub by typing the following command into your command line.
```
git config --global url."https://github.com".insteadOf git://github.com
```
For more information on what this does see the [Git documentation](https://git-scm.com/docs/git-config#git-config-urlltbasegtinsteadOf).

### Cloning & Compiling
```
git clone --recursive https://github.com/OpenEmu/OpenEmu.git
cd OpenEmu
xcodebuild -workspace OpenEmu.xcworkspace -scheme "OpenEmu" -configuration Release
```
The compiled OpenEmu.app binary is located in the default DerivedData path, `~/Library/Developer/Xcode/DerivedData` within a generated `OpenEmu-...` folder and then inside `Build/Products/Release`

To get the core plugins, change `"OpenEmu"` to `"Build All"`

To get the 'experimental' core plugins, change `"OpenEmu"` to `"Build All + Experimental"`

## Visual Install Guide (Easy mode)
### Step 1

Download and install the latest version of [Xcode](https://itunes.apple.com/us/app/xcode/id497799835?mt=12) from the Mac App Store.

<img src="https://i.imgur.com/N5oyW28.png" alt="Xcode on The Mac App Store" width="1352">

### Step 2

**Warning: Do not download the ZIP! It will not work!**

With Xcode downloaded and installed on your computer, we now need to clone the source code for OpenEmu. 
Install [GitHub Desktop](https://desktop.github.com/) for Mac, then navigate to the [OpenEmu repo](https://github.com/OpenEmu/OpenEmu) and click Clone > Open in Desktop.

<img src="http://i.imgur.com/ubNbwe0.png" alt="Clone Panel" width="357">

![Clone in Github for Mac](https://i.imgur.com/gXVVjd9.png)

**Note for advanced users:**
If you cloned OpenEmu from the command line you also need to initialize the submodules with: 
````
git submodule update --init --recursive
````

### Step 3

Once Github for Mac has finished cloning, browse to the 'OpenEmu' folder it cloned to.

<img src="http://i.imgur.com/ih36Zv4.png" alt="Browse to the OpenEmu Folder" width="882">

### Step 4

Open the 'OpenEmu' folder and browse through the files until you find the Xcode workspace file called 'OpenEmu.xcworkspace'. Double click this file and it should open in Xcode.

<img src="http://i.imgur.com/EykWlqL.png" alt="OpenEmu Folder" width="882">

### Step 5

With Xcode open, you will see a lot of files and 'cores' that make up the OpenEmu application in the left sidebar. At the top of the application, you will see a lot of buttons. You need to click on the long bar to the right of the 'Stop' button and select the correct 'Scheme'.

<img src="http://i.imgur.com/u5ZJg4q.png" alt="The Scheme Bar" width="272">

Click on the left-most portion of this bar, and be sure to scroll through the popover and select 'OpenEmu' > 'My Mac'...

<img src="http://i.imgur.com/D72UpRS.png" alt="Selecting The Correct Scheme" width="364">

### Step 6

With the correct scheme selected in Step 5, you are now ready to compile the application. To do so, either press ⇧⌘I or click on 'Product' > 'Build For' > 'Profiling' in the menu bar. This makes sure that you get a release build that makes use of optimizations.

<img src="http://i.imgur.com/NHeFbIG.png" alt="Build for Profiling" width="344">

### Step 7

OpenEmu and all of its cores will now begin compiling. This process should take around 5 minutes to complete.

<img src="http://i.imgur.com/kBXHLvD.png" alt="OpenEmu Compiling - Status" width="417">

### Step 8

Once Xcode has compiled OpenEmu, simply search for OpenEmu.app in using [Spotlight](https://support.apple.com/en-us/HT204014).

<img src="http://i.imgur.com/zTsmaWE.png" alt="OpenEmu.app Spotlight Search" width="792">

This should show you the application inside the 'Release' folder.

<img src="http://i.imgur.com/X94eOeo.png" alt="OpenEmu.app Inside the 'Release' Folder" width="882">

You can launch the app directly from this folder or move it over to your Applications folder.

### Step 9

From here, you can begin adding and playing your favorite games and using the application as normal (assuming that the source code you downloaded is in a usable state!)

<img src="http://i.imgur.com/7p4VtP7.jpg" alt="OpenEmu: All Fresh & New" width="942">

## Cleaning Up Previous Versions

If you have installed or used earlier versions of OpenEmu, some things have changed that require manual cleanup to ensure proper functionality of OpenEmu 2.0.

### A) Remove older core and system plugins.

Navigate to your ~/Library/Application Support/OpenEmu/Cores/ folder and delete it.

Navigate to your ~/Library/Application Support/OpenEmu/Systems/ folder and delete it (If applicable. This is old and not everyone has this folder).

### B) Remove older key bindings.

Navigate to your ~/Library/Application Support/OpenEmu/Bindings/ folder and delete it.

### C) Remove older preferences

Run the following command in Terminal.app: `defaults delete org.openemu.OpenEmu`

### D) Proceed to Step 1 to compile OpenEmu.