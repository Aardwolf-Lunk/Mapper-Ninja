# MUSHclient-Aardwolf-Mapper_Ninja
Lunk's Mapper-Ninja for MUD Aardwolf
mninja help in-game will bring up this help :
Lunk's : 
             _____/~~~~~~~~~~~~~~~~~~~~_____
        ___ /=--- + *  Mapper Ninja  * + ---= ___
==========================================================

*** MAPPER  MOVEMENT : DATABASE ENTRY ***

mno  --->  enters north through a unlocked door into mapper database
mea  --->  enters east through a unlocked door into mapper database
mso  --->  enters south through a unlocked door into mapper database
mwe  --->  enters west through a unlocked door into mapper database
mup  --->  enters up through a unlocked door into mapper database
mdo  --->  enters down through a unlocked door into mapper database

mnol  --->  enters north through a locked door into mapper database
meal  --->  enters east through a locked door into mapper database
msol  --->  enters south through a locked door into mapper database
mwel  --->  enters west through a locked door into mapper database
mupl  --->  enters up through a locked door into mapper database
mdol  --->  enters down through a locked door into mapper database

mwait * --->  ONLY use this before attempting to enter a cexit into the database with multiple commands (seperated by ; or ;; if ; is already your command stacking character 
maze *  --->  enters movement direction (where * is a direction; n, e, s, w, u, d) and destination room into mapper database (good for navigating mazes)

*** MAPPER MOVEMENT : USING DATABASE ***

mgo *  --->  moves player to room i.d *

*** MAPPER SEARCHING ***

mfi *  --->  searches mapper database for room * in current area
mdb *  --->  searches mapper database for room * (whole database)

*** MAPPER PORTALS ***

mpor1 *                 --->  takes you to the destination of portal *
mapper portal mpor *    --->  enters portal * into mapper database
mporbag *               --->  sets * as portals bag
mporbag                 --->  displays portals bag
mhold *                 --->  sets hold item * for mapper portal database entry/general use
mhold                   --->  displays hold item
mporlist                --->  lists all portal mapper database entrys
mpordel #*              --->  deletes portal entry * where * is the portal index (#)
mlporbag                --->  looks (examines) your portals bag to show which portals you have 
  
*NOTE 1* : the # is necessary to indicate which portal to delete (the index of the database entry) so for example i wanted to delete portal at index 42 I would use : mpordel #42
*NOTE 2* : check the portals list after removeing each portal for multiple removals (when 1 is deleted all the ones after go down a digit) 

*** MISC ***

mroom   --->  displays cexits for current room
mclear  --->  removes custom exit database entrys for the current room
mxs     --->  sets target room (the room you are in) for current area (requires ww's S&D)
open    --->  attempts to open all compass direction (n,e,s,w,u,d)
close   --->  attempts to close all compass directions (n,e,s,w,u,d)
closel  --->  attempts to close and lock all compass directions (n,e,s,w,u,d)
mimt    --->  sets current room to mapper ignore mismatch = "true" (use in mazes or rooms where a normal cexit doesn't work)
mimf    --->  sets current room to mapper ignore mismatch = "false" (if accidentally set to true and any cexit is not working as intended)
mnpt *  --->  sets current room * (room I.D use "mroom") to no-portal = "true" (use if you already know the room is no-portal)
mnpf *  --->  sets current room * (room I.D use "mroom") to no-portal = "false" (use if you mistakenly used mnpt)
mnrt *  --->  sets current room * (room I.D use "mroom") to no-recall = "true" (use if you already know the room is no-recall)
mnrf *  --->  sets current room * (room I.D use "mroom") to no-recall = "false" (use if you mistakenly used mnrt)
rtp     --->  takes you to the beginning of the upper and lower planes so long as you have amulet of the planes in your portals bag

*NOTE 1* : mapper ignore mismatch is default to false for all rooms in the standard MUSHclient package
*NOTE 2* : mapper no-portal is default to false for all rooms in the standard MUSHclient package
*NOTE 3* : the mapper will always take the quickest path with ww's xrt including rooms set as no-portal and/or no recall
