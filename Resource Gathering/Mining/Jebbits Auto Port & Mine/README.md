Open EUO version of this script

viewtopic.php?t=45778

not all features in yet but let the author know how it works

If you are on a shard that does not have AOS like say Metropolis the script posted with NOT work for you.

If you get the message Target Cannot Be Seen [/size]this means that no tiles could be found in a range that are reachable by event macro and need to be manually mined. However that said this script will find all possible minable spots next to you and try, if it finds none with in acceptable depth limits it will auto move on. If you are on OSI change the setting %sa from 20 to 100. This script will now show a menu for ingot count. It will display ANY ingot from any shard ( at least so far ) as long as you have aos installed and the item id id enk.

Settings in script you can modify by hand
set %house_extra 2 <----number of runes you have behinde your maine port home rune incase its blocked ( always set number + 1 ) so if your main home rune is 6 and you have 1 extra after it you would set the setting 1 extra rune + 1 = 2
set %tinkershovels off <----set to on for tinkering shovels
set %floor no <----set to "yes" if mining out of caves
set %magery #true <------set this to #true for Magery #false for Chiv
set %hidefield #false <------set this to #true if you wish to hide at each rune location #false if not
set %color #false <-----This will seperate colored rock in its own spot in chest if set to #true
set %manaset #FALSE <----- set if you want to med up at secure
set %hideme #false <-----set if you wish to hide at the secure(GOOD PRACTICE)
set %smelt #true <-----set #TRUE FOR SMELTING
set %s 3 <-----set this to the amount of shovels you want to pull from your secure
set %mark 14 <-----set this to 15 if using at the bank
set %ingotcount #true <-----#true to see menu counter
Image

Things you will need

Home setup
A wood or metal chest secure
A small red wooden box inside the secure
A bag if tinkering
a reg free suit ( can use regs but is slim lined to not get more )
Shovels inside the secure
Shovels on you to start.
An anvil and forge if smelting next to the secure
A rune book with a rune in it to port home/bank
A rune books with runes to your dig spots


Here is a picture of set up if you need
http://www.hostguilds.com/lumbermine.htm
BELOW THIS IS THE AUTOMATED SET UP INFO

Well here is the automated version of the Jebbits mining script LOCATED BELOW I promised some of you. This script will fully automate setup. The object of this is to help those that know UO but are not that familiar with Scripts. There is a small amount of work on your side, but if you can rename a book its that simple. and you will be restricted to other setting such as if your skill in hiding is under 80 it will not try to hide you during mining.
Set up in UO

Step one
How to name your books ( in game not in the script )
if you have one book with 12 spots for gold in it and name it like this.

ore 12

Home book setup
if it is the 6th spot in your book simply name the book

Home 6
It is recommended that you put at least one extra rune after this one incase its blocked, you can actually have as many safety recall runes after your main one as long as you change the %house_extra setting as described above.

Note: You can put a backup rune after the location you choose and it will use it if the first is blocked. meaning if you use the example above and set home 6 and that location is blocked it will try location 7 then 8 then 9...until it is successfull. there is no safety for this so the script will fail if you have no backups locations and the location is blocked.

For your runebooks have as many as you like in your pack with the name ore and the number of runes on the book. examples below

ore 14 <---14 runes in book
ore 12 <---12 runes in book
ore 16 <--- 16 runes in book
ore 5 <--- 5 runes in book

You can put other info afterwords if want. like.

ore 7 gold
ore 13 verite/agapite

Yes you MUST have a forge and an anvil next to you for the smelting part of this script.

Overweight Issues
set %maxweight #maxweight - 25
set 25 to an increasingly higher number as needed for over weight issues.

Additions
Script can now be set for Chiv or magery{{{NewV1.5}}}
Rock miners now have the ability to have the ore separated into their own piles. {{{New V1.12}}}}
Pulled out a lot of not needed code and updated some script ideas {{{New V1.11}}}
Added some timeout loops to help with lag, Even more stable {{{New V1.11}}}
This script Now uses CEO's healthwatch as a call {{{New v1.10}}}
Put in a safety for those that have the occasional overweight problem, it will drop
1 regular ore at a time until you are no longer overweight{{{NewV1.10}}}
;Auto walk to secure is dependant on the spot you stand when you start the script {{{NewV1.9}}}{{{NewV1.10}}}
;Reworked the entire script and pulled out about 40 lines of code{{{NewV1.10}}}
All new revamp of script, fully reworked and more relaible auto dig
Updated to use tile find sub from Orngrimm {{{V.2.0}}}

;Ability to hide at each location if set in script.

;-------------------------------------------------------------------------------
; Script Name: Jebbits Auto Port & Mine
; Author: Jebbit
; Version: 1.6
; Client Tested with: 5.0.0
; EUO version tested with: 1.5.3
; Shard OSI / FS:  OSI/FS
; Revision Date: 4/7/06
; Public Release: 04/12/03
; Purpose:Auto Rune Book Mining NO PROGRAMMING NEEDED
; All menu driven with in game setup
;-------------------------------------------------------------------------------