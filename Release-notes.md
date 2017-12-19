#### 2.0.6.1 — Dec 19, 2017

[Release notes](http://openemu.org/rnotes/2.0.6.html)

#### 2.0.5 — Mar 22, 2017

[Release notes](http://openemu.org/rnotes/2.0.5.html)

#### 2.0.4 — Nov 18, 2016

[Release notes](http://openemu.org/rnotes/2.0.4.html)

#### 2.0.3 — Aug 12, 2016

[Release notes](http://openemu.org/rnotes/2.0.3.html)

#### 2.0.2 — Jul 1, 2016

[Release notes](http://openemu.org/rnotes/2.0.2.html)

#### 2.0.1 — Dec 24, 2015

[Release notes](http://openemu.org/rnotes/2.0.1.html)

#### 2.0 — Dec 23, 2015

[Release notes](http://openemu.org/rnotes/2.0.html)

#### 1.0.4 — Oct 15, 2014

[Release notes](http://openemu.org/rnotes/1.0.4.html)

#### 1.0.3 — May 31, 2014

[Release notes](http://openemu.org/rnotes/1.0.3.html)

#### 1.0.2 — Mar 4, 2014

[Release notes](http://openemu.org/rnotes/1.0.2.html)

#### 1.0.1 — Jan 3, 2014

**Enhancements**
* Added `.sgb` to supported extensions for Game Boy ROMs. ([`57553571ba`](https://github.com/OpenEmu/OpenEmu/commit/57553571ba6677ca90513c3240e018a97fc36a49))
* Added debug options to take screenshots at native size and without aspect ratio correction. ([`12a8195d0b`](https://github.com/OpenEmu/OpenEmu/commit/12a8195d0b1a21faabca6096ccca566737dd1afb), [`126f396ffc`](https://github.com/OpenEmu/OpenEmu/commit/126f396ffc4824e330eb24a36e590b34630ac39a))
* Implemented detection for PC Engine CD-ROM games. ([`7167a96a04`](https://github.com/OpenEmu/OpenEmu/commit/7167a96a04021773a08ce44fce3e967c2478b344))
* Improved cover art and meta-data look-up behaviour. ([`ad38c71f10`](https://github.com/OpenEmu/OpenEmu/commit/ad38c71f10ddf0bd43e2d16cc8443163dbd40628), [`99d099ff79`](https://github.com/OpenEmu/OpenEmu/commit/99d099ff79d7fe03c92bf03dee5fec612126eb26), [`f896aa7c2a`](https://github.com/OpenEmu/OpenEmu/commit/f896aa7c2aa6c51aa2e9d16a7c64b3086bda7772), [`814856465f`](https://github.com/OpenEmu/OpenEmu/commit/814856465f8951f7b54907785a4c378255cdf97d))
* Improved the behaviour of the search bar. ([`442d434f2f`](https://github.com/OpenEmu/OpenEmu/commit/442d434f2fc35c3260e4f891e1e3fae71f8034c2))
* Added a *Restart System* menu item. ([`cb5e05ed7b`](https://github.com/OpenEmu/OpenEmu/commit/cb5e05ed7bbcb48b11b0f2c1ee0fca1d3964a16b))
* Added a *Help* menu. ([`4a357b8ed6`](https://github.com/OpenEmu/OpenEmu/commit/4a357b8ed62e47cb1f05ac1721743798bddcb22e), [`639203a82a`](https://github.com/OpenEmu/OpenEmu/commit/639203a82a93513f8e7768e1b4b92139ff1c06f1))
* Various other minor enhancements.

**Fixes**
* Corrected an issue which could cause an erroneous path to be returned when resetting the library folder location. ([`af00cbdd3c`](https://github.com/OpenEmu/OpenEmu/commit/af00cbdd3c1d7d4d0a898ab570fd3154e511d32b))
* Corrected an issue with archive handling which could cause problems when importing Mega Drive and arcade ROMs. ([`aae80b9420`](https://github.com/OpenEmu/OpenEmu/commit/aae80b9420141f32439ef1260c930a0b0b2dc6d0))
* Corrected an issue which could prevent the import of folders whose names contain a dot. ([`c713afacee`](https://github.com/OpenEmu/OpenEmu/commit/c713afacee3ddee603c405b89bca8c701e9767d8))
* Corrected an issue which could prevent the editing of control bindings after the Preferences window has been closed. ([`8e1b973cdd`](https://github.com/OpenEmu/OpenEmu/commit/8e1b973cdd460cd4a63d8d0f1b857ea34b594553))
* Corrected an issue which could cause the application to crash upon deleting a game from a Smart Collection. ([`0d84eab052`](https://github.com/OpenEmu/OpenEmu/commit/0d84eab0529b5e37b569e8ca37fa101c8c882e4c))
* Corrected an issue which could cause crashing on OS X 10.7. ([`153fb71998`](https://github.com/OpenEmu/OpenEmu/commit/153fb71998b947d7a43958b0e93e3488fb95c6ab))
* Corrected an issue which prevented the *Quit Emulation* menu item from working in pop-out mode. ([`a7bcdd5e20`](https://github.com/OpenEmu/OpenEmu/commit/a7bcdd5e20c6cf5443b2a7cef6b4f56e9aa6c90c))
* Corrected issues which could cause the application to crash when importing/scanning a large number of games. ([`b6dc687b2f`](https://github.com/OpenEmu/OpenEmu/commit/b6dc687b2f0fc0728972c850d13b9fa5e453d938), [`99d099ff79`](https://github.com/OpenEmu/OpenEmu/commit/99d099ff79d7fe03c92bf03dee5fec612126eb26), [`b088f6e332`](https://github.com/OpenEmu/OpenEmu/commit/b088f6e332528f231f306f3732cd4a21316fab7b))
* Corrected an issue which could prevent access to the *Special Keys* control bindings on OS X 10.7. ([`4e59b67ecd`](https://github.com/OpenEmu/OpenEmu/commit/4e59b67ecd05deedb0e2cbc0ec3faf6d0ee444ea))
* Corrected an issue which could cause loss of the current battery save when quitting the application. ([`2b8462e9aa`](https://github.com/OpenEmu/OpenEmu/commit/2b8462e9aaca0d4b00d7029030a576dcc9b297c8))
* Various other minor fixes.

**Other**
* Removed RetroUSB controller auto-mapping (for now) to prevent conflicts with different controllers which all share the same hardware IDs. ([`738c90b202`](https://github.com/OpenEmu/OpenEmu/commit/738c90b2021595d606ee663c3003b4346fbca67b))

#### 1.0 — 2013-12-23

* Initial public release.