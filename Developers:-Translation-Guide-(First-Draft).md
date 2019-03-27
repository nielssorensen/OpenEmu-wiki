If you have any questions or suggestions regarding the translation process. Join #OpenEmu on irc.freenode.net (http://webchat.freenode.net/?channels=openemu) and let us know.

### Preparation
* Make sure no one is working on the language you want to translate ([Here](#translation-progress))
* get OpenEmu source code (https://github.com/OpenEmu/OpenEmu/wiki/Compiling-From-Source-Guide)

### Setup

* Open OpenEmu.xcworkspace with Xcode, then select the OpenEmu project on the left. Under 'Localizations' hit the plus button and add your language. Keep the defaults in the dialog that comes up and click Finish.

![Imgur](http://i.imgur.com/Tx5Fvu9.png?1)
![Imgur](http://i.imgur.com/2142ODt.png) 


...

### Debug
You can use the `plutil` command to check the syntax of your `.strings` files:
```
plutil OpenEmu/ca.lproj/*.strings
```

Expected output:
```
OpenEmu/ca.lproj/ControlLabels.strings: OK
OpenEmu/ca.lproj/InfoPlist.strings: OK
OpenEmu/ca.lproj/Localizable.strings: OK
...
```

### Merging Changes

When you're done with the translation you can either create a pull request (preferred way) or zip your .lproj directory and send it in by mail so we can add your changes to the main OpenEmu repository.

### Translation Progress

Language   | ID | Status                | Credits
-----------|----|-----------------------|------------- 
English    | en | Development Language  | 
German     | de | Done                  | @J-rg
Portuguese | pt | WIP                   | @ivanhtp
Russian    | ru | Abandoned             | @phoenixweiss
Spanish    | es | Done                   | Juan Pablo Atienza Martinez
French     | fr | Done / Review         | @cyril634
Italian    | it | Done                  | @shysaur
Dutch      | nl | Done / Review         | [Dylan Meysmans (@mettekou)](https://github.com/mettekou)
Catalan    | ca | Done                  | [Pere Orga (@pereorga)](https://github.com/pereorga)
Japanese | ja | Done?       | [Kota Ura (@kotaura)](https://github.com/kotaura)
Chinese (Simplified)   | zh-Hans | Done      | [King Chung (@unbored)](https://github.com/unbored)
Chinese (Traditional)   | zh-Hant | Done       | [Tzeng Yuxio (@tzengyuxio)](https://github.com/tzengyuxio)
| | |
| | |
Afrikaans   | af |     |
Albanian    | sq |     |
Amharic     | am |     |
Arabic      | ar |     |
Armenian    | hy |     |
Assamese    | as |     |
Aymara      | ay |     |
Azerbaijani | az |     |
Basque      | eu |     |
Bengali     | bn |     |
Breton      | br |     |
Bulgarian   | bg |     |
Burmese     | my |     |
Byelorussian | be |    |
Croatian | hr |        |
Czech | cs |           |
Danish | da |          |
Dzongkha | dz |        |
Esperanto | eo |       |
Estonian | et |        |
Faroese | fo |         |
Farsi | fa |           |
Finnish | fi |         |
Galician | gl |        |
Georgian | ka |        |
Greek | el |           |
Greenlandic | kl |     |
Guarani | gn |         |
Gujarati | gu |        |
Hebrew | he |          |
Hindi | hi |           |
Hungarian | hu |       |
Icelandic | is |       |
Indonesian | id |      |
Inuktitut | iu |       |
Irish | ga |           |
Javanese | jv |        |
Kannada | kn |         |
Kashmiri | ks |        |
Kazakh | kk |          |
Khmer | km |           |
Kinyarwanda | rw |     |
Kirghiz | ky |         |
Korean | ko |          |
Kurdish | ku |         |
Lao | lo |             |
Latin | la |           |
Latvian | lv |         |
Lithuanian | lt |      |
Macedonian | mk |      |
Malagasy | mg |        |
Malay | ms |           |
Malayalam | ml |       |
Maltese | mt |         |
Manx | gv |            |
Marathi | mr |         |
Moldavian | mo |       |
Mongolian | mn |       |
Nepali | ne |          |
Norwegian | nb |       |
Nynorsk | nn |         |
Oriya | or |           |
Oromo | om |           |
Pashto | ps |          |
Polish | pl |          |
Punjabi | pa |         |
Quechua | qu |         |
Romanian | ro |        |
Rundi | rn |           |
Sami | se |            |
Sanskrit | sa |        |
Scottish | gd |        |
Serbian | sr |         |
Sindhi | sd |          |
Sinhalese | si |       |
Slovak | sk |          |
Slovenian | sl |       |
Somali | so |          |
Sundanese | su |       |
Swahili | sw |         |
Swedish | sv |         |
Tagalog | tl |         |
Tajiki | tg |          |
Tamil | ta |           |
Tatar | tt |           |
Telugu | te |          |
Thai | th |            |
Tibetan | bo |         |
Tigrinya | ti |        |
Tongan | to |          |
Turkish | tr |         |
Turkmen | tk |         |
Uighur | ug |          |
Ukrainian | uk |       |
Urdu | ur |            |
Uzbek | uz |           |
Vietnamese | vi |      |
Welsh | cy |           |
Yiddish | yi |         |