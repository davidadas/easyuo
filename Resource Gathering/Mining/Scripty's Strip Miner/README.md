THIS IS AN EUO SCRIPT! NOT OEUO! UPDATE YOUR EUO TO THE LATEST VERSIONS AVAILABLE BEFORE ASKING FOR HELP WITH PROBLEMS OR YOU WILL GET NO SUPPORT.

This script now saves your mining spots on a per character basis in your registry.

Code:
;================================================================
;   _____ _       _        
; /   __/  __ _ _(_)_ _ | |_ _ __
; \__   \(  _/ `_/ / ` \|  _| | | |  ================
;  __|   | (_| | | | |) | | | \_| |  www.pkpalace.com
; \_____/\___| | |_|  _/\__\ \   /   ================
;            | |   | |  _____/  /
;            |_|   |_| |______/
;================================================================
; Script Name: Scripty's Strip Miner
; Author: Scripty
; Version: Alpha
; Client Tested with: Latest latest
; EUO version tested with: latest
; Shard OSI / FS: OSI
; Revision Date: 2/5/22
; Public Release: 'When it's done.'
; Latest Update: 8/11/11
; Credits: Myself, Cyberpope, Machine, Cheffe, TM
; Useage: To pwn farming.
;================================================================


SCRIPT IS POSTED ON BOTTOM OF SECOND POST!

Subs used:

Machines Craftitem Sub | Scripty's PseudoIgnore Sub

This script was written to show people that you can mine in Ter Mur without using tiles. With all the scripters giving up on their mining scripts, I had to write one that would successfully mine in the new lands. The larger version of this script actually lumberjacks and fishes in Ter Mur also. All using multiple rune books with easy auto setup, and best of all, the script does it's best to avoid people. SCRIPT HAS BEEN UPDATED! It now uses tiles. I'll run down setup instructions below.

Script info:

A lot of work has went into making sure this script is easy to setup. That being said, you MUST know how to setup runes to successfully use this script. I recommend using Cyperpope's newest mining radar: Cyberpope's Mining Radar v4.1d_F002 to find your ore spots. This is an AMAZING easyuo script and he put a lot of effort into it. It works great for this purpose. If you can't get it working, you're not going to get the most from THIS script. Finding spots that have at LEAST 2 unique ore locations will go a long way for you and help you enjoy the script to it's fullest. This image displays how easy it is to find spots by standing at the red plus sign. In this image, there's only 2 spots, but you get the idea, if you find spots where the two red lines meet over the top of rocks, or a rock wall, you'll get 4 mining spots. Those are the corner of the games 8x8 gridlines. Like this:
Image

I personally wont mark a rune unless it has 3 to 4 ore spots, anything less is a waste of time. The script will do it's best to find ore spots for you in a 2 tile radius around your character! It "learns" your books when you run it. No need for a lengthy setup file, or to setup ore mining spots for your books. I always hated that. The script DOES save your locations! It will ALWAYS try to learn your spots on the first run of the script, and it will just work after that.

The best part of this script, and the part that I spent some time perfecting, is that it does it's best to avoid all people. If a person is seen, it will recall away, and IGNORE the rune spot for an editable amount of time that you select. It keeps track of banks and ore spots separately for this. Banks and rune locations can have their own ignore timers. What this means is you need to have a decent amount of rune books marked (2 plus) as the script will constantly ignore spots that have people/monsters at them. Oh yea... you can have a separate timer for monsters at rune/bank locations also. The more books you have the more likely you are to NOT have problems. I have actually had the script ignore all my spots because people showed up at every one! Eventually it will continue on it's route, but it will wait until spots are "unignored" to do so. The script will do this constantly so your recall patterns and ore intake will change throughout the entire time you run this script. The interesting thing about this is you will intake ore in about the exact chances of getting ore. You'll see what I mean upon running it.

Lag and this script:

I have a fast connection. I DO try to accommodate lag in my scripts. Actually I try to gracefully recover from lag. I have also added a button that will increase and decrease ALL timers in the script to help you fight lag. If you notice you are getting a few "You must wait to perform" messages, just increase the waits in the script by 1 or 2 on the menu. That will add a 1-2 10ths of a second onto the script. You can go as far as adding a full second to all waits in the script with this button. I figured if you needed to go farther, you probly need a new connection, not more waits. ;)

