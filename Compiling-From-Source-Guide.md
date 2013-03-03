Using the guide below, we will try and walk you through the steps required to download and compile the OpenEmu application from source. You will need a Macintosh computer running OSX 10.7 or 10.8. We recommend updating to the latest version and ensuring all software is up to date...

If you have used earlier OpenEmu versions (Version 1.0b7, please see "Cleanup Earlier Versions" at the bottom before compiling OpenEmu)

###Step 1

Download and install the latest copy of XCode from the Mac App Store: <https://itunes.apple.com/gb/app/xcode/id497799835?mt=12> This is free software provided by Apple. It is a hefty download weighing in at 1.5GB at time of writing. So download it, grab a coffee and see you for step 2 once the download is complete!... 

![XCode Is Available Via The Mac App Store](http://f.cl.ly/items/0Q3u3G2N351Z120t0823/0.jpg)

###Step 2

With Xcode downloaded and installed on your computer, we now need to go and grab the source code for OpenEmu. To get this, please go to the following page: <https://github.com/OpenEmu/OpenEmu> and download the latest .zip repository. You will see a button labelled 'ZIP' with a little cloud like icon next to it. Click that, and your download will begin...

![Download The ZIP Repository](http://f.cl.ly/items/1T443P381a2U2r2G2L13/1.png)

###Step 3

Once the ZIP repository has finished downloading, the .zip file should automatically extract and you will be left with a folder called 'OpenEmu-master' in your download location (commonly your download location will be the 'Downloads' folder in your home repository)

###Step 4

Open the folder called 'OpenEmu-master' and browse through the files until you find the XCode project file called 'OpenEmu.xcworkspace'. Double click this file and it should launch Xcode....

![OpenEmu-master Folder](http://f.cl.ly/items/202V3S0R1c1o0x0s1V3z/3.png)

###Step 5

With Xcode open, you will see a lot of files and 'cores' that make up the OpenEmu application in the left sidebar. At the top of the application you will see a lot of buttons. You need to click on the funky looking long bar and select the correct 'Scheme'...

![The Scheme Bar](http://f.cl.ly/items/1O0f2P1m0u1P2w450d0W/4.png)

Click on the left-most portion of this bar, and be sure to scroll through the popover and select 'Build All' > 'My Mac 64 Bit'...

![Selecting The Correct Scheme](http://f.cl.ly/items/0y400G2o3B0q30311Q0J/5.png)

###Step 6

With the correct scheme selected in Step 5, you are now ready to build and compile the application. To do so, either press ⇧⌘I or click on 'Product' > 'Build For' > 'Profiling' in the menu bar up top. This makes sure that you get a release build that makes use of all those optimizations.

![Build for profiling](http://f.cl.ly/items/1Z3G1G3X3E332Q0f0Q3T/profiling.png)

###Step 7

This will begin compiling the application. This process should take around 5 minutes or so to complete...

![OpenEmu Compiling - Status](http://f.cl.ly/items/1g060b2B3t2N2b2U0W02/6.png)

###Step 8

XCode has compiled OpenEmu, and placed a link to it in the Products folder in the XCode Project. Make sure you are on the Project Navigator tab (underneath the Run button, you should see a Folder icon, make sure it is selected). Reveal the files in the OpenEmu Project by clicking the disclosure triangle on the OpenEmu Project, and then press the disclosure triangle for the "Products" folder. You can then control click on OpenEmu.app, and "Show in Finder".

![OpenEmu Product location](http://i.imgur.com/2oKbN.png)


![OpenEmu.app Inside The 'Debug' Folder](http://f.cl.ly/items/2z0W3B1P1O2i0w142f0I/8.png)

You can of course launch the application directly from this folder, or, feel free to move it over to your applications folder so it is easier to find and launch next time!.

###Step 9

From here, you can begin playing your favorite games and using the application as normal (assuming that the source code you downloaded is in a usable state!)....

![OpenEmu: All Fresh & New](http://f.cl.ly/items/220f2f270x270B3r1I3p/7.png)

### Cleaning Up Previous Versions

If you have installed or used earlier versions of OpenEmu, some things have changed that require manual cleanup to ensure proper functionality of OpenEmu 1.0.

### A) Remove older cores.

Navigate to your /Library/Application Support/OpenEmu folder and delete it.

### B) Remove older preferences

Navigate to you home folder, library: ~/Library/Preferences/ and remove the org.openemu.OpenEmu.plist preferences file there, and any files labeled OpenEmu.

### C) Procede to Step 1 to compile OpenEmu.