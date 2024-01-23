;-----------------------------------------------------------
; Script Name: Alamar's MultiSkill Trainer (with jewelry)
; Authors: Alamar, Artgenos
; Version: 1.41
; Client Tested with: 4.0.5a
; EUO version tested with: 1.42.009A
; Shard: OSI (FS Unsupported)
; Revision Date: 19Oct2004
; Public Release: 15July2004
; Purpose: Trains Multiple Skills Using Jewelry.  See Thread.
;-----------------------------------------------------------

Most of the script has been tested by myself and several guildmates. If you find a problem, please come back here and tell me exactly what happened so I can fix it.

Preface:
This script is designed to take you from 70+ to GM (or higher) It should be completely pre-setup, and should require very little intervention on your part until the script has completed. There are several sections that I have not fully tested yet, but I'm working on new characters so I can.

What This Script Does: This script will help raise skills from 70+ to GM (75 to 105, 80 to 110, etc). It finds your gain spot exactly like 8x8'ing, but instead of moving, it stays put when it finds a gain. It stays there until the gains stop or you cap out. This works best if your caps are between 105 and 120, but will work to GM on most skills. Please note that if you get your GGS, you won't get a 2nd on the same spot, and will continue to work the skill. This is NORMAL. Sometimes it takes as much as 2 hours to get your first gain. This is also NORMAL. There is nothing that anyone can do about the server being stingy with gains.

What You Need: You have to have at LEAST 70 base skill to use this script. Period. You must also have enough skill jewelry to get your displayed skill to your cap. i.e., with 70 skill, you need to have +30 total skill jewelry for a GM cap.

If you don't understand exactly what I mean, please post your current REAL skill, your current cap, and the highest skill jewelry pieces you have. I'll tell you if this will work for you or not.

If you dont' have the required base skill or the jewelry to cap, use Mytilus' Magery Trainer, Hellspawn's 8x8, or Dilbert's Corsair. They're all good scripts.

You also need a boat. Put it in the water over between Moonglow and the East Serverline. The antiblock will NOT go around continents.

To start: Download the script. Get your jewelry on. Get on the boat. Hit play. Choose the skill you want to work. Sit back and watch in awe.

Right now, the script DOES NOT search for regs, etc. Have all your stuff together and be ready when you hit start. If the instrument you're using breaks, the script should now choose the next one (v1.2)

As always, feedback is welcome, please remember to come back and vote when you're done!

Revision History


v1.41
Tweaked Eval wait times
Corrected a spot of bad code (Thx Tecmo!)

v1.4
v1.4b : Streamlined lots of things, see thread
v1.4c : Fixed delays for Eval (broken by streamlines in v1.4b)
v1.4d : Added FS for Mage cap under 105

v1.3
Fixed Chiv
Added Music
More boat work
Streamlined several subs (mana, skillgains, etc)

v1.2
Added instrument check
Fixed lots of antiblock problems
Added Necro

v1.1
Updated wait timer between Eval casting.
Updated antiblock
Fixed mishandled subs, lengthened casting timer again

v1.0
Original Release, contains subs for Magery, Eval, Peace

Future Upgrades:
- Add Med, others as I get time.
- Add a counter on each skill (so you can see how long it took to get your gain)
- Misc cleanup due to serverlines sucking on OSI shards.

Important Notes:

I do not support UMing. Your boat may get stuck. My antiblock is only provided to get you around most simple spots. I fully expect you to be there to move if your boat really gets stuck.

DO NOT use a -magery item when working magery. All of these skills need you to have your displayed and cap skill the same. All of these skillwork subs will work as far as 40 points away from your cap, providing you have the jewelry for it. I know not everyone has a +40 magery set, but I do have a +27 set. So I can use this skill from 73 to GM, eat my 120 Magery PS, and goto 120 on two spots.

I hear anecdotal evidence supports that you should have a pet on your boat when you're working peacing. If you think this is true, dismount your horse when you work the skill. I personally noticed no difference.

I have seen several cases in my testing where you could work several skills on the same spot, i.e., Cap magery, then change jewelry and cap eval on the same spot, then change again to cap Meditation on the same spot still. So make sure you have all your goodies with you to cap as many skills as you can.