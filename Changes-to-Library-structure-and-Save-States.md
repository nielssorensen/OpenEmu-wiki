
## Library
In order to outsource cover artwork from the main database file, structure of the library folder (default path ~/Library/Application Support/OpenEmu/Game Library/) will change a little bit.

If "Copy game files to library" or "Keep games organized" is enabled rom files will be copied to subfolders of ROMs/ which are named with the system's identifier and localized to display nicely (no change there, except for localization).

Cover Images go to Covers/original and are named with UUIDs that are stored in the database. To improved grid view performance we can create thumbnails of various sizes (stored in separate subfolders of Covers/) and event pre-render effects like gloss and shadow.

The new folder structure will look like this:

### Library Folder

	Library.storedata
	ROMs/
		unsorted/				**folder name is localized**
		com.openemu.nes/		**folder name is localized**
			somerom.nes
	Covers/
		original/							**folder holds original cover images**
			A73314C4-8298-44A5-83DE-D57E7B5B98BE
			EE1D36B5-501C-4781-A0FE-55BB65C0C8BF
			FC75299B-FD23-4CA8-B6D9-6AFE4494043
		150/								**folder with resized cover images (and effects?)**
			A73314C4-8298-44A5-83DE-D57E7B5B98BE
			EE1D36B5-501C-4781-A0FE-55BB65C0C8BF
			FC75299B-FD23-4CA8-B6D9-6AFE4494043
		350/								**folder with resized cover images (and effects?)**
			A73314C4-8298-44A5-83DE-D57E7B5B98BE
			EE1D36B5-501C-4781-A0FE-55BB65C0C8BF
			FC75299B-FD23-4CA8-B6D9-6AFE4494043

I'd like to convert the folder to a bundle (like iPhoto Libraries) so we can give it an icon and make changing libraries easy (just double-click a .oelib or something).



## Save States

I think save states should also be bundles. (Just noticed that they are in the public version 1.0b7).
So we should go back to that, with slight changes to the info plist. I suggest the following:

	Some Save State.oesavestate/
		StateData.data
		Image.data
		Info.plist
			Version			: 	0.1
			Name			:	"some save state"
			Description		:	"This is a description of the state"
			ROM MD5			:	"0d3186e5319dc2d21b14a7a2a59581ee"
			Core Identifier	:	"com.openemu.snes9x"
		
			**up for discussion:**
			ROM bookmarkData	:	<d41d8cd98f00b204e9800998ecf8427e51d86f3e60bd
							42b6e145deeeb4a660f0d41d8cd98f00b204e9800998e
							cf8427e>
			Creation Date		:	1331304341