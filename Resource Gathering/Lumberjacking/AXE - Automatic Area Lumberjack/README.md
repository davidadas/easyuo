AXE Automatic Area & Recall Lumberjack Version 1.24


AXE is a fully automatic Lumberjack you can use for recall Lumberjacking and / or Area Lumberjacking.

Image
AXE Status Window...


Features:

- No rails to set up -> just mark runes in promising areas
- Easy to use Graphical setup (See pictures below)
- Supports bank / house storage
- Supports bag of sending
- Cuts all wood types if carpentry skill is high enough
- Can even configure for single wood types to be cut or not
- Built in Logs2Boards function if you have carpentry on other char or account
- Stores all new resources as well
- All types of recalling supported - LRC Awareness
- Support for (must be bonded) pack horses, pack llamas and giant beetles (may be unbonded as well)

Preparation (most of it only has to be done once):

Important: turn off all skill increase messages cause the script is unable to see system messages otherwise!
Also important: UsingUOA you should turn off stacking of resources or not use uoa anyway you do not need it for this script
Even more important: Do not have any "normal" bags in your pack or bank/secure as they have same item type as Bag of sending
Attention: Do not use the "DO NOT COLOR" option from the carpentry menu, this will produce unusable boards (in my opinion) and it will screw statistics as well...

1. Mark up to 15 runes to areas with lots of trees as close as possible, make sure there are no big obstacles like houses (small houses are ok)

2. Mark a rune at an "always working" bank spot or at the stairs of your house
   If using house put a secure within a reachable distance to the marked spot (remember things not on your stairs do not show when recalling there)

3. Bank / Secure setup:

- Put a container into the root of your secure or bank box, this will hold the boards or logs if storage is not bag of sending
- If recalling with normal magery drop recall regs into bank or secure root or wear a 100% LRC suit
- If recalling with scrolls drop a bunch of scrolls into your bank or secure be sure to have some on your person o at least have your runebook charged)
- If recalling with chival, make sure you have enough tithing points left
- If using bag of sending drop some powder of translocation into your bank or secure, also drop a spare BoS in case it dies
- If you want to make boards drop one or more tinkers tools in your bank or secure

Image
Your bank or secure should look somehow like this...


4. Backpack setup

The script will fetch anything, regs, bag of sending scrolls powder of translocation tinkers tools. I recommend to take the following stuff in the beginning:

- A runebook as previously described - rename the book to AXE for runebook auto sensing
- Some regs or recallscrolls if not using chival or 100% LRC
- Some carpentry tools or a tinkers tool (suficient skill required) if you want to make tools yourself
- If you desire to use a bag of sending have it in your pack (it auto charges and auto fetches powder. You also may want to carry a few powder with you. (If not the script will get it from bank or secure anyway)

OH -> An axe would be great !

Image
Your backpack should look somehow like this...


Start the script and set up according to your preferences:


Image
AXE Setup Window


Storage Section:

- Select your preferred storage method from the drop down menu
- Check "make boards" if you generally want to cut wood to boards
- Check "make planes" to automatically create carpentry tools
- Check "pack animal" if you have a bonded packhorse or pack llama. Beetles do not need to be bonded !


Area Size Section:

- Set the size (in units of 5 tiles) of the area to run.
- Set this to 0 for recall Lumberjacking
- select turbo to disable stats and have an exterem chopping experience



Recalling Section:

- Choose you preferred recall method from the drop down menu
- Set the number of runes in you book
- Check "loop" to begin at the first rune when all runes are done
- Check "100% LRC" if you are using a LRC Suit


Woodtypes Section:

- Check "auto" to let AXE decide what to cut and what not OR Check the wood types you want to cut to boards on the fly. (You still need the skill)
- Use the Logs2Boards button if you just want to cut logs to boards. This is useful if your lumber does not have the carpentry skill. (Still the setting from Woodtypes apply)

Advanced options:

Click the Advanced button to get more control over the scripts internal settings:

Image
AXE Setup Window with advanced settings opened

Small wait: used whenever there is a need for a very small delay
Wait: used as a default wait
Bigwait: delay for actions that are known to take long (like opening paperdoll)
Recallretries: Number of tries when recallin gfails for any reason
Carry this many recall regs: Amount of regs that are restocked
Wait time to move back to last spot after recall: well - Guess you know ;-)
Wait time to move to next tile: Timeout when moving to next unit
Restock Regs if under: Min regs before the script goes and gets some of the bank
Maximum weight: On request this is now edible, still you will not be able to save unless you change it in the code
Cut weight limit: This is used to prevent AXE from cutting small amounts of logs when near weight limit - play with it and figure yourself ;-)
LPC: got a fast machine ? This affects performace - At your own risk !




After saving your settings click Next and the script will help you select your packhorse, runebook, dropbox and such.

Now sit back and watch the logs and other resources fly in !

A word on Rating

I have put a lot of spare time into this script. please give me a fair rating !

- If you use it rate it !
- Do not rate this script bad just because you have a problem, post your problem here and give me a chance to fix it
- Be patient I have other scripts to finish also !


One last word:

I you like this and really use it often, please donate to Alexandria the official EasyUO freeshard !


MANY MANY THANKS TO SORROWMASTER AND CHIATT FOR LOTS HOURS OF TESTING THIS !!!

Code:
;======================================================================
; Script Name:                  AXE.TXT
; Author:                       Shadowknight
; Version:                      1.24
; Client Tested with:           5.0.1a Patch 22
; EUO version tested with:      1.5 0064
; Shard OSI / FS:               OSI only
; Revision Date:                2005/10/26
; Public Release:   2005/10/12
; Global Variables Used:        *AXE (uses KALXML Global Storage now)
; Purpose:                      Area based Lumberjack and much more
;======================================================================
