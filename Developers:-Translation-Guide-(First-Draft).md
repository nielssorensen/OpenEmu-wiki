If you have any questions or suggestions regarding the translation process. Join #OpenEmu on irc.freenode.net (http://webchat.freenode.net/?channels=openemu) and let us know.

###Preparation
* Make sure no one is working on the language you want to translate ([Here](#translation-progress))
* get OpenEmu source code (https://github.com/OpenEmu/OpenEmu/wiki/Compiling-From-Source-Guide)
* download helper app https://www.dropbox.com/s/4shjhllw2t57gha/OELocalizer.zip (Source: https://github.com/cyco/OELocalizer). This is used translate strings that appear in code and to sync up changes in language files and source code.

###Setup

* Open OELocalizer, and point it to the OpenEmu source files
![PickSource](http://i.imgur.com/k9te9u0.png)	

* Pick language, click on load, then click on save

Window should look like this now
![Imgur](http://i.imgur.com/kW9IAaN.png)
	
* This created a new directory that contains all the files that need to be translated.
![Imgur](http://i.imgur.com/fsl5XgG.png)
![Imgur](http://i.imgur.com/TtvXFx0.png)

###Translation

As you can see above there are several different file types that need different treatments:

* _Localizeable.strings_, can be edited directly with OELocalizer.app. Make sure to load your language when you start OELocalizer and save before you quit. You can use OELocalizer to start OpenEmu with the selected language (shortcut cmd + r). If you want to review your changes make sure to save and then use the rebuild and run menu action (shortcut cmd + shift +r) 
![Imgur](http://i.imgur.com/vNZ9czd.png)

* _ControlLabels.strings_, must be edited manually (use a text editor like TextEdit.app). Labels that are actually visible on the controller should not be translated (like Start and Select buttons on SNES/Super Famicom).

* _Credits.rtf_ should also be edited using TextEdit. No need to translate licenses.

* _.xib files_, these files must be translated using Xcode (make sure you have at least version 5.something). You should not move or delete elements, if you need more space to fit in a sentence or word we can adjust the layout later.

###Merging Changes

When you're done with the translation you can either create a pull request (preferred way) or zip your .lproj directory and send it in by mail so we can add your changes to the main OpenEmu repository.

###Translation Progress

Language   | ID | Status                
-----------|----|---------------------- 
English    | en | Development Language  
Portuguese | pt | WIP                   
Russian    | ru | In Progress?          
Spanish    | es | WIP                   
| |
| |
Afrikaans   | af | 
Albanian    | sq | 
Amharic     | am | 
Arabic      | ar | 
Armenian    | hy | 
Assamese    | as | 
Aymara      | ay | 
Azerbaijani | az | 
Basque      | eu | 
Bengali     | bn | 
Breton      | br | 
Bulgarian   | bg | 
Burmese     | my | 
Byelorussian | be | 
Catalan   | ca | 
Chinese   | zh | 
Croatian | hr | 
Czech | cs | 
Danish | da | 
Dutch | nl | 
Dzongkha | dz | 
Esperanto | eo | 
Estonian | et | 
Faroese | fo | 
Farsi | fa | 
Finnish | fi | 
French | fr | 
Galician | gl | 
Georgian | ka | 
German | de | 
Greek | el | 
Greenlandic | kl | 
Guarani | gn | 
Gujarati | gu | 
Hebrew | he | 
Hindi | hi | 
Hungarian | hu | 
Icelandic | is | 
Indonesian | id | 
Inuktitut | iu | 
Irish | ga | 
Italian | it | 
Japanese | ja | 
Javanese | jv | 
Kannada | kn | 
Kashmiri | ks | 
Kazakh | kk | 
Khmer | km | 
Kinyarwanda | rw | 
Kirghiz | ky | 
Korean | ko | 
Kurdish | ku | 
Lao | lo | 
Latin | la | 
Latvian | lv | 
Lithuanian | lt | 
Macedonian | mk | 
Malagasy | mg | 
Malay | ms | 
Malayalam | ml | 
Maltese | mt | 
Manx | gv | 
Marathi | mr | 
Moldavian | mo | 
Mongolian | mn | 
Nepali | ne | 
Norwegian | nb | 
Nynorsk | nn | 
Oriya | or | 
Oromo | om | 
Pashto | ps | 
Polish | pl | 
Punjabi | pa | 
Quechua | qu | 
Romanian | ro | 
Rundi | rn | 
Sami | se | 
Sanskrit | sa | 
Scottish | gd | 
Serbian | sr | 
Sindhi | sd | 
Sinhalese | si | 
Slovak | sk | 
Slovenian | sl | 
Somali | so | 
Sundanese | su | 
Swahili | sw | 
Swedish | sv | 
Tagalog | tl | 
Tajiki | tg | 
Tamil | ta | 
Tatar | tt | 
Telugu | te | 
Thai | th | 
Tibetan | bo | 
Tigrinya | ti | 
Tongan | to | 
Turkish | tr | 
Turkmen | tk | 
Uighur | ug | 
Ukrainian | uk | 
Urdu | ur | 
Uzbek | uz | 
Vietnamese | vi | 
Welsh | cy | 
Yiddish | yi | 