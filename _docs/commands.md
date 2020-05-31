---
title: Commands
tags: 
 - convars
 - commands
 - developers
 - server owners
description: Documentation for commands in the game
---

# Commands

## Client commands

### Essentials

#### toggle_noclip

__Usage:__ `toggle_noclip`  
__Description:__ Toggle noclip on yourself  
__Affected by:__

* [sv_allow_client_noclip](configuration#sv_allow_client_noclip)
* [sv_noclip_speed](configuration#sv_noclip_speed)

#### toggle_block

__Usage:__ `toggle_noclip`  
__Description:__ Toggle blocking on yourself  
__Affected by:__

* [sv_allow_client_block](configuration#sv_allow_client_block)

#### setpos

__Usage:__ `setpos <float:x> <float:y> <float:z>`  
__Description:__ Set position on yourself  
__Affected by:__

* [sv_allow_client_saveloc](configuration#sv_allow_client_saveloc)
* [sv_allow_client_setpos](configuration#sv_allow_client_setpos)

#### setang

__Usage:__ `setang <float:x> <float:y>`  
__Description:__ Set angles on yourself  
__Affected by:__

* [sv_allow_client_saveloc](configuration#sv_allow_client_saveloc)
* [sv_allow_client_setang](configuration#sv_allow_client_setang)

#### setvel

__Usage:__ `setvel <float:x> <float:y> <float:z>`  
__Description:__ Set velocity on yourself  
__Affected by:__

* [sv_allow_client_saveloc](configuration#sv_allow_client_saveloc)
* [sv_allow_client_setvel](configuration#sv_allow_client_setvel)

### Saveloc

Saveloc's is managed by clients, and enabled by servers via the convar [`sv_allow_client_saveloc`](link-to-convar).  
  
This is a key feature that allows clients to perfectly predict teleporting to saveloc's with desired position, velocity and angles which makes practicing intricate and narrow paths very pleasant.  
  
Internally the saveloc system is just a list of saveloc's that can be accessed with a name or index number through various commands.  

#### saveloc_toggle_use_pos

__Usage:__ `saveloc_toggle_use_pos`  
__Description:__ Toggles if [saveloc_teleport](commands#saveloc_teleport) should use position when teleporting  

#### saveloc_toggle_use_ang

__Usage:__ `saveloc_toggle_use_ang`  
__Description:__ Toggles if [saveloc_teleport](commands#saveloc_teleport) should use angles when teleporting  

#### saveloc_toggle_use_vel

__Usage:__ `saveloc_toggle_use_vel`  
__Description:__ Toggles if [saveloc_teleport](commands#saveloc_teleport) should use velocity when teleporting  

#### saveloc_teleport

__Usage:__ `saveloc_teleport [idx|name]`  
__Notes:__ If no argument is given, current index is used instead  
__Description:__ Triggers a teleport event with saveloc information  
__Affected by:__

* [sv_allow_client_saveloc](configuration#sv_allow_client_saveloc)

#### saveloc_delete

__Usage:__ `saveloc_delete [idx|name]`  
__Notes:__ If no argument is given, current index is used instead  
__Description:__ Deletes saveloc entry in list  

#### saveloc_clear

__Usage:__ `saveloc_clear`  
__Description:__ Deletes all saveloc entries for current map  

#### saveloc_insert

__Usage:__ `saveloc_insert <"after"|"before"> [idx|name]`  
__Notes:__ Needed argument "after" or "before" which puts the entry after or before the index used, if no argument is given, current index is used instead  
__Description:__ Inserts a new saveloc entry that uses the players information for pos/ang/vel  

#### saveloc_save

__Usage:__ `saveloc_save`  
__Description:__ Alias for `saveloc_insert` which inserts it at current index  

#### saveloc_select <idx|name>

__Usage:__ `saveloc_select <idx|name>`  
__Description:__ Change caret to desired index  

#### saveloc_next

__Usage:__ `saveloc_next`  
__Description:__ Alias for `saveloc_select current_index - 1`  

#### saveloc_prev

__Usage:__ `saveloc_next`  
__Description:__ Alias for `saveloc_select current_index - 1`  

## Server commands
