### Required BIOS Files for Cores

| System | Core | BIOS/Firmware Info |
| --- | --- | --- |
| Atari 5200 | Atari800 | `5200.rom`<br>MD5: 281f20ea4320404ec820fb7ec0693b38 |
| Atari Lynx | Mednafen | `lynxboot.img` or `lynxa.bin`<br>MD5: fcd403db69f54290b51035d82f835e7b |
| ColecoVision | CrabEmu | `coleco.rom` or `313 10031-4005 73108a.u2`<br>MD5: 2c66f5911e5b42b8ebe113403548eee7 |
| Famicom Disk System | Nestopia | `disksys.rom` or `rp2c33a-01a.bin`<br>MD5: ca30b50f880eb660a320674ed365ef7a |
| Intellivision | Bliss | Executive ROM<br>`exec.bin`<br>MD5: 62e761035cb657903761800f4437b8af<br><br>Graphics ROM<br>`grom.bin` or `ro-3-9503-003.u21`<br>MD5: 0cd5946c6473e42e8e4c2137785e427f<br><br>Intellivoice ROM<br>`ivoice.bin` or `sp0256-012.bin` (Optional)<br>MD5: d5530f74681ec6e0f282dab42e6b1c5f<br><br>Entertainment Computer System ROM<br>`ecs.bin` (Optional)<br>MD5: 2e72a9a2b897d330a35c8b07a6146c52 |
| Odyssey² / Videopac | O2EM | `o2rom.bin` or `o2bios.rom`<br>MD5: 562d5ebf9e030a40d6fabfc2f33139fd |
| PC-FX | Mednafen | PC-FX BIOS (v1.00 - 2 Sep 1994)<br>`pcfx.rom` or `pcfxbios.bin`<br>MD5: 08e36edbea28a017f79f8d4f7ff9b6d7 |
| PlayStation | Mednafen | SCPH-5500 (v3.0 09/09/96 Japan)<br>`ps-30j.bin` or `scph5500.bin`<br>MD5: 8dd7d5296a650fac7319bce665a6a53c<br><br>SCPH-5501 (v3.0 11/18/96 America)<br>`ps-30a.bin` or `scph5501.bin` or `scph7003.bin`<br>MD5: 490f666e1afb15b7362b406ed1cea246<br><br>SCPH-5502 (v3.0 01/06/97 Europe)<br>`ps-30e.bin` or `scph5502.bin` or `scph5552.bin`<br>MD5: 32736f17079d0b2b7024407c39bd3050 |
| Sega CD / Mega-CD | Genesis Plus GX | Model 1 (v1.00 921027 Europe)<br>`BIOS_CD_E.bin` or `megacd_model1_bios_1_00_e.bin`<br>MD5: e66fa1dc5820d254611fdcdba0662372<br><br>Model 1 (v1.00p 911217 Japan)<br>`BIOS_CD_J.bin` or `epr-14088e.bin`<br>MD5: 278a9397d192149e84e820ac621a8edd<br><br>Model 1 (v1.10 921011 USA)<br>`BIOS_CD_U.bin` or `mpr-15045b.bin`<br>MD5: 2efd74e3232ff260e371b99f84024f7f |
| Sega Saturn | Mednafen | Sega Saturn BIOS (v1.01 941228 Japan)<br>`sega_101.bin`<br>MD5: 85ec9ca47d8f6807718151cbcca8b964<br><br>Sega Saturn BIOS (v1.01a 941115 NA/EU)<br>`mpr-17933.bin`<br>MD5: 3240872c70984b6cbfda1586cab68dbe |
| SNES | Higan | [Multiple](https://github.com/OpenEmu/OpenEmu/wiki/User-guide:-BIOS-files#snes-chip-dumps-for-higan) |
| SNES Satellaview | Snes9x* | `BS-X.bin` (Optional)<br>MD5: fed4d8242cfbed61343d53d48432aced |
| TurboGrafx-CD / PC Engine CD | Mednafen | Super CD-ROM System (v3.0 Japan)<br>`syscard3.pce` or `[BIOS] Super CD-ROM System (Japan) (v3.0).pce`<br>MD5: 38179df8f4ac870017db21ebcbf53114<br><br>Note: The Japan BIOS is required because the US version won't play some Japan region games (e.g. Mirai Shounen Conan, Sylphia).<br><br>**Important:** Dumps of `syscard3.pce` containing a 512-byte copier header are considered "bad" and will not import. If you have the version with the MD5 hash `ff1a674273fe3540ccef576376407d1d`, run the following command in Terminal to convert it to the "good" version:<br><br>`dd bs=512 skip=1 if=syscard3.pce of=syscard3fix.pce` |

\* **Note: As an exception, only BSX-BIOS must be copied directly to your BIOS folder.**