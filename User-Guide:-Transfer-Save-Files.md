### GBA: Transfer save file from VisualBoyAdvance to mGBA

1. First open the game with the mGBA core plugin so that all necessary folders are created. While running the game, click the cog wheel icon on the HUD bar, choose Core > mGBA.

2. Navigate to the folder `~/Library/Application Support/OpenEmu/VisualBoyAdvance/Battery Saves` (~ meaning your Home folder where ~ is your username. See the [guide here](http://osxdaily.com/2016/12/12/show-user-library-folder-macos-sierra/) if you don't know this).

3. Copy the \<ROM name>.**sav2** save file to the folder `~/Library/Application Support/OpenEmu/mGBA/Battery Saves`

4. Rename \<ROM name>.**sav2** to \<ROM name>.**sav**

5. Launch OpenEmu, go to the Library sidebar, right click on "Game Boy Advance" > Default Core, and select mGBA

6. Go to OpenEmu > Preferences > Library, click "Reset warnings"

7. Open your game and click "No" if prompted to "Continue where you left off"

### SNES: Transfer save file from SNES9x to Higan
1. First open the game with the Higan core plugin so that all necessary folders are created. While running the game, click the cog wheel icon on the HUD bar, choose Core > Higan.

2. Navigate to the folder `~/Library/Application Support/OpenEmu/SNES9x/Battery Saves` (~ meaning your Home folder where ~ is your username. See the [guide here](http://osxdaily.com/2016/12/12/show-user-library-folder-macos-sierra/) if you don't know this).

3. Copy the \<ROM name>.sav save file to the folder `~/Library/Application Support/OpenEmu/Higan/Super Famicom/<ROM filename>`

4. Rename \<ROM name>.sav to save.ram

5. Launch OpenEmu, go to the Library sidebar, right click on "Super Nintendo" > Default Core, and select Higan

6. Go to OpenEmu > Preferences > Library, click "Reset warnings"

7. Open your game and click "No" if prompted to "Continue where you left off"
