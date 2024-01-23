Mytilus Freeshard Magery Trainer

After many people have asked how to modify my magery script in order to use it on a freeshard I have done some modifications for freeshard functionality. I was simply going to change my script to work for both, but whispered boat commands dont work on many freeshards, and I really like this feature as it is much less obvious that you are macroing when you dont see the spamming of "forward one" over and over. I have also changed all of the spells to "target self" type spells which negates the target tillerman problem of freeshards. It casts paralyze on yourself which kind of sucks but there is no other spell that will work for that spell circle. You can however use a mage wand to bypass that spell circle if you wish (wand will drop you down to the lower circle then when you get back to paralyze with the wand remove the wand until you clear it again).


IMPORTANT: As with my OSI magery trainer you may need to adjust the spell values those can be adjusted here

;Minimum skill that each spell will be cast (you can adjust these as necessary)
set %cure 125
set %bless 250  
set %gheal 450  
set %paralyze 600  
set %invis 740  
set %massdispel 850  
set %earthquake 960


ALSO IMPORTANT: I don't normally play freeshards and this may or may not work. I have not tested this at all but it should work on most freeshards. If for some reason you have trouble or problems with this script please post your problems in the thread and I will address them accordingly. I ask that if you do have trouble to please not rate this until I have a chance to fix the problems. Thank you and enjoy


;==================================
; Script Name:   Mytilus Freeshard Magery Trainer
; Author: Mytilus
; Version: 1.00
; Client Tested with: 4.0.4b
; EUO version tested with: 1.42 [build 0098]
; Shard OSI / FS: FS
; Revision Date: 10/01/04
; Public Release: 10/01/04
; Global Variables Used:
; Purpose: 8x8 Magery with antiblock, slow forward to find gains, for freeshards
;==================================


If you have trouble downloading this script you will need to right click the download link and click "save target as". This is a problem due to Windows XP service pack 2.