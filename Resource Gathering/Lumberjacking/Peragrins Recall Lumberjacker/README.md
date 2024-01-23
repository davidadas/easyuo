Requires EUO 1.5

OVERVIEW
Recall lumberjack script, use from your house to recall to pre marked trees in as many runebooks as you like. Makes boards from the logs and stores them as you go.

INSTRUCTIONS
. Mark your runes next to the tree you wish to chop.
. Have a runebook named HOUSE or HOME with the rune to your house in the first slot. (for reliability have a spare rune in slot 2 for a different recall spot next to your house.)
. Have FULL runebooks of runes to trees marked as above, name the books TREE1, TREE2 etc (just needs to have TREE in it really.)
. Have an axe in your pack,
. Use a LRC suit as regs/tithing points are not taken into consideration.
. Have enough magery/chivalry to recall reliably.
. Start next to your secure in your house, click the secure when prompted and then sit back and watch the logs fly in.

THINGS TO NOTE
. Now requires EUO1.5 tv57 or better to run. Do not post about problems if you are not running the script on that, I'll just hide your post and then ignore you for being a moron.

. Written for OSI and Alexandria Freeshard, if your freeshard has different rules then I shall attempt to help you with advice, but you will have to modify the script yourself.

. The runes MUST be marked right next to the tree in one of the eight squares surrounding the trunk.

. Because this script can take you all round the map, the gains for lumberjacking can be quite good, so even if you have low lumber skill, give it a go.

. For use from a house, your secure must be reachable from the point you recall to.

. Auto detects multiple runebooks.


UPDATES:
v1.7
. Threat finder changed to remember threat types from previous runs.
. Major rework of many subs.
. Recall sub now quicker AND more reliable.
. Weight check sub now takes extra resources on Feluca into account.
. Chop subroutine now scans journal to check for messages rather than using #sysmsg. Also changed to stop the script moving to next tree when a special resource was found.
. Heal and cure subroutine now use chivalry if needed.
. Stats taken out as they weren't working right.

v1.6
. Modified DROP_OFF subroutine to use new exevents, as a result drop off is now unbreakable under normal circumstances.

v1.51
.Changed drop off subroutine slightly so that all types of log are dropped off. My thanks to Kamelbarn for providing the answer whilst I was absent.

v1.4
. Tweeked problem with script not 'remembering' blocked locations
. Tweeked recall sub to avoid runebook staying open after recall/SJ

v1.3c
. Fixed problem with not using invis or hiding.

v1.3b
. Fixed problem with using SJ and the secure not being set.

v1.3a
. Tiny tweek to the stats to get the proper logs/hr after 1 hour

v1.3 (tested for 1Hr 20Mins, no faults and over 4000 logs collected. Had looped to first runebook and resources had not respawned, will have to get more runebooks.)
. Added function to use hiding if your magery is below 92% (level at which you can cast invisibility 100%)
. Tweeked monster finding to include brigands but exclude other NPCs

v1.2
. Added support for traveling using sacred journey, if your Chivalry is higher than your magery, you will be asked if you wish to use Sacred Journey.
. The option to go invisible if you are attacked is now in, just select your preference when asked.
. Will now heal if injured apon returning home.
. Fixed small bug in recall sub with endless loop if no tree was found at the location resulting in repeated attempts to recall to the spot you are standing on.

v1.1
. New tweeks to recall sub. (Tested for an hour without breakage.)

v1.0
. New recall subroutine error checks for lag and is fail safe.
. New tile scanning sub finds trees in the 8 squares round you so rune marking need not be so precise.

v0.4
. put in active checks for runebook page flipping to stop error with script using charges during lag

v0.3
. Tweeked the weight error checks

. Changed the runebook setup to recognise 'HOME' and 'HOUSE'

. Fixed the resource stats counter for the currnet rune posiyion and current amount of logs

v0.2 (downloaded 31 times)
. Added other axe types.

. Changed rearm sub to use event macros rather than darag and UOA macros

;==================================
; Script Name: Peragrins Recall Lumberjacker
; Author: Peragrin
; Version: 1.7
; Client Tested with: 5.0.0b
; EUO version tested with: 1.5 tv 64
; Shard OSI / FS: OSI & Freeshard (tested on Alexandria)
; Revision Date: 13/11/05
; Public Release: 11/11/04
; Purpose: recalls to trees and chops them for logs
;============================================