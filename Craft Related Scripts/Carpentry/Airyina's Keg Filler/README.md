After searching the PSL for a keg filling script to do what I wanted it to do, I could not find one. So I wrote this script.

This script will create Kegs for you, then fill them. It checks your secure container for resources, pulls from there first if there are any, otherwise it creates the tools you need, and the kegs you need, then proceeds to filling the keg, and then stores the keg in a specified location. You MUST have atleast 1 tinker tool to run this script, and atleast the required carp and tink to create the kegs, otherwise it will not work.

This script works 100% flawlessly from what I can tell (I created over 200 kegs with it and it didnt break). Im posting this on the debug forum because I want help adding a menu, and targeting the containers you want to use. I want the menu to allow you to choose what type of potion you want to make, how many kegs to fill and which container is your resource container and finished keg container.

I tried to fiddle around with menus, but I just cant understand them :/ So any help is appreciated. Im not asking someone to fully write the menus or anything, just help me out understanding how menus work please.

So, here is the script. It uses a couple of s7's subs; s7makeanything, s7waitforvars, and s7waitforaction. And one of Cstalkers subs, moveitem.

EDIT: Updated post to include a new version with more features and menus!

-It will now ask you for your secure container and finished keg bag after menu setup. You can hardcore these values so it doesnt ask you everytime if you wish.
-Added in many more error checks and script runs even better than before!

Finalized now... hope someone finds some good use of it :)