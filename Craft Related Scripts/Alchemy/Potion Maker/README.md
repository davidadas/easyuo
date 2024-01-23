:wav:
CEO: This is the 1000th script to be added to our Public Script Library!
:wav:

After many sleepless days, and hard nights work, here is my first script. It is designed to make potions, and fill kegs. It will fill partially full kegs first, and then use empty kegs. If you run out of regs for a particular potion type, it will move on to the next potion type, and update the status menu indicating which potion it could not complete, and how many it did not make. Please send me a PM if you have any comments, especially thoughts on how to make the script better.

Cael

Code:
;*************************************************
;*  Potion Maker
;*  Special Thanks To:  Kinslayer
;*  Author:  Cael
;*  Version:  2.3.7
;*  Client Tested with: 4.0.4b
;*  EUO version tested with: 1.42.0098
;*  Shard OSI / FS: OSI
;*  Revision Date: 10/02/04
;*  Public Release: 10/02/04
;*  Global Variables Used:
;*    *SecureContainer
;*    *SecureRegContainer
;*    *SecureFullContainer
;*    *SecurePartialContainer
;*    *SecureEmptyContainer
;*  Purpose: Create Potions & Fill Kegs including partiall full kegs.
;+=+=+=+=+=+=+=+=+=+=+=+=+=+=+=+=+=+=+=+=+=+=+=+=+=+=+=+=+=+=+=+=
;*  Instructions:
;*    1.  If you want to change any variables,
;*        check sub SetVars, such as whether to hide, lag time, amount to move...
;*    2.  Press Play.  If this is the first time
;*        you have run the script, click each button
;*        to set the IDs of the different bags.  
;*        You only need to do this once.
;*        Secure ID - container secured on house floor.
;*        Bag ID - container for resources inside secure.
;*        Full ID - container to store completed kegs.
;*        Partial ID - container that has partially full kegs
;*          that the script uses to complete orders.
;*        Empty ID - container to store empty kegs.
;*+++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++
;*+   3.  MOVE all bags to locations so that they are         +
;*+       NOT stacked on top of each other.  If you do not do +
;*+       this, script WILL FAIL.                             +
;*+++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++
;*    4.  Click Ok.  Follow the Menus.
;*    End of Instructions.
;*  Notes:
;*    You must have a minimum of 21 tinkering to even ATTEMPT
;*      to craft your own mortars & pestels.
;+=+=+=+=+=+=+=+=+=+=+=+=+=+=+=+=+=+=+=+=+=+=+=+=+=+=+=+=+=+=+=+=
;*  Things To Do:
;*    1.  Turn this into COMPLETE Alchemy Solution.
;*
;*  Version History:
;*  Version 0.1:  Initial Release
;*  Version 1.0:  Public Release
;*  Version 2.1:  Added Partial Keg Support
;*  Version 2.2:  Added out of regs, move to
;*                next potion support
;*  Version 2.3:  Added memory of Secure IDs
;*************************************************


;+=+=+=+=+=+=+=+=+=+=+=+=+=+=+=+=+=+=+=+=+=+=+=+=+=+=+=+=+=+=+=+=
;* Instructions:
;* 1. If you want to change any variables,
;* check sub SetVars, such as whether to hide, lag time, amount to move...
;* 2. Press Play. If this is the first time
;* you have run the script, click each button
;* to set the IDs of the different bags.
;* You only need to do this once.
;* Secure ID - container secured on house floor.
;* Bag ID - container for resources inside secure.
;* Full ID - container to store completed kegs.
;* Partial ID - container that has partially full kegs
;* that the script uses to complete orders.
;* Empty ID - container to store empty kegs.
;*+++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++
;*+ 3. MOVE all bags to locations so that they are +
;*+ NOT stacked on top of each other. If you do not do +
;*+ this, script WILL FAIL. +
;*+++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++
;* 4. Click Ok. Follow the Menus.
;* End of Instructions.
;* Notes:
;* You must have a minimum of 21 tinkering to even ATTEMPT
;* to craft your own mortars & pestels.