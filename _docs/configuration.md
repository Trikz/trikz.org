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

### Convars

## Server configuration

### Convars

A list of server convars and a description.

#### sv_allow_client_saveloc

type: bool
values:
    1: Allows clients to use saveloc functionality
    0: Disallows clients to use saveloc functionality

Affects:
    [`sv_allow_client_setpos`](link-to-convar)
    [`sv_allow_client_setang`](link-to-convar)
    [`sv_allow_client_setvel`](link-to-convar)

#### sv_allow_client_setpos

type: bool
values:
    1: Allows clients to use setpos functionality
    0: Disallows clients to use setpos functionality

Affects:
    `sv_allow_client_saveloc`](link-to-convar)

#### sv_allow_client_setang

type: bool
values:
    1: Allows clients to use setang functionality
    0: Disallows clients to use setang functionality

Affects:
    `sv_allow_client_saveloc`](link-to-convar)

#### sv_allow_client_setvel

type: bool
values:
    1: Allows clients to use setvel functionality
    0: Disallows clients to use setvel functionality

Affects:
    [`sv_allow_client_saveloc`](link-to-convar)

#### sv_allow_client_noclip

type: bool
values:
    1: Allows clients to use noclip functionality
    0: Disallows clients to use noclip functionality

#### sv_allow_client_block

type: bool
values:
    1: Allows clients to use blocking functionality within their team
    0: Disallows clients to use blocking functionality within their team

#### sv_sidespeed

type: float
default: 400.0
values:
    any float: Sets maximum sidespeed per tick

#### sv_forwardspeed

type: float
default: 400.0
values:
    any float: Sets maximum forwardspeed per tick
