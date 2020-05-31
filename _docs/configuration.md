---
title: Configuration
tags: 
 - convars
 - commands
 - developers
 - configuration
 - server owners
description: Documentation for configuration in the game
---

# Configuration

## Client configuration

## Server configuration

### Client restrictions

#### sv_allow_client_saveloc

__Type:__ `bool`  
__Description:__ Enable/disable clients ability to use [saveloc_teleport](commands#saveloc_teleport)  
__Affects:__

* [saveloc_teleport](commands#saveloc_teleport)
* [sv_allow_client_setpos](configuration#sv_allow_client_setpos)
* [sv_allow_client_setang](configuration#sv_allow_client_setang)
* [sv_allow_client_setvel](configuration#sv_allow_client_setvel)

#### sv_allow_client_setpos

__Type:__ `bool`  
__Description:__ Enable/disable clients ability to set desired position  
__Affects:__

* [setpos](commands#setpos)
* [sv_allow_client_saveloc](configuration#sv_allow_client_saveloc)

#### sv_allow_client_setang

__Type:__ `bool`  
__Description:__ Enable/disable clients ability to set desired view angles  
__Affects:__

* [setang](commands#setang)
* [sv_allow_client_saveloc](configuration#sv_allow_client_saveloc)

#### sv_allow_client_setvel

__Type:__ `bool`  
__Description:__ Enable/disable clients ability to set desired velocity  

__Affects:__

* [setvel](commands#setvel)
* [sv_allow_client_saveloc](configuration#sv_allow_client_saveloc)

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
