**Important: Do not manually copy a file to your BIOS folder. If files aren't automatically copying, that means you have incorrect files. Please follow the guide below.**

In order to emulate some systems, BIOS files are needed due to increasing complexity of the hardware and software of modern gaming consoles.  If the core you are currently trying to use needs a BIOS file, OpenEmu will alert you with a popup message.  Before installing a BIOS, make sure that its filename and md5 hash are correct, or it will not work!  Installing a BIOS is as simple as adding a game to OpenEmu, just drag-and-drop a BIOS onto your library!

You can check the hash of your file by opening Terminal.app, typing <code>md5 /path/to/file</code> and pressing Enter.  Instead of typing the file path in manually, you can just drag the file onto the Terminal window.

### Required BIOS Files for Cores

<table>
<tr>
<th>Console</th>
<th>Core</th>
<th>BIOS Filename</th>
<th>md5 Hash</th>
</tr> 

<tr>
<td>3DO</td>
<td>4DO</td>
<td><code>panafz10.bin</code></td>
<td>
<code>51f2f43ae2f3508a14d9f56597e2d3ce</code>
</td>
</tr>

<tr>
<td>Atari 5200</td>
<td>Atari800</td>
<td><code>5200.rom</code></td>
<td>
<code>281f20ea4320404ec820fb7ec0693b38</code>
</td>
</tr>

<tr>
<td>Atari Lynx</td>
<td>Mednafen</td>
<td><code>lynxboot.img</code></td>
<td>
<code>fcd403db69f54290b51035d82f835e7b</code>
</td>
</tr>

<tr>
<td>ColecoVision</td>
<td>CrabEmu</td>
<td><code>coleco.rom</code></td>
<td><code>2c66f5911e5b42b8ebe113403548eee7</code></td>
</tr>

<tr>
<td>Famicom Disk System</td>
<td>Nestopia</td>
<td><code>disksys.rom</code></td>
<td>
<code>ca30b50f880eb660a320674ed365ef7a</code>
</td>
</tr>

<tr>
<td>Game Boy Advance</td>
<td>Higan*</td>
<td><code>bios.rom</code></td>
<td><code>a860e8c0b6d573d191e4ec7db1b1e4f6</code></td>
</tr>

<tr>
<td>PC-FX</td>
<td> Mednafen </td>
<td><code>pcfx.rom</code></td>
<td><code>08e36edbea28a017f79f8d4f7ff9b6d7</code></td>
</tr>

<tr>
<td>Playstation (JP)</td>
<td>Mednafen</td>
<td><code>scph5500.bin</code></td>
<td><code>8dd7d5296a650fac7319bce665a6a53c</code></td>
</tr>

<tr>
<td>Playstation (NA)</td>
<td>Mednafen</td>
<td><code>scph5501.bin</code></td>
<td><code>490f666e1afb15b7362b406ed1cea246</code></td>
</tr>

<tr>
<td>Playstation (EU)</td>
<td>Mednafen</td>
<td><code>scph5502.bin</code></td>
<td><code>32736f17079d0b2b7024407c39bd3050</code></td>
</tr>


<tr>
<td>Sega CD (EU)</td>
<td>GenesisPlus</td>
<td><code>BIOS_CD_E.bin</code></td>
<td><code>e66fa1dc5820d254611fdcdba0662372</code></td>
</tr>

<tr>
<td>Sega CD (JP)</td>
<td>GenesisPlus</td>
<td><code>BIOS_CD_J.bin</code></td>
<td><code>278a9397d192149e84e820ac621a8edd</code></td>
</tr>


<tr>
<td>Sega CD (NA)</td>
<td>GenesisPlus</td>
<td><code>BIOS_CD_U.bin</code></td>
<td><code>2efd74e3232ff260e371b99f84024f7f</code></td>
</tr>


<tr>
<td>SNES</td>
<td>Higan</td>
<td><a href="https://github.com/OpenEmu/OpenEmu/wiki/User-guide:-BIOS-files#snes-chip-dumps-for-higan">Multiple</a></td>
<td><a href="https://github.com/OpenEmu/OpenEmu/wiki/User-guide:-BIOS-files#snes-chip-dumps-for-higan">Multiple</a></td>
</tr>



<tr>
<td>TurboGrafx-CD / PC Engine-CD</td>
<td>Mednafen</td>
<td><code>syscard3.pce</code></td>
<td><code>ff1a674273fe3540ccef576376407d1d</code></td>
</tr>


</table>

\* **Note: The default GBA core, VisualBoy Advance, does not require a BIOS**

-----

### SNES Chip Dumps for Higan
Many SNES games came with additional coprocessor chips on their cartridge, so the dependencies are per-game. A full list of games that require them can be [found here] (http://en.wikipedia.org/wiki/List_of_Super_NES_enhancement_chips#List_of_Super_NES_games_that_use_enhancement_chips).


<table>
<tr>
<th>Filename</th>
<th>md5 Hash</th>
</tr> 

<tr>
<td><code>cx4.rom</code></td>
<td><code>037ac4296b6b6a5c47c440188d3c72e3</code></td>
</tr>

<tr>
<td><code>dsp1.rom</code></td>
<td><code>428fdb968d54353d9c9eced1b0586671</code></td>
</tr>

<tr>
<td><code>dsp1b.rom</code></td>
<td><code>332273cc0df5775d3803f2fd88e95d18</code></td>
</tr>

<tr>
<td><code>dsp2.rom</code></td>
<td><code>9ebbdcec67c0c01d5a0593d3cf167c9e</code></td>
</tr>

<tr>
<td><code>dsp3.rom</code></td>
<td><code>484908d68405d44e2be757b4e1e75d15</code></td>
</tr>

<tr>
<td><code>dsp4.rom</code></td>
<td><code>f229fda2d7b33c5a218cba28147ab9b8</code></td>
</tr>

<tr>
<td><code>st010.rom</code></td>
<td><code>636093910fbaff60c8b327be00aefbd9</code></td>
</tr>

<tr>
<td><code>st011.rom</code></td>
<td><code>5c209ce0283632b6574ad835bf862bee</code></td>
</tr>

<tr>
<td><code>st018.rom</code></td>
<td><code>dafae0e0c71c924075811c595c61a30e</code></td>
</tr>

</table>