The process for adding [CD](http://en.wikipedia.org/wiki/Compact_disc)-based game ROMs — like those for the PlayStation and Mega CD — to OpenEmu is slightly different than for [cartridge](http://en.wikipedia.org/wiki/ROM_cartridge)-based games. Rather than using a single ROM file, OpenEmu requires the use of a [cue sheet](http://en.wikipedia.org/wiki/Cue_sheet_%28computing%29) — a file that describes how the data on a CD is laid out.

A cue sheet is a plain-text file with a `.cue` extension which accompanies one or more data files (in the case of game ROMs, usually a `.bin` or `.iso` file) and describes how the data files are used to represent the CD they were derived from. A very simple cue sheet for a game disc might look like this:

```
FILE "gamename.bin" BINARY
  TRACK 01 MODE1/2352
    INDEX 01 00:00:00
```

However, some are more complicated.

Usually, a cue sheet will be distributed with the ROM download. If it is not, one can be generated in some cases by hand or by using a third-party utility (Google 'cue sheet maker'). However, this is not always possible, and a proper cue sheet must be obtained elsewhere. It is recommended to simply obtain ROM downloads from a source which packages them properly.

Since a cue sheet does not actually contain any ROM data, any files it references must accompany it, usually in the same directory. **It is vitally important that the data file name matches the file name in the cue sheet** — if you change the name or path of the data file (the `.bin` or `.iso`) without updating the cue sheet, OpenEmu will not be able to load it.

### Limitations

1. OpenEmu will not load CD-based games from an archive (e.g., `.zip`) file.

2. Game discs are sometimes distributed with the CD audio in MP3 or WAV format; OpenEmu can not load games in this format. Removing any references to the `.mp3` or `.wav` files from the cue sheet will allow OpenEmu to load the disc properly, but the game will probably not have any sound.