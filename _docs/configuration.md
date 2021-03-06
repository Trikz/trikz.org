---
title: Configuration
tags: 
 - convars
 - commands
 - developers
 - configuration
 - server owners
description: Documentation for convar configuration in the game
---

# Configuration

## Dedicated servers

### Downloading server

## Server convars

### Client restrictions

#### sv_allow_client_saveloc

__Type:__ `bool`  
__Default:__ `1`  
__Description:__ Enable/disable clients ability to use [saveloc_teleport](commands#saveloc_teleport)  
__Affects:__

* [saveloc's](commands#saveloc)
* [sv_allow_client_setpos](#sv_allow_client_setpos)
* [sv_allow_client_setang](#sv_allow_client_setang)
* [sv_allow_client_setvel](#sv_allow_client_setvel)

<a href="convars/sv_allow_client_saveloc"><button class="btn btn-primary">Detailed summary</button></a>

#### sv_allow_client_setpos

__Type:__ `bool`  
__Default:__ `1`  
__Description:__ Enable/disable clients ability to set desired position  
__Affects:__

* [saveloc's](commands#saveloc)
* [sv_allow_client_saveloc](#sv_allow_client_saveloc)

<a href="convars/sv_allow_client_setpos"><button class="btn btn-primary">Detailed summary</button></a>

#### sv_allow_client_setang

__Type:__ `bool`  
__Default:__ `1`  
__Description:__ Enable/disable clients ability to set desired view angles  
__Affects:__

* [saveloc's](commands#saveloc)
* [sv_allow_client_saveloc](#sv_allow_client_saveloc)

<a href="convars/sv_allow_client_setang"><button class="btn btn-primary">Detailed summary</button></a>

#### sv_allow_client_setvel

__Type:__ `bool`  
__Default:__ `1`  
__Description:__ Enable/disable clients ability to set desired velocity  
__Affects:__

* [saveloc's](commands#saveloc)
* [sv_allow_client_saveloc](#sv_allow_client_saveloc)

<a href="convars/sv_allow_client_setvel"><button class="btn btn-primary">Detailed summary</button></a>

#### sv_allow_client_noclip

__Type:__ `bool`  
__Default:__ `1`  
__Description:__ Enable/disable clients ability to toggle noclip  
__Affects:__

* [toggle_noclip](commands#toggle_noclip)

<a href="convars/sv_allow_client_noclip"><button class="btn btn-primary">Detailed summary</button></a>

#### sv_allow_client_block

__Type:__ `bool`  
__Default:__ `1`  
__Description:__ Enable/disable clients ability to toggle blocking within a team  
__Affects:__

* [toggle_block](commands#toggle_block)

<a href="convars/sv_allow_client_block"><button class="btn btn-primary">Detailed summary</button></a>

### Movement

#### sv_gravity

__Type:__ `float`  
__Default:__ `800.0`  
__Description:__ Sets global gravity  
__Affects:__

* Movement

<a href="convars/sv_gravity"><button class="btn btn-primary">Detailed summary</button></a>

#### sv_sidespeed

__Type:__ `float`  
__Default:__ `400.0`  
__Description:__ Sets maximum sidespeed per tick  
__Affects:__

* [sidemove](commands#sourcemod-TODO)

<a href="convars/sv_sidespeed"><button class="btn btn-primary">Detailed summary</button></a>

#### sv_forwardspeed

__Type:__ `float`  
__Default:__ `400.0`  
__Description:__ Sets maximum sidespeed per tick  
__Affects:__

* [forwardmove](commands#sourcemod-TODO)

<a href="convars/sv_forwardspeed"><button class="btn btn-primary">Detailed summary</button></a>
