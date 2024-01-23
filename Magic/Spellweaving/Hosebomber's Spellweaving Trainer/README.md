;======================================================
; Script Name: Hosebomber's Spellweaving Trainer
; Author: Hosebomber
; Version: 1.3
; Client Tested with: 5.0.1d
; EUO version tested with: 1.5 (test ver 64)
; Shard OSI / FS: OSI
; Revision Date: 11-10-05
; Public Release: 11-10-05
; Global Variables Used: N/A
; Purpose: Train the Spellweaving skill using the 8x8 method
;          from 0 - 120 (skillcap)
; Props to nilmer - used his "Everything property sub"
;======================================================


THIS SCRIPT REQUIRES THE ABILITY TO CAST SUMMON FEY.

You must have the spells Nature's Fury, Reaper Form, Summon Fey, Essence of Wind, Wild Fire, and Word of Death

Directions:
Place yourself on a boat that is placed in the ocean, in a spot that you can sail around the world without hitting land.
Press Play.
Answer any questions the script may ask you.

There is only 1 user variable that may be set (this is not needed and 100% optional)

; ======================================================
; ----------------- User Defined Variables -------------
; ======================================================
; Do you wish to use active meditation? (requires 60.0 Meditation skill)
;    set this to #false if you do not wish to activly meditate.
set %med #true


Version 1.0
What it does:
1. Trains Spellweaving using the approprate spell for your skill level.
2. Auto sets user screen. (opens paperdoll, status bar, & backpack)
3. Auto insures boat key if not already insured.
4. Auto refreshes boat.
5. Auto checks facet.
6. Auto calculates LMC, LRC, and checks durability of armor.
7. Auto adjust spell casting max level if you have eaten a powerscroll.
8. Auto halts script if you lose the ability to heal yourself.
9. Auto halts script if you reach your skill cap.
10. Uses the most effective means to gain skill.
11. Auto unblocks the boat if you run into other boats.
    Version 1.1
    Added Talisman to list of armor (for lmc check)
    Added Menu display.
    Added Fix for unblock during gain run.
    Version 1.2
    Fixed a typo with the spelling of ginseng.
    Attempted fix at sticking in unguilding loop.
    Version 1.21
    Fixed the typo in heal timer.
    Fixed the bandaid timer for times between *.1 and *.4 (caused to never heal with aids)
    Version: 1.3
    Fixed the typo in %horse_types.
    Fixed issue with not being able to cast on horse.
    Fixed issue with getting stuck in boat key insure loop.
    This may have been something with them allowing to rename keys again.

As always... If you use it, RATE IT!