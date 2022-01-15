---
layout: default
title: 20 Easy Steps
nav_order: 1
parent: Obsolete Loops
---

# 20 Easy Steps

## Prerequisites

* The Gitrog Monster on the battlefield
* A discard outlet on the battlefield
* An empty Graveyard and library
* At least one open black mana source

## Description

Now I'm not going to get into how to draw the deck with only Gaea's Blessing and Dakmor Salvage (Titanless), as that has already been covered in multiple posts before and that method has not changed. Nor am I going to get into how you would end up drawing the library without Dakmor Salvage - there are ways, just very convoluted ones I won't be covering either here - its just that this particular empty library deterministic loop does not use Dakmor Salvage at all. This may become more relevant at a later time when Gitrog lists discover another efficient way to draw the library in addition to Dakmor Salvage (something else I've been working on).

Following in line with Noobzaur's 60 Easy Steps; in order to help you keep track of the loop and make it easier for you to verify I will be using the following notation and definitions:

C= 1 Colourless Mana

G= 1 Green Mana

B= 1 Black Mana

[]: Square brackets are used to keep track of the values that change within the loop and are of the form:

[Positive mana – Negative mana, Life change, Draw triggers, Cards in Library, Cards in Grave]

e.g. [0,0,0,0,0] - This means that there is no mana floating, no life has been gained/lost, no draw triggers are on the stack, no cards are in the library, and no cards are in the graveyard. The starting state for this particular loop will actually be [0,0,0,0,1] since Ad Nauseam will be in the graveyard at the start of each loop iteration.

I will always assume that the spell has resolved unless otherwise specified or priority is held.

## Procedure

To begin with, discard Ad Nauseam. The starting state of the loop shall be defined by having an empty library and Ad Nauseam in the graveyard.

1. Starting state (with Ad Nauseam in the graveyard) [0,0,0,0,1]
1. Cast Dark Ritual [BB,0,0,0,2]
1. Cast Mana Crypt and tap it for mana [CCBB,0,0,0,2]
1. Cast and use Lotus Petal for a green mana [CCBBG,0,0,0,3]
1. Discard any four irrelevant non-land cards like Necropotence/Wild Growth [CCBBG,0,0,0,7]
1. Cast Cabal Ritual with threshold [CCBBBBBG,0,0,0,8]
1. Cast Gaea’s Blessing targeting Dark Ritual, Cabal Ritual, and Lotus Petal [CBBBBB,0,0,2,6]
1. Cast Mox Diamond, discarding a land and drawing a card [CBBBBBG,0,0,1,7]
1. Discard a land, drawing the last card in your library [CBBBBBG,0,0,0,8]
1. Cast Nature’s Claim using Mox Diamond, targeting Mox Diamond [CBBBBB,4,0,0,10]
1. Cast Dark Ritual / Cabal Ritual with Threshold / Lotus Petal for green mana again [CBBBBBBBBBBG,4,0,0,13]
1. Cast Noxious Revival, paying 2 life, targeting Gaea’s Blessing [CBBBBBBBBBBG,2,0,1,13]
1. Cast Entomb, putting Gaea’s Blessing into your graveyard, triggering Gaea’s Blessing [CBBBBBBBBBG,2,0,0,15]
1. Shuffle your graveyard into your library [CBBBBBBBBBG,2,0,15,0]
1. Cast Demonic Tutor, putting Entomb in your hand [BBBBBBBBG,2,0,14,1]
1. Cast Entomb, putting Gaea’s Blessing into your graveyard (hold priority) [BBBBBBBG,2,0,13,3]
1. Discard 13 lands, drawing your entire library [BBBBBBBG,2,0,0,16]
1. Cast Nature’s Claim targeting Mana Crypt [BBBBBBB,6,0,0,18]
1. Shuffle your graveyard into your library [BBBBBBB,6,0,18,0]
1. Cast Ad Nauseam for your entire library [BB,0,0,0,0]

This should have netted you 0 life and 2 black mana. If you run Ebony Charm then you can just actually add it to your initial cast, right after Dark Ritual at the start even and you won’t need to change anything to kill your opponents. Once you generate an arbitrary amount of black mana, you can fit in Emergence Zone via the method below to begin generating an arbitrary amount of green mana (this requires you to be at least at 5 or more life):
* Steps 1-7 are the same as above
* At step 8 discard Emergence Zone specifically
* Steps 9-15 are the same as above
* Before step 16:
    1. Cast Crop Rotation using the floating green mana available, sacrificing a land
    1. Cast Vampiric Tutor in response to the Gitrog trigger, putting Lotus Petal on top
    1. Draw Lotus Petal
    1. Resolve Crop Rotation, getting Emergence Zone
    1. Activate Emergence Zone, sacrificing it and getting a Gitrog trigger
    1. Draw a card and resolve Emergence Zone
    1. Cast and use Lotus Petal for a green mana
* Step 16 will now require 11 lands instead of 13
* Steps 17-19 are the same as above

This should have cost you exactly 4 life and 2 mana (one for Vampiric and one to activate Emergence Zone). And yes, you can in fact perform this on your very first iteration of the original loop above. In order to generate infinite green all you have to do is cast and use Lotus Petal for green mana between steps 16 and 17 for now on. To loop Assassin’s Trophy or any other card for now on, you just need to cast it before step 13 after generating an arbitrary amount of both green and black mana.

*This content was originally [posted on Reddit](https://old.reddit.com/r/CompetitiveEDH/comments/dbek5k/a_deterministic_gitrog_monster/) by Forge10.*
