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

#### toggle_noclip

usage: `toggle_block`
description: Toggle noclip on yourself

affected by:
    [`sv_allow_client_noclip`](link-to-convar)
    [`sv_noclip_speed`](link-to-convar) 

#### toggle_block

usage: `toggle_block`
description: Toggle blocking on yourself

affected by:
    [`sv_allow_client_block`](link-to-convar)

#### setpos

usage: `setpos <float:x> <float:y> <float:z>`
description: Set position on yourself

affected by:
    [`sv_allow_client_setpos`](link-to-convar)
    [`sv_allow_client_saveloc`](link-to-convar)

#### setang

usage: `setang <float:x> <float:y>`
description: Set angles on yourself

affected by:
    [`sv_allow_client_setang`](link-to-convar)
    [`sv_allow_client_saveloc`](link-to-convar)

#### setvel

usage: `setvel <float:x> <float:y> <float:z>`
description: Set velocity on yourself

affected by:
    [`sv_allow_client_setvel`](link-to-convar)
    [`sv_allow_client_saveloc`](link-to-convar)

### Saveloc

Saveloc's is managed by clients, and enabled by servers via the convar [`sv_allow_client_saveloc`](link-to-convar).

This is a key feature that allows clients to perfectly predict teleporting to saveloc's with desired position, velocity and angles which makes practicing intricate and narrow paths very pleasant.

Internally the saveloc system is just a list of saveloc's that can be accessed with a name or index number through various commands.

#### saveloc_toggle_use_pos

usage: `saveloc_toggle_use_pos`
description: Toggles if [`saveloc_teleport`)[link-to-cmd] should use position when teleporting

#### saveloc_toggle_use_ang

usage: `saveloc_toggle_use_ang`
description: Toggles if [`saveloc_teleport`)[link-to-cmd] should use angles when teleporting

#### saveloc_toggle_use_vel

usage: `saveloc_toggle_use_vel`
description: Toggles if [`saveloc_teleport`)[link-to-cmd] should use velocity when teleporting

#### saveloc_teleport

usage: `saveloc_teleport [idx|name]`
    If no argument is given, current index is used instead

description: Triggers a teleport event with saveloc information
affected by: [`sv_allow_client_saveloc`](link-to-convar)

#### saveloc_delete

usage: `saveloc_delete [idx|name]`
    If no argument is given, current index is used instead
description: Deletes saveloc entry in list

#### saveloc_clear

usage: `saveloc_clear`
description: Deletes all saveloc entries for current map

#### saveloc_insert

usage: `saveloc_insert <"after"|"before"> [idx|name]`
    Needed argument "after" or "before" which puts the entry after or before the index used
    If no argument is given, current index is used instead
description: Inserts a new saveloc entry that uses the players information for pos/ang/vel

#### saveloc_save

usage: `saveloc_save`
description: Alias for `saveloc_insert` which inserts it at current index

#### saveloc_select <idx|name>

usage: `saveloc_select <idx|name>`
description: Change caret to desired index

#### saveloc_next

usage: `saveloc_next`
description: Alias for `saveloc_select current_index - 1`

#### saveloc_prev

usage: `saveloc_next`
description: Alias for `saveloc_select current_index - 1`

## Server commands
