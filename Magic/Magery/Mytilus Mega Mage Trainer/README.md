Mytilus Mega Mage Trainer
This has been a work in progress for me for quite a while. When I first saw the new multi-trainers being worked on I pretty much gave up on this script. But after thinking about it a bit more I decided there could still be a place for a simple mage/eval trainer for those people that are easyuo challenged and have trouble figuring out scripts that need several instances of easyuo in order to work properly. Or even those people that would rather just mess with one script. This script will go slow forward and milk both eval and magery runs. It also will toggle between eval and magery mode since recasting on fizzles isn't necessary during an eval run (you will gain eval on fizzles unlike magery). I bought my mage/eval down from 120/120 to test this script and work out the bugs so I hope that everybody enjoys it. This script works best with gm meditation and if you can spare the skill points turning focus skill up will help out big time too. Also try to get a mage lowering wand in order to increase your gains. And last but certainly not least, If you enjoy this script Please take the time to vote for it so it can be approved like the magery script. Thanks for trying this out!

---1.50 Updates--- (3/27/04)
*Script will now automatically locate and configure tillerman for targeting
*Added additional tillerman types to fix some problems with other ships

---2.00 Updates--- (5/04/04)
*Health check added to script
*Script will now re-attempt to meditate if you fail
*Added brand new menu display to keep track of gains with status box for your 8x8 amusement
*Resets tillerman to #ltargetid before every cast so it wont break script if you kill something
*Script only opens status bar if its closed, and will open it again if you close it accidentally
*Script now auto-configures both skillcaps, simply enter a number in place of auto if you would like it to stop sooner
*Script will now stop boat during meditation and restart after if not in a gain run

---2.50 Updates--- (10/21/04)
*Added fix for mage wand bug
*Eval gain on fizzle will not ruin magery run (keep casting til you get mage gain)
*Added Harm and Magic arrow for new chars to start with a mage wand
*Added support for less than 100% lrc (possible to gm with as little as 1% lrc)
*Added CEO's gaincheck sub for casting EQ (no longer mess up by FC jewels)

More updates to come soon as I work on this!!!!

IMPORTANT: The boat antiblock is only designed to move around boats not continents!! Get your boat into 8x8 Alley east of moonglow before starting this script. It is at the far east side of the map where the map wraps around to the other side.

If you find you are succeeding all the time or fizzling all the time and you are not gaining you will need to adjust these values:
;Minimum skill that each spell will be cast (you might need to adjust these as necessary!!!)
set %harm 125
set %fireball 250  
set %lightning 440  
set %paralyze 600  
set %ebolt 740  
set %flamestrike 850  
set %earthquake 960


If you find that the boat seems to go too far after you gain before the boat stops. Or if you get a gain and then the script casts a second time before stopping the boat or moving 8 spaces you will need to adjust this value as stated in the script:
;You may need to adjust this based on your connection.
;Lower if you dont stop the boat right away after getting a gain.
;Increase if script doesn't see gain until you have casted a second time.
set %aftercastwait 15


You may change the number of times you try to recast by changing this value:
;Set number of recast attempts to get gain
set %loopmax 3


One more note... If you find you are getting alot of .1 only gains with no runs you may be playing on a north to south shard rather than south to north. If you aren't gaining for crap and are unsure which way the gain lines run on your shard then try running south.

Please read the instructions and please do not post questions like \"I'm casting but all I do is fizzle what's wrong I think your script is borken\", I have obviously answered that question here, as well as many other common problems. As always thank you for trying my scripts and if you enjoy it please take the time to rate it!!


;==================================
; Script Name:   Mytilus Mega Mage Trainer
; Author: Mytilus
; Version: 2.50
; Client Tested with: 4.0.5a
; EUO version tested with: 1.42 [build 009A]
; Shard OSI / FS: OSI
; Revision Date: 10/21/04
; Public Release: 3/17/04
; Global Variables Used:
; Purpose: 8x8 Magery and Eval with antiblock, slow forward to find gains.
;==================================



If you have trouble downloading this script please right click and click "save target as". This is a problem due to service pack 2.