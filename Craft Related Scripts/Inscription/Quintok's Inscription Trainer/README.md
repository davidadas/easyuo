;==================================
; Script Name: Quintok's Inscription Trainer
; Author: Quintok
; Version: 2.15
; Client Tested with: 4.0.5b
; EUO version tested with: 009D
; Shard OSI / FS: OSI
; Revision Date: 24 November 2004
; Public Release: 09 Oct 03
; Global Variables Used: *50 *51
; Purpose: 32-GM Inscription Trainer!
;==================================


How To Use This Script:
Download the Script, making sure if it does not download correctly right click on the link to download and select save target as
Make sure that in UO options, you have Offset interface windows rather than perfectly stack them checked!
Open EasyUO and load the downloaded script into EasyUO, click the green triangle [play] or press F9
A Menu pops up. First lets ignore that menu and get your bags set up correctly
Are you using your bank as a secure? tick the checkbox that says so
Are you tinkering your own pens? [requires atleast one tinker kit and ingots] if so, tick that checkbox also.
Your Secure should contain:
Resource Bag with
Regs
Blank Scrolls
Iron ingots if your tinkering your own scribe pens
Scribe pens if you are not tinkering your own scribe pens
Empty Mages Pouch
click the 'S' Button, if you are using a bank, it will be automated, otherwise it'll ask you to target your secure.
click the 'R' Button, and it will ask you to select your 'Resource Bag' in your secure container.
click the 'C' Button, it will ask you to target the empty mages pouch in your secure container.
click 'Save Setup' and this will save for future use of this script, wait until it's done (this save is character specific).
click 'Start'.

Problems:
Lag - on the menu, there is a number, which is 20 by default. if you have any lag based problems, increase this value
Containers don't move to the right spot - go to UO, click options on your paperdoll, go to the mouse looking option and 'tick' "Offset interface window rather than perfectly stacking them"
part xyz doesn't work - are you sure you've read the instructions? have you got the latest build? if you do, and your certain it's my end Post here, with a detailed explination to what you think is causing it and where the problem is.
I'm on a freeshard.... - it won't work, I'm not going to break down to all the possible reasons, try it if it doesn't work then it won't work.


Update 1.00 to 1.10:
- Added status bar
- Cleaned up some skill changing issues

Update 1.10 to 1.11:
- Code cleanup
- Newbie Setup yes/no option

Update 1.11 to 1.12:
- Added med only if failed med change to medfull sub
- Closes menu gump before it starts collecting resources
- Cleaned up code some more

Update 1.12 to 1.13:
- added the ability to tinker new pens, to do so have your IRON ONLY ingots in your resource bag along with your regs etc...
- big thanks to SgtBull for testing this script so fully.
- added ability to set the drag amount - that's for you Sgt :P
- Dynamic Contkind collecter

Update 1.13 to 1.14:
- Should be lag proof when checking for pens/scrolls/regs in your resource bag...

Update 1.14 to 1.15:
- Added ability to train at the bank [not suggested!]

Update 1.15 to 1.16
- Added container double check... can't do much more then this for lag.

Update 1.16 to 1.17
- Bug fix, Thanks Dumpy.

Update 1.17 to 1.18
- Bug Fix, now uses %regCnt when checking the reg number in makeLast :P

Update 1.18 to 1.19
- 'fixed' meditateFull sub, or atleast made it better, aparently :P

Update 2.03
- drag problem should be fixed
- dropping made scrolls should be fixed

Update 2.04
- Thankyou Freddy
- Fixed CraftItem sub
- Fixed tinker check bug
- Fixed tinker scanning check

Update 2.05
- Tripple Checking for damn scrollBag

Update 2.06
- secureID tripple check... for no good reason what so ever.

Update 2.07
- more a re-release than anything, nothing really changed.

Update 2.08
- Should Hide indefinetly now
- added #backpackID support

Update 2.09
- added rewrite of MoveItemToPos from QSubs to v1.1
- uses #Jindex for _ensureInJournal

Update 2.10
- found & solved Wait problem
- changed menu slightly
- slowed down certain collection of and replacing back of items

Update 2.11
- Added ability to remove regs when changing skill level
- Added new bag [resource]
- Added change to reg/scroll/pen setup

Update 2.12
- Fixed the 'finditem' bug.

Update 2.13
- remembered why #debug was important.

Update 2.14
- fixed problem with 'closeMenu' sub
- fixed resource collecting problem
- made it easier to find out what resource is missing

Update 2.15
- fixed 'wrong' reg/spell problem
- fixed secure container issue