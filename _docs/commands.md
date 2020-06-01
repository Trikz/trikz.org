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

These commands are essential to properly predicting client movement when teleporting around, or when the client wants to modify his movement instantaneously.

#### toggle_noclip

__Usage:__ `toggle_noclip`  
__Description:__ Toggle noclip on yourself  
__Affected by:__

* [sv_allow_client_noclip](configuration#sv_allow_client_noclip)
* [sv_noclip_speed](configuration#sv_noclip_speed)

<a href="commands/toggle_noclip"><button class="btn btn-primary">Detailed summary</button></a>

#### toggle_block

__Usage:__ `toggle_noclip`  
__Description:__ Toggle blocking on yourself  
__Affected by:__

* [sv_allow_client_block](configuration#sv_allow_client_block)

<a href="commands/toggle_block"><button class="btn btn-primary">Detailed summary</button></a>

#### setpos

__Usage:__ `setpos <float:x> <float:y> <float:z>`  
__Description:__ Set position on yourself  
__Affected by:__

* [sv_allow_client_setpos](configuration#sv_allow_client_setpos)
* [sv_allow_client_saveloc](configuration#sv_allow_client_setpos)

<a href="commands/setpos"><button class="btn btn-primary">Detailed summary</button></a>

#### setang

__Usage:__ `setang <float:x> <float:y>`  
__Description:__ Set angles on yourself  
__Affected by:__

* [sv_allow_client_setang](configuration#sv_allow_client_setang)
* [sv_allow_client_saveloc](configuration#sv_allow_client_saveloc)

<a href="commands/setang"><button class="btn btn-primary">Detailed summary</button></a>

#### setvel

__Usage:__ `setvel <float:x> <float:y> <float:z>`  
__Description:__ Set velocity on yourself  
__Affected by:__

* [sv_allow_client_setvel](configuration#sv_allow_client_setvel)
* [sv_allow_client_saveloc](configuration#sv_allow_client_saveloc)

<a href="commands/setvel"><button class="btn btn-primary">Detailed summary</button></a>

### Saveloc

Saveloc's is managed by clients, and enabled by servers via the convar [sv_allow_client_saveloc](configuration#sv_allow_client_saveloc).  
  
This is a key feature that allows clients to perfectly predict teleporting to saveloc's with desired position, velocity and angles which makes practicing intricate and narrow paths very pleasant.  
  
Internally the saveloc system is just a list of saveloc's that can be accessed with a name or index number through various commands.  

#### saveloc_toggle_use_pos

__Usage:__  `saveloc_toggle_use_pos`  
__Description:__ Toggles if [saveloc_teleport](#saveloc_teleport) should use position when teleporting  

<a href="commands/saveloc_toggle_use_pos"><button class="btn btn-primary">Detailed summary</button></a>

#### saveloc_toggle_use_ang

__Usage:__  `saveloc_toggle_use_ang`  
__Description:__ Toggles if [saveloc_teleport](#saveloc_teleport) should use angles when teleporting  

<a href="commands/saveloc_toggle_use_ang"><button class="btn btn-primary">Detailed summary</button></a>

#### saveloc_toggle_use_vel

__Usage:__  `saveloc_toggle_use_vel`  
__Description:__ Toggles if [saveloc_teleport](#saveloc_teleport) should use velocity when teleporting  

<a href="commands/saveloc_toggle_use_vel"><button class="btn btn-primary">Detailed summary</button></a>

#### saveloc_teleport

__Usage:__ `saveloc_teleport [idx|name]`  
__Description:__ Triggers a teleport event with saveloc information  
__Affected by:__

* [sv_allow_client_saveloc](configuration#sv_allow_client_saveloc)

<a href="commands/saveloc_teleport"><button class="btn btn-primary">Detailed summary</button></a>

#### saveloc_delete

__Usage:__ `saveloc_delete [idx|name]`  
__Description:__ Deletes saveloc entry in list  

<a href="commands/saveloc_delete"><button class="btn btn-primary">Detailed summary</button></a>

#### saveloc_clear

__Usage:__ `saveloc_clear`  
__Description:__ Deletes all saveloc entries for current map  

<a href="commands/saveloc_clear"><button class="btn btn-primary">Detailed summary</button></a>

#### saveloc_insert

__Usage:__ `saveloc_insert <"after"|"before"> [idx|name]`  
__Description:__ Inserts a new saveloc entry that uses the players information for pos/ang/vel  

<a href="commands/saveloc_insert"><button class="btn btn-primary">Detailed summary</button></a>

#### saveloc_save

__Usage:__ `saveloc_save`  
__Description:__ Alias for `saveloc_insert` which inserts it at current index  

<a href="commands/saveloc_save"><button class="btn btn-primary">Detailed summary</button></a>

#### saveloc_select

__Usage:__ `saveloc_select <idx|name>`  
__Description:__ Change caret to desired index  

<a href="commands/saveloc_select"><button class="btn btn-primary">Detailed summary</button></a>

#### saveloc_next

__Usage:__ `saveloc_next`  
__Description:__ Alias for `saveloc_select current_index - 1`  

<a href="commands/saveloc_next"><button class="btn btn-primary">Detailed summary</button></a>

#### saveloc_prev

__Usage:__ `saveloc_prev`  
__Description:__ Alias for `saveloc_select current_index - 1`  

<a href="commands/saveloc_prev"><button class="btn btn-primary">Detailed summary</button></a>
