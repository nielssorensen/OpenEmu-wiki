1. [Getting Started](https://github.com/OpenEmu/OpenEmu/wiki/User-guide:-CD-based-games#getting-started)
2. [Importing](https://github.com/OpenEmu/OpenEmu/wiki/User-guide:-CD-based-games#importing)
3. [Supported Formats](https://github.com/OpenEmu/OpenEmu/wiki/User-guide:-CD-based-games#supported-formats)
4. [Cue Sheets](https://github.com/OpenEmu/OpenEmu/wiki/User-guide:-CD-based-games#cue-sheets)
5. [How to Dump a Physical CD](https://github.com/OpenEmu/OpenEmu/wiki/User-guide:-CD-based-games#how-to-dump-a-physical-cd)

Help

* [My cue sheet or CCD won't import](https://github.com/OpenEmu/OpenEmu/wiki/User-guide:-CD-based-games#q-my-cue-sheet-or-ccd-wont-import)
* [I have no music at all, only sound effects most of the time](https://github.com/OpenEmu/OpenEmu/wiki/User-guide:-CD-based-games#q-i-have-no-music-at-all-only-sound-effects-most-of-the-time)
* [I only have a single .BIN or .ISO file](https://github.com/OpenEmu/OpenEmu/wiki/User-guide:-CD-based-games#q-i-only-have-a-single-bin-or-iso-file)
* [I have a multi-disc game](https://github.com/OpenEmu/OpenEmu/wiki/User-guide:-CD-based-games#q-i-have-a-multi-disc-game)
* [I have an .ECM or .APE file](https://github.com/OpenEmu/OpenEmu/wiki/User-guide:-CD-based-games#q-i-have-an-ecm-or-ape-file)
* [I have a .CHD file from Archive.org](https://github.com/OpenEmu/OpenEmu/wiki/User-guide:-CD-based-games#q-i-have-a-chd-file-from-archiveorg)
* [I have a .MDF and a .MDS file](https://github.com/OpenEmu/OpenEmu/wiki/User-guide:-CD-based-games#q-i-have-a-mdf-and-a-mds-file)
* [I have a .SBI file](https://github.com/OpenEmu/OpenEmu/wiki/User-guide:-CD-based-games#q-i-have-a-sbi-file)

### Getting Started
Compressed archives (such as .rar, .zip, .7z, etc) are **NOT** supported for CD-based games — you must [uncompress](https://itunes.apple.com/us/app/the-unarchiver/id425424353?mt=12) them first.

### Importing
Dumped copies of CD-based games must be loaded in with [Cue sheets](https://en.wikipedia.org/wiki/Cue_sheet_%28computing%29) or [CloneCD](https://en.wikipedia.org/wiki/CloneCD_Control_File) files only.

Simply drag and drop a `.cue` or `.ccd` file into your library and OpenEmu will add all associated files along with it from the same folder. If a game is made up of multiple discs, please follow the [multi-disc guide](https://github.com/OpenEmu/OpenEmu/wiki/User-guide:-CD-based-games#q-i-have-a-multi-disc-game) instead.

Please make sure you are importing valid files by carefully reading the sections below.

### Supported Formats
PC Engine CD/TurboGrafx-CD, PC-FX, PlayStation, Sega Saturn (using Mednafen)
* CUE+BIN, both single and [multiple .BIN tracks](http://redump.org/)
* CUE+IMG, CUE+ISO
* CUE + BIN/IMG/ISO + [CDDA](https://en.wikipedia.org/wiki/Compact_Disc_Digital_Audio) tracks with [WAV/OGG/FLAC](http://www.mega-nerd.com/libsndfile/#Features). MP3 is **NOT** supported.
* CloneCD CCD+IMG+SUB

Mega CD/Sega CD (using Genesis Plus GX)
* CUE+BIN, CUE+IMG, CUE+ISO
* CUE + BIN/IMG/ISO + [CDDA](https://en.wikipedia.org/wiki/Compact_Disc_Digital_Audio) tracks with WAV/OGG. MP3 is **NOT** supported.

### Cue Sheets
A [cue sheet](https://en.wikipedia.org/wiki/Cue_sheet_%28computing%29) is a [plain text](https://en.wikipedia.org/wiki/Plain_text) file with a `.cue` extension containing [metadata](http://digitalx.org/cue-sheet/index.html) used to describe the layout of a CD, normally accompanied by one or more data files dumped from the original disc.

Below demonstrates how a cue sheet could be written for a PlayStation game with CDDA, depending on how it was dumped.

**Single binary track**
```
FILE "Castlevania - Symphony of the Night (USA).bin" BINARY
  TRACK 01 MODE2/2352
    INDEX 01 00:00:00
  TRACK 02 AUDIO
    INDEX 01 50:55:45

```
**Single binary track — pregap length and subcode flags**
```
FILE "CASTLEVANIA.BIN" BINARY
  TRACK 01 MODE2/2352
    FLAGS DCP
    INDEX 01 00:00:00
  TRACK 02 AUDIO
    FLAGS DCP
    PREGAP 00:02:00
    INDEX 01 50:53:45

```
**Single binary track — pregap start time with INDEX 00**
```
FILE "Castlevania - Symphony of the Night (USA).img" BINARY
  TRACK 01 MODE2/2352
    INDEX 01 00:00:00
  TRACK 02 AUDIO
    INDEX 00 50:53:45
    INDEX 01 50:55:45

```
**Multiple binary tracks. Data track + separate file for each audio track (common with [Redump](http://redump.org/))**
```
FILE "Castlevania - Symphony of the Night (USA) (Track 1).bin" BINARY
  TRACK 01 MODE2/2352
    INDEX 01 00:00:00
FILE "Castlevania - Symphony of the Night (USA) (Track 2).bin" BINARY
  TRACK 02 AUDIO
    INDEX 00 00:00:00
    INDEX 01 00:02:00

```
**Single binary track with WAVE audio track file**
```
FILE "Castlevania - Symphony of the Night (USA) (Track 1).iso" BINARY
  TRACK 01 MODE2/2352
    INDEX 01 00:00:00
FILE "Castlevania - Symphony of the Night (USA) (Track 2).wav" WAVE
  TRACK 02 AUDIO
    INDEX 00 00:00:00
    INDEX 01 00:02:00

```

### How to Dump a Physical CD
Try Redump's [CD dumping guide](http://wiki.redump.org/index.php?title=Dumping-Guides).

## Help
### Q. My cue sheet or CCD won't import
It is important that cue sheets are saved as [plain text](http://apple.stackexchange.com/a/17435), without ["smart quotes" or "smart dashes"](http://scttdvd.com/post/65242711516/how-to-get-rid-of-smart-quotes-osx-mavericks) and that tracks do not contain hardcoded paths, only filenames.

Open your cue sheet in TextEdit or another [plain text editor](https://macromates.com/download) and verify that the filename for `BINARY`:
* matches the filename of your `.bin/.img/.iso` file and is in the correct case
* has an extension: `FILE "CASTLEVANIA.BIN" BINARY` and **NOT** `FILE "CASTLEVANIA" BINARY`
* does not contain a hardcoded path: `FILE "C:\WINDOWS\DESKTOP\CASTLEVANIA.BIN" BINARY`

If using a CloneCD `.ccd`, you must also have a `.img` and `.sub` with matching filenames.

### Q. I have no music at all, only sound effects most of the time
It means you have a bad dump or the cue sheet is missing correct CDDA track information. There is no solution but to obtain a proper dump.

### Q. I only have a single .BIN or .ISO file
**It is strongly recommended to simply obtain another dump that is packaged properly.**

This is considered a bad/incomplete dump. It is necessary your game dump has an associated cue sheet because they are used to describe data and audio for the disc. Attempting to create your own without knowing the layout of the disc and how it was dumped, especially for a game that uses CD Audio (CDDA), will only result in problems.

### Q. I have a multi-disc game
You need to create a `.m3u` file containing the filenames of all the cue sheets for the game. The file **must be saved in a folder together with all the cue sheets and their associated files** in order for them to be automatically imported. Also, the cue sheets for the game must not already be pre-imported in your library. **Note: Mega CD/Sega CD is not supported.**

Example:

1. You have a multi-disc game such as *Chrono Cross* with two cue sheets `Chrono Cross (USA) (Disc 1).cue` and `Chrono Cross (USA) (Disc 2).cue`.

2. Now create a `.m3u` file by opening up your favorite [plain text editor](https://macromates.com/download) and copy and pasting the filenames of your cue sheets, one per line appearing as:

    ```
    Chrono Cross (USA) (Disc 1).cue
    Chrono Cross (USA) (Disc 2).cue
    ```
**Note: For CloneCD rips, only add the `.ccd` filenames to the `.m3u` file.**
![screen shot 2015-05-17 at 6 41 52 pm](https://cloud.githubusercontent.com/assets/1303132/7672776/71744a82-fcc4-11e4-983a-4918553460d2.png)

3. **IMPORTANT** — Save the file as **plain text** (if using TextEdit, select "Make Plain Text" from the Format menu) with a .m3u extension, for example ``Chrono Cross (USA).m3u``

4. Import only the `.m3u` file into your library as normal and the cue sheets will be automatically imported. It will appear in your PlayStation library and you can load it.

```
Folder containing all Chrono Cross files/
└╴Chrono Cross (USA) (Disc 1).bin
└╴Chrono Cross (USA) (Disc 1).cue
└╴Chrono Cross (USA) (Disc 2).bin
└╴Chrono Cross (USA) (Disc 2).cue
└╴Chrono Cross (USA).m3u    <-- import this file
```

Now, when you reach a point in-game where you must swap discs, select the required disc from the HUD control bar "Select Disc" menu like so:

![disc 2](https://cloud.githubusercontent.com/assets/1303132/7672801/e2dc3dd2-fcc5-11e4-9cf2-0c25a8069887.png)

### Q. I have an .ECM or .APE file

Dumps with `.ecm` and `.ape` are compressed data and audio tracks. These files must be uncompressed before they can be used.

Our example will use a cue sheet named `Castlevania - Symphony of the Night (USA).cue` with the contents and files:
```
FILE "Castlevania - Symphony of the Night (USA) (Track 1).bin" BINARY
  TRACK 01 MODE2/2352
    INDEX 01 00:00:00
FILE "Castlevania - Symphony of the Night (USA) (Track 2).bin" BINARY
  TRACK 02 AUDIO
    INDEX 00 00:00:00
    INDEX 01 00:02:00

```
```
Castlevania - Symphony of the Night (USA)/
└╴Castlevania - Symphony of the Night (USA) (Track 1).7z    <-- uncompress this file
│ └╴data.bin.ecm
└╴Castlevania - Symphony of the Night (USA) (Track 2).ape
```

**ECM**

The `.ecm` file must be decoded and renamed to match the `BINARY` track filename from the cue sheet.

1. Download [unecm](https://web.archive.org/web/20140330233023/http://www.neillcorlett.com/downloads/cmdpack-1.03-macosx-x86_64.tar.gz) (via the Command-Line Pack v1.03 by [Neill Corlett](https://web.archive.org/web/20140330233023/http://www.neillcorlett.com/cmdpack/))
2. [Uncompress](https://itunes.apple.com/us/app/the-unarchiver/id425424353?mt=12) cmdpack-1.03-macosx-x86_64.tar.gz and copy the `unecm` file to the same folder as your game with the `.ecm` file
 * If you have the [Homebrew package manager](http://brew.sh/), you might also use `brew install ecm`
3. Open your cue sheet in TextEdit or another [plain text editor](https://macromates.com/download) and notice the filename of the `BINARY` track and also the `.ecm` filename in your folder. e.g. `Castlevania - Symphony of the Night (USA) (Track 1).bin` and `data.bin.ecm`
4. Navigate to your game's folder in Terminal. Follow guides [here](http://apple.stackexchange.com/questions/11323/how-can-i-open-a-terminal-window-directly-from-my-current-finder-location) or [here](http://www.howtogeek.com/210147/how-to-open-terminal-in-the-current-os-x-finder-location/) to do this.
5. Decode your `.ecm`. In Terminal, enter the following command and press enter, making sure to add the correct filenames:

    `./unecm "data.bin.ecm" "Castlevania - Symphony of the Night (USA) (Track 1).bin"`

**APE**

The `.ape` file must be converted to PCM and renamed to match the `AUDIO` track filename from the cue sheet.

1. Download [X Lossless Decoder (XLD)](http://tmkk.undo.jp/xld/index_e.html)
2. Open XLD.app — the application is not signed, so you must right click and select Open
3. Go to XLD > Preferences menu and set the Output format to **PCM (little endian)**
4. To convert your file, just click on Open from the File menu, and navigate to your `.ape` file
5. The converted file will be named, for example, `Castlevania - Symphony of the Night (USA) (Track 2).pcm` which must then be renamed
6. To rename, right click on the `.pcm` file and select Get Info. From the Name & Extension section, change the file extension from `.pcm` to match the corresponding audio track inside the cue sheet, presumably `.bin`, resulting in `Castlevania - Symphony of the Night (USA) (Track 2).bin`

### Q. I have a .CHD file from [Archive.org](https://archive.org/details/software)

Some CD dumps are stored in a MAME/MESS-specific format capable of multiple layers of compression (LZMA/zlib/FLAC/Huffman) called CHD (Compressed Hunks of Data or Compressed Hard Disk images), containing a `.cue` and `.bin` file. These files must be uncompressed with `chdman` before they can be used.

1. Download and install the [SDL2](http://www.libsdl.org/download-2.0.php) framework for OS X.
2. Download a pre-compiled version of MAME or MESS 64-bit (x86_64) from [SDLMAME](http://sdlmame.lngn.net/)
3. [Uncompress](https://itunes.apple.com/us/app/the-unarchiver/id425424353?mt=12) the `.zip` file and copy the `chdman` file found inside the "tools" folder to the same folder as your game with the `.chd` file
4. Navigate to your game's folder in Terminal. Follow guides [here](http://apple.stackexchange.com/questions/11323/how-can-i-open-a-terminal-window-directly-from-my-current-finder-location) or [here](http://www.howtogeek.com/210147/how-to-open-terminal-in-the-current-os-x-finder-location/) to do this.
5. Extract your `.chd`. In Terminal, enter the following command and press enter, making sure to add the correct filenames:

    `./chdman extractcd -i "sonic cd (usa).chd" -o "sonic cd (usa).cue" -ob "sonic cd (usa).bin"`

### Q. I have a .MDF and a .MDS file

These are an alternative format to iso/bin images created by some software like Alcohol 120%. They are very easy to convert into .bin/.cue.

1. Install a command-line tool named mdf2iso using either macports or homebrew.

    `$ brew install mdf2iso`
2. In the directory with both .mdf and .mds files, run the following command to convert into .bin/.cue.

    `$ mdf2iso --cue name_of_file.mdf`
3. This will generate compatible .bin/.cue files in the same directory, with the same name as the original image.

### Q. I have a .SBI file

Hundreds of PAL region PlayStation games used [LibCrypt](http://wiki.redump.org/index.php?title=PlayStation_1:_LibCrypt_protection), a copy protection mechanism that stored non-standard data in subchannels on the disc. If missing from a backup, this crippled games by disabling input ([Ape Escape](https://tcrf.net/Ape_Escape_(PlayStation)#Anti-Piracy)), impossible difficulty (Lucky Luke: Western Fever), mysterious bugs ([Spyro: Year of the Dragon](https://tcrf.net/Spyro:_Year_of_the_Dragon#Anti-Piracy_Message)) or freezing at boot (Resident Evil 3: Nemesis) or during a level (Wip3out).

Dumped copies that use **cue sheets** require additional `.sbi` subchannel data files in order for these games to work.

Download `.sbi` files for affected games from [redump.org](http://redump.org/discs/libcrypt/2/) by first choosing your game and then finding "SBI subchannels" at the top of the page.

Drag and drop the `.sbi` to import it alongside your game. **IMPORTANT** — The `.sbi` file **must** be named exactly as the base filename of your cue sheet including case e.g.
* `Ape Escape (Europe).cue` and `Ape Escape (Europe).sbi`
* `Wip3out (Europe) (En,Fr,De,Es,It).CUE` and `Wip3out (Europe) (En,Fr,De,Es,It).SBI`

**Note: [multi-disc games](https://github.com/OpenEmu/OpenEmu/wiki/User-guide:-CD-based-games#q-i-have-a-multi-disc-game) such as Final Fantasy VIII, Final Fantasy IX, Galerians and Parasite Eve II must have all `.sbi` files for each disc imported.**