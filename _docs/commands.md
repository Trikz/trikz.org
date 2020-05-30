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

Client commands

### Essentials

#### toggle_noclip

Usage: `toggle_noclip`  
Description: Toggle noclip on yourself  
__Affected by:__

* [sv_allow_client_noclip](configuration#sv_allow_client_noclip)
* [sv_noclip_speed](configuration#sv_noclip_speed)

#### toggle_block

Usage: `toggle_block`  
Description: Toggle blocking on yourself  
__Affected by:__

* [sv_allow_client_block](configuration#sv_allow_client_block)

#### setpos

Usage: `setpos <float:x> <float:y> <float:z>`  
Description: Set position on yourself  
__Affected by:__

* [sv_allow_client_saveloc](configuration#sv_allow_client_saveloc)
* [sv_allow_client_setpos](configuration#sv_allow_client_setpos)
  
#### setang

Usage: `setang <float:x> <float:y>`  
Description: Set angles on yourself  
__Affected by:__

* [sv_allow_client_saveloc](configuration#sv_allow_client_saveloc)
* [sv_allow_client_setang](configuration#sv_allow_client_setang)

#### setvel

Usage: `setvel <float:x> <float:y> <float:z>`  
Description: Set velocity on yourself  
__Affected by:__

* [sv_allow_client_saveloc](configuration#sv_allow_client_saveloc)
* [sv_allow_client_setvel](configuration#sv_allow_client_setvel)

### Saveloc

Saveloc's is managed by clients, and enabled by servers via the convar [`sv_allow_client_saveloc`](link-to-convar).  
  
This is a key feature that allows clients to perfectly predict teleporting to saveloc's with desired position, velocity and angles which makes practicing intricate and narrow paths very pleasant.  
  
Internally the saveloc system is just a list of saveloc's that can be accessed with a name or index number through various commands.  

#### saveloc_toggle_use_pos

Usage: `saveloc_toggle_use_pos`  
Description: Toggles if [saveloc_teleport](commands/#saveloc_teleport) should use position when teleporting  

#### saveloc_toggle_use_ang

Usage: `saveloc_toggle_use_ang`  
Description: Toggles if [saveloc_teleport](commands/#saveloc_teleport) should use angles when teleporting  

#### saveloc_toggle_use_vel

Usage: `saveloc_toggle_use_vel`  
Description: Toggles if [saveloc_teleport](commands/#saveloc_teleport) should use velocity when teleporting  

#### saveloc_teleport

Usage: `saveloc_teleport [idx|name]`  
Description: Triggers a teleport event with saveloc information  
Notes: If no argument is given, current index is used instead  
__Affected by:__

* [sv_allow_client_saveloc](configuration#sv_allow_client_saveloc)

#### saveloc_delete

Usage: `saveloc_delete [idx|name]`  
Description: Deletes saveloc entry in list  
Notes: If no argument is given, current index is used instead  

#### saveloc_clear

Usage: `saveloc_clear`  
Description: Deletes all saveloc entries for current map  

#### saveloc_insert

Usage: `saveloc_insert <"after"|"before"> [idx|name]`  
Description: Inserts a new saveloc entry that uses the players information for pos/ang/vel  
Notes: Needed argument "after" or "before" which puts the entry after or before the index used, if no argument is given, current index is used instead  

#### saveloc_save

Usage: `saveloc_save`  
Description: Alias for `saveloc_insert` which inserts it at current index  

#### saveloc_select <idx|name>

Usage: `saveloc_select <idx|name>`  
Description: Change caret to desired index  

#### saveloc_next

Usage: `saveloc_next`  
Description: Alias for `saveloc_select current_index - 1`  

#### saveloc_prev

Usage: `saveloc_next`  
Description: Alias for `saveloc_select current_index - 1`  

## Server commands
