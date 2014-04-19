Like many emulators, OpenEmu allows the use of [cheat codes](http://en.wikipedia.org/wiki/Cheating_in_video_games) to change the way a game plays (invincibility, level skipping, &c.).

Cheat-code support in OpenEmu is determined by each [core](https://github.com/OpenEmu/OpenEmu/wiki/User-guide:-Preferences:-Cores) and its underlying emulation code. Some cores do not support cheat codes; OpenEmu knows which cores those are, and its cheat functionality will not be available when they are in use.

### Adding cheats

To add a cheat code, you must be running a game. Within the game window, move the mouse to produce the [HUD bar](#), and click the cog/gear icon near the centre. If the core supports cheat codes, a menu item called *Select Cheat* will be available. In this menu, there will be another item labelled *Add Cheat...* — click here to input a new code.

![HUD Select Cheat menu](https://raw.github.com/okdana/OpenEmu-documentation/master/assets/img/user%20guide/HUD%20-%20Select%20Cheat%20-%20Add%20Cheat%20%28no%20game%29.png)

In the dialogue that opens, you can enter a name for the cheat (to identify it in the *Select Cheat* menu), as well as the code itself. Enter codes in whatever format the core supports; usually, these formats will be identical to the most popular cheat devices available for the system in question (such as Action Replay or Game Genie). You can also choose to enable a cheat right away or wait to enable it later.

![Add Cheat dialogue](http://i.imgur.com/6nQUt58.png)

The following table shows a non-exhaustive list of common code types:

<table>

<tr>
<th>Console</th>
<th>Cheat type</th>
<th>Example code</th>
</tr>

<tr>
<td>Famicom / NES</td>
<td>Action Replay</td>
<td>02A2:01</td>
</tr>

<tr>
<td>Famicom / NES</td>
<td>Game Genie</td>
<td>APEETPEY</td>
</tr>

<tr>
<td>Game Boy</td>
<td>Game Genie</td>
<td>FA1-B9C-4C1</td>
</tr>

<tr>
<td>Game Boy (Color)</td>
<td>GameShark</td>
<td>0101CEC1</td>
</tr>

<tr>
<td>Game Boy Advance</td>
<td>GameShark v3</td>
<td>CD93194F 089CE0B4</td>
</tr>

<tr>
<td>Game Boy Advance</td>
<td>GameShark v1/v2</td>
<td>A62B1D67 EB2D</td>
</tr>

<tr>
<td>Game Gear</td>
<td>Action Replay</td>
<td>00D3-C280</td>
</tr>

<tr>
<td>Mega Drive / Genesis</td>
<td>Action Replay</td>
<td>FFFE21:0032</td>
</tr>

<tr>
<td>Mega Drive / Genesis</td>
<td>Game Genie</td>
<td>NN8A-AADN</td>
</tr>

<tr>
<td>N64</td>
<td>GameShark</td>
<td>8033B177 0015</td>
</tr>

<tr>
<td>NDS</td>
<td>Action Replay</td>
<td>22085A50 00000001</td>
</tr>


<tr>
<td>Sega Master System</td>
<td>Action Replay</td>
<td>00C0-2502</td>
</tr>

<tr>
<td>Super Famicom / SNES</td>
<td>Action Replay</td>
<td>7E1490:FF</td>
</tr>

<tr>
<td>Super Famicom / SNES</td>
<td>Game Genie</td>
<td>14B4-6F07</td>
</tr>

</table>

For multi-line codes, use a plus (`+`) to separate each line. For example: `AVSOYOSZ+ELEAPOZE+AIEAZPAP`

**Note**: Although OpenEmu knows which core emulators support cheat codes, it does not necessarily track what formats the emulators support, and performs only minimal syntax-checking.

### Using cheats

After you've added a cheat, you'll need to enable it. Return to the *Select Cheat* menu, and you will now see the cheat that was just added in the list. Click on it to enable it. If you need to disable it later (currently only supported for N64), simply return to this menu and click it again.

![HUD Select Cheat menu with cheat added](https://raw.github.com/okdana/OpenEmu-documentation/master/assets/img/user%20guide/HUD%20-%20Select%20Cheat%20-%2099%20lives%20%28no%20game%29.png)

### Limitations

OpenEmu currently has no way of saving cheats — any codes entered will be lost as soon as you leave the game. Improved cheat-code functionality (potentially including a built-in database of codes) is planned for a future version of the application.