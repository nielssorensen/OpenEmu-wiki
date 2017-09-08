**Important: Do not manually copy a file to your BIOS folder. If files aren't automatically copying, that means you have incorrect files. Please follow the guide below.**

In order to emulate some systems, BIOS files are needed due to increasing complexity of the hardware and software of modern gaming consoles.  If the core you are currently trying to use needs a BIOS file, OpenEmu will alert you with a popup message.  Before installing a BIOS file, make sure that its associated core plugin is installed and the filename and MD5 hash are correct, or it will not work!  Installing a BIOS is as simple as adding a game to OpenEmu, just drag-and-drop a BIOS onto your library!

You can check the hash of your file by opening Terminal.app, typing <code>md5 /path/to/file</code> and pressing Enter.  Instead of typing the file path in manually, you can just drag the file onto the Terminal window.

### Required BIOS Files for Cores

| System | Core | BIOS Filename | MD5 Hash |
| --- | --- | --- | --- |
| 3DO | 4DO | `panafz10.bin` | `51f2f43ae2f3508a14d9f56597e2d3ce` |
| Atari 5200 | Atari800 | `5200.rom` | `281f20ea4320404ec820fb7ec0693b38` |
| Atari Lynx | Mednafen | `lynxboot.img` or `lynxa.bin` | `fcd403db69f54290b51035d82f835e7b` |
| ColecoVision | CrabEmu | `coleco.rom` or <br>`313 10031-4005 73108a.u2` | `2c66f5911e5b42b8ebe113403548eee7` |
| Famicom Disk System | Nestopia | `disksys.rom` or `rp2c33a-01a.bin` | `ca30b50f880eb660a320674ed365ef7a` |
| Intellivision | Bliss | `exec.bin` | `62e761035cb657903761800f4437b8af` |
| Intellivision | Bliss | `grom.bin` or `ro-3-9503-003.u21` | `0cd5946c6473e42e8e4c2137785e427f` |
| Intellivision | Bliss | `ivoice.bin` or `sp0256-012.bin` (Optional) | `d5530f74681ec6e0f282dab42e6b1c5f` |
| Intellivision | Bliss | `ecs.bin` (Optional) | `2e72a9a2b897d330a35c8b07a6146c52` |
| Odyssey² / Videopac | O2EM | `o2rom.bin` or `o2bios.rom` | `562d5ebf9e030a40d6fabfc2f33139fd` |
| PC-FX (v1.00 - 2 Sep 1994) | Mednafen | `pcfx.rom` or `pcfxbios.bin` | `08e36edbea28a017f79f8d4f7ff9b6d7` |
| PlayStation (v3.0 09/09/96 J) | Mednafen | `ps-30j.bin` or `scph5500.bin` | `8dd7d5296a650fac7319bce665a6a53c` |
| PlayStation (v3.0 11/18/96 A) | Mednafen | `ps-30a.bin` or `scph5501.bin` or `scph7003.bin` | `490f666e1afb15b7362b406ed1cea246` |
| PlayStation (v3.0 01/06/97 E) | Mednafen | `ps-30e.bin` or `scph5502.bin` or `scph5552.bin` | `32736f17079d0b2b7024407c39bd3050` |
| Mega-CD (Model 1 1.00 Europe) | Genesis Plus GX | `BIOS_CD_E.bin` or `megacd_model1_bios_1_00_e.bin` | `e66fa1dc5820d254611fdcdba0662372` |
| Mega-CD (Model 1 1.00p Japan) | Genesis Plus GX | `BIOS_CD_J.bin` or `epr-14088e.bin` | `278a9397d192149e84e820ac621a8edd` |
| Sega CD  (Model 1 1.10 USA) | Genesis Plus GX | `BIOS_CD_U.bin` or `mpr-15045b.bin` | `2efd74e3232ff260e371b99f84024f7f` |
| SNES | Higan | [Multiple](https://github.com/OpenEmu/OpenEmu/wiki/User-guide:-BIOS-files#snes-chip-dumps-for-higan) | [Multiple](https://github.com/OpenEmu/OpenEmu/wiki/User-guide:-BIOS-files#snes-chip-dumps-for-higan) |
| SNES Satellaview | SNES9x* | `BS-X.bin` (Optional) | `fed4d8242cfbed61343d53d48432aced` |
| TurboGrafx-CD / PC Engine-CD | Mednafen | `syscard3.pce` | `ff1a674273fe3540ccef576376407d1d` |

\* **Note: As an exception, only BSX-BIOS must be copied directly to your BIOS folder.**

-----

### SNES Chip Dumps for Higan
Many SNES games came with additional coprocessor chips on their cartridge, so the dependencies are per-game. A full list of games that require them can be [found here](http://en.wikipedia.org/wiki/List_of_Super_NES_enhancement_chips#List_of_Super_NES_games_that_use_enhancement_chips).


| Filename | MD5 Hash |
| --- | --- |
| `cx4.rom` | `037ac4296b6b6a5c47c440188d3c72e3` |
| `dsp1.rom` | `428fdb968d54353d9c9eced1b0586671` |
| `dsp1b.rom` | `332273cc0df5775d3803f2fd88e95d18` |
| `dsp2.rom` | `9ebbdcec67c0c01d5a0593d3cf167c9e` |
| `dsp3.rom` | `484908d68405d44e2be757b4e1e75d15` |
| `dsp4.rom` | `f229fda2d7b33c5a218cba28147ab9b8` |
| `st010.rom` | `636093910fbaff60c8b327be00aefbd9` |
| `st011.rom` | `5c209ce0283632b6574ad835bf862bee` |
| `st018.rom` | `dafae0e0c71c924075811c595c61a30e` |
