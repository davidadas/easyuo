Original Poster: Rambo
Original Subject: Rambos Multitrainer Version 1.2 (Blacksmithy, Tailoring, Carpentry, Tinkering, and Bowcraft) AOS Rdy
Original Post URL: http://www.easyuo.com/old/viewtopic.php?TopicID=9295

; Rambo's Multitrainer version 1.2



; READ ALL THIS ESPECIALLY IF YOU ARE HAVING PROBLEMS

; I would appreciate it if people would test this one out. I've gmd my character while making the original multitrainer
; and I havent done alot of testing on this one. It seems to work fine and is ready for AOS.

; This trainer will train 5 skills (blacksmithy, tailoring, bowcraft, tinkering, and carpentry) all up to gm or higher if it applies.

; The trainer will allow you to set either 1 or 2 resource bags. The bags need to be on the floor and not inside each other. If you plan to train a skill for a long period
; of time, I would recommend you fill both bags up with kits and have alot of resources.

; In these bags you can put all of your kits and resources, but you can also keep them in your inventory.

; All skills will ask you to set the trashcan at the beginning, but some skills dont use it.

; Lockpicks and bandages if you make them will be put in your 1st resource bag.

; If you pick bowcraft, have alot of fletchers tools, either on you or in one of your 2 settable resource containers. Also have alot of boards in one of
; your containers. You have to be within range of a trash can for this skill too. Bowcraft is by far the slowest skill, because of the trashcan weight limit.

; If you pick blacksmithy, make sure you have an anvil and forge close by. Have alot of tongs preferably and ingots on you or in one of the resource bags.

; If you pick tinkering, make sure you have tinkers tools in one of the bags and alot of ingots. You also need to be within range of a trash can for this skill.

; If you pick tailoring, make sure you have plenty of sewing kits in one of the 2 resource bags or on you and make sure you have plenty of cloth or
; leather or bones and leather depending on what your skill is. This trainer works with both types of leather and multiple stacks of cloth. It is recommended
; that you keep all your cloth in one stack, because I think the trainer runs faster.

; If you pick carpentry, make sure you have plenty of boards in one of the 2 resource bags, and make sure you have plenty of carpentry tools.
; Also carry any type of axe on you and be in range of the trash can.

; Basically, make sure you have plenty of resources and kits.
; Be in range of the anvil and forge if it applies, the trash can and your resource bags.

; I would highly recommend you do this trainer in a safe house, with the door locked. Some skills will make alot of noise (blacksmithy especially)
; so you need to make sure you're not using this in an area with that has frequent noobs or anyone else that might tell on you.

; Remember even if you dont have much hiding skill, you still have a high chance of hiding inside a house. I recommend you let the trainer hide you.
; If you are lagging you might get the message failed to hide when you successfully hide.

; Im not sure if it matters but I tested this script with my windows resolution set at 1024x768. I had UO set at 800x600 in a window, not fullscreen,
; with the black borders around.

; If you have problems with things being placed out of the screen, try setting uo to 800x600 "game play window size".

; **I think I fixed this problem**
; IF YOU HAVE FRESHLY BOOTED UP UO, MAKE SURE YOU MANUALLY USE THE LAST TARGET FUNCTION ON SOMETHING BEFORE YOU START THIS!
; I dont know why, but last target never works in EUO when you have just restarted UO until you use it yourself manually.

; Dont start the trainer with your resource bags open or your trash can but anything else shouldnt matter.

; I havent tested this on slow connections, so if you have one good luck.
; Im not sure how the excessive lag that OSI still hasnt fixed will affect this trainer.

; I have heard of the problem where items being placed in the trash can get stuck in your hand and cannot be thrown away. I think I've got a fix in for this,
; but I cant seem to replicate this problem so theres no way I can be sure. The problem seems to be lag related though.

; Ive also heard of the problem where not enough resources is triggered when resources are there. I believe this one is also lag related. It seems to happen
; when the finditem command doesnt find the resource that is right there in the open bag. Im not sure why this happens but if the resource isnt found once,
; the trainer will wait 3 seconds and search for it again. This should make this problem happen much less.

; If your trash can doesnt open in the proper place (bottom left corner) it is most likely because of your screen size. I use the #nextcpos variable for that and
; sometimes things being placed even a little bit off the screen will cause #nextcpos to default to the upper left corner.

; IF YOU'RE DOING CARPENTRY MAKE SURE TO HAVE AN AXE ON YOU!!!

; Change the screensetupwait variable below if the paperdoll, inventory, or statusbar keep loading up in the wrong places. This problem is lag related. Default is 10.