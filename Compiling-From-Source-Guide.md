
Using the guide below, we will try and walk you through the steps required to download and compile the OpenEmu application from source. You will need a Macintosh computer running OSX 10.8 or above. We recommend updating to the latest version and ensuring all software is up to date...

{{insert some mention or insutructions if you have compiled or installed the app before?}}

###Step 1

Download and install the latest copy of XCode from the Mac App Store... 

![XCode Is Available Via The Mac App Store](http://cl.ly/image/283l3Y201r1C)

This is free software provided by Apple. It is a hefty download weighing in at 1.5GB at time of writing. So download it, grab a coffee and see you for step 2 once the download is complete!

###Step 2

With Xcode downloaded and installed on your computer, we now need to go and grab the source code for OpenEmu. To get this, please go to the following page: <https://github.com/OpenEmu/OpenEmu> and downlaod the latest .zip repository. You will see a button labelled 'ZIP' with a little cloud like icon next to it. Click that, and your download will begin...

![Download The ZIP Repository](http://cl.ly/image/1L2U3H1u2x02)

###Step 3

Once the ZIP repository has finished downloading, the .zip file should automatically extract and you will be left with a folder called 'OpenEmu-master' in your download location (commonly your download location will be the 'Downloads' folder in your home repository)

###Step 4

Open the folder called 'OpenEmu-master' and browse through the files until you find the XCode project file called 'OpenEmu.xcworkspace'...

![OpenEmu-master Folder](http://cl.ly/image/1h2z0J0i061t)

Double click this file and it should launch Xcode.

###Step 5

With Xcode open, you will see a lot of files and 'cores' that make up the OpenEmu application in the left sidebar. At the top of the application you will see a lot of buttons. You need to click on the funky looking long bar and select the correct 'Scheme'...

![The Scheme Bar](http://cl.ly/image/3n2P0g2C1i1v)

Click on the left-most portion of this bar, and be sure to scroll through the popover and select 'Build All' > 'My Mac 64 Bit' {{insert some note here about that?}}...

![Selecting The Correct Scheme](http://cl.ly/image/2n1a0q2B1w3w)

###Step 6

With the correct scheme selected in Step 5, you are now ready to build and compile the application. To do so, click on the 'Run' button top left of Xcode (it looks like a Play button). This will begin compiling the application. This process should take around 5 minutes or so to complete...

![OpenEmu Compiling - Status](http://cl.ly/image/0T1s0Y2J2X1j)

###Step 7

Once Xcode has finished compiling the application, it should launch OpenEmu. (if not you can find the application and launch it manually by going to Step 8 below)...

![OpenEmu: All Fresh & New](http://cl.ly/image/2w1f1S3K1W3V)

From here, you can begin playing your favorite games and using the application as normal (assuming that the source code you downloaded is in a usable state!).

###Step 8

You will most likely want to use OpenEmu again after quitting the application or quitting Xcode in Step 7. XCode has compiled and placed the application in a rather unusual place. From the desktop, hold down the 'alt' key on your keyboard and click on the 'Go' item in the menubar. With the alt key still held down, click on the  item labelled 'Library'. This will open up your user Library folder. From here, navigate through the following folder hierarchy:

Library > Developer > Xcode > DerivedData > OpenEmu-eshbhsb... (or something similar) > Build > Products > Debug > OpenEmu.app

![OpenEmu.app Inside The 'Debug' Folder](http://cl.ly/image/0l0m3c2l3U0d)

You can of course launch the application directly from this folder, or, feel free to move it over to your applciations folder so it is easier to find and launch next time!.