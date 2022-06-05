---
layout: default
title: Titanless
nav_order: 2
parent: Auxiliary Loops
---

# The 25 Easy Steps

The *X Easy Steps* series is an evolution of loops which allows Gitrog to win without access to a Titan shuffle effect. These are sometimes refered to as "Titanless loops". The first was Noobzaurs’ *60 Easy Steps* which was refined by ForgottenKane (Forge10) into the *20 Easy Steps*, then finally bendinguy’s two loops *25 Easy Steps* and *Budget Easy Steps*. Credit goes also to biopower and mazeTemporal of course.

The main premise of these loops is to use Gaea's Blessing as a shuffler for comboing. This is done with 3 cards: Blessing, Noxious Revival, and Entomb. The combination of these cards allows us to cast and recast any spell multiple times before using Ad Nauseam to get them all back.

This loop cuts 5 cards (Cabal Ritual, Emergence Zone, Demonic Tutor, Crop Rotation, and Vampiric Tutor) from the current standard: 20 Easy Steps. That's a lot of cards we don't need for these loops anymore. The loop below only requires 9 different and specific cards to work (it also needs 23 lands but the deck runs ~34 anyways)

Here I'll also post the updated method to drawing the deck without a titan available as a shuffler:

Accumulate draw triggers until you have at least N+4 draw triggers on the stack where N is the number of cards in your library. Continue to dredge your library until you shuffle everything back in and then perform the following steps:

1. Resolve draw triggers until you have no cards left in your library and then hold priority
1. Cast Dark Ritual
1. Discard Gaea’s Blessing
1. Cast Noxious Revival targeting Gaea’s Blessing
1. Cast Entomb getting Gaea’s Blessing
1. In response to the the shuffle trigger, discard X-4 nonland cards where X is the number of draw triggers left on the stack.

## Requirements

The starting state will be defined as: an empty library, one black mana, Ad Nauseam in graveyard, Gitrog and an outlet in play, all other cards in hand. 

## Procedure

1. Cast Dark Ritual
1. Cast Lotus Petal and activate for a green
1. Cast Mana Crypt and activate
1. Cast Nature’s Claim targeting Mana Crypt
1. Discard Gaea’s Blessing
1. Cast Noxious Revival, paying two life, targeting Gaea’s Blessing
1. Cast Entomb finding Gaea’s Blessing and shuffle
1. Discard 8 lands to draw 8 cards
1. Cast Dark Ritual
1. Cast Lotus Petal and activate for a green
1. Cast Mana Crypt and activate
1. Cast Nature’s Claim targeting Mana Crypt
1. Discard Gaea’s Blessing
1. Cast Noxious Revival, paying two life, targeting Gaea’s Blessing
1. Cast Entomb finding Gaea’s Blessing and shuffle
1. Discard 8 lands to draw 8 cards. Discard one of the lands drawn this way and continue discarding lands drawn in this step until your library is empty
1. Cast Dark Ritual
1. Cast Lotus Petal and activate for a green
1. Cast Mana Crypt
1. Cast Nature's Claim targeting Mana Crypt
1. Discard Gaea's Blessing
1. Cast Noxious Revival, paying 2 life, targeting Gaea's Blessing
1. Cast Entomb and shuffle
1. Cast Ad Nauseam for your entire library

## Modifications

This loop costs a black to start and produces: 2 black mana and 3 colorless mana. Repeating this process will net you an arbitrary amount of black mana.

After making black mana, skip step 17 and you will net 1 life for each subsequent cycle. Use this to gain an arbitrary amount of life. We need this life-gain to proceed to making green, as well as being a useful means of facilitating a win.

Once you have black mana and life, you can make green mana by skipping steps 19 and 20,  saving the green mana generated in step 18. With all our resources at arbitrary values, you can loop any spell by casting it between steps 17 and 18. I recommend looping Assassin's Trophy and Thoughtseize to ensure nobody has any resources left. You can kill people by pumping Gitrog with Finale of Devastation and any creatures you happen to have left on board (others are exiled, remember).

This is also subject to some swapping due to the redundancy of certain effects we run:

1. Cabal Ritual is a direct replacement for Dark Ritual, but requires an extra colorless to start. No modifications needed to gain threshold bonus as it easily nets mana with the exact steps.
1. Mana Vault directly replaces Mana Crypt except in step 19, but will instead produce 1 black and 2 colorless. After the first iteration, switch to casting Mana Vault for colorless instead of black to net black mana.
1. Chrome Mox directly replaces Mana Crypt in step 19, don’t imprint anything.
1. Mox Diamond replaces Chrome Mox, but requires some tweaks: In step 16, instead of discarding a land to draw the last card in your deck, cast Mox Diamond and let that serve as the draw for that step.

*This content was originally [posted on Reddit](https://old.reddit.com/r/CompetitiveEDH/comments/f58tvk/gitrog_monster_titanless_combo_in_25_easy_steps/) by bendinguy.*
