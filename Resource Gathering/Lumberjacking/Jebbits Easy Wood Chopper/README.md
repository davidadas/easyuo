It chops wood fast. It can recall back to first location. It can use multiple rail files. It can change secures. You can build Temp or Perm rail files.

NOTE THAT THE INITIAL SAVING OF THE RAIL CAN TAKE BETWEEN 1-10 MIN DEPENDING ON THE SIZE OF YOUR RAIL WHEN USING THE PERM SYSTEM in 98 AND ME.

Other things the script does
*Auto sets up your house or bank
*Creates a rail on the fly
*Returns to home or bank to deposit wood
*Will cut up wood if saw available
*Auto calculates over weight & drops just enough.
*Auto pickup of dropped wood/boards on pass by.
*Can set up consecutive rails and secures.
*Uses a smart feature to return to last spot after drop off.
*Opens doors if set
*Script will run/recall you back to house or bank and halt if you run out of saws.
*Built in feature to use CEO's Healthwatch


Recognition For Sub Enhancements
Thanks goes to BadManic for the Pathfinding call script
Thanks Goes To Roadkill for for His Fast Writing Sub
Thanks Goes To Orgrim for the tree tile sub in the moded version.

set %straighthome #false
If you set this to true it will walk the straightest path home and back to you last spot chopped. THIS SETTING WILL NOT DO MIRACLES, IT WILL NOT WALK AROUND STRUCTURES/BUILDINGS/WATER/MOUTAINS.
The best time to use this setting is when you are out chopping and can basically draw a line at any given point in the rail back to your house. It will work its way around trees, rocks, stones. Open door will not work with this setting.

set %extrasecures #false
Set to #true if you would like the script to find another chest when one gets full. You must set each chest up with a wood box in each, some axes also if you wish to resupply from them as well.

Settings to change.
set %multi #false ( Optional setting )If you choose to make different rails that reside at the same starting point this setting will allow you to alternate between them at the end of each rail. You MUST use the profiles lumber0.txt, lumber1.txt, lumber2.txt in order for the script to rotate from rail to rail. THIS FEATURE ONLY WORKS WITH THE PERM RAIL SYSTEM AS IT HAS TO CALL THE SAVED FILES.

%multi setting continued ( Optional setting )
Multiple rail file usage.
This feature when set in the script ( %multi ) will allow you to call the next file after the first rail is complete, and start a completely different rail. You may have as many different rails as you like premade for the script to call. it will call the files in the order of

lumber0.txt, lumber1.txt, lumber2.txt

The script will then start back at lumber0.txt when it finds no more concurent files.

To use this file you need to.

1. Save a rail file using this script.
2. Rename the file to next number sequence lumber1.txt, lumber2.txt either in the script ( %file ) or the file itself located on your hard drive.
3. Do this for each rail until you have all the rails you want.
4. Set the %multi setting to #true in the script. Save script
5. Start the script and click on yes to " Do you have a rail made, and do you wish to use it.

Set %fullpath ( Optional Setting )
This script comes with a second script attached to it called RKspotautowaker.txt. Written by Roadkill, When turned on ( if you know how to use it ), it will use Roadkills awesome smart pathing and unblocking feature, the benifit is you will be able to walk further then a screens length and the pathfinder will find its way there.

set %turnoffsaw #false ( Optional Setting )
This setting allows you to turn off wood cutting if you need or chose to

set %file ( only change if saving multiple rails or prefrence )
This setting is use to name the file for saving a rail. The default name is lumber0.txt. You can rename the file name to save a different route. route1.txt, route2.txt.

%home ( Optional setting )
This will set how many moves you make before you actually start mining assuming you need to travel any distance before you can mine. Simply hit the Esc button on these spots to save them or click somewhere on the screen.

%axe ( some free shards only )
if your shard does not use a tool to convert wood change this setting to #true to use the axe instead, to convert logs to boards.

%bank
set %bank #false
to
set %bank #true if you are using the bank


Standard set up
home: Wood chest, Small red wood box inside wood chest, Saws inside wood chest.

Bank: Small wood box in bank along with extra saws in bank.

