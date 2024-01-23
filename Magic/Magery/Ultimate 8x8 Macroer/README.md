;==================================
; Script Name: Ultimate 8*8 Macroer
; Author: Hellspawn
; Version: Final 1.99
; Client Tested with: 4.06a (Patch3)
; EUO version tested with: 1.42.009D
; Shard OSI / FS: OSI
; Revision Date: 25/11/04
; Public Release:
; Purpose: 8x8 multiple skills
;==================================

New Freeshard Version 1.0

Note with new freeversion you only need the In Defiance file No need for the old boatstopper as this isnt 8*8. Enjoy :)

Note : The "Freeshard version" also should work on osi shards as to my knowledge 8*8 has been removed there now. (Although if I were you id goto www.defianceuo.com and start playing there. 10* better than osi and many of the old bugs fixed + many improvements)


New Version 1.99

see version history below for updaes.

Currently trains : Magery, Eval int, Necro, Spirit speak, Chiv, Hide, Stealth, Music, Peace, Heal, Vet, Focus, Med, Anatomy, Bushido & Ninjitsu.

Instructions:

To start macroer

1. Load Uo and get on a boat that is facing NORTH
2. Simply load the main macro into 1 instance of easyuo and load part 2 (called boatstopper.txt) into another instance of easyuo.
3. Start the boatstopper macro 1st and minimize it then start the main macroer, dont minimize it or the menu gets minimized too !
4. Choose the skill you wish to macro, set up any options and press Start
5. Wait till your GM/capped/Eaten by water eles :p

Note: Unlike other 8*8ers this doesnt use an unblocker as such, the boat simply ping pongs up and down the line. This is intentional as I found that sticking to a good gainline once found gave me the best gains.

Important BUSHIDO & NINJITSU info

1. When bushido starts it asks you to target a golem and a uni, this isnt required till your at 97.5 so if you have none target yourself.
2. When you are at 97.5 Bushido you need a Golem, a 100% poison weapon, a Released unicorn, Positive karma, be in felucca & either have a bit of magery / chivalry / a friend to heal uni. If you are using magery poison weapon needs to be spell chaneling.
3. Best to wear a high MR suit, carry a weapon & have 1 - 2 pets (Cats are Ideal) then the macroer will be able to go all the way to your skillcap. If you cant get a cat to the boat use a horsewhich you can ride there.


General Tips

1. Either dont use UOAssist or disable the display of stat/skill changes and container counts as this can interfere with the macroer.
   In general if you have a problem with an easyuo macro dont load assist then retry it.
2. Remove pause keys from both instances of easyuo to avoid accidentaly pausing one or the other. Ive done it before :p
3. Trawl mode is there for a reason Use it - If youve had to stop and come back and you know your on or near a gainspot use trawl mode then it will pick gain up again immediately.
4. The macroer can look will look for gains both north and south. You can set the initial direction on main menu or change direction when macroing by pressing the REVERSE button on the boat menu.
5. To use jewelry method simply cap your skill with jewlelry ie if you have 80 magery and wish to cap it wear +20 or greater jewels. For magery unless your over 100 use -mage weapon method.
6. Magery is the one skill that can be made easier to train by equiping a -Mage weapon. Look out for a -29 spell channeling mage weapon (a wand is ideal) and equip that when your skill is getting higher (50+). Dont use it untill you have atleast the -ve in your magery skill though.
7. A useful tip if you find a good line is to park a boat at each end so you just milk the gainline ;-)
8. Something I observed about gainlines is a gainspot is a gainspot for the skill at a certain level ie. I was on a gainline at 75 magery. I made a note of the location and put jewelry on but couldnt gain there or anywhere near the spot, when I then took jewelry off and put boat back on spot I picked up gainline again. From this in theory if you made a note of x/y coords you got a gain at in a skill you ought to be able to start the gains ther on a different character at the same level of skill ;-)

Version History

new for In Defiance 1.0

1. Ripped out all the boat / 8*8 code
2. Tidied up old menu
3. Thats it.... maybe more to follow :)

new in 1.99
1. Bushido Training over 97.5 in felucca with a golem , a 100% poison damage wep (pref spell channel) and a released uni and positive karma on char your training
2. Updated ninjitsu & bushido to use chooseskill and event macros.

new in 1.98
1. Fixed Bushido issues with counter attack.

new in 1.97
1. Minor jewelry fix
2. Adjusted ninjitsu to do focus till 95.
3. Bushido & Ninjitsu now do all follow me when you start or unpause incase you have pet with you.
4. Jewelry msg now displayed when on jewelry gainspot
5. I Noticed boat sometimes missed to stop on jewel gainspot, it should check back/forward a square now if it gets no gains
6. Button writing nolonger goes green / yellow on boat menu when you press it.
7. Bushido / Ninj check to see if dropping skill is 0. macroer than pauses.
8. Auto log out feature when skill in training reaches cap.
9. Script now Opens and closes ninj / bush books and casts a spell before you start so no need to do it now.
10. Momentum strike removed because no way Ive found to macro it, now sticks with Evasion but 97.5 seems to be the cap with that.

new in 1.96
1. Changed all nested else`s to ifs, code should be more stable now.
2. Success check for death strike - ninjitsu should go all the way now
3. Momentum strike set on 97.5 now
4. New Boatstopper too be sure to download it.

new in 1.95
1. Fixed 8*8 bug where it would not register all gains
2. Added code to stop ninjitsu getting stuck in focus / deathstrike loop
3. Ninjitsu should now also override Activemed once you go above 75 skill.

new in 1.94
1. Ninjitsu now does rat form 20-40 then mirror - 75 - focus -92.5 - deathstrike beyond. From 75 you need a pet and be unguilded in trammel and have a weapon in hand.
2. Added snicker7`s sub to kill off mirror images
3. Focus / deathstrike should now works properly - thanks snicker7
4. Added jewelry option for bushido / ninjitsu (untested as i have none but should work).
5. Altered training info
6. Fixed stealth invis bug (i think)
7. Fixed bug with ninj/bush where %skill wasnt updating properly so it would go on casting wrong spell and not switch to new spell.

new in 1.93
1. Bushido now does confidence till 55 then counter till 75 then evasion
2. Bushido and chiv no longer try to med if you have weapon equiped and your casting counter / conc wep.
3. Added resist to list of skills to drop
4. FIXED BOATSTOPPER - MAKE SURE YOU HAVE V1.93 - 1.9 is bugged on all skills but ninjitsu/bushido

new in 1.92
1. Bushido now does confidence till 60 then counter till 80 then evasion.
2. Ninjitsu now does mirror till 70. above 70 still broke.
3. Fixed bug that crept in so macroer now follows a gainline south again properly

new in 1.91
1. Removed shadowjump from ninjitsu now does mirror to 65 then switches to focus

new in 1.90
1. Added Med , Focus , Anatomy , Bushido & Ninjitsu
2. Also jewelry training available with all but bushido ninjitsu and anatomy
3. About 100 bugs ! :p

new in 1.75
1. Below 30 training for magery/necro/chiv
2. Fixed some server boundary issues
3. Vet now retargets bonded pets if they are killed and ressed

Version 1.7

The original 8*8 that I published just after the release of AOS. It trained 11 skills (Mage,Ev int,Necro,Spirit,Chiv,Hide,Stealth,Music,Peace,Heal & Vet)