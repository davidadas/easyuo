---------------------------------
Edit by Orngrimm:

Find info on script-abandonment @ viewtopic.php?f=3&t=53061

As the autor didnt visit for >4 years (Sun Aug 19, 2012 21:22 as of 16.Jan2017)
i declare this script as
ABANDONED

Whoever wants to take over the script may do so by:
- Posting an updated version in an own thread
- PM me the URL of this thread here and the new thread

End Edit
---------------------------------

***I am no longer actively playing UO. I do try to check my current PSL threads, so feel free to post. I try to support my scripts as much as time permits.***

Well here is my first script. I hope you guys can get some use out of it. This script will train a character from 0 - 120 Spellweaving without moving.

Quick Note:
1) There is a bug with casting Word of Death on tamed creatures while in a private house. The bug will cause you to lose access to house items and occasionally will ban you from house temporarily. Going to an inn and logging out will fix this problem. This is not an error in the script as it will occur when casting WoD without the script also.
   EDIT***This bug seems to have been fixed***

2) The script works best when unguilded and in TRAMMEL. There is a check for both built in. Also when you get to 92.0, the script will start casting WoD on your horse(required). As long as your are unguilded and in TRAMMEL, you will not do damage to the horse and the horse will not damage you. However, horse may still interrupt your spells on occasion. For best results, place your horse so that it cannot get to you.(i.e. ban from your house or place in a pen of some kind)

;==================================
; Script Name: ScripterBob's Legendary Arcanist Trainer
; Author: ScripterBob
; Version: 6.2
; Client Tested with: 5.0.1j
; EUO version tested with: 1.5.69
; Shard OSI / FS:  OSI
; Revision Date: 9/7/06
; Public Release: 3/20/06
; Global Variables Used:
; Purpose: Train spellweaving from 0-120 without moving.
;==================================


Credits
I incorporated two really great subs into this script in order to clean up the pixie release process.
Hosebomber - Pixie release sub
Nilmer - Everything Property sub(Also used to calculate FCR)

Thank you both!

Updates:
5.01 - Fixed spamming issue with releasing pixies...Thanks Hosebomber!
5.02 - Fixed issue with horse falling out of guard mode.
6.00 - Cleaned up the menu, with some suggestions from Hosebomber.
6.01 - Fixed typo in meditation sub
6.02 - As requested, Added calculation for FCR to speed up script if equipped
6.2 - Added ability to use non-horse pets

If you download this script then please rate!