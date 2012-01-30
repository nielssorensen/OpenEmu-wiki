#NEW UI BUILD (25TH JAN 2012)

##GENERAL / MAIN UI

1 -	Noticed a weird display area with the bottom left and right corners of the UI. I don't know if there is some weird anti-aliasing
	problem but it seems to have a few errant white pixels in the corners. This started appearing in more recent builds (after the 	summer roughly), as it looked fine before. I know that this dark grey/black bar and its gradient are done in the code so, there 	might be something going on with how OSX is displaying it in later Lion builds? Screenshot below is a blow-up of the bottom 
	left corner showing you the white pixels (see also corresponding right corner)..

2 -	Search bar default and input text: double check the shadow text direction on all states. The shadow text should be at a 90 	degree angle. Shown below is the live version on the left, and the original psd mockup on the right..

3 -	<strike>he grid view slider glyph on the right hand side (large one) looks blurry and is displaying incorrectly. I remember, that I made
	a mistake with this graphical element in a previous build. I double checked the latest graphical resources for the two squares used
	as part of the grid view slider (elements: 'grid_slider_small.png' ..and.. 'grid_slider_large.png') and they are correct on 	DropBox. So, just need to double check what is going on in the code etc to see what the issue is. Are we are using the correct files? 
	(using the small one when it should be large? maybe)..	</strike>

4 -	The drop down triangle next to headings / sections in the sidebar (Consoles & Collections shown below), needs a 1px, -90 degree, drop shadow to match that of the text 
	heading next to it. Shown below is the drop down triangle in question, see how it doesn't have a 1px shadow like the text to the right?..

5 -	This is more of a request than a visual issue, but, when the app launches on first run, can we make sure that the Collections section is expanded. 
	Also can OE remember the users choice here / window state when quiting the app as well? Don't forget we will need to add some more default smart collections to that list 
	at some point. For example..  'Recently Added', 'Top 25 Most Played' etc. etc.

6 -	We should start adding tooltips to a lot of buttons and other pieces. Particularly for unique custom stuff OE does like the gameplay hud bar.

7 -	We need to add in a feature at some point where you can cntrl+click on game, be it grid, list or the list portion of overflow and get additional options.
	(see this in Dropbox > Notes > Adding Artwork and the workflow image shows the options here and highlights adding artwork via this popover), the image
	below shows some of the suggested options we can do for this, but these are only a suggestion and we should determine as a group what options we
	make available here at some point before release..

