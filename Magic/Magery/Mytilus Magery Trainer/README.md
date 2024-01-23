Mytilus Magery Trainer
Here it is! This will go slow forward until you find a gain and then milk the gain run with 8x8. Will recast if you fizzle and try to recast on a 8x8 spot 3 times to get a gain. If you dont gain 3 times in a row then it goes back to slow forward and searching for a new run. It also will meditate when your mana gets too low and script will shut down when you reach your skill cap. Hope this works good for everybody. If you like it please take a second and RATE it :)

--1.50 Updates--
*Added code that will start boat moving again when it's stopped and shouldn't be
*Fixed an endless loop issue when crossing server line with wand in hand
*Converted the values the spells are cast at to variables the user can easily change as necessary
*Removed warning gump from beginning of script, just be sure to target tillerman before starting.
*Will now stop and anchor boat when script is done

--2.00 Updates--
*Removed user defined %manafull variable and made it automatic
*Tested script on 0078 easyuo version
*Changed all boat commands to event macro 3 0 to avoid typing problems
*Script will now automatically locate tillerman for targetting!
*fixed bug from not having all tillerman types in script

--2.50 Updates--
*Finally added some eye candy, nice menu to keep track of skill gain
*Fixed possible bug with %loop not being reset to zero after every gain
*Added code to re-attempt meditation until success or mana is full
*Script will now stop boat during meditation and restart after if not in a gain run
*Script only opens status bar if its closed, and will open it again if it closes for some reason
*Healthwatch sub added to script
*Script will now automatically stop at skillcap, simply enter a number in place of auto if you would like it to stop sooner
*Script now saves tillerman id to a variable and resets #LTARGETID before every cast so it wont break script if you kill something

--3.00 Updates--
*Totally new menu display with cool stats like best run, elapsed time, and more!
*FIXED MAGE WAND BUG!! When crossing server lines with a spell wand it will bug your skill and cause you to cast the wrong spell. Now the script will know you crossed servers and re-open your back pack, and disarm/rearm wand to reset skill
*Added support for suits with less than 100% lrc, it is now possible to gm with as little as 1% lrc (not recommended unless you are really bored..lol)
*Added a skillcheck so script will continue on if you gain off a fizzle at low levels
*CEO's suggestion: Added magic arrow and harm to cast sub so now you can start with a mage wand from the very beginning of script!! (very helpful for all characters but especially for nubies with low mana!)

--3.01 Updates--
*Added gaincheck sub to fix boatstopping problem when casting Earthquake

IMPORTANT INSTRUCTIONS PLEASE READ!!!
If you find that you stop gaining for a long period of time you will probably need to adjust the spell values a little. Magery seems to vary a little from character to character and will also depend on how hungry you are. If you find that you are ALWAYS fizzling or ALWAYS succeeding while casting then you will need to adjust the values that each spell is cast at. These values can be adjusted in this section near the top of the script

;Minimum skill that each spell will be cast (you can adjust these as necessary)
set %harm 125
set %fireball 250
set %lightning 450
set %paralyze 600
set %ebolt 740
set %flamestrike 850
set %earthquake 960


If you use this script and enjoy it please take a moment to rate it. If you have used this script in the past (before my major fixes) and had given it a \"so-so\" rating please take a moment and fix your rating. With its mage wand re-equip code and built in health check this is by far the most complete magery trainer in the PSL.

;==================================
; Script Name:   Mytilus Magery Trainer
; Author: Mytilus
; Version: 3.01
; Client Tested with: 4.0.4b
; EUO version tested with: 1.42 [build 0098]
; Shard OSI / FS: OSI
; Revision Date: 10/12/04
; Public Release: 2/5/04
; Global Variables Used:
; Purpose: 8x8 Magery with antiblock, slow forward to find gains.
;==================================


If you have trouble downloading this script you will need to right click the download link and click on "save target as".