Like my scripts? Consider a Paypal donation. Click here for more info.

(This script will not work for Freeshards using older EasyUO versions. It is now compatible with most RunUO shards *if* you choose a RunUO training method.

Choosing a training/skill table: If you are on a RunUO/Freeshard ONLY use the tables with RunUO in their names. Conversely, these tables WILL NOT work for an EA shard. IE, if you're on an EA shard, use any table EXCEPT the RunUO ones. Understand? When you select a training table, the script adjusts for that kind of shard, using a table not designed for your shard will cause the script to have problems.

The client must be set to english. This is a requirement for any script that examines #property or #journal for specific phrases.

With the new Mondain's Legacy expansion there are now several types of boards. This script only uses normal boards, but can not tell the difference between those and the new special boards as they are the same type and there's no coding to examine #findcol. So you need to remove all special type boards from view of the script by putting them away in a bag somewhere. Please don't post about this as a "bug", it's a simple pre-setup thing that needs to be done now for those running UOML.

If you need to modify stuff for freeshards (button positions most likely) see this post: HERE. Do not post any further freeshard issues, it's just not supported and you're on your own.

This is my fifth script in the "Turbo" line of scripts.

Here's the feature list:
You can use at a bank or in your house. (Auto-detects).
One-time setup, it'll reopen your bank/secure/resource bags the next time you run it without doing any file saving.
Remembers setup and lots of stats using the CEO*Filesystem.
If you have hiding skill it'll hide you (and rehide you if needed).
A very nice stats/progress screen (see below)
And of course like my other Turbo scripts, it's fast!

Estimated Resource/Stats
Time to GM (from 25-100): 10-12 hours
Boards needed: 75k-100k
Planes used: 100-120 (all exceptional, 2-3x more if not)
Minimum Tinkering Skill: 15.0[/clolor]

For an average of stats posted so far compiled by Googleyflub click here.

Status Window
Image

Skill Chart - 8 Different training methods + 2 user defined!

Image
You can define your own training method by creating a file called carp1.txt or carp2.txt in your scripts directory. This can be very handy for freeshard users with menu items in different positions. Note: If you chose a method or create one that makes ballot box deeds, the deeds will be tossed in the house or bank trashcan. For house training, you must be within 2 paces of the trash barrel. For bank training, you must be within 12 paces of the trash chest.

See CyberPope's script HEREthat'll assist you in generating alternate training methods (thanks CyberPope!).

----------------------------
; Setup Instructions:
;
; 1. Start CEOTurboCarpenter
; 2. Remove all extra stuff not needed for training out of your pack,
;     including bags, bod books, deeds, contract, and bank checks!
; 3. Follow the step-by-step setup.
; 4. Identify Secure (or it'll use your bankbox automatically)
; 5. Identify Resource container. (Inside your secure or top level in bank box!)
;               Make sure to have all necessary boards/ingots/tools in your resource container.
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

Other Stuff
When training in a house, you have to be an owner or co-owner in order to be able to destroy wood items with your axe, even though they're in your backpack(stupid). You can train this at a house you're friended to by having a secure with friend access placed on the steps and train "outside" the house off the steps. \":)\" Make sure it's a house in a safe place with no spawn!

I'm not going to detail the all the setup instructions, everything else you need (ignoring tailor specific comments) can be found in the CEOTurboTailor thread. If you're unsure about anything, read the CEOTurboTailor setup instructions, except for tailoring stuff, it's pretty much the same setup/requirements for this one. Too much to retype and I don't think many people read them anyways. The setup of this script is pretty self-guiding and only needs to be done once.

Note, if you are having problems and want to post about it, help me out by including this information in your first post: EasyUO version with build, Client Version, OSI/FS, your current skillcap, current carpentry skill, and characters stats. Also what training method you are using!

Thanks to the following beta testers:
CyberPope. Special thanks to Scriptfellow for his donation of 60k boards and a temporary home to train in.

Thank you and enjoy!
\":wav:\"

The script is in the attachment below that says CEOTurboCarpenter2.zip. Click on the download button to get it.
Note: The archive will always contain the latest version.

This script is copyright by CEO under the CEO Public License (CPL) agreement.

;-----------------------------------------------------------
; Script Name: CEOTurboCarpenter
; Author: CEO
; Version: 2.1
; Client Tested with: 7.0.0.4
; EUO version tested with: 1.5_154
; Shard OSI / FS: OSI
; Revision Date: 100109
; Public Release: 051104
; Global Variables Used:  *CEOTurboCarpenter
; Purpose: Trains Carpentry to GM.
;-------------------------------------------------------------

Like my scripts? Consider a Paypal donation. Click here for more info.
