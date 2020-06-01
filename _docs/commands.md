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

<button class="btn btn-primary" href="commands/toggle_noclip">Detailed summary</button>

#### toggle_block

__Usage:__ `toggle_noclip`  
__Description:__ Toggle blocking on yourself  
__Affected by:__

* [sv_allow_client_block](configuration#sv_allow_client_block)

<button class="btn btn-primary" href="commands/toggle_block">Detailed summary</button>

#### setpos

__Usage:__ `setpos <float:x> <float:y> <float:z>`  
__Description:__ Set position on yourself  
__Affected by:__

* [sv_allow_client_setpos](configuration#sv_allow_client_setpos)
* [sv_allow_client_saveloc](configuration#sv_allow_client_setpos)

<button class="btn btn-primary" href="commands/setpos">Detailed summary</button>

#### setang

__Usage:__ `setang <float:x> <float:y>`  
__Description:__ Set angles on yourself  
__Affected by:__

* [sv_allow_client_setang](configuration#sv_allow_client_setang)
* [sv_allow_client_saveloc](configuration#sv_allow_client_saveloc)

<button class="btn btn-primary" href="commands/setang">Detailed summary</button>

#### setvel

__Usage:__ `setvel <float:x> <float:y> <float:z>`  
__Description:__ Set velocity on yourself  
__Affected by:__

* [sv_allow_client_setvel](configuration#sv_allow_client_setvel)
* [sv_allow_client_saveloc](configuration#sv_allow_client_saveloc)

<button class="btn btn-primary" href="commands/setvel">Detailed summary</button>

### Saveloc

Saveloc's is managed by clients, and enabled by servers via the convar [sv_allow_client_saveloc](configuration#sv_allow_client_saveloc).  
  
This is a key feature that allows clients to perfectly predict teleporting to saveloc's with desired position, velocity and angles which makes practicing intricate and narrow paths very pleasant.  
  
Internally the saveloc system is just a list of saveloc's that can be accessed with a name or index number through various commands.  

#### saveloc_toggle_use_pos

__Usage:__  `saveloc_toggle_use_pos`  
__Description:__ Toggles if [saveloc_teleport](#saveloc_teleport) should use position when teleporting  

<button class="btn btn-primary" href="commands/saveloc_toggle_use_pos">Detailed summary</button>

#### saveloc_toggle_use_ang

__Usage:__  `saveloc_toggle_use_ang`  
__Description:__ Toggles if [saveloc_teleport](#saveloc_teleport) should use angles when teleporting  

<button class="btn btn-primary" href="commands/saveloc_toggle_use_ang">Detailed summary</button>

#### saveloc_toggle_use_vel

__Usage:__  `saveloc_toggle_use_vel`  
__Description:__ Toggles if [saveloc_teleport](#saveloc_teleport) should use velocity when teleporting  

<button class="btn btn-primary" href="commands/saveloc_toggle_use_vel">Detailed summary</button>

#### saveloc_teleport

__Usage:__ `saveloc_teleport [idx|name]`  
__Description:__ Triggers a teleport event with saveloc information  
__Affected by:__

* [sv_allow_client_saveloc](configuration#sv_allow_client_saveloc)

<button class="btn btn-primary" href="commands/saveloc_teleport">Detailed summary</button>

#### saveloc_delete

__Usage:__ `saveloc_delete [idx|name]`  
__Description:__ Deletes saveloc entry in list  

<button class="btn btn-primary" href="commands/saveloc_delete">Detailed summary</button>

#### saveloc_clear

__Usage:__ `saveloc_clear`  
__Description:__ Deletes all saveloc entries for current map  

<button class="btn btn-primary" href="commands/saveloc_clear">Detailed summary</button>

#### saveloc_insert

__Usage:__ `saveloc_insert <"after"|"before"> [idx|name]`  
__Description:__ Inserts a new saveloc entry that uses the players information for pos/ang/vel  

<button class="btn btn-primary" href="commands/saveloc_insert">Detailed summary</button>

#### saveloc_save

__Usage:__ `saveloc_save`  
__Description:__ Alias for `saveloc_insert` which inserts it at current index  

<button class="btn btn-primary" href="commands/saveloc_save">Detailed summary</button>

#### saveloc_select

__Usage:__ `saveloc_select <idx|name>`  
__Description:__ Change caret to desired index  

<button class="btn btn-primary" href="commands/saveloc_select">Detailed summary</button>

#### saveloc_next

__Usage:__ `saveloc_next`  
__Description:__ Alias for `saveloc_select current_index - 1`  

<button class="btn btn-primary" href="commands/saveloc_next">Detailed summary</button>

#### saveloc_prev

__Usage:__ `saveloc_prev`  
__Description:__ Alias for `saveloc_select current_index - 1`  

<button class="btn btn-primary" href="commands/saveloc_prev">Detailed summary</button>