Things to note:

1. This script ASSUMES you will use protection. And have tons of mana regen/med and or focus! Enough to keep up with constant recalling.

2. This script DOES NOT have beetle support. It IS in my version, but I will not be releasing it. It allows for too much gathering of ingots and I feel that would be a bad thing at this time. I might change my mind on this later. But don't count on it.

3. NO script is completely GM proof. That being said, you run this at YOUR OWN RISK.

4. This script DOES work in Ter Mur!

6. Setup is easy, put ONE bag/box/container in your bank, a large stack of iron ingots in the BOTTOM level of your bank, NOT in a bag, and have ONE tinker kit in your pack and enough tinkering to make shovels. Even if you can barely make them you should be ok. Also have enough magery/chiv to recall. The script auto detects which you will use. When you start the script, just click your storage container in the bank, and away you go. (Its possible to make a new character, put max tinker, max magery, use a suit and make a miner/tinkerer in no time.)

7. Prospecting is NOT in at this time! I left it on the menu so I didn't have to redesign it. ;)

8. The script does bank stone and gems also. So yes it can farm those too. It can also be used on beaches to farm sand and works just as well inside caves/dungeons. When I upgrade to High Seas I'll add support for saltpeter also. If I upgrade. ;)

9. The script will "vacuum" up ore and logs that are left by other miners. I'm PRETTY sure I left the log vacuum function in there... I always hated people who left ore around, it's like a sign that screams OMG I'M MACRO MINING! ;)

10. The script might appear to be stuck in a loop at times while mining, but it is NOT. For the entire first loop of your books, the script is searching out mining spots and ore. After the first loop, the script speeds up by a LOT as it ONLY mines spots that have ore at that point, if everything went well and you're not laggy.

12. The script will ignore all "dead" runes. Any rune with no mining spots will be ignored and not recalled to for 5 hours I believe. Then it will be rechecked. Sand spots are figured into this. If you find sand, the spot will be considered a "live" or good rune.

-----------------------------

NOTE: THIS HAS ONLY BEEN TESTED ON PRODUCTION SHARDS! NO FREE SHARD SUPPORT WILL BE GIVEN AT THIS TIME!

Image

Setup instructions:

On the bottom of the menu you see an information box. This box gives you information and times for events that happen in the script. Like people, and monsters, and where/what rune those events happened. If you look at the first line, you'll notice I have prospecting selected and ONLY verite selected on the menu, and when the script prospected and what rune it found the ore at is in the menu. It shows it found it in BOOK 3 at RUNE 9, on CYCLE 2 of the script, at 8:13:53 PM. There's other info like What monster with name, rune, book, and time also. And when it sees people it shows that on the menu with a person name also. The iron ore shows spots that are ONLY iron. I use that for a feature in my own version that ignores all iron spots to maximize color intake. ;)

The boxes that show the facet names are for mining spots. I wanted a total number for mining spots found for information sake. This just shows the exact number of minable spots found per shard. That was 71 spots for 2 books. A little over an average of 2 spots per rune. It also shows the number of swings you made at that spot. Information I used to help fix a couple targetting issues while writing the script.

Sometimes there will be a B or O in front of the first number value. That designates if you are on a BANK book or an ORE book. In my version it goes further, and I have T for trees, and F for fishing.

The current rune and bank boxes just let you know what bank book and what rune number you are at respectively. I also added the FACET you happen to be on to all of the menu items. Just for information really. The resource box is informational only also, when and if I turn prospecting on, the script remembers each spots color, and continually scans each spot as you return to it, keeping you completely up to date on what ore you are mining from what spots. So you never have to update your rune libraries because the script finds the ore colors for you. I was CONSIDERING a feature that allows you to mark a rune at certain color spots. So you can just remark the colors you don't want and continually and easily update your books for the best colors. :) We'll see.

User vars:

set %bankIgnore 120           ; Time to ignore bank runes when people/monsters found at bank in MINUTES.

