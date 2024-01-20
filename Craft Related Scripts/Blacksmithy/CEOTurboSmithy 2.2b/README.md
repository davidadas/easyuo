Like my scripts? Consider a Paypal donation. Click here for more info.

(This script will not work for Freeshards using older EasyUO versions. It is now compatible with most RunUO shards *if* you choose a RunUO training method.

The client must be set to english. This is a requirement for any script that examines #property or #journal for specific phrases.

Choosing a training/skill table: If you are on a RunUO/Freeshard ONLY use the tables with RunUO in their names. Conversely, these tables WILL NOT work for an EA shard. IE, if you're on an EA shard, use any table EXCEPT the RunUO ones. Understand? When you select a training table, the script adjusts for that kind of shard, using a table not designed for your shard will cause the script to have problems.

If you need to modify stuff for freeshards (button positions most likely) see this post: HERE. Do not post any further freeshard issues, it's just not supported and you're on your own.

This is my fourth script in the "Turbo" line of scripts.

Here's the feature list:
You can use at a bank or in your house. (Auto-detects).
If at a bank, you can use recall/sacred journey or rails to a forge.
If using rail/recalls you can have a packy following you. (Requires some EUO knowledge/learning to setup, NOT SUPPORTED otherwise).
One-time setup, it'll reopen your bank/secure/resource bags the next time you run it without doing any file saving.
Remembers setup and lots of stats using the CEO*Filesystem.
If you have hiding skill it'll hide you (and rehide you if needed).
A very nice stats/progress screen (see below)
And of course like my other Turbo script, it's fast!
Estimated Resource/Stats
Time to GM (from 25-100): 10-12 hours
Ingots needed: 60k-100k depending on mining skill
Tongs used: 100-120 (all exceptional, 2-3x more if not)

Status Window

Image

Skill Chart - 14 Different training methods + 2 user defined!

Image
You can define your own training method by creating a file called smithy1.txt or smithy2.txt in your scripts directory. This can be very handy for freeshard users with menu items in different positions.

Sample smithy1.txt file
set %skillTableSize 3
set %desc1 daggers
set %needed1 3
set %product1 TSF
set %category1 5
set %selection1 5
set %nextpage1 0
set %high1 440
;
set %desc2 Short_Spears
set %needed2 6
set %product2 XRH
set %category2 7
set %selection2 7
set %nextpage2 0
set %high2 830
;
set %desc3 Plate_Gorgets
set %needed3 10
set %product3 NSH
set %category3 2
set %selection3 10
set %nextpage3 0
set %high3 1000
;
%skillTableSize is the number of items in the file. In this case 3.

Desc: The name of the item to make, all stats recorded are based on the name.
Needed: The number of ingots required to make the item
product: This is the item typeof what is made.
category: How far down to click the FIRST click position in the makefirstitem sub for the buttons on the far left.
selection: How far down to click the SECOND click position in the makefirstitem sub for the 2nd column of buttons.
nextpage: Will almost always be 0. Only needed if the item you're making is on a multipage display. I don't think there are any in Smithy.
high: This is used to determine when to switch to the next skill. Set this to the value of skill level to make this. Skill is in 10ths. IE. Skill level 853 = 85.3, 1000 = GM.
(category/selection both count from the top-down the button number to click)

Using the example smithy1.txt file above, the script would train daggers from 25-44, short spears from 44.1-83.0, and then plate gorgets from 83.1 - 100.

(Alternate Methods)
Click HERE for another alternate method from 25-120 posted by Ura Thayne.
Click HERE for another alternate method from 25-GM posted by FunkyFF.
Click HERE for another alternate method that does Circlets/Royal Circlets (UOML) from IDontCheat.

Another alternate method:
Gadabout_Guy wrote:
Not my work, but I thought I would post a corrected Smithy1.txt for the newer gump.

It's based on using Circlets, Royal Circlets, Plate Hiro Sade & Battle Kuboto's at the higher levels.
It's also fairly aggressive. It switches when the next item in the list is around a 50% failure. It's a fast gainer but eats ingots.

Click HERE for another alternate method from 25-GM posted by Gadabout_Guy.

----------------------------
; Setup Instructions:
;
; 1. Start CEOTurboSmithy
; 2. Follow the step-by-step setup.
; 3. Identify Secure (or it'll use your bankbox automatically)
; 4. Identify Resource container. MUST be inside your Secure or bankbox!
;               Make sure to have all necessary ingots/tools in your resource container.
;               NOTE: ANY opened bag with resources will be used, the resource
;                               container is also used to drop left over tinkering stuff.
;               The script automatically learns your bank/secure/resources setup using
;               the CEO*filesystem. To reset these, start the script away from your resource
;               container and away from the bank.
; Note: Your paperdoll MUST be visible and the backpack in the paperdoll VISIBLE with
;               nothing blocking it's view as the script drops direct to the backpack.
;               The resource container in your secure or bank box must also be visible with nothing
;               blocking it. It can be just about any valid container type.
;

Note: Resource container must be in bank box or house secure. See this linkfor more information.

Be sure to remove ALL items in your backpack that may possibly be smelted or there's a high probability they'll get smelted. Best to start with just tongs and ingots in your pack.

I'm not going to detail all the setup instructions, everything else you need (ignoring tailor specific comments) can be found in the CEOTurboTailor thread. If you're unsure about anything, read the CEOTurboTailor setup instructions, except for tailoring stuff, it's pretty much the same setup/requirements for this one. Too much to retype and I don't think many people read them anyways. The setup of this script is pretty self-guiding and only needs to be done once.

Rail Tips
If you're not training in a house you can start the script at a bank, following the instructions and it'll auto record a rail as you walk to a forge. Here are some tips to recording a working rail:

1. Always start recording at the bank and at a spot the bankbox will always open.
2. Get off your mount.
3. Walk don't run to the nearest forge.
4. When turning corners or entry a narrow spot, record a spot on both sides of the entry/exit points. This is important, or the rail might work fine in one direction, but not so good the other way.
5. While recording is automatic, if you wait in one spot for 5 seconds it'll record that spot. Use this method to record inbetween spots for places describe in 4 above.
6. The forge must be easily accessible, with NO doors to go open.
   As usual, please post your comments and problems in this thread. I'd greatly appreciate it if you drop a post here when you've skillcapped your character and tell me your statistics and how well the script performed. Rate the script too so that others will benefit from your experience with this script.

Note, if you are having problems and want to post about it, help me out by including this information in your first post: EasyUO version with build, Client Version, OSI/FS, your current skillcap, current smithy skill, and characters stats.

Thanks to the following beta testers:
CyberPope, Meepian, SteelKrom, Arcen, Raziel, jraven, UOsams, havesum2, Kestrel, Masterplan, pcgamer03, Ura Thayne
Special thanks to Warlock and AnonVet for their contribution of some custom skill tables based on scientific research and statistical obfusacation!

Thank you and enjoy!

Version History
Version 1.0, Released: Sun Apr 25, 2004 11:18

The script is in the attachment below that says CEOTurboSmithy.zip. Click on the download button to get it.
Note: The archive will always contain the latest version.

This script is copyright by CEO under the CEO Public License (CPL) agreement.

;-----------------------------------------------------------
; Script Name: CEOTurboSmithy
; Author: CEO
; Version: 2.2b
; Client Tested with: 7.0.0.4
; EUO version tested with: 1.5_154
; Shard OSI / FS: OSI
; Revision Date:  10/04/09
; Public Release: 042504
; Purpose: Trains Smithy to 120.
;-------------------------------------------------------------

Like my scripts? Consider a Paypal donation. Click here for more info.
