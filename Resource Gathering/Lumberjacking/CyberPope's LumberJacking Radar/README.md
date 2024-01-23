;==================================
; Script Name: CyberPope's LumberJacking Radar
; Author: CyberPope
; Version: 1.0t
; Client Tested with: 5.0.1j
; EUO version tested with: 1.5 build 69
; Shard OSI / FS:  OSI & Most Freeshards
; Revision Date: 9/11/06
; Public Release: 3/14/06
; Global Variables Used:
; *LJSetup
; *LJColor_SHARDNAME_GridArea_Facet#
; *LJLoc_SHARDNAME , Index#
; *LJDBW_SHARDNAME , Facet#
; *CPLR_Export
; *CPLR_Import
; *CPLR_Drop
; *CPLR_Stats_SHARDNAME
; *CPLR_WOODS_SHARDNAME
; *CPLR_Axes_SHARDNAME  (only used if changed from Default)
; *CPLR_Tiles_SHARDNAME  (only used if changed from Default)
; Purpose: To select by tile where you want to Chop,
; record wood types for LJ locations, and to write
; UOAutoMap .map files
; Copyright: 2006/3/14 CyberPope
;==================================


Cyberpope's LumberJacking Radar v1.0t
Before using it Please read this entire post and the one below it that gives information on each of the updates so that you know what options you have with this script.

1) This script may or may not work on freeshards, if it doesn't I am sorry, I will try my best to help you out to get it to work but no promises.
2) This is not intended to be, and never will be, an automated Lumberjacking script.
3) If you want this script to do more (ie. craft axes, cut boards, ....) you will have to add it yourself.


Notice: Currently this script does not function in any of the 'new' regions that are part of the latest expansion. This is not a script issue but an EUO limitation. So until EUO is updated with these new regions they are unmappable with this script.

The tool looks like this:
Image

The Menu Interface
HOW TO USE: Tiles that are chopable will be represented by buttons, just press the button to mine that tile.
I've also added lines to show you the resource boundaries so you can chop more accurately/efficiently.
STATUS: Just what it says, this updates you to let you know what's going on.
RESET Button: This will only appear if you have selected yes for Recording Depleted Tiles. Press this button to clear out all the past depleted tiles.
OPTIONS Button: This will open the Menu Options. (See Below)
STOP Button:This will only appear while you are chopping. Press this button to stop chopping immediately.
Cur-X/Y: This is the current X and Y position of your character.
Dig X/Y/Z, Tile-T, & lt-Kind: This is the current X, Y, and Z axis of the tile you are chopping.
Tile-T is the #Tiletype of the tile being choped.
lt-Kind is the #ltargetkind used for the tile you are choping.
(Note: If you have problems choping a spot this is the info I will need from you as well as the Facet you were on)


Options	(All options are saved using the CEO*Filesystem)

Legend
Image	If at any time you are not sure what you are looking at just Press the Options button, Then the Legend button and a display of the different icon types will appear.

Any additional Woodtypes added by the user will also show up in the Legend.


