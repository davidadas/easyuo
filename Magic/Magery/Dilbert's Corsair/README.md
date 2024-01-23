I was not happy with what I saw as 8x8 engines, and I did not really want to keep UOAM and UOA open to see the skillgain and the position of the ship on the map. So I started to tinker with this and you see the result here.

I have spent quite some time on this, and it sure looks fancy.

Image

But thats not all by far! Meet the Crew!
The tillerman
keeps the ship sailing, waits for orders from captain, navigator or lookout
The navigator
plots the ships position on the map, gives position and 8x8 cell info,
tells the tillerman to sail to the channel if the ship is off course
The lookout
tells the tillerman to evade when he notices other ships ahead
The trainer
decides on the current task for the trainee, makes sure the trainee keeps training as hard as necessary and montiors the progress

Here is what the script does in more detail:

Crew checks ship status
The crew will first of all check if the ship is in order, if the anchor is up, and if the ship is ready to set sail.
Lookout - makes tillerman Dodge ships!
The lookout is continously is watching for ships which are nearby. Most of the time - that is if Corsair is not distracted by another ship, a collision and the resulting unblocking will be avoided completely. The lookout will guide the tillerman to steer the ship just enough west or east so it can pass without a scratch.
Navigator - Map, position and 8x8 cell info
A Corsair allways needs to know where he is! The navigator judges the position by the stars and plots it on the map for the captains convinience. Since the ship is always moving and the captain knows the waters well, the navigator maintains only a schematic map.
The navigator indicates the ships position on the map, so the captain can see with a glance where the ship is.
The navigators reading of the position itself and the position broken down to cells 8 x 8 tiles is indicated on the maps lower border.
Note:The UO world is split into cells wich contain 8 x 8 tiles each. Each of those cells can have ore, wood, sand or what interests us here - gains.
Trainer - Sets tasks, train dealy for the trainee, monitors progress
The trainer makes the trainee attempt tasks which are very likely to allow the trainee an easy improvement of the trainees skill.
If there are messages that indicate that the trainee is not ready to try again when the trainer prompts him to do so, the trainer will increase the delay between training attempts automatically to make it easier and more effective for the two of them.
The trainer watches the trainees progress closely, and notes at which skill a training has started and how much the trainee improved his skill in the current training session.

Chivalry, Hiding, Magery*, Musicianship, Necromancy, Peacemaking and Spirit Speak are supported from NPC train value to 120.
Resist and Evaluate Intelligence are assistants for finishing training in those skills with Jewellery. What you do is you wear items that increase your skill up to your skillcap. When you then get a gain with corsair you can get a lot of gains in that specific location, with a bit of luck to your skillcap

*When training magery, the use of a 'mage weapon -29 skill' is recommended. If a such a weapon is armed or present in the backpack of the trainee, the trainer will arm it or keep it armed. The weapon needs to be reset each time a server border is passed to keep the malus, this is done automatically.
Tillerman - Unblocking, shipcontrols, sailing to and keeping in channel
Unblocking
Should the lookout fail to notice a ship in time, the lookout will get a beating and the tillerman will then proceed to get the ship under full sail again. He knows his stuff, so it is unlikely that he will not be able to get the ship clear again. The tillerman boasts unless he is blocked in by other pira..ehm ships he will keep sailing.
Instead of listening to the crew the tillerman will use his own sense of position and judgement to find out if the ship can move in a direction or not.

Ship controls
A well trained crew is one thing, but there are times when the captain has to take the con. To make this work, the tillerman will pay attention to the captains directions, even if he just raises an eyebrow into the right direction.

Sails to the channel (see pic)
I put this in because I felt silly manually sailing my ship to the channel and stopping it in the right time.
Corsair will turn the ship west or east respectively and sail towards the serverborder between Ice Isle / Moonglow / Avatars Isle and Yew / Skara / Jhelom. If it hits something, there is a primitive evade function that takes care of a ship in the way.
As soon as the ship, or rather the chars position has reached the middle of the 80 tile wide strip next to the server border - called channel here - it will stop and turn the ship north.

