Good day all... I've been downloading and using scripts for a while now... but I cant seem to find some of the scripts I want, so I decided to write my own. I've been reading the boards and all the intros and stuff for about 8 hours now, and this is my first script I have written.

Change Log:
* 5/2004 - Initial Release
* 11/16/2004 - Revisiting the script. Added in some user variable for changing loot and weights easier, and fixed some syntax issues for stability.
v1/28/05 - Finally got around to adding some error checking. In the past, any bag would trigger it (bags of sending and regular bags have same itemtype). It should ONLY work with bags of sending now, ignoring all other bags.
* 6/27/05 - Version 1.3 - Updated the script to find loot in main pack OR in a user defined loot pack. Cant beleive that one went unnoticed for so long...
* 8/28/05 - Version 1.4 - Updated the script to open your loot bag when you are using a sub pack as loot bag. Also added a counter to keep track of how much gold you have sent to the bank and how many charges off your Bag of Sending you have used.

COMMENTS OR SUGGESTIONS FOR FURTHER UPDATES? PM ME OR POST THEM HERE! THANKS!
```
Code:
;===================================
; Script Name: Ambrosia's Bag Of Sending Script
; Author: Ambrosia
; Version: 1.4
; Client Tested With: 5.0.0a [patch18]
; EUO version tested with: V1.42.00B0
; OSI / FS :  OSI
; Public Release 5/27/2004
; Edit Release 8/28/05
; Purpose: Automates Sending gold to bank via Bag of Sending.
;===================================
```