8 -	We will need to determine wether we can introduce the creation of additional user created smart collections. This is the final 	component that is missing from my mockups. We will need to provide the ability to create and edit a smart collection in a similar 	manner to iTunes smart playlist creation (example of smart playlist creation in iTunes, in the image below. I would say we don't have to do 
	this for 1.0, but we should consider it, if time allows..

9 -	<strike>In the sidebar, in the Preferences > Controls, the blank slate and even through box art sizes in Grid View and CoverFlow.. I want OpenEmu to use names, icons and
	box art that users recognise and are used in their country / region. For example, I have produced a 16px sidebar icon for the NES console as it appears for Western countries..
	Of course, for the Asian region, the NES was called Famicom and the hardware looked a lot different, so, here we would use a relevant icon and name for our asian users..
	The NES example used in the sidebar, also applies to the Preference > Controls section, where we again use an icon and label to define these systems..
	I have also produced country specific controller illustrations. These can be quite subtle in terms of the SNES controllers.. the button colours were different in the USA 
	than those in Europe, but even the Asian SNES controller looks exactly the same as European one.. but the Nintendo logo is different (it says Super Famicom
	instead of Super Nintendo.. all these SNESS controller variants have artwork ready for OE).
	So, what I am saying is, we need to keep this in mind, and put in place some of this if it isn't already there ready? I can maybe define this in a separate document at some point
	what icons, labels and controllers we need to use per region country. Box art related region issues I cover a little later under GRID VIEW in this document.</strike>
	
###BLANK SLATE

10 -	Make sure the heading (i.e. NeoGeo Pocket) and the text below are aligned as indicated by the red line. This applies to ALL blank slates not just NeoGeo of course. 
	This text is basically visually left-aligned with the dashed line box above..

11 -	Make sure this body-text (see red arrow) has an RGB text colour of #dbdbdb (just double checking this)..

12 -	This is my fault, I neglected to demonstrate some interaction on the 'Core Provided By..' links. The text itself needs inactive, hover and press states to compliment the glyph.
	The interaction is in place for the little glyph circled arrow at the right of each project link , but we need to put in place the text style to match (thistext would be 'Nestopia'
	in the proceeding examples below)..

Inactive (this is already in place essentially?).
RGB text color: #dbdbdb
text shadow: 90 degrees, #000000

Rollover
RGB text color: #ffffff
text shadow: 90 degrees, #000000

Press
RGB text color: #ffffff
text shadow: 90 degrees, #000000
outer glow (as defined by photoshop, but try to visually match the style in code): colour #ffffff, 40% opacity, spread of 5px.

13 -	I don't see this as an issue yet, so this is more of a need to know, but the gap between the left hand text and the icon and
	'Core Provided By..' text as indicated by the red lines in the image below.. can we make sure this gap is no less than 20-25px..

14 -	We need a little more space between the project link and the circle arrow glyph. (space in the diagram below as demonstrated by the red lines). An 8px gap should do it..

15 -	The little circled arrow glyph, as seen in the image above.. if you can move it down by 1px for all core projects. 
	Sort of want to vertically & visually align it by eye with a lowercase letter.

16 -	Final one for the blank slate is to do with the line spacing of the text. The diagram below perhaps shows this best. The mockup is shown on the left hand side, and
	the live version is shown on the right. The red lines show the baseline where I would like to have each line of text. You will see the live version (right side) is a little out.
	I know this is super fussy, but.. the details! the details!..

###LIST VIEW

17 -	Biggest one, as chris (cyco) has mentioned is List View stops drawing the alternate background after a few items

18 -	This is just a heads up, I wasn't too keen on the press state of the header bar columns as demonstrated in the image below. It seemed too 'pressed in', so the
	graphical resource file that this uses has been updated on Dropbox (see the image file called: list_column_header_bar.png)..

19 -	Be careful with the column gridlines, the last most column shouldn't have a gridline on its far right side (this applies to the list portion of coverflow as well)..

20 -	There is an alignment issue with items in list view. The image below best explains it, but the list of games should be left aligned to the column header name (careful some
	fields are right aligned such as the Play Count column.. so refer to the mockups!). The red line in the image below demonstrates the alignment issue..

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

28 -	At times, the game title in CoverFlow view changes to a big white bar / box. Very odd..

29 -	This is more of a question, but, is it possible to add a custom scrollbar to this coverflow view? I know we are using either a hacked coverflow using Apples hidden API's or
	some open source stuff to do this? ..but, a scrollbar would be consistent with how Apple does this in Tunes (and make scrolling through covers useful / easier).

###GRID VIEW

30 -	Chris (cyco) has mentioned this, but Grid view sometimes crashes when quickly scrolling and sometimes when resizing the thumbnails.

31 -	Archive.vg API: Adding a game should use the api database (I know we have had weird issues with it), this includes cleaning up the rom file name we use by default by using
	the game name Archive has for it and pulling in the cover art from Archive's database.

32 -	Manually adding artwork (i.e. drag n' drop onto a game from my desktop), works, but the image disappears when I change to a different console or collection in the sidebar
	and is also lost or disappears after I quit the app and relaunch.

33 -	Grid view allows a user to change the artwork via drag n drop. Chris (cyco) came up with an initial animation fro this, and I have since tweaked it and refined it.
	(see this in Dropbox > Notes > Adding Artwork > Animated Mockup for various videos of this)

34 -	A selected game is indicated with a blue 'ring' around the box art perimeter (image below). In a previous build we had a nice quick little fade in / fade out transition with this selector.
	Its not really an issue, but I do miss it.. one of those small requests that would remove a common action users do and make it look less 'clunky'..


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

###In Window Gameplay

40 -	When I go fullscreen, the dark toolbar at the bottom goes with it (bar with the view options, search field, grid size slider etc). The fullscreen button via the gameplay HUD bar
	(in image below) should only show me the game window in fullscreen and nothing else..

41 -	When I quit, via the 'power off' looking button far right of the gameplay hud bar, the gameplay window fades out back to the main ui, but, annoyingly the hud bar will still remain.
	For example, I launch and play Mario 2, then go to quit it by pressing the red power off button, the game quits and fades out, but, the hud bar doesn't fade out.. what I am
	left with is seeing my games in grid view and the hud bar floating over the top of it. What should happen is, as soon as I hit that power off button on the hud bar, the hud bar is
	no longer active or responding to my mouse inputs.. and the game and the hud bar fade out in unison back to the main ui.

###Popout Gameplay Window

42 -	As mentioned by chris, it would be nice to get the 'window frame' or the look of the pop out gameplay window looking like that of the mockup (resource are sliced, there and ready
	to go.. check DropBox).. 

43 -	The gameplay hud bar is missing from this pop out window in the latest live build I am using.

44 -	We also don't need to add a fullscreen button on the top right of this window (as the image below depicts), this button is available in the gameplay hud bar..

##PREFERENCES

###General Comments / Tweaks

45 -	Random overly fussy one to start, but I notice that the first time I open preferences from a new build, the window does a weird flickery /  flash thing. This also happens sometimes
	after I quit, relaunch the app and open the preferences sometimes too. I assume what is happening is, we are loading all of the bits and pieces it needs at the same time the 
	window is opening, so this flicker is the split second as the window draws itself on screen?

46 -	This is one of those crazy designer tweaks. In the image below, looking at the green lines, it shows the distance between content and the bottom edge of a window. Can we 	double check the gap or space here is always 22px **in Library, Gameplay & Controls** (in Controls it is the gap between the recessed panel and the window edge).. 

47 -	Also the distance from the top of the tool bar and content should also be a 22px gap like like the image below (excluding the Controls section). This also applies for the 	spacing either side of a divider. In the example below, a 22px gap from the 'Change' button to the divider should be in place, and as demonstrated a 22px gap from 	the divider and the content below it 'Organisation Methods' header. This is just using one section as an example. This rule should be applied to all content excluding the 	Cores section..

###Library Section

48 -	Everything here is fine.. just obviously refer to the content spacing issues described in the last two points in 'General Comments / Tweaks' above. (images with the green lines)

###Gameplay Section

49 -	First, refer to the content spacing issues described in the last two points in 'General Comments / Tweaks' above. (images with the green lines)

50 -	For these kind of popover buttons (image below), when the popover is active, and the user is selecting content in the popover, (filter modes in this example),
	can we use the inactive state for the popover button behind, rather than staying on the pressed state as shown in the image below?..

51 -	The Filter effects graphic is not in place yet, I'll need some help in producing a graphic image for each one so it changes based on the one selected in the popover.
	For now, I see there is a default image file for each filter effect in the graphic resources of the app. 

###Controls Section

52 -	First, just make sure the gap between the recessed box and the window edge is 22px (as discussed in 'General Comments / Tweaks' previously)..

53 -	Next is the popover buttons to select which system, which player and which input type. What I would like to do is use the inactive button state when the popover is active / visible.
	As you see from the image below, this is to select and sort between available consoles and behind the black popover, we see a pressed state button.. would prefer the inactive state
	for this. This also applies to player selection popover and input popovers and their button..

54 -	<strike>UX interaction of the blue circle / ring indicator: I like this interaction, how it helps guide people to map/re-map buttons etc. What we do need to change, or add is the ability to
	cancel this blue ring effect and 'return to normal' (unfocus it so to speak). That means, when a button map field is highlighted.. I want to click anywhere outside of it to remove the blue 	ring effect and go back to normal.</strike>Also, I have noticed that sometimes, when changing to a different system and back, the field highlighted can get stuck (always focused) and on a rare 	occasion I have had the darkened controller graphic and blue ring always appear with no way to turn it off, even after closing the Pref window. I think it should cancel, unfocus when 	you switch away from it, either by changing to a different system, or changing the tab or even closing the pref window..

55 -	<strike>This one is more of a general question for you guys: we can highlight the fields and change button maps (blue circle thing etc).. I wonder if we shouldn't also allow people to
	click the buttons they see on the controller illustration to highlight the field below? Just an idea.. one to think about, lets talk about it before anyone implements that. Some
	interaction things to consider with that idea.</strike>  Testing this. Mucx creates some masks.

56 -	In IRC recently, there was an issue where the start and select button map fields were labelled the wrong way around. Cyco has since added a fix for that.
	I thought ti would also be good to note here, that the order of these fields loosely follows the order of buttons on the controller front starting from the left.. going to the right.
	Of course, as mentioned this is loosely how I did it, sometimes things like a shoulder button are squeezed in randomly, but for most controllers select comes before start based
	on this loose 'rule'. Don't go insane and change all the buttons based on this rule at the moment.. just start and select from what I have seen.

57 -	For the various button map fields which have a key or gamepad button mapped to it already (image left), if I click the field to focus it, the field goes blank (image right). 
	This shouldn't happen as we are hiding information from the user..

58 -	For the Sega Master System, there is a physical button on the console which is used for some games (insane I know), this button field should be labelled 'Console Pause'
	it is currently labelled wrong as the image below shows (change 'Start' as shown below to 'Console Pause')..

###Cores Section

59 -	There is a divider line appearing on the far right (near the far edge of the window in the image below), that shouldn't be there..

60 -	Not sure the list column headers here need to be clickable or sortable? (Core, System, Version column header bars) If you want to have this sortable, then they will need a sort arrow 	like we have in list view (image below is a quick mockup to explain what this is - see the Core column header?.. follow it to the right.. thats the sorting arrow)..

61 -	Final item for the Cores section / tab is to double check the font weight and colour. 
	The Core column in this list should be bold with a rgb text colour of: #e4e4e4
	All other columns should be normal font weight with an rgb colour of: #dbdbdb
	For uninstalled cores (greyed out looking ones), the same font weight rules apply, but the text colour **across all columns** (excluding the Install button of course), is: #707070

62 -	Double check the install core buttons text. (image below of inactive state for reference).
	The inactive button text colour should be: #e4e4e4 ..with 1px shadow text at 90 degrees, #00000 colour at 40% opacity
	Pressed state text colour should be: #bdbcbc ..with 1px shadow text at 90 degrees, #00000 colour at 40% opacity