Simply start the script and it will get the ids you need to get started assuming you have the items as listed above. This scripts uses a menu setup for easy viewing of what is being set up and error descriptions
After it checks for everything it will start the rail portion of the script.
Click yes,walk ( this means a straight line not around buildings and not off the screen, the first rail spot is intended for travel and will not chop ), then hit escape. click yes again and go to your first tree, use the target on it. This will save not only your tree location but your spot as well. If you click on a spot and its bad simply click cancel and it will remove that attempt and allow you to try again. The script will not save a location until you click on a spot. Just clicking YES will remove the the display and give you a cursor. You can still move around and the script will only save after you click a spot. After you have created your rail click on NO and the rail will start automatically. It will initially have your char move back to the starting point and then start cutting. Its that simple.


Run Through Instructions

It says "Can't get there" after starting with saved rail?
This script will do a check to ensure you have "disable execute" un-clicked
a couple reason why you might have this error. 1. you made a rail spot ( waypoint) to far away from another one and UO is unable to look that far ahead. 2. you made a rail point around a corner instead of a straight line from the last point.3. The file can not be found. There should be a check for this.

I saved another perm rail but its using the old one?
You forgot to put a different name in for the file name, or you did not delete the old file with the same name.

I am using the rail system and the beginning or end is messing up
If you use the rail making part of the script more then once, or you mess up, Easyuo will not overwrite what you have but simply keep adding lines to the file. If you want to make another rail make another file name or delete the file and try again.

I go through a door does this script do that?
Yes it dose. You need to set this in the script and save it before you start anything. The setting is set %opendoor #false. Simply set it to #true[/b].

I set the script to open doors but it will not open mine?
Either it dose not have the right door id. ( open your door, get the id, and put in in the script. ) Or you are to far away. need to be within 3 paces of the door.

Why does the script move everywhere but where i set it to?
Very common when you have uoassist or razor on. Turn them off and everything should be fine.

It wont cut the first tree, why?
The %home setting in the script is set to 1 by default. This means your first rail spot will only be used for travel. Set this way because most people use this out of their houses, and the setting can be set higher for those that need to travel. If you simply hit the escape key and then yes to another rail spot you should be fine.

It cuts once and moves on. Why?
Some shards use different wording that may cause this script to think it needs to move on. Also some shards have issues with #ltargetkind Without going into to much detail. Set %alwaysclick to #true to correct this issue in most cases.

I started the rail and im not moving?
This is usually caused by text being on your screen, Hit enter and the movement will continue. Script will try to remove it in most cases for you.

After i get to a spot i wander a step or 2 and come back?
Partially do to lag, or computer lag. The Easyuo will step over the spot intended and then move back to it. The pathfinding that is now used helps with this issue some.

I stop moving before I get to a spot
This usually means you set the rail point to far away for the script to make it there before it times out. Make sure you don't go any further then the length of your screen when moving from rail spot to rail spot. Also to increase or decrease times change the %movetimer at the top of the script to change the time it allows to get there


PLEASE DO NOT RATE THIS SCRIPT WITH CHANGES TO BE MADE FOR YOUR NEEDS OR MODED SHARD. DO NOT RATE UNLESS YOU HAVE READ ALL THE INSTRUCTIONS AND HAVE ASKED QUESTIONS. DO NOT RATE IF YOU CANT GET IT WORKING. ITS ALREADY A PROVEN WORKING APPROVED SCRIPT.
;
=========================================================================
; Script Name: Jebbits Easy Rail Lumberjack
; Author: Jebbit
; Version: 2.2
; Client Tested with: 4.0.3c
; EUO version tested with: 1.5
; Shard OSI / FS:OSI ( unmodified )
; Revision Date: 11-23-05
; Public Release: 7-11-04
; Very easy to use, Temp/or perm rail Lumberjack script. Use from house or bank.
; No set up, easy, rail based...
=========================================================================


THIS SCRIPT IS ONLY SET UP TO RUN WITH OSI AND NON MODIFIED RUNUO SHARDS. SOME SHARDS CHANGE WORDING AND HAVE OTHER MODIFICATIONS THAT MAY STOP SOME SCRIPTS FROM WORKING. THERE WILL BE NO SUPPORT FOR OTHER FREE SHARD MANAGERS. FEEL FREE TO MODIFY SCRIPT IN ANYWAY YOU WANT TO WORK WITH THEM.

Click below for visual aid ( when the site is up )
http://uoforums.servegame.com/lumbermine.htm


Make sure your res for uo is 800X600 or the script WILL slow down to a crawl or fail to work altogether.
400 previous downloads before repost

No longer works with 1.42 you must use 1.5