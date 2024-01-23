i think i'd better release the Lumberjacking Guide i used to have in my Script Library as a Macro for the PSL...

Code:
;==================================
; Script Name:  Lumberjacking Complete Rail Macro
; Author: Janus
; Version: 1.1
; Client Tested with: 4.0.0a
; EUO version tested with: 1.35 Build 000A
; Shard OSI / FS: FS, Crystalgate
; Revision Date: 01/17/04
; Public Release: 01/17/04
; Purpose: Lumberjack a Route without click commands
;==================================
initevents

set %ljtool xxx ; set your ljtool here

start:
GOSUB LJING xxxx xxx xxxx
GOSUB LJING xxxx xxx xxxx
GOSUB LJING xxxx xxx xxxx
goto start

sub ljing
move %1 %2 1
finditem %ljtool
set #lobjectid #findid
event macro 17 0
target 10s
set #ltargetx %1
set #ltargety %2
set #ltargetz %3
set #ltargetkind 3
set #ltargettile %4
event macro 22 0
wait 7
set %overtime #scnt + 25
gosub scan
return

sub scan
scan:
if THERE'S_NOT_ENOUGH_WOOD_HERE_TO_CHOP in #sysmsg
return
if #scnt >= %overtime
return
goto scan


for the shards where it doesnt chop until the tree has no more wood:
Code:
;==================================
; Script Name:  Lumberjacking Complete Rail Macro
; Author: Janus
; Version: 1.1
; Client Tested with: 4.0.0a
; EUO version tested with: 1.35 Build 000A
; Shard OSI / FS: FS, Crystalgate
; Revision Date: 01/17/04
; Public Release: 01/17/04
; Purpose: Lumberjack a Route without click commands
;==================================
initevents

set %ljtool xxx ; set your ljtool here

start:
GOSUB LJING xxxx xxx xxxx
GOSUB LJING xxxx xxx xxxx
GOSUB LJING xxxx xxx xxxx
goto start

sub ljing
move %1 %2 1 60s
ljagain:
finditem %ljtool
set #lobjectid #findid
event macro 17 0
target 10s
set #ltargetx %1
set #ltargety %2
set #ltargetz %3
set #ltargetkind 3
set #ltargettile %4
event macro 22 0
set %overtime #scnt + 7 ; change this if its too long, its a timeout if the #sysmsg check fails
gosub scan
wait 5
if %nexttree 2
set %nexttree #false
return
goto ljagain

sub scan
scan:
if YOU_PUT_THE in #sysmsg || #scnt >= %overtime
return
if YOU_FAIL_BLA_BLA_BLA in #sysmsg
return
if THERE_IS_NOTHING in #sysmsg 2
set %nexttree #true
return
goto scan


Here the set Route Tool:
Here the link to the old tool

Code:
initevents
set %tree 0
start:
event macro 13 3
wait 10
targloop:
if #targcurs = 1
goto targloop
set #lobjectid #ltargetid
if %ltargetx = #ltargetx && %ltargety = #ltargety
{
event sysmessage error. try again
goto start
}
execute cmd.exe /c echo >>ljroute2.txt GOSUB LJING #ltargetx #ltargety #ltargetz #ltargettile
set %ltargetx #ltargetx
set %ltargety #ltargety
set %tree %tree + 1
event sysmessage Done with Tree Nr. %tree
wait 10
goto start

here the tile "auto find" set tree tool which was lost back in the day when the hurricanes broke the forum...
Code:
set %maxrange 40 ; +/- from your char position

set #lpc 1000
tile init noOverrides

