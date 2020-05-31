---
title: Convars
tags: 
 - convars
 - commands
 - developers
 - configuration
 - server owners
description: Documentation for convar configuration in the game
---

# Convars

## Client

### Convars

Nothing to show!

## Server

### Client restrictions

#### sv_allow_client_saveloc

__Type:__ `bool`  
__Description:__ Enable/disable clients ability to use [saveloc_teleport](commands#saveloc_teleport)  
__Affects:__

Affects:
    [`sv_allow_client_setpos`](config-variables/link-to-convar)
    [`sv_allow_client_setang`](config-variables/link-to-convar)
    [`sv_allow_client_setvel`](config-variables/link-to-convar)

#### sv_allow_client_setpos

__Type:__ `bool`  
__Description:__ Enable/disable clients ability to set desired position  
__Affects:__

Affects:
    `sv_allow_client_saveloc`](config-variables/link-to-convar)

#### sv_allow_client_setang

__Type:__ `bool`  
__Description:__ Enable/disable clients ability to set desired view angles  
__Affects:__

Affects:
    `sv_allow_client_saveloc`](config-variables/link-to-convar)

#### sv_allow_client_setvel

__Type:__ `bool`  
__Description:__ Enable/disable clients ability to set desired velocity  

__Affects:__

Affects:
    [`sv_allow_client_saveloc`](config-variables/link-to-convar)

#### sv_allow_client_noclip

__Type:__ `bool`  
__Description:__ Enable/disable clients ability to toggle noclip  
__Affects:__

* [toggle_noclip](commands#toggle_noclip)

#### sv_allow_client_block

__Type:__ `bool`  
__Description:__ Enable/disable clients ability to toggle blocking within a team  
__Affects:__

* [toggle_block](commands#toggle_block)

#### sv_sidespeed

__Type:__ `float`  
__Default:__ `400.0`  
__Description:__ Sets maximum sidespeed per tick

#### sv_forwardspeed

__Type:__ `float`  
__Default:__ `400.0`  
__Description:__ Sets maximum sidespeed per tick
