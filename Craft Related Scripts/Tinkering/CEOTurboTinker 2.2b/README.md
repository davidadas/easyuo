Like my scripts? Consider a Paypal donation. Click here for more info.

(This script will not work for Freeshards using older EasyUO versions or Freeshards
with a different menu layout then the standard OSI one. Sorry.) Pre-AOS freeshard? Forget it, no event property. Most of the TurboScripts probably won't do so well.


The client must be set to english. This is a requirement for any script that examines #property or #journal for specific phrases.

Choosing a training/skill table: If you are on a RunUO/Freeshard ONLY use the tables with RunUO in their names. Conversely, these tables WILL NOT work for an EA shard. IE, if you're on an EA shard, use any table EXCEPT the RunUO ones. Understand? When you select a training table, the script adjusts for that kind of shard, using a table not designed for your shard will cause the script to have problems.

Also note for freeshards, if your shard uses a keyring and pushes heating stands to the 7th button on the menu ONLY use RUNUO2.

If you need to modify stuff for freeshards (button positions most likely) see this post: HERE. Do not post any further freeshard issues, it's just not supported and you're on your own.

This is my third script in the "Turbo" line of scripts.

Here's the feature list:
You can use at a bank or in your house. (Auto-detects)
One-time setup, it'll reopen your bank/secure/resource bags the next time you run it without doing any file saving.
Remembers setup and lots of stats using the CEO*Filesystem.
If you have hiding skill it'll hide you (and rehide you if needed).
A very nice stats/progress screen (see below)
And of course like my other Turbo script, it's fast!


If using it at a bank, you need to be within 12 paces of an endless trash dumpster. At 90-100 tinkering, the script makes heating stands and will walk your character to the trash dumpster, dump them all and walk back to your bank spot and reopen your resources bag. If training at a house, make sure the trash barrel can be opened from where you're training. Usually 2 paces is fine.

Note: If training at a bank, please pick a bank that has a dumpster away from other chests. Other chests of the same type may cause it to walk to the wrong place. There's some logic to try and find the closest chest and one on the same Z axis, there are a few banks with multiple chests and some on the roof, but I suggest staying away from those banks and find one with one trash chest within a few paces of a place you can stand and reliably open your bank box all the time. There are a few banks where the chest is right at the bank wall so you don't even have to move, that's the best place to train. I've added about 6 types of chests, I'm sure there are others. DO NOT post telling me it can't find the dumpster. It will be because it doesn't know the type (or you're too far away). Find the dumpster type and add it to this line in the user setup section yourself:

; These are the types for the bank dumpsters. There may be more so I've included
; them in this section.
set %bankgarbage IKF_BUD_JIF_HIF_IIF_KIF


Finding the type of an item is one of the most basic things you should know before using EasyUO. This utility will help you do that:

Ma$$acre's Item Identifier

Although it's even easier then that with some EasyUO knowledge. Feel free to PM me with other types you find and I'll be more then happy to add them to later updates.

Estimated Resource/Stats
Time to GM (from 25-100): 10-12 hours
Ingots needed: 35k
Tinker kits used: 120
(make them on the fly, after all you are tinkering! As you get higher, you'll make exceptional ones with lots of charges)

Status Window

Image

Skill Chart

Image


I'm not going to detail the instructions, everything you need (ignoring tailor specific comments) can be found in the CEOTurboTailor thread.
If you're unsure about anything, read the CEOTurboTailor setup instructions, except for tailoring stuff, it's pretty much the same setup/requirements for this one. Too much to retype and I don't think many people read them anyways. The setup of this script is pretty self-guiding and only needs to be done once.

As usual, please post your comments and problems in this thread. I'd greatly appreciate it if you drop a post here when you've skillcapped your character and tell me your statistics and how well the script performed. Rate the script too so that others will benefit from your experience with this script.

Note, if you are having problems and want to post about it, help me out by including this information in your first post: EasyUO version with build, Client Version, OSI/FS, your current skillcap, current tinkering skill, and characters stats.

Thanks to the following beta testers:
Codenewb, lazuris, and Victor Lacroix.
Special thanks to Victor Lacroix for providing me with my initial supply of ingots to get started.

Thank you and enjoy!
\":wav:\"


;-----------------------------------------------------------
; Script Name: CEOTurboTinker
; Author: CEO
; Version: 2.1
; Client Tested with: 7.0.0.4
; EUO version tested with: 1.5_154
; Shard OSI / FS: OSI
; Revision Date: 100309
; Public Release: 032804
; Purpose: Trains Tinkering to 100.
;-------------------------------------------------------------

Like my scripts? Consider a Paypal donation. Click here for more info.

The script is in the attachment below that says CEOTurboTinker.zip. Click on the download button to get it.
Note: The archive will always contain the latest version.

This script is copyright by CEO under the CEO Public License (CPL) agreement.