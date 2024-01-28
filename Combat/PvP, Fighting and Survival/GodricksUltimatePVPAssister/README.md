```
Code:
;========================================
; Script Name: GodricksPvPAssister.txt
; Author: Godrick
; Version: 5.0
; Client Tested with: 7.0.15.1
; EUO version tested with: 1_5_196
; Shard OSI / FS: FS Alexandria; FS UODemise
; Revision Date: 0507/12
; Public Release: 091209
; Purpose: Automatically applies bandages, can manually/automatically
; use cure, heal, refresh, agility, and strength potions, provides weapon swapping assistance,
; and automatically re-arms weapon when disarmed. Easily the fastest, most stable, and most all-encompassing pot
; chugging script in the PSL. Perfect for PvP.
;=========================================
```

Image Image Image Image

Easily the fastest chugging script on the boards as well as having Automated Bandaids

Features:
In Automatic Mode the script does not require hotkeys.

The script will not UNHIDE you.

The script automatically applies aids if you have them.

The script can auto Cure, Heal, and Refresh at a health or stamina point that the user thinks is comfortable.

The script can support multiple weapon sets for weapon-switching users.

The script will auto re-arm users who have been disarmed by opponents.

If inflicted with a lethal poison the script will cure it as quickly as possible, rather than constantly re-arming and disarming the script will drink cure pots to remove.

If you use razor make sure to disable the auto Unequip hands before chugging a potion. As well as turn off Auto-Queue Delayed actions. This may cause problems.

USING RAZOR FOR BANDAGES
There is a variable:
set %RazorBandageKey No

Simply setup the Bandageself macro in Razor to an assigned key and then also input that same key in place of the No. That simple.

FAQ
1) I started the script and the buttons are turned "ON" but it won't chug!
   A) Click the button labeled "Potioninfo" and setup the Potion config.

2) I'm Mortalled but it won't use an apple!
   A) The script is hardcoded to only use an apple when your character is half health + 20 HP. Line 196 can be changed to the value you want to use an apple at by changing #hits < #maxhits / 2 + 20 and replacing it with something like #hits < 30, or #hits < 99. I don't let the user set it because I feel this is the best possible value to automatically use an apple.

3) How do I get the script to recognize potions in a bag in my pack?
   A) Click the small button in between the hour glass looking design. It won't save your bag. Every time you load the script the script will default back to checking the backpackID, so you'll need to set it each time.

4) My shard uses the [bs command to apply bandages. How do I get it to work?
   A) There is a question a few lines down in the script change #false to #true.

Thanks!

Feedback is always encouraged! Have fun!

UPLOADED VERSION 4.0
V 4.0 1/23/11- Rewritten from the ground up to be more stable/efficient.
V 4.0 1/23/11- New Menu system for handling multiple weaponsets/potion information.
V 4.0 1/23/11- Removed looting feature.
V 4.1 1/30/11- Added a button to set a potionbag other than the main backpack.
V 4.2 2/14/11- Adjusted Wait times after some stress tests.
V 4.2 2/14/11- Put in a Safety reset sub for Strength/Dexterity Monitor
V 4.2 2/14/11- Fixed a minor Weaponconfig Menu Refresh issue
V 4.2 2/14/11- Added Default Potion Settings for First time use.
V 4.3 6/07/11- Added Header to Godrick's PvP Helper
V 4.3 6/07/11- Now counts multiple stacks of apples
V 4.3 6/07/11- Modified Bandage vs Potion priority in favor of bandages.
V 4.3 6/07/11- Added Bandage/Potion checks in key places of the script to improve performance
V 4.3 6/07/11- Updated Journal Scanning on Mortal
V 4.3 6/07/11- Added Sysmessages
V 4.3 6/07/11- Moved Hotkey checks to secondary script to improve response times.
V 4.4 10/23/11- I had an if statement somewhere that was causing the mainloop to rarely check the menustatus.
V 4.5 11/21/11- I added a Razor BandageHotkey Support.
V 4.6 12/01/11- IMPORTANT: People can no longer spam "You have been mortally wounded" to disable the script. This update is in the PvP Assister Helper so you'll need to redownload both scripts.
V 4.6 12/01/11- Fixed a moveitem bug that may have caused some unexpected item dropping after death.

V 5.0 5/07/12 - Now uses bandages if chain chugging cure potions.
V 5.0 5/07/12 - Weapon Set menu overhauled to have up to 10 weapon sets.
V 5.0 5/07/12 - Fixed potion queuing issue that caused potions to not queue.
V 5.0 5/07/12 - Extra failsafes added to potion chugging
V 5.0 5/07/12 - Autorearming will now include the shield
V 5.0 5/07/12 - Weapon Swapping overhauled to be more reliable/efficient.
V 5.0 5/07/12 - Bandages no longer work off a wait timer to adjust for lag and minor timing issues.
V 5.0 5/07/12 - Added Party Support for auto accepting parties
V 5.0 5/07/12 - Added Cursor Check to potions (will no longer cancel cursor). This used to be a part of the script but was taken out for survival reasons. Regardless, it was re-added.
V 5.0 5/07/12 - Removed menu update delay
V 5.0 5/07/12 - Status will return to Idle after Resurrection




DOWNLOAD AND RUN BOTH AT THE SAME TIME