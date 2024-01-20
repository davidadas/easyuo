RuneBook Mining 3.5 by Spewy [Oct. 17th, 2005]

You Must have your files In the same folder as EUOX 1.5!!!

Image

Say thx to Bferriter for taking his time to design a new ore counter!
Image


Requirements for Use and Step by Step Tutorial (External link)<----READ ME FIRST!

Having problems setting up your mining spots?<----Use Cyberpopes Mining Radar!


Note:
- This script uses global variables 126+ (*126,*127,..., *200+) for the interactive setup.

<- Please, if you Use It, Rate It

spewy wrote:
So Long...
I realized that I hadn't taken the time to say goodbye. My time here has been really fun.
I spent a year not playing UO but still maintained and improved this script and a couple others.
Thanks to everyone that took the time to say a kind word. Thanks to Cheffe and the active members that has made this a real community.

(For anyone that cares, I've been playing WoW everyday now... and making the occasional helpful AddOn for fun).



Take care, I had a blast.


CEO: Notice of ownership change!

Spewy has left UO for WoW and is no longer updating his scripts. However, Tracergod has received permission from Spewy to take over Runebook Mining. Sorry to see you go Spewy, hope you drop by now and then. Thanks to Tracergod for assuming the roll of continuing to make this easily the best miner script available.

I've changed the ownership of this thread to Tracergod as well so that he can update and support the script in the original thread and keep all the history intact. Please direct all future requests and bug reports towards him in this thread or however method he prefers. Thx

I just wanted to thank Spewy for all his hard work on this script. I know thousands of people use and love it. Thx Spewy for making Mining something we can all love :wink: Hope you are enjoying WoW!


Orngrimm: Tracergod hasnt logged in since 2 years as of September 2018. Be aware that this script may soon become abandoned.

TracerGod

;==================================
; Script Name: Runebook Mining
; Author: Spewy
; Version: 3.5
; Client Tested with: 5.0.1c
; EUO version tested with: 1.5 build 62
; Shard OSI / FS: FS/OSI Tested
; Revision Date: October 17th, 2005
; Public Release: September 16, 2003
; Purpose: Efficient mining with the use of runebooks and pack animal
;==================================

----------------------------

RuneBook Mining by Spewy [FAQ]

:!: 1) How do increase my chances of escaping?

i) Cast Protection. It will be effective until you cast it again. This will prevent damage from interupting your recall escape casting. Usually a red will get 1-2 spells off before you have successfully recalled out. And with a reasonable character you should be able to survive such an attack.
ii) Specify your escape target. This can save you almost a second from your recall attempt and there is less change of things going wrong. It could be the difference from 2 spells being cast on you or 3.
iii) Pick your escape location so it never gets block. If your house rune has an occasional spawn find a different location.
iv) Choose your mining locations wisely. I bought my mining runebooks but I only use 10-12 runes out of the 16 because the mining locations were simply too dangerous.
v) Wear some armor. Low reg suit are nice for resist and counters theives :)
vi) Use Hiding. Let the script hide you and let your character gain skill.
vii) Be lucky :)

:!: 2) After I unload the ore to the bank/house, I do not recall back to the place I was mining, instead I go to the next rune. That can't be right!

This is acutally a feature. There is quite a bit of overhead recalling getting setup to dig, and for most efficient mining results you want to be able to stay 'out on the field' as long as possible. By recalling to an partially mined rune location you are incurring the recalling penalty for less digs than if you went to a fresh mining spot.

You can manually change a variable in the script and it will recall back to where you came from look for:
Set %NextRuneOnBaseUnload #true

And set it to #false.

If you are using the interactive setup you will want to find the second occurrence of that line. I will eventually add that property to the interactive setup, its just its a minor feature and its really tough to come up with a short sentence to explain what it would do :)

NOTE: I'll have to get a different tutorial since the next two are obsolete since defining mining locations is done using a new interface.
:!: 3) How do enter my own mining locations?

We'll use world coordinates since they are more reliable.

- Open the script and find the SetDigLocations sub (Ctrl-F, "Sub SetDigLocations" ), and login with your mining character
- First thing we need to fill in is the runebook id in the following line.
  GoSub FindRunebook XXXXXXX ; or %_RuneBook1 if you blah blah

Double click on the runebook and look at the #LObjectID variable (Make sure the variable pane is up Ctrl-R). Replace the Xs with the value of #LObjectID (and you can delete the comment). Example:
GoSub FindRunebook ABCDEFG