set %runeIgnoreHuman 120      ; Time to ignore mining spots when a human is found in MINUTES.

set %runeIgnoreMonster 90     ; Time to ignore mining spots when a monster is found in MINUTES.

set %weightOffset 60          ; 0 means #maxweight is used anything else is SUBTRACTED from maxweight. Will be changed.

set %bank n/a                 ; Set to id of bankbox or autosetup.

set %oreStorageBank n/a       ; Set to id of container in bank for ore storage or autosetup.

set %ingotCnt 50              ; Amount of ingots to drag to pack when below this number.


1. Bag in bank.

Image

2. Ingots in bank.

3. Tinker kit in YOUR backpack.

4. Enough magery/chiv to recall, 100 percent lrc suit.

5. You MUST name your runebooks correctly! Ore books will be named ore with the number of runes in the books. So if you have 5 runes you would name your book, ORE05. If you have 12 runes you would name it ORE12. The script auto senses book names for setup. Bank books will be BANK in the same manner. So 10 runes would be BANK10. Also, one other book, TRASH. This is for dumping garbage. Blackrock. Same as before, TRASH04 would be 4 trash runes in the book.

6. Make SURE you have enough runes to keep you mining for a while. If you only mark one book with 2 mining locations at each spot that will NOT be enough runes/mining spots. You MUST have at least TWO full books of runes with GOOD mining spots at each rune.

7. Hit play, follow the one instruction. Do NOT be mounted. (Other version auto detects beetle and mounted. This one does not.)

8. ENSURE that you have enough mana/regen/med/focus to keep up with recalling... and use 2/6 casting. 4/6 with chiv. Those small things will increase the speed of the script greatly.

9. MAKE SURE that you have at LEAST 2 full books of runes marked WELL for mining. Have at LEAST one full book of BANK runes. And have a few runes of trash cans. I'd mark at least 6 at trash cans around UO.

10. This has ONLY been tested on OSI.

11. YOUR RUNE LOCATIONS *MUST* BE WITHIN *TWO* TILES OF YOUR CHARACTER. This is why you use OEUO Visual Grid Editor by wvanderzalm to find rune locations! You can find a ton of spots on the very corners of resource grids, making it easy to mark spots that have 4 unique mining locations!

12. I have added SAND runebooks to the script. If you are mining large amounts of sand, you MUST use a runebook named SAND and the number of runes in the book. Such as SAND05 for 5 runes in the book. It IS possible to intermix a sand rune here and there in your ore books tho if you'd like. But if you plan on mining TONS of sand, use it's own book.

13. *REMOVED* I added HOME books. These CAN be used in conjunction with bank books (It works JUST like a bank book.) EXCEPT, you MUST set the home secure variable at the top of the script to the ID of your SECURE AT YOUR HOUSE. It will use multiple runes also, so that it never gets blocked at your door. BE AWARE: The ignoring function is TURNED OFF for house secure mining. If you get caught mining from your house, you WILL be paged on. BE CAREFUL WHEN YOU USE IT THIS WAY. I highly recommend using the bank option and NOT the home secure option. Also, it's UNTESTED, so let me know how it works for you. A BOOK NAMED HOME12 would have TWELVE RUNES IN IT MARKED AT THE HOME SECURE.

14. This script now farms Saltpeter. You don't have to do anything special except mine in dungeons and have High Seas expansion. I was considering adding a "dungeon" book, that way I could add special functions/features to those books/runes when mining in dungeons. We'll see.

15. The script now supports FORGE books. They work the same way as any other book, but you mark the runes by public forges in the game. The script will automatically know you're using a forge book and start recalling to them to smelt ore. Then bank the ingots only.

16. PLEASE MAKE SURE YOU DO NOT HAVE ANY BOOKS MATCHING THE NAMES OF THIS SCRIPT IN YOUR PACK WHEN YOU RUN THE SCRIPT! THIS IS VERY IMPORTANT. HOME BANKS SAND TREES FISHING LEATHER TRASH AND ORE ARE ALL USED BY THE SCRIPT!!!

DONT FORGET TO VOTE!: