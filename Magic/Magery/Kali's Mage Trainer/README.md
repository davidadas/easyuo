This is my first script that I've ever submitted so please feel free to give me any criticisms or suggestions that you may have.

Since the end of 8x8 I've been looking for a simple script to train magery in my house. I gave up and made a reliable (as far as I've found) script to train magery from 13-120. If you want to stop before you'll have to set %maxskill to what ever you want after I initialize the variable. This script is well ogranized, the main loop is 5 lines, (4 functions and a wait) with very well written subs. No difficult set up, load script (edit recoverytime if you want, default will work), press play, target one item. Then very fast, effecient, and reliable training of magery commences!

What You Need!

1. 100% LRC! It's a must, I did not script reg checks into this program
2. At least 15 skill (just buy 40 from new haven :) )
3. A spell book with harm, Fireball, Lightning, Paralyze, Ebolt, FlameStrike, Earthquake.
4. A valid target (I used a locked down sword in my house) to dump on
5. Set %RecoverTime 30 will need to be adjusted to find the best for your recoverytime. I used 10 with 5FCR and 30 with 0FCR.

Suggested:
1. 2 Faster Casting
2. 6 Faster Cast Recovery
3. 40% Lower Mana Cost
4. As much mana regen as you can wear
5. At high levels, might help to hold a magic wand with -20+ skill. Saves Med time.

My Conditions and Results
100% LRC, 1 FC, 5 FCR, GM Focus/Med (only because I'm training do I have gm focus) and I was in lich form ( Necro skill that gives mad mana regen buffs).
Don't mind the time, I had a lot of debugging to do and infinite loops to be caught in :) 21 Hours, 45.1 - 100.

Future Plans
If asked for I'd be willing to script this into it and some I just might do on my own.
1. Make it a more versatile mage trainer. Select what skills to train Magery/Necro/Med/SS/Eval/Weaving. For instance, if you train magery to 120 but your eval is only 117, don't quit casting until you make that 120 mark.
2. Work with regs.
3. Autocalculate delay times for Suit FCR.
4. Auto find dump target.
5. Menu Changes if anyone things there is something they'd like on it.

v1.1:
Added code to improve stability


;==================================
; Script Name:   Kali's Mage Trainer
; Author: KaliofLS
; Version: 1.1
; Client Tested with: 7.0.2.1
; EUO version tested with: 1.5 v.156
; Shard OSI / FS: OSI
; Revision Date: 03/19/13
; Public Release: 11/10/09
; Global Variables Used: *51 with CEOFilesystem
; Purpose: Magery in static location.
;==================================