Settings
Record Depleted Tiles: Depleted tiles will be marked the designated color.
Track Wood Types: Check to have the script track the types of wood that are chopped in each location.
Display Text on Tile: This will display the designated letter for the wood on the tile button.
Display Color on Tile: This will display the designated Color for the wood on the tile button.
Test Z-Axis: This will help cut down the number of 'Unreachable' Tiles by avoiding tiles that are +/- 19 or more of #charposz. (Mostly for Freeshards)
Halt on Colored Wood: This will immediatly halt the chopping process as soon as colored wood is detected and record it. This can help increase the speed at which you map an area.
Use Any Available Axe: If this is selected the script will attempt to arm any available axe it finds in the first layer of your characters backpack. This is for shards that have breakable axes. Note: This will use ANY axe that is in the item type list including any valuable axes such as 'Axe of the Heavens' ect.
Grid Drawing Delay: This is the amount of time (in seconds) your character must stand still before the radar grid will draw. (Note: a delay of 1 or less may cause your system to bog down)
Chopping Delay: This is the amount of time you want your lumberjack to wait between each axe strike (20 = 1 second)
Maximum Chop Range: This is the maximum tiles away that you can sucessfuly chop a tree. Trees outside this range will NOT appear as buttons and thus unchopable.
Grid Area: This is the resource grid type for your shard. On all OSI shards this is X:8 Y:8 and on most RunUO shards this is X:4 Y:3. Some freeshards have their own settings and could be 1x1 (meaning every tile has its own resource). You'll have to experiment to figure out what your particular shard's resource area is.
Depleted Color: This is the color tiles will appear when they are depleted and you have Record Depleted Tiles selected. Press the colored button to update it with what you have entered.(Note: The only colors that can be specified by name are: Aqua, black, blue, fuchsia, gray, green, lime, maroon, navy, olive, purple, red, silver, teal, white, yellow or btnface. You can also use a hexidecimal descriptor or pixel color. See Menu Font Color for an example.)
Lines Per Cycle:This will change the rate at which EasyUO will run the code. For more information on Lines Per Cycle please click HERE.
SUBMIT Button: This will save your changes, if any.

Image

Export
Image	Export ID: This is your ID for exporting files. This Identifies who you are to the person importing your file. Please keep the name short and recognizable. Like your EasyUO handle.
Export Path: This is the path that you wish to export your location data to. Like the UOAM Path this needs to be in DOS format. (You should use a different path for Exporting than you do for Importing)
File Name: This is the name you wish to call your Export file.
Shard: This Combobox holds all the shards you have recorded chopable locations for. Changing the shard selected will update the data below with that shard's information.
Number of Locations: Simply the number of locations you have recorded on this shard.
Last Location Written: This is the last location you wrote to your Export file.
Create New/Append Old File: If you select "New File" you will re-write the old file with all the recorded locations. If you select "Append Old" you will simply start adding new locations to the map starting with the next location after the Last Location Written.
Write/Re-Write UO Export File Button: This will begin the file writing process. If you have already written all the current locations the button will appear as "Re-Write" so that you can re-write the file.

Import
Last Import Path: This is the Last Path you used to import a file from. As before this must be in DOS format, Read more in the FAQ below. (Your Import path should not be the same as your Export Path)
Last File Name: The name of the last file you imported will be displayed here.
Get File Data Button: This will attempt to retrieve the data from the file and path entered above.
File From: This is the Export ID of the user who created the Import File.
Shard: Name of the shard to which the data is from.
Shard Type: This is the resource grid that the Exporter uses on this shard.
(I have put in some precautions to protect you from receiving mis matched data. i.e. someone recorded your shard at 6x6 when you record it at 8x8)
Last Imported Loc: This is the location number of the last location you imported from this user for this shard. This will allow you to skip previously recorded locations if you so desire.
Start with Location X: This box allows you to select if you wish to start at the beginning of the file or the next location you haven't previously imported.
Upgrade Normal Wood Spots: If this is checked then if a location that was previously recorded as Ordinary is now showing as a different color it will be upgraded to the new wood type.
Import Locations from File Button: As the button states this will begin the Importation process.
Locations will either be Added, Upgraded, or Skipped. Locations will be skipped if they are:
1) Already in your database or
2) Fail certain validity checks
   Image

UOAM (aka UO Auto-Map)
Path for UOAM File: This is the destination folder for you map file. Enter only the path, the script will generate the file name.(path needs to be in DOS format read below)
Select Icon Type: Allows you to select whether you want to use Wood or Terrain Icons for your UOAM markers. (read more about Wood Icons Below)
UOAM Style: This is how you prefer to have UOAM displayed.
Icon Offsets: This is how far away from the upper left corner of the 8x8 resource Square you want the icon to be drawn. (see examples below)
Shard: This Combobox holds all the shards you have recorded lumberjacking locations for. Changing the shard selected will update the data below with that shard's information.
Number of Locations: Simply the number of locations you have recorded on this shard.
Last Location Written: This is the last location you wrote to your UOAM file.
Create New/Append Old Map: If you select "New Map" you will re-write the old file with all the recorded locations. If you select "Append Old" you will simply start adding new locations to the map starting with the next location after the Last Location Written.
Write/Re-Write UO Auto Map File Button: This will begin the file writing process. If you have already written all the current locations the button will appear as "Re-Write" so that you can re-write the file with different settings, or if for some reason you lose your old map file.
Image

