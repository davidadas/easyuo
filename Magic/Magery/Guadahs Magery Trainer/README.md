; ; ############################################
; Script Name: Guadahs Magery Trainer 2.0.8
; Author: Guadah
; Version: 2.0.8
; Client Tested with: EA 7.0.16.1 (Patch 53)
; EUO version tested with: 1.5 Version 198
; Shard OSI / FS: OSI Servers
; Revision Date: 08-12-2011
; Public Release: 10-08-2007
; Purpose: To Train Magery from 25.0 to 120.0
; ############################################


Title: Guadah's Magery Trainer

Current Version: v2.0.8

Skill(s) Trained:
* Magery
* Meditation (secondary)
* Evaluating Intelligence (secondary)

Set-up Difficulty: Minimal

Comments:
This script is designed to count your Lower Reagent Cost, Lower Mana Cost, Faster Casting & Fast Cast Recovery. In the early stages I had a smart casting built in that would auto adjust after you started, now in the later stages the script will cast at the top maximum speed depending on your Faster Casting & Fast Cast Recovery. LRC & LMC do not matter for the script performance anymore, but I still count and display them for cosmetics.

Recomendations: Use a 100% Lower Reagent Suit with 40% Lower Mana Cost & 3-6 Casting (Use a Magic Wand with -27 or higher, which will lower you to 2-6 Casting). If you can get Mana Regeneration of at least 8 on your suit, you will have the best results possible during training.

Menu Image:
Image

Updates:
08-12-2011 v2.0.8
* Adjusted how meditation is called.
* Corrected FCR Delays
* Modified code
  07-13-2008 v2.0.7
* Reformatted the technique and codework in which Suit Statistics are Calculated
* Changed Menu Look
* Added in Spell Name during Casting Display in Status
* Changed Menu Update Codework
* Added Mana Regeneration Statistic to Menu
* Calculated Suit Statistics prior to clicking Play for user benefit
* Decreased size of script by over 500 Lines!
* Removed the Journal Scan to check for low mana, and added in Math to calculate amount of mana required, and a check to see if minimal amount of mana is available.
* Adjusted Meditation Sub to monitor pause and total time macro'ing to calculate during your time meditating.
  Corrected issue with casting Invisibility Spell
  07-12-2008 v2.0.6
  Removed Journal Scan to track Mana and when to go to Meditate Sub
  07-11-2008 @ v2.0.5 Beta
  Review Beta Information
  06-09-2008 @ 12:42am
  Update!
  10-08-2007 v 1.22
* Updated to Bob 2.0
* Adjusted Meditation Wait & Re-Meditate if Failed Attempt
* Improved Display of Menu (Eye Candy)
* Added Smart Cast Adjustment for improved Speed in Casting
  10-08-2007 v 1.22
* Improved the Speed of Casting
* Improved the Quality of the Codework
* Fixed an display issue with 'casting spell' section
  10-07-2007 v 1.2.1
* FC FCR LMC & LRC Counter Working
* Menu Updated
  10-07-2007 v 1.1.1
* Updated Script to train Magery Quicker
* Added Display of Currently Casted Spell
* Prep'd Script for Upcoming FC FCR Checking
* Corrected an issue with Skill Check vs Real Skill Check
  10-06-2007 v 1.1.0
* Now Tracks Magery, Meditation & Eval
* Corrected Issue with Skill Tracking
  10-05-2007 v 1.0.0
* Public Release

Image of old version:
Image