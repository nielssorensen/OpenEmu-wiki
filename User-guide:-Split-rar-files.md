### Extracting split rar archive files
Sometimes a game might be packaged as a split archive inside a rar archive, or multiple rar's inside of a rar file. When this happens, there is usually a main `.rar`, `.part1.rar`, `.r00`, or `.001` file that you need to decompress which will begin decompressing all of the other files to end up with your game file. Follow the steps below to deal with these files.

1. Open up Terminal.app and install [Homebrew](http://brew.sh/)
2. Type `brew install unrar` and press enter to install the unrar package.
3. Type `cd ` (cd including a space at the end) and drag and drop the folder where your .rar files are into the Terminal window and press enter.
4. Type `unrar x ` (unrar x including a space at the end of the x) and drag and drop the first part of your split rar file, .part1.rar, .r00, .001 - whatever it is, into the Terminal window and press enter.