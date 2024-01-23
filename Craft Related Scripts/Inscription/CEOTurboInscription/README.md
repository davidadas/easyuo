Like my scripts? Consider a Paypal donation. Click here for more info.

(This script will not work for Freeshards using older EasyUO versions or Freeshards
with a different menu layout then the standard OSI one. Sorry.)

The client must be set to english. This is a requirement for any script that examines #property or #journal for specific phrases.

Choosing a training/skill table: If you are on a RunUO/Freeshard ONLY use the tables with RunUO in their names. Conversely, these tables WILL NOT work for an EA shard. IE, if you're on an EA shard, use any table EXCEPT the RunUO ones. Understand? When you select a training table, the script adjusts for that kind of shard, using a table not designed for your shard will cause the script to have problems.

If you need to modify stuff for freeshards (button positions most likely) see this post: HERE. Do not post any further freeshard issues, it's just not supported and you're on your own.

This is my seventh script in the "Turbo" line of scripts.

Here's the feature list:
You can use at a bank or in your house. (Auto-detects).
One-time setup, it'll reopen your bank/secure/resource bags the next time you run it without doing any file saving.
Remembers setup and lots of stats using the CEO*Filesystem.
If you have hiding skill it'll hide you (and rehide you if needed).
A very nice stats/progress screen (see below)
And of course like my other Turbo scripts, it's fast!

Estimated Resource/Stats(EA/OSI)
Time to GM (from 25-100): 30-50 hours
Blank scrolls needed: 15k-25k
Scribe tools: 150-300 (All exceptional, 3-5x more if not)
Reagents: 20k-40k of each reagent depending on skill table
Note: EA/OSI stats are estimates based on RunUO stats.
As soon as a few people post their results I'll update the info above to be more accurate.

Estimated Resource/Stats(RunUO)
Time to GM (from 25-100): 4-5 hours (depends alot of chars mana and regen ability!)
Blank scrolls needed: 2500-3000
Scribe tools: 50-60 (All exceptional, 3-5x more if not)
Reagents: 2-3k of each reagent depending on skill table

Status Window

Image

Skill Chart - 8 Different training methods (4 EA/4 RunUO) + 2 user defined!

Image
You can define your own training method by creating a file called inscription1.txt or inscription2.txt in your scripts directory. This can be very handy for freeshard users with menu items in different positions.


----------------------------
; Setup Instructions:
;
; 1. Start CEOTurboInscription
; 2. Remove all extra stuff not needed for training out of your pack,
;     including bags, bod books, deeds, contract, and bank checks!
; 2. Follow the step-by-step setup.
; 3. Identify Secure (or it'll use your bankbox automatically)
; 4. Identify Resource container. The resource container MUST be inside the secure or bankbox container!
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

I'm not going to detail all the setup instructions, everything else you need (ignoring tailor specific comments) can be found in the CEOTurboTailor thread. If you're unsure about anything, read the CEOTurboTailor setup instructions, except for tailoring stuff, it's pretty much the same setup/requirements for this one. Too much to retype and I don't think many people read them anyways. The setup of this script is pretty self-guiding and only needs to be done once.

Note, if you are having problems and want to post about it, help me out by including this information in your first post: EasyUO version with build, Client Version, OSI/FS, your current skillcap, current inscription skill, and characters stats.


Thank you and enjoy!
\":wav:\"

;-----------------------------------------------------------
; Script Name: CEOTurboInscription
; Author: CEO
; Version: 2.1b
; Client Tested with: 7.0.0.4
; EUO version tested with: 1.5_154
; Shard OSI / FS: OSI
; Revision Date: 100209
; Public Release: 061105
; Global Variables Used:  *CEOTurboInscription
; Purpose: Trains Inscription from 25 to GM.
;-------------------------------------------------------------


Like my scripts? Consider a Paypal donation. Click here for more info.

The script is in the attachment below that says CEOTurboInscription2.zip. Click on the download button to get it.
Note: The archive will always contain the latest version.

This script is copyright by CEO under the CEO Public License (CPL) agreement.