Advanced
Chop All: If this is checked, the LJ Radar goes into a different mode that makes any tile able to be chopped. (Read more about Chop All below.)
Path Check: Path Check is used to determine the validity of the Import & Export path assigned by the user. If this is unchecked it the script will not warn the user of an invalid path name.
Prewood: This is the EXACT text that precedes the wood type when it is chopped from a tree. It must be exactly the same as it would appear in #journal, so spaces need to be replaced with underscores. For example in: You_chop_some_Ordinary_logs_and_place_them_in_your_pack. You_chop_some_ is the value for Prewood.
Postwood: This can be any amount of the text that follows the wood type in the journal message when you chop a tree starting with the first character after the wood type. In the example above _logs is acceptable and so is _logs_and_place but place_them_in would be invalid.
Edit Axe Types: This list contains all of the axe types recognized by this script. If you have an axe type that is not being found you can add it here. You can remove any you don't want to use by selecting them in the list a pressing the Del button. If you want the list to go back to the default values just press the default button.(If you do find an axe type that is not in the list please PM me the axe type so I can add it to the script)
Edit Tile Types: These are all the tile types that are recognized as being choppable for wood. You can remove any you don't want to use by selecting them in the list a pressing the Del button. If you want the list to go back to the default values just press the default button. (as above if you find one that is not on the list please let me know)
Wipe All Saved Locations: Pressing this button will delete every saved location you have for the shard you are on, clear all stats, etc.
Blue Question Marks: These just give a general description of what each item does, much like the stuff you just read.	Image

Drop (Must use EUO 1.5)
Image	Drop Style: There are Three drop styles available.
Overweight - This will drop items when you go over your Weight Check weight. (see Settings)
UOAssist - This will drop items in the same fashion the UOAssist does, after each chop.
Do Not Drop - This option turns off item dropping.
Drop After Depletion: If checked, you will drop any designated items you still have on you after the tree you are chopping has run out of wood.
Drop Wait: This is the amount of time you character waits between dropping items to the ground. If you get lots of ghost images and failed drops or 'you must wait' messages I'd recommend increasing this number. (20 = 1 second)
Log Types to Drop: Any wood type you have checked will be dropped to the ground by your character (depending on your Drop Style).
Misc Items to Drop: As above except that any items checked will be dropped to the ground.

(Please note that dropping items to the ground can at times be unpredictable due to odd terrain, housing, ect., while my script is very efficient at doing this there can be problems with the drop process)

Wood Types
If you play on a freeshard that has other wood types you can add them here in the ADD section. You must give the following information:
Name - This is the name of the wood type as it appears in the journal message.
Button Text - This is where you put the letter(s) that will appear on the button to chop. (only a max of 2 letters will appear properly)
Button Color - This is the color you would like the button to appear on the Radar. (you can use the same options for color as mentioned above for Depleted Color)
Text Color - This is the color you would like the Button Text to appear on the Radar (same color rules apply)
Wood Findcol - This is the #findcolof the wood type. You will have to figure this out yourself using finditem.
You can edit existing types much the same way in the EDIT section. (Note however that if you change or delete an existing wood type that has been previously recorded you will have to wipe your entire database. Also I do not recommend changing the defaults to reorder them and such as you will only be able to import locations from people who have the same wood types in the same order as you do.)	Image

Stats
Image	As you chop trees throughout your shard the Lumberjacking Radar tracks the number of each type of location found and on what facets. As you can see it gives you approximate percentages for each catagory. (there will be rounding issues with the percentages)

While on this menu you can change to any other shard you have used the LJ Radar on to view the stats for that shard as well. Other shard with differing wood types will be displayed properly.

The Chop All Interface
Image	As you can see when you are in Chop All mode all the tiles are now represented with a button which displays a number. This number represents the number of tiles in that square.

By pressing one of the buttons you will cause the bottom of the radar to be updated with the tiles in that square. If you wish to chop one of those tiles, simply press the corresponding yellow button. All tiles that are recognized as choppable will appear with the tile type in green, all others are red.

This is primarily a debugging mode that I used to try and find tile types that were choppable but not in my list. You can do the same, or whatever you want with it. If you do find a tile type not recognized by this script please PM it to me.

Useful Knowledge for Using UO Auto-Map
DOS style Path names: Since the execute command is using DOS to write your filename it is most likely that the path to write your file in will need to be in dos format as well. By default when you install UOAM it goes to C:\Program Files\UOAM\.
DOS Folder names cannot have spaces and must be 8 characters or less.
As such C:\Program Files\UOAM\ Becomes C:\Progra~1\UOAM\ in DOS. This is the default setting for this script.
If you simply changed the drive you installed UOAM to you can easily just change C: to the appropriate drive letter.
If you Installed to a totally different directory you will have to go into DOS and try and figure out the name of the folders in your UO Auto map Path.
For more info on Execute, and DOS commands Read: Roadkill / MinocMinerMurderer 's Execute/DOS/.BAT tutorial
I Cannot Find My Map File: Most likely this is from a bad Path name. Try searching your computer for any .map files on your computer. If you recorded the map using the Tilt UOAM Style the Filename will be YourShardName_wood_tilt.map. If you recorded it using Square it will simply be YourShardName_wood.map. If you can't find it after that try setting the path to C:\ and try Re-Writting the map and just look in the root directory of your hard drive and then move the map to the UOAM folder yourself.
I Selected Wood Icons But all I got were Blue Markers: You either Don't have Wood Icons set up in your UOAM. Or You have named them something different than this script recognizes them as. If you don't have Wood Icons you can download them at the bottom of this script. This script writes wood to the UOAM file as the following names: Ordinary, Oak, Ash, Yew, Heartwood, Frostwood, & Bloodwood. For more on adding the Icons to UOAM read THIS
I can't see the 8x8 Resource Grid in UOAM: Well you'll have to either find the Grid Map Files online somewhere or Draw your own.
I Have The Resource Grid but my Icons don't look right on the map: This is a problem with your Icon Offset settings. When I am out mining I use UOAM on a x4 setting. The Offset Defaults are based on the Icons I use at a x4 setting. If you use different Wood Icons or use a different Zoom setting you'll need to play around with the offests to get them right.
You keep talking about Offsets, I don't know what that means!: If the Offsets are set to Zero, then the Icons will be drawn in the upper left most spot of the 8x8 resource square. Below are some example of How the Offsets are used. The red Square is the upper left most spot of the 8x8 square and the yellow is where the Icon is placed After the Offset is applied.
Image	Square Map: On the right is an Icon placed ON the upper left corner of the 8x8 square.
On the left one that has been placed with an Offset of X: 1 Y:1
Image	Tilted Map: On the right is an Icon placed ON the upper left corner of the 8x8 square.
On the left one that has been placed with an Offset of X: 1 Y:4

(Yes I know these are ore icons but you get the point)