Keeps the ship in the channel
This means that if Corsair dectecs that the char has left the channel countermeasures will be used to sail back to the center of the channelside you are on.

To-be implemented list

The following suggestions have been made, considered a good idea by me but not yet implemented. Please do not suggest them again, I will get to it in time.
add pause button
add marks for gain lines on the map
add option to backtrack if no gain is found in the cell north of a gain cell
add option to return to the beginning of a gain chain and try it again
add option to go south or north depending on the shard.

Please note these Limitations:
This script is written for OSI shards, NOT freeshards. If you are on a freeshard and it doesnt work for you, fix it yourself by changing the variables that are differnt on your shard!
As of now this script sails north not south, you can swap the names of Sub's ForwardEight and BackwardEight to make 8x8 chains work for shards on which the gains run south, but there is no comfortable little switch as of yet.
The script assumes a LRC suit for magery/chiv/necro and ample instruments. There is no reagent or instrument control as of yet. If you dont have one and run out of reagents, the script wont notice.
There is no defense against monsters. I don't plan to put this in since it isnt needed often in the first place and would only encourage unattended macroing.

Problems? Read this!
If you encounter a problem with the script, please check first if your problem is due to:
being on a Freeshard,
being in the wrong location on an OSI shard or
not reading the description above, in particular the limitations and the not yet implemented functions.
If your problem still exists please reply to this thread with the following information so I can help you:
What shard are you on?
Where did you start the script?
Did the initialisation work? (status:orders captain?)
Which skill did you select?
What happened?


© COPYRIGHT Dilbert 2003

You MAY NOT PUBLISH any script that uses this code, OR any derivative work without written permission from Dilbert.
You may only use this for private, unpublished work.
You may NOT DISTRIBUTE this script, its available to everyone here.

Code:
;==================================
; Script Name:   Dilbert's Corsair
; Author:  Dilbert
; Version: 1.12f
; Client Tested with: 4.07b
; EUO version tested with: 1.42.009b
; Shard OSI / FS: OSI
; Revision Date: 16 Jan 2005
; Public Release: 27 Nov 2003
; Purpose: menu driven 8x8 boat tool, keeps channel, unblocks, dynamic training delay
;                       premade subs for training magery, chiv, necro, spirit, hiding
;==================================
;
; ACTUAL SCRIPT SEE DOWNLOAD BELOW ;-]



EDIT:
changed boatinit, so that it uses planks and the tillerman rather than the mast and the tillerman.
The previous way did not work with large dragon ships, thanks Artgenos!

EDIT:
fixed bug in channelcheck sub. works better now.
added warning for people who expect Corsair to pathfind from
Brit harbour to the channel.

EDIT: 19th Nov 2003
put script in a download rather than in code tags.

Edit: 19th Nov 2003
fixed retry count bug, uploaded new version, thanks Godfetish!

Edit: 20th Nov 2003
fixed bug in channelcheck, prevented sailwesttochannel.

Edit: 27th Nov 2003
added position info in tiles and in 8x8 tile cells
added #menuaction checks during all pauses.
added DODGE fuction.
added custom gain retry controls
improved unblock function

Edit: 2nd Dec 2003
added longer description
added to-do list

NEW RELEASE: Version 1.10
9th September 2004
added boat refresh to the ship checking at startup.
added check key insurance to the ship checking at startup
improved GUI with more information about gains
fixed Chiv/mana message bug

10th October 2004
removed debug leftovers

29th October 2004
added ignore option for sub checkshipkey
fixed typo in SUB CheckMageryEval. Thanks RoadKill.

22nd November 2004
added Banboo Flute and Standing Harp to instrument types. Thanks Monnie.

16th December 2004
set menu window color to default at menuinit

16th January 2005
added magic wand support to magery training
added stop & message/sound on reaching skillcap
added sound on gain
added shard detection - Thanks WarSwine for reporting a bug related to this!
various optimisations


Did this script work error-free for you and perform as intended?
If yes, please vote for it by clicking the link on the top left of this post.