#NEW UI BUILD (25TH JAN 2012)

##GENERAL / MAIN UI

6 -	We should start adding tooltips to a lot of buttons and other pieces. Particularly for unique custom stuff OE does like the gameplay hud bar.

8 -	We will need to determine wether we can introduce the creation of additional user created smart collections. This is the final 	component that is missing from my mockups. We will need to provide the ability to create and edit a smart collection in a similar 	manner to iTunes smart playlist creation (example of smart playlist creation in iTunes, in the image below. I would say we don't have to do 
	this for 1.0, but we should consider it, if time allows..
	
###BLANK SLATE

13 -	I don't see this as an issue yet, so this is more of a need to know, but the gap between the left hand text and the icon and
	'Core Provided By..' text as indicated by the red lines in the image below.. can we make sure this gap is no less than 20-25px..

###LIST VIEW

21 -	We should also define as a group what columns we need to have. My mockups have columns for: Name (game Name), Rating, No. of Save Games and Play Count.
	The live version has additional columns for: 'System' and 'Last Played' date. (I'd like to format that field better e.g. 20th Feb 2012 if possible).

22 -	Slight UX issue with the rating stars. This was also mentioned in a previous review but seems to have returned?
	As a user, in list view I can click and highlight any game in the list by clicking it. However, if I click to highlight a game via the Rating column, it not only highlights the
	game, but also changes the rating at the same time. What we need to do, is make sure, that it takes two clicks before I can change the Rating in this instance.. 1. click to highlight 	a game in the rating column.. 2. Click again to select the number of stars I want to rate it. Right now those two happen in one click!.

23 -	The column divider line that crosses over the blue highlight is too bright (see image below.. red arrow points at this divider). If possible, can we set this colour to #2263bf..
	
24 -	Similarly, for the unfocused or grey highlight column divider line, can we set this colour to: #747474..
	
###COVERFLOW VIEW

25 -	Obviously, all the issues related to list view described previously, also apply to Coverflow.

26 -	There is a weird issue where the list view seems to keep collapsing down the bottom and I need to drag it back up into place to see the list.
	Even after dragging it back into a sensible position, if I change the view option (i.e to grid view), and then come back to coverflow view.. it collapses again..
	
27 -	The image below left is our default cover artwork in coverflow currently. Is it at all possible to use the default artwork as used in grid view for this (rough mockup image to the right)..

29 -	This is more of a question, but, is it possible to add a custom scrollbar to this coverflow view? I know we are using either a hacked coverflow using Apples hidden API's or
	some open source stuff to do this? ..but, a scrollbar would be consistent with how Apple does this in Tunes (and make scrolling through covers useful / easier).

###GRID VIEW

35 -	I would like to start setting ratios for some of the default box art per-system or console. Let me explain: Looking at NES games as the starting point..
	NES games are traditionally rectangular, in a portrait view. So, currently, the way we display this in the live build of OE is correct..

However, looking at SNES games, the box art is traditionally in a landscape format. So, using SNES as an example, I would like to use the correct aspect ratio for these boxes.
As you can see, it looks very odd when you have some artwork in place, and the default artwork next to it.. it almost doesn't feel like they belong together or are from the same
console /platform..

The two examples above use NES and SNES games to illustrate the point, but, I would like to go through and define, and set the aspect ratio to be used for all consoles we
emulate. Some of this I have done already, you can look through the mockups (or better yet go to DropBox > Assets > Game Tiles: check the file names) and see what other systems like Megadrive etc and their box art ratio's should look like. 
However, it gets a little complicated when it comes to other countries / regions. In the West, we had the SNES, and our box art was in a rectangular landscape format. However, in
Japan as an example, they used a very tall and thin rectangular portrait box for their games. (see Mario World in the image above?)
So, I would like us to set these box art ratios for default artwork in OE and also cater for different ratios per system and per region / country. (**This should also apply to CoverFlow!**)

##GAMEPLAY

###General Issues

36 -	In / For the Gameplay HUD bar, we will need to add tooltips for the various glyphs / icons and buttons that appear in the Hud..

37 -	I'm not sure what has happened, but the red quit game button looks a little desaturated on my screen see image above). I'll need to maybe play with the graphical resource myself
	and see if I can't get it looking a little more 'vibrant' but, it would be good to check with you guys to see if anything weird isn't happening in the code with it.

38 -	I think this one might have been a design mistake by me. The popover that appears when clicking the save game glyph (as the image below shows) or even the
	additional settings under the cog icon are sometimes not that legible, or just not that obvious (black on black). The save game one, when the user has no saves and
	the basic popover appears with the single entry 'Save Current Game' it just looks wrong. The basic solution I have for this at the moment is to use a white popover instead
	so it contrasts with the black behind it.. or slightly modify it so it is a little more iPad style. Or, we might have some more default options in here like 'Load Save Game From File..'
	and 'Import Saved Game From File..' which would make this popover taller and a little less weird looking like the image below (any thoughts guys?)..

39 -	Related to the Save games, when there are a LOT of save games, this needs to be scrollable. I remember showing Chris (cyco) and example of how this would work by
	demonstrating a movie in Quicktime that had chapters I think.

###Popout Gameplay Window

44 -	We also don't need to add a fullscreen button on the top right of this window (as the image below depicts), this button is available in the gameplay hud bar..

##PREFERENCES

###General Comments / Tweaks

###Library Section

###Gameplay Section

51 -	The Filter effects graphic is not in place yet, I'll need some help in producing a graphic image for each one so it changes based on the one selected in the popover.
	For now, I see there is a default image file for each filter effect in the graphic resources of the app. 


