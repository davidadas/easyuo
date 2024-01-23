Endings LumberHacker 5.3.1
This script requires EUO 1.5.

---------------------------------

What it does: Just a lumberjacking script with beetle support. Auto chops logs into boards when you get full (then places them on the beetle), and automatically retargets the tree after each chop. Great for the trees in Del since they have massive amounts of wood. I guess this would be a semi-auto script since you have to target the tree, but thats all. Make sure you read the updates so you know all the features.

Instructions: Jump on a beetle and have an axe in your pack. Make sure you have carp tools. The rest will be displayed on the menu by "Status".
Mad Tamer wrote:
Working perfectly. I noticed it crashed my client over and over when i had UOA open but i closed it and now its working better than ever! Good Job.


Note: If you notice it doesn't recognize your axe, that means that I do not have that type in the axe list. If so, please post a reply with the axe name and (if you can) object type. Thanks

Updates:
v5.3.1 - Updates logs2boards to use axe and enhances to journal scanning.
v5.2.1 - Fixed dismount sub, fixed scan sub, corrected the status display when the packy is full.
v5.2 - Allows for packy use. No commenting required.
v5.1.2 - Another type...thanks regs2.
v5.1.1 - Fixed a typo, line 1 (gosub init) was commented out by accident. This was the problem with it not recognizing axes.
v5.1 - Added in skill gain checking (forgots, whoops!). Fixed scanner--if failed to hack tree, continued instead of an infinite loop.
v5.0 - Another rewrite. Seems to be the best yet. Journal scanning issues fixed.

v4.10 - Fixed Double Axe objType (NSF) and added nails (YFG and XFG). Equips axe when needed.
v4.0A - Rewritten for ML wood and EUO 1.5. Many updates planned.
v3.13 - No backpack positioning required, so it will work with any backpack/beetle's pack position.
v3.12b - Increased some wait times to account for the lag on the OSI servers due to SE's release. Also when the beetle is full, you press resume on the menu instead of going to EUO and pressing play.
v3.12 - Fixed the clicking for the carpentry and tinker gumps so whatever resolution and position your gump is, it works. Added a pause/resume feature and also changed the menu up a bit (visually, not statistically). Added a 'stash before beetle fatigue option' and will display the amount of boards on your beetle in red if its over 555 (over 555 boards means your beetle will be fatigued when you try and run).
v3.11 - Added in a Status section of the menu if you forget what your doing :P.
v3.10 - New menu!!! Shows lots of neat stats as you hack away at the trees. Another big, big thanks to Tecmo for helping me with this, and the rest of my script. Hope you all enjoy the new release and if you have time, please give some feedback :).
v2.11 - Fixed loading the beetle. Often trees would get in the way, now you wont have to worry about trees. Also, your char can only hold about 430 stones max. I didn't put a check in there to see if you go over 430, now I did.
v2.10 - I fixed the beetle support. It now should be much more stable although I added one step in the setup. Just got to target your beetle, not too hard eh? :) Have fun! Oh, and everyone give thanks to Roadkill for lending me his dismount sub.

If you use, please vote and give feedback if there is a problem. Thanks.

; Script Name: Ending's LumberHacker
; Author: ending
; Version: 5.2.1
; Client Tested with: 5.0.1c
; EUO version tested with: 1.5 TV 62
; Shard OSI / FS: OSI
; Revision Date: 26Oct05
; Public Release: 28Oct04
; Purpose: Free hand lumberjacking with beetle support


New version should work for pre-ML servers.