if %maxrange > 70 2
display ok Error!$$The set maximum range is too high.$$Macro stopped.
halt
display ok Please be patient!$$You can change the Amount of Tiles you want
+ to Check by changing the variable " , % , maxrange , " to a value under 70.
  start:
  if %lposx = N/A
  set %lposx #charposx
  if %lposy = N/A
  set %lposy #charposy
  set %x1 %lposx - %maxrange
  set %y1 %lposy - %maxrange
  set %x2 %lposx + %maxrange
  set %y2 %lposy + %maxrange
  for %y %y1 %y2
  {
  for %x %x1 %x2
  {
  if #tilename <> N/A
  set %tiles %tiles + 1
  tile get %x %y 2
  if ( leaves in #tilename || tree in #tilename ) && #tilename <> yew_tree
  {
  set %cnt %cnt + 1
  set %exec . %cnt gosub , #spc , ljing , #spc , %x , #spc , %y , #spc , #tilez , #spc , #tiletype , #spc
  set %lposx %x
  set %lposy %y
  }
  }
  }

display yesno The Macro found %cnt Trees out of %tiles Tiles.$$Would you like to execute them?
idle:
if #dispres = no
halt
if #dispres = yes
{
if EXEC notin #opts 2
display ok Error. Execute is NOT enabled$$You have to enable Execute in Tools -> Options -> Permissions to use this Function!
halt
display ok Now lean back...put your feets on the desk....and relax...$$This may take approx %cnt seconds.
str left #osver 1
If #strres = 1
set %command command.com
If #strres = 2
set %command cmd.exe
for %e 1 %cnt
{
execute %command /c echo >>route.txt %exec . %e
}
display ok DONE!$$Please rate this Script #smc , )
halt
}
goto idle


Here some Addons which you can implement with a little euo know-how:
a recall function:
Code:
; settings:
set %runebookid xxxxxxx
set %spots 6 ; how many spots you use in your runebook (max 12)

; not to be changed.
set %currentspot 0
set %spotcount 0
set %click 1

if %currentspot = 2
{
set %currentspot 0
set %click %click + 1
}

recalling:
set #lobjectid %runebookid
event macro 17 0
if #contkind <> %contkind
goto recalling
for %cnt1 1 %click
{
click 335 20
wait 7
}
if %currentspot = 0
{
click 95 170
}
if %currentspot = 1
{
click 260 170
}
wait 4s
set %currentspot %currentspot + 1
set %spotcount %spotcount + 1
if %spotcount > %spots
{
set %spotcount 0
event sysmessage all spots done...
goto start ; you can add a "goto store" here or aswell...
}
gosub ljspots
goto recalling


a gate check o. recall on sight check (in the scan part):
http://www.easyuo.com/forum/viewtopic.php?t=2183

you might want to add a create boards part but i can just give you some snippets...

sub checkweight
if #weight > #maxweight
{
finditem xxx ; tool i.e. saw here
set #lobjectid #findid
event macro 17 0
target 5s
finditem xxx ; id of logs here
set #ltargetid #findid
event macro 22 0
wait 7s ; the time it takes to create boards here...
}
return

depending on the shard/merchant system you play on you will have to target boards or click in the menu or something like that...

You can also add a auto eating part simpe with finditem -> use item i.e. event macros...

FAQ:

How to set the Macro up?
Actually you just need to set the %ljtool at the beginning and the route, well the route takes a while to set but its simply one of the best ways to lj.... The way to set the route read some rows down.

My Character just runs to each spot and gives me the message there is no more wood here, what's wrong?
If this happens you 99%' made some errors with setting your own route. you can test my example points (4th post).

My Character just runs to each spot without doing anything.
You probably didnt set a ljtool "set %ljtool xxx"

My Character doesnt move at all
Maybe you use an wrong or old client, try out one of the newer for 4.xxx to be sure its no error in the script.

How to use the old Rail/Route Tool (the one with the Menu)?
You need to mark the exact location of the tree...so think logical
if you move east-west (y) you can execute the x variable now north-south (x) you can execute the y variable then chop the tree once and #ltargettile will change now execute this one, in the *.txt file you will have to stick the parts togheter so its one row like "GOSUB LJING xxxx xxx xxxx" IMPORTANT: Mark the EXACT location of the tree.

How to use the new Rail/Route Tool (Target Cursor and SysMessages)?
Just enable "event sysmessage" and "execute" then start it and target the trees you want to mark.

Please just ask Questions that have nothing to do with the Points in the FAQ.

