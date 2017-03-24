### Required m3u file missing
<p align="center"><img src="http://i.imgur.com/QQdcQ1J.png" alt="Required m3u file missing" width="532"></p>

This message means you are trying to load a game that requires multiple discs. Follow the [Multi-disc Guide](https://github.com/OpenEmu/OpenEmu/wiki/User-guide:-CD-based-games#q-i-have-a-multi-disc-game) to properly import your game. If you had previously saved progress, follow the steps below to transfer your save data.

### Transfer your save data

1. In the app, go to OpenEmu > Preferences > Library, click "Reset warnings"

2. Delete all the currently imported single discs for your game. Select your games and right click > Delete Game, at the prompt click "Delete Game" and then "Move to Trash" at the next prompt.
<img src="http://i.imgur.com/GwZFKuj.jpg" alt="Imported single discs" width="942">

3. Ensure you have properly imported your game by following the [Multi-disc Guide](https://github.com/OpenEmu/OpenEmu/wiki/User-guide:-CD-based-games#q-i-have-a-multi-disc-game).

<img src="http://i.imgur.com/vwfyQ61.jpg" alt="Imported multi discs" width="942">

4. Load your game and let it reach the in-game title screen (past the PlayStation startup screens) so that it will generate new save files based on the imported m3u file. Afterwards, close your game.

5. Navigate to the folder `~/Library/Application Support/OpenEmu/Mednafen/Battery Saves` (~ meaning your Home folder where ~ is your username. See the [guide here](http://osxdaily.com/2016/12/12/show-user-library-folder-macos-sierra/) if you don't know this).

6. In your `Battery Saves` folder, it has the newly generated save files and your original save files.
<img src="http://i.imgur.com/YZtERot.png" alt="Battery Saves Folder" width="882">

Rename your original save files to match the newly generated save files. For example, first delete the newly generated files but take note of the filenames. Then, rename your original save files to match the filenames of the newly generated files that you just deleted.

Original save files:

`Metal Gear Solid (USA) (Disc 1) (v1.1).4fe57a0bbcf59082a2d11ef886f8f0bd.0.mcr`\
`Metal Gear Solid (USA) (Disc 1) (v1.1).4fe57a0bbcf59082a2d11ef886f8f0bd.1.mcr`

Renamed to match newly generated save filenames:

`Metal Gear Solid (USA) (v1.1).2f876f4966ab9a14472349c43b3d64a4.0.mcr`\
`Metal Gear Solid (USA) (v1.1).2f876f4966ab9a14472349c43b3d64a4.1.mcr`

```
Folder containing Battery Saves files/
└╴Metal Gear Solid (USA) (Disc 1) (v1.1).4fe57a0bbcf59082a2d11ef886f8f0bd.0.mcr <-- rename this file
└╴Metal Gear Solid (USA) (Disc 1) (v1.1).4fe57a0bbcf59082a2d11ef886f8f0bd.1.mcr <-- rename this file
└╴Metal Gear Solid (USA) (v1.1).2f876f4966ab9a14472349c43b3d64a4.0.mcr
└╴Metal Gear Solid (USA) (v1.1).2f876f4966ab9a14472349c43b3d64a4.1.mcr
```

Your `Battery Saves` folder should now only contain your **renamed** original save files.
<img src="http://i.imgur.com/tW3DzXO.png" alt="Battery Saves Folder" width="882">

7. Finally, open your game and click "No" when prompted to "Continue where you left off" to play using your transferred save data.