Other Probable Questions That Might Come Up (F.A.Q.)
I PRESS PLAY AND NOTHING HAPPENS: This script makes use of the tile command and as such requires the old .mul files in order to work. You can get the old .mul files either by installing an old version of UO that still has them and grabbing them or searching for them on the interwebs. (Links come and go but you can try HERE) Once you have the .mul files just throw them in the same folder your client.exe resides in.
Important Notes on Importing scripts: Please be aware that when you are importing a file from someone you are calling another EasyUO script. While most people are nice and can be trusted it is possible for someone to put in malicious code that could ruin your day. You should open the import file with EasyUO and look at it before calling the file. It should look like this:
SET !EXPORTID CyberPope  
SET !ExpShard Chesapeake  
SET !ExpShardTypeX 8  
SET !ExpShardTypeY 8  
SET !ExpWood -1  
SET !Number_of_WoodTypes 7  
SET !NameWoodType1 Ordinary  
SET !TextWoodType1 L  
SET !ColorWoodType1 $1e69d2  
SET !TextColorWoodType1 white  
SET !WoodFindcol1 0  
SET !NameWoodType2 Oak  
SET !TextWoodType2 O  
SET !ColorWoodType2 $0b86b8  
SET !TextColorWoodType2 white  
SET !WoodFindcol2 2010

;and continue through all the wood types.....

IF %1 = TEST 2  
SET #RESULT -1  
EXIT
set !loc1 4312_1088_2_1  
set !loc2 4304_1088_2_1  
set !loc3 4312_1080_2_1
;etc, etc, etc
In addition, if you are importing to a shard you have already recorded locations to, it would be very advisable to export your locations before you import. That way if you get bad data from someone or something unforseen happens you have some sort of a backup of your location data.
Somehow my locations are wrong, how do I reset my saved locations?: Simply go to the Advanced Options and press the Wipe All Saved Locations button.
When I Run The Script, All I Get are Purple Tiles. This could be a couple of things. Some areas have not been hard coded into the tile function. Like the Elvish lands. These tiles cannot be scanned. This is not a script issue but instead a EUO limitation. Second, If you are playing on a freeshard with a custom map then this script will not work or may not give the proper information. The tile function is limited to the OSI mapset. If you are playing on an OSI shard or clone and are not in newer areas like the Elvish lands, then there are two possible soluctions. First, try the solution found HERE. If that doesn't work, other's have had success by reinstalling the UO client.
My Radar Only Shows Question Marks "?" Why Doesn't it Show Me the Wood Types?: This is one of two problems. First, make sure that you have Track Wood Types checked in Settings in the Options. You will know you are in Tracking Mode because the radar will say ++Track Wood++ at the bottom. The other reason for seeing only question marks is you haven't bothered to mine the location with the radar. This is a wood TRACKER not a diviner. It has no way of know what type of wood exists in a location until you use this tool to chop it. You Must Chop the Location in Tracking Mode to See the Wood types.
My Shard Has other Wood Types how can I Track them?:Simply press the Woods button on the Options menu and add your wood types there.
What Exactly is this Test Z-Axis For?: I have not had any problems on RunUO or OSI with Z axis so I recommend you leave this unchecked. However, if you find that trees are unchoppable that are at a greatly higher or lower elevation than your character you should check this option

Many Thanks
At this time I'd like to thank my beta testers who have given me many a post in the Debug Threadto chew over.

Script Credits
CEO for CEO*FileSystem (pseudo filesystem). 1.1
Janus for Replace Sub
Roadkill for Determining OS for Filewritting (taken from write fast DOS Array)
Kal In Ex for Fast File Writing Subs
Gravix for String Implode/Explode Sub
Snicker7 for his Equip Axe sub and Drop Item to Ground sub
Tecmo and Bad Maniac for their MoveItem sub.

In Closing
If you have problems with this script DO NOT PM ME. Post your issues here. If you have problems it is likely that others might also and could benefit from the problem being resolved in public.

Feel free to post ideas and comments.

IF YOU USE THIS SCRIPT THEN RATE IT.

If YOU USED THIS SCRIPT AND RATED IT LESS THAN 10'S AND LIKE THIS VERSION BETTER CHANGE YOUR VOTE!

Peace,

CyberPope

Edit by Orngrimm:
As EUO changed how menus are handled, the menu of this script is broken out of the box.
Find a menu-fixed version at viewtopic.php?p=437553#p437553