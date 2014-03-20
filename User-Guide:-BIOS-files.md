In order to emulate some systems, BIOS files are needed due to increasing complexity of the hardware and software of modern gaming consoles.  If the core you are currently trying to use needs a BIOS file, OpenEmu will alert you with a popup message.  Before installing a BIOS, make sure that its filename and hash are correct, or it will not work!  Installing a BIOS is as simple as adding a game to OpenEmu, just drag-and-drop a BIOS onto your library!

### Required BIOS Files for Cores

<table>
<tr>
<th>Console</th>
<th>Core</th>
<th>BIOS Filename</th>
<th>md5 Hash</th>
</tr> 


<tr>
<td>Atari 5200</td>
<td>Atari800</td>
<td>5200.rom</td>
<td>
<pre><code>281f20ea4320404ec820fb7ec0693b38</pre></code>
</td>
</tr>

<tr>
<td>Atari Lynx</td>
<td>Mednafen</td>
<td>lynxboot.img</td>
<td>
<pre><code>fcd403db69f54290b51035d82f835e7b</pre></code>
</td>
</tr>

<tr>
<td>ColecoVision</td>
<td>CrabEmu</td>
<td>coleco.rom</td>
<td><pre><code>2c66f5911e5b42b8ebe113403548eee7</pre></code></td>
</tr>

<tr>
<td>Famicom Disk System</td>
<td>Nestopia</td>
<td>disksys.rom</td>
<td>
<pre><code>ca30b50f880eb660a320674ed365ef7a</pre></code>
</td>
</tr>

<tr>
<td>Game Boy Advance</td>
<td>Higan*</td>
<td>bios.rom</td>
<td><pre><code>a860e8c0b6d573d191e4ec7db1b1e4f6</pre></code></td>
</tr>

<tr>
<td>Playstation</td>
<td>Mednafen</td>
<td>scph5500.bin</td>
<td><pre><code>8dd7d5296a650fac7319bce665a6a53c</pre></code></td>
</tr>

<tr>
<td>Playstation</td>
<td>Mednafen</td>
<td>scph5501.bin</td>
<td><pre><code>490f666e1afb15b7362b406ed1cea246</pre></code></td>
</tr>

<tr>
<td>Playstation</td>
<td>Mednafen</td>
<td>scph5502.bin</td>
<td><pre><code>e56ec1b027e2fe8a49217d9678f7f6bb</pre></code></td>
</tr>


<tr>
<td>Sega CD</td>
<td>GenesisPlus</td>
<td>BIOS_CD_E.bin</td>
<td><pre><code>d8b8b720dea6c6ba25c309ed633930f4</pre></code></td>
</tr>

<tr>
<td>Sega CD</td>
<td>GenesisPlus</td>
<td>BIOS_CD_J.bin</td>
<td><pre><code>278a9397d192149e84e820ac621a8edd</pre></code></td>
</tr>


<tr>
<td>Sega CD</td>
<td>GenesisPlus</td>
<td>BIOS_CD_U.bin</td>
<td><pre><code>2efd74e3232ff260e371b99f84024f7f</pre></code></td>
</tr>


<tr>
<td>SNES</td>
<td>Higan</td>
<td>Multiple**</td>
<td>Multiple</td>
</tr>



<tr>
<td>TurboGrafx-CD / PC Engine-CD</td>
<td>Mednafen</td>
<td>syscard3.pce</td>
<td><pre><code>ff1a674273fe3540ccef576376407d1d</pre></code></td>
</tr>


</table>

\* (Note: The default GBA core, VisualBoy Advance, does not require a BIOS)

\** (Many SNES games came with additional chips on their cartridge, so the dependencies are per-game)

