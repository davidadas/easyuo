The fill Bod portion of this script no longer works, however the rest does.There are no updates in progress for this.
Mega thanks to «§»Dalcon«§» For allowing me to plug in the smith bod filler into this do all script. I have broken most of it down into subs to keep it as fast as possible. Its still a work in progress but every thing functions great with out the need for anyone to do any programming to it. Smith Bod part may not work for thoes with SE installed

ENJOY

This script is to help those that live the life of the miner. Its an easy set up that needs no personal info from you.
There are several choices and I will explain how each works

The first choice is the Fill Smith Bods
For this portion you need to be next to your forge and anvil. Have smithing tools on you, and the bods you want filled in your pack. You will need access to the chest you will be pulling ingots from and a pack or chest to put the completed deeds into.

The second choice is to Fill/Organize/Count Commodity deeds.
For this you need a pack in your bank box with the ingots you want deeded in it.
You will need a pack in your backpack to put the filled deeds into.
and you will need empty deeds either in your backpack or in the pack that holds your ingots.
Example of how this works is you put only the ore you want to be deeded into the ore bag soooo...if you want 1 dull copper deeds with 100 and 2 copper deeds of 100 each you would put 100 dull copper and 200 copper into the bag and set the amount to deed 100. once you run that part it should be obvious.
Obviously you need to be at the bank for this to work :P
Thats it for the UO side. Start the script and it will ask you to open and close the 2 packs and then sit back and watch it run.

The third choice is the organize and count.
For this one you do not have to be at the bank. You simply need the pack that holds all your deeds to be in your main pack. The script will ask you to open and close this pack then it will run. It will organize the deeds in the pack and give you a count of each It gives you an up counter as its working so you know its working.

The 4th choice is the count only.
Again for the 4th choice you do not need to be at the bank. You need the pack that holds all your deeds to be in your main pack. The script will ask you to open and close this pack then it will run. since it only counting and not organizing it will give you a "count up " as it is running and then display the results of the count. This is great for when you have supplied your vendor and wish to know how many of what you have left and every thing is already organized.

The fifth is the ability to transfer deeds from one pack to another.
it will ask you to target the first pack then the next. The transfer into pack need to be on you. It would be best if both were on you but it seems to run fine as long as both packs are in some sort of container. This will transfer deeds/bods/and repair deeds.

The sixth feature is for the vendor miners
This portion marks runes for you. Make sure you have runes in your pack or in an open container in your pack and separated. The script will ask you to input what you want it to say if you are marking outside the house.

The 7th feature is for helping with mining scripts
This is my menu script that will give you all kinds of info you will probably need setting up a mining script. Current location/will lock dig spot for accurate ding spot numbers/live mouse and char location/Monster Id grabber/unique ids for any item targeted/findmod/full properties of any item/Item type/and color id.

======================================================
; Script Name: JEBBITS Do All For The Hard Core Miner
; Author: Jebbit, Dalcon
; Version: 1.5
; Client Tested with: 4.0.0q
; EUO version tested with: 1.4 (005b)
; Shard OSI / FS:
; Revision Date: 11-30-04
; Public Release:11-30-03
; Purpose:Commodity deed filler/organizer/counter/smithbod filler/Runemaker
;Deed bag transfer/Mining script set up helpper
;======================================================






ONLY USE A PACK DO NOT USE A POUCH OR BAG