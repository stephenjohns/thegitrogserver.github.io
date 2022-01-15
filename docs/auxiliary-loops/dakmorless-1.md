---
layout: default
title: Dakmorless 1
nav_order: 7
parent: Auxiliary Loops
---

# Dakmorless Loop Method 1

These are new Dakmorless infinite mana loops with Crop Rotation and Gaea's Cradle utilizing Survival of the Fittest to shuffle the graveyard into the library by discarding and searching an Eldrazi titan through Survival. This method of shuffling allows us to shuffle in our graveyard without adding another card to our yard/library. Crop Rotation serves as our very own Ancestral Recall because it draws us a card for the additional cost we pay, searches a land from our library and by discarding the land we draw off the gitrog trigger during the loop we generate our third draw. Before each “draw” we shuffle in with survival/titan.

## Requirements

As this is a Dakmorless line we are assuming we emptied our library with Tainted Pact, as this is the only reliable way of doing so without Dakmor.

* Note the cards in your graveyard (`N`)
* A total of 5 creatures in play
* A discard outlet in play
* The Gitrog Monster in play
* Survival of the Fittest in play
* Crop Rotation in hand
* Gaea’s Cradle in hand
* A titan in hand
* `N` lands in hand
* GGG mana available with at least one land in play

## Procedure

### Setting up, getting Gaea’s Cradle into play

1. Cast Crop Rotation sacrificing a land, holding priority on the draw trigger
1. Discard titan to Survival and hold priority on the draw trigger
1. Discard N lands (including Gaea’s Cradle) and then resolve N+1 draw triggers (this is a fixed amount for any given situation)
1. Discard a land drawn in step 3 (you will always have at least one) and continue discarding lands as they are drawn until your library is empty
1. In response to Crop Rotation discard titan to Survival
1. Resolve Crop Rotation finding Gaea’s Cradle and activate for GGGGG

### Gaea’s Cradle on the board and Crop Rotation in the graveyard

1. Discard titan to Survival and shuffle
1. This step depends on your specifics a. If N > 1, discard 2 lands b. if N = 1, discard a land and skip step 3
1. Discard a land drawn in step 2 (you will always have at least one) and continue discarding lands as they are drawn until your library is empty
1. Discard titan to Survival and shuffle
1. Cast Crop Rotation sacrificing Gaea’s Cradle, draw a card, holding priority on CR
1. Discard titan to survival and shuffle
1. Resolve Crop Rotation finding Gaea’s Cradle

To win the game, the first thing you need to do is clear your library / graveyard of extra lands. We can do this by using Life From the Loam as it removes 3 lands, while needing only 1 to draw it back. Because this phase is very vague, I’ll just describe it rather than list out steps.

* Chain your lands so that your library is empty and your graveyard is full of lands
* Cast Loam to get back 3 of those
* Discard your titan through Survival to shuffle in
* Chain your land discards to draw your library and repeat until you reach a point where Loam is the only card in your graveyard

### Looping spells

1. Cast your spell of choice (use Lotus Petal as an example)
1. Discard titan through Survival to shuffle
1. Discard 2 lands to draw two cards
1. Cast Lotus Petal
1. Discard titan through Survival
1. Discard two lands to draw two cards
1. Discard the land drawn in step 6
1. Cast Loam targeting the lands in your graveyard

Note that this can be used to generate black mana by casting Dark Ritual or Lotus Petal at sorcery speed.

Alternatively, you can use this method to switch from Gaea's Cradle to a black land:

1. Cast Crop Rotation sacrificing Gaea’s Cradle, holding priority on the draw trigger
1. Discard titan to Survival and hold priority on the draw trigger
1. Discard N lands (including a Swamp or any black producing land) and then resolve N+1 draw triggers (this is a fixed amount for any given situation)
1. Discard a land drawn in step 3 (you will always have at least one) and continue discarding lands as they are drawn until your library is empty
1. In response to Crop Rotation discard titan to Survival
1. Resolve Crop Rotation finding the Swamp and activate for B

Once the swamp is in play, it's the same process as with Cradle to loop it.

If we are limited to instant speed loops we can use Ad Nauseam to loop Assassin’s Trophy after creating infinite mana of any color.

1. After resolving Crop Rotation cast Ad Nauseam to draw your library which only includes lands at this point.
1. Cast Assassin’s Trophy
1. Discard titan to Survival and shuffle
1. Discard three lands, one at a time to draw your library
1. Discard titan to survival and shuffle
1. Cast Ad Nauseam for the lands discarded in step 4

Repeat steps 2-6, but discard two lands during step 4 to destroy all permanents.