- Now the script knows which runebook your are defining mining spots for lets go ahead and create our first mining spot

a) Recall to the first mining rune and mine until you get the vein you wish the script to mine.
b) Find the Last Action section of the variables and take note of the #LTargetX, #LTargetY, #LTargetZ, #LTargetKind, #LTargetTile. These are the values that you need to enter into the script.

GoSub SetUserDigCoord <RuneBook Index> <Rune Index 1-16> <#lTargetX> <#lTargetY> <#lTargetZ> <#lTargetKind> <#lTargetTile>
GoSub SetUserDigCoord %sdlBook 1 1390 2915 5 2 1141

- The #LTargetTile is only applicable inside a cave, if you aren't in a mine just put in 0 (zero).

- Now recall to the next rune and follow the same steps, but increment the number after %sdlBook. So the next rune will look something like:
  GoSub SetUserDigCoord %sdlBook 1 1390 2915 5 2 1141
  GoSub SetUserDigCoord %sdlBook 2 1391 2913 5 2 0

- To define a second mining spot at the same recall spot just create a second line without incrementing the number, like so:
  GoSub SetUserDigCoord %sdlBook 1 1390 2915 5 3 1141
  GoSub SetUserDigCoord %sdlBook 2 1391 2913 5 2 0
  GoSub SetUserDigCoord %sdlBook 2 1394 2910 12 2 0

- Rinse and repeat until you have all the recall runes are defined. One runebook definition would look like this:
  GoSub FindRunebook ABCDEFG
  Set %sdlBook %return
  if %sdlBook > 0
  {
  GoSub SetUserDigCoord %sdlBook 1 1390 2915 5 3 1141
  GoSub SetUserDigCoord %sdlBook 2 1391 2913 5 2 0
  GoSub SetUserDigCoord %sdlBook 2 1394 2910 12 2 0
  ; a bunch more lines (Yeah I'm lazy :) )
  }

Remember if you remove a rune, or reorder the runes you need to reorder your mining definition.

\":!:\" 4) How do specify my mining locations in external files (not in the script)?

- Read the first tutorial to get an understanding on how to define mining locations. I will assume you have already done this and will show how external files differ from definition within the script.

- Download RuneFunction.euo from the link above. You must save this file in the same folder as the mining script (do not rename it).

- Specify which external files should be used with which runebooks. This is done when you add your runebooks:
  ;Syntax: GoSub AddRunebook <RuneBook ID> <# of Mining Runes> [Color] [External Definition Filename]
  GoSub AddRunebook ABCDEFG 14 %Valorite SpewRunes.euo


The line above adds the runebook with ID ABCDEFG to the list of usable runebooks. The script is told that this runebook holds runes to valorite veins (the %Valorite) and that it should look for the file \"SpewRunes.euo\" for the mining locations.

Important: You must not have any spaces in the filename (a limitation of EUO).

When defining additional runebooks, you can specify the same external file, a different one, or none at all (in which case you need to define the dig locations in SetDigLocations.

- Replace the 'Gosub' with 'Call RuneFunctions.euo' That is only one difference between external definitions and those in SetDigLocations.

Using the example from the first tutorial, what would have appeared in SetDigLocations as follows:
GoSub FindRunebook ABCDEFG
Set %sdlBook %return
if %sdlBook > 0
{
GoSub SetUserDigCoord %sdlBook 1 1390 2915 5 3 1141
GoSub SetUserDigCoord %sdlBook 2 1391 2913 5 2 0
GoSub SetUserDigCoord %sdlBook 2 1394 2910 12 2 0
; a bunch more lines (Yeah I'm lazy :) )
}

In SpewRunes.euo it gets converted to:
Call RuneFunctions.euo FindRunebook ABCDEFG
Set %sdlBook %return
if %sdlBook > 0
{
Call RuneFunctions.euo SetUserDigCoord %sdlBook 1 1390 2915 5 3 1141
Call RuneFunctions.euo SetUserDigCoord %sdlBook 2 1391 2913 5 2 0
Call RuneFunctions.euo SetUserDigCoord %sdlBook 2 1394 2910 12 2 0
; a bunch more lines (Yeah I'm still lazy :) )
}


The RuneFunctions.euo is the file that you had to download at the beginning of this process. Hust a Search and Replace for 'Gosub ' to 'Call RuneFunctions.euo ' (don't forget to do the FindRunebook line) and everything else stays the same.