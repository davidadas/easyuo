;==================================
; Script Name:  LeeCH's Inscription Trainer
; Author: LeeCH
; Version: 3.0a
; Client Tested with: 4.0.9b
; EUO version tested with: V1.42.00A5
; Shard : OSI ; RunUO
; Purpose: Train Inscription to GM
;==================================


Image


\":arrow:\" Quick Start Guide
Usage Instructions:
This script requires a secure container, and a plain brown back pack INSIDE the secure. Place all reagents, scrolls, and scribes pens in the TOP LAYER of the secure container. You may use your bank box in place of a secure container. Simply make sure your bank box is arranged similar to the secured chest below.

Image

Click for Larger Pic


Once you have set-up your containers. Start the script. You will be prompted via the menu (see above) to open either your secure container, or bank box. The script will intelligently determine which option you choose throughout the usage. After you open your secure (or bankbox) you will be given a targeting cursor, and asked to click on your scroll bag. (The brown bag you put inside your secure or bankbox) If you try to use your secure, (or bank box) the scroll will fail to drop when it moves them. This will hang the script, and COULD cause your client to crash.

\":idea:\" On a side note, you should really try to make sure that your main back pack is empty, or as close to it as you can get. The variable for the amount of resources to gather is hardcoded (see below).

That's it. The script should be off and running. If it's not, follow this simple checklist:

\":?:\" 1.)Do I have enough of these items in my secure?
- Blank scrolls
- Regents for the scroll I am making
- Scribes pens
  The menu will display a warning if you are out of one of these.

\":?:\" 2.)Is the container I am using SECURE or locked down? It must be SECURE.

\":?:\" 3.)Do I have a plain brown back pack in my resource container or bank box? If you do not, the script will not function well, or at all.

\":?:\" 4.)Am I browsing the internet or doing something else while this script is running? This can lead to misclicks, and possibly even drop resources or made scrolls on the floor. (Worse yet, on the ground at the bank)

This script CAN be modified via the \"lag adjust\" section at the top. Does this mean you HAVE to modify it? NO. But you may, if you think something is too fast, or too slow for your connection.

\":arrow:\" Fine tuning instructions
Description of Lag Adjustments:
;************************************
;Lag adjustments and Fine tuning
;************************************
set %delay 25
set %drag 25
set %makedelay 50  
set %manafail 205
set %manapass 205
set %maxmana #maxmana ; change this to the most mana you want


Delay is the basic delays for the script. Modifying this IS universal and will cause the script to run slower on MOST tasks.

Drag is the delay for dragging items like scrolls or regs, too and from your main pack. Increase it to wait longer, decrease it to wait less time.

Makedelay is the amount of time it waits between clicks. I do NOT recommend changing this, unless you have a CLUE of what you are doing.

Manafail and Manapass were added by request. When the script meditates, it will wait the length of time specified by manafail, if it fails. Just the opposite is true of mana pass.

Maxmana is used incase you decide that you do not want the script to wait for a full mana recharge. This value could be modified as such:

set %maxmana 90

\":arrow:\" Resource Amounts and Weight Problems
Some folks have been concerned about being overweight when the script is running. The truth is, the items will not fall to the ground so long as you do not go over 425 stones. If you find you are going over this, remove some items from your backpack, or try setting this line:

;********************************
;Amount of Resources to grab
;********************************
set %amount 200


to a lesser amount. I COULD base this on max weight of the char, but I see no need as it would DRASTICALLY reduce the efficency of the script.


:arrow: Special Instructions
Titlebar and System message instructions are BOTH DISABLED by default now. However, if you still want to use the event system message setup instructions, here's the instructions for it.

In order to see the system messages, you need to allow it in Easyuo.
Go to OPTIONS: CONFIGURATION : ENABLE EVENT SYSTEM MESSAGE.

:arrow: Special Thanks:
To everyone who has bothered to post and give me feed back. You shape the script, and make it what it is.


:!: Changelog:
**Update**
Modified for mana on 8th circle. Also sped up setup time by about 30%. Only deposits scrolls when getting more resources, period. Reduced default mana timers to match default meditation speed.

**Update**
Added a weight check for moving made scrolls. Should combat the drop.WARNING! If you are overweight before you begin, it may drop scrolls on every single pass.

**Update**
Modified the skill checks and seperated the subs better. No longer spends so much time putting away made scrolls, thus, optimizing for speed.

**Update**
Spelling error :/ Repaired now. Bank works again.

**Update**
Up to version 2.0 now. Includes a semi-nifty menu for status reporting. Status bar reporting has been disabled by default now.

**Update**
Added Mana tweaks. Adjusted timings.

**Update**
Bug fixes and timing tweaks.

**Update**
The bank box is now an option for your secure container. Simply say bank, instead of opening your secure container. From there on out if the secure container is not found, it will attempt to open your bank box instead. I also modified some of the gump waits. A new mana system is now in place that should be more effective.

**Update**
Modified the click locations so that they are no longer "static" they will be based on the location of the crafting gump.

**Update**
MASSIVE amount of fixes and speed changes. Tested with Alexandria as well.

**Update**
Now updated to 1.1. Made some lag adjustments, removed checks for proper containers chose, and added code for upcoming LCC.

**Update**
Apparently, the target cursor wasn't clearing after choosing the containers. Added KEY ESC to combat this. Should work smoother.

Also, please remember that you REALLY need 50-100 intellegence for this script to run at optimum speed. If you find that it is trying to meditate too quickly, change the line %mana for the scroll type you are working on