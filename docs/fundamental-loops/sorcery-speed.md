---
layout: default
title: Sorcery Loop
nav_order: 5
parent: Fundamental Loops
has_children: true
permalink: docs/fundamental-loops/sorcery-speed/
---

# Basic Sorcery-speed Loop

You can use this basic loop to cast any sorcery an arbitrary number of times. For example you can [loop Lotus Petal](../basic-loops/lotus-petal.md) to create an unbounded amount of mana.

## Requirements

* A discard outlet in play
* Empty stack, library
* Graveyard contains only Life from the Loam
* Unbounded mana

## Procedure

1. Cast and resolve [*sorcery*]
1. Discard a titan, resolve shuffle trigger
1. Discard 3 lands and resolve those draw triggers
1. Cast Life from the Loam targeting the 3 lands in your graveyard

You are now back at your initial board state after having cast a sorcery spell.
