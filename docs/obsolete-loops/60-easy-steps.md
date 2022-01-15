---
layout: default
title: 60 Easy Steps
nav_order: 2
parent: Obsolete Loops
---

# 60 Easy Steps

Some people have requested a description of the loop in words and not just listing the steps (a sort of TL;DR) so here we go...

You want to deterministically and shortcutably put draw triggers equal to the number of cards in your deck on the stack so that you can loop rituals to generate infinite mana. This is done using two tricks. The first trick draws you cards equal to the number of non-land cards, and the second trick draws you cards equal to the number of lands, which sum together for your whole deck.

Trick 1 - make a bunch of mana + life using rocks and nature's claim, shuffle them into your library with Gaea's Blessing + Noxious Revival, discard a bunch of lands equal to nonland cards to create draw triggers. Put those cards back into your hand without consuming the draw triggers using Ad Nauseam (which is why you needed to make the mana + life)

Trick 2 - discard all the lands in your hand to get the required number of draws, then use Chains of Mephistopheles + LED to create a "mill 1" effect, which you can't normally get from dredging dakmor. That lets you bin Gaea's Blessing for a shuffle, and then you can resolve the draw triggers to put deck in hand.

Once you have infinite mana you can loop assassins trophy as an outlet card by casting it while performing trick 2.

## Description

The following is a deterministic shortcutable loop that allows one to combo through an in play Anafenza assuming you are starting from a point of no mana and requiring only the standard Gitrog + Discard Outlet + Dakmor. This line requires no additional cards beyond what is already in most standard new-school lists. There are 3 main components to the combo: Drawing the Deck, The Setup, and the Loop. The first two of these steps are non-shortcutable and have failure conditions so keep that in mind as you will need to play them out.

In order to help you keep track of the loop and make it easier for you to verify I will be using the following notation and definitions...

Empty State: No cards are in your library or graveyard, and the stack is empty.

C= 1 Colourless Mana

G= 1 Green Mana

B= 1 Black Mana

(): Round brackets are for extra information

[]: Square brackets are used to keep track of the values that change within the loop and are of the form…

[Positive mana – Negative mana, Life change, Draw triggers, Cards in Library, Cards in Grave]

e.g.

(Empty State)

[0,0,0,0,0]

* Cast Dark Ritual

[-B,0,0,0,0]

* Resolve Dark Ritual

[BB,0,0,0,1]

Note: Unless I specify “respond to cast/activation” I will be jumping straight from cast to resolution.

## Drawing the deck

Getting to the Empty State from the starting state of Gitrog and Discard outlet in play and only Dakmor in hand.

Discard and dredge Dakmor, accumulating draw triggers until you hit GB (Gaea’s Blessing) at which point you let the shuffle resolve and continue on. Continue accumulating draw triggers until you have at least as many as you have cards in your library and graveyard (N). If you have exactly N draw triggers after resolving GB shuffle then simply resolve all your triggers and you’re done. Otherwise…

* Dredge Dakmor until you hit GB
* Resolve the shuffle
* Resolve your draw triggers until there is only 1 card left in library
* Discard GB
* Cast Noxious Revival targeting GB
* Discard and dredge Dakmor
* In response to GB shuffle discard either X-3 (if last card is a non-land) or X-2 (if last card is a land) non-lands where X is the number of draw triggers left on the stack
* Resolve shuffle trigger
* Resolve remaining draw triggers

## The Setup

Generating necessary initial mana and exiling superfluous non-lands.

## Phase 1: Mana

(From empty state)

* Cast Chrome Mox imprinting a non-necessary green card

Add G

[G,0,0,0,0]

* Discard 3 non-lands

[G,0,0,0,3]

* Cast GB targeting the 3 non-lands

[-C,0,0,2,1]

* Cast GSZ (Green Sun Zenith) for x=0

[-GC,0,0,3,1]

* Cast NR (Noxious Revival) targeting GB

[-GC,-2,0,4,1]

* Cast LP (Lotus Petal)

Crack for B

[B-GC,-2,0,4,2]

* Cast DR (Dark Ritual)

[BB-G,-2,0,4,3]

* Discard 4 non-lands

[BB-G,-2,0,4,7]

* Cast CR (Cabal ritual)

[BBBBB-G,-2,0,4,8]

* Cast LED (Lion’s Eye Diamond)

[BBBBB-G,-2,0,4,8]

* Discard and dredge Dakmor

[BBBBB-G,-2,0,2,10]

* Respond to shuffle trigger by cracking LED for GGG

[BBBBBGG,-2,1,2,all]

* Dredge Dakmor

[BBBBBGG,-2,0,0,all-dakmor]

* Resolve GB shuffle

[BBBBBGG,-2,0,all-dakmor,0]

We are now back where we were before the Drawing the Deck step except we now have the requisite mana to move to the second phase of setup…

## Phase 2: Mana + Exile

Perform the Drawing the Deck step to arrive at empty state.

(From empty state)

[BBBBBGG,-2,0,0,0]

* Cast Necropotence

[BBGG,-2,0,0,0]

* Discard unnecessary non-lands letting them get exiled to the Necropotence trigger such that at most you have M-1 non-lands including Necropotence (M = the total number of lands in hand at empty state including Dakmor)
* Cast NC (Nature’s Claim) targeting Necropotence

[BBG,2,0,0,2]

* Cast GSZ for x=0

[BB,2,0,1,2]

* Discard GB

[BB,2,0,1,3]

* Cast NR targeting GB

[BB,0,0,2,3]

* Cast LP and crack for G

[BBG,0,0,2,4]

* Cast LED and crack LED for GGG

[BBGGGG,0,1,2,all]

* Dredge Dakmor

[BBGGGG,0,0,0,all-dakmor]

* Resolve GB shuffle

[BBGGGG,0,0,all-dakmor,0]

* Perform the Drawing the Deck step to arrive at empty state

[BBGGGG,0,0,0,0]

We are now back where we were before the Drawing the Deck step except we have now reduced our non-lands in our deck by an appropriate amount and have the requisite mana to do the loop.

## The Loop

Generating infinite mana and looping a payoff spell.

After performing the previous steps this is our state: [BBGGGG,0,0,0,0]

This is sufficient to perform the loop but for clarity I’m going to use [0,0,0,0,0] as a starting state for the loop and use negative mana.

(From empty state)

* Cast LED

[0,0,0,0,0]

* Cast LP

[0,0,0,0,0]

* Cast MC (Mana Crypt)

Add CC

[CC,0,0,0,0]

* Cast NC targeting MC

[CC-G,4,0,0,2]

* Cast GB targeting NC

[C-GG,4,0,0,2]

* Cast Chain of Mephistopheles

[-BGG,4,0,0,2]

* Cast GSZ x=0

[-BGGG,4,0,1,2]

* Cast MD (Mox Diamond)

Add G

[-BGG,4,1,1,2+1]

* Responding to the draw trigger discard N-1 lands

[-BGG,4,N,1,2+N]

* Cast NR targeting GB

[-BGG,2,N,2,2+N]

* Discard and Dredge Dakmor

[-BGG,2,N,0,4+N]

* Responding to GB shuffle crack LP for G

[-BG,2,N,0,5+N]

* Cast NC targeting MD

o [-BGG,6,N,0,7+N]

* Cast CR

[BB-GG,6,N,0,8+N]

* Cast DR

[BBBB-GG,6,N,0,9+N]

* Resolve GB shuffle

[BBBB-GG,6,N,9+N,0]
​
(At this point your library should be: GB, DR, CR, NC, MD, LP, GSZ, NR, MC, + N lands)

* Cast Ad Nauseum drawing the whole library

[-GGC,-2,N,0,1]

* Discard GB

[-GGC,-2,N,0,2]

* Cast NR targeting GB

[-GGC,-4,N,1,2]

* Discard all lands in hand including Dakmor (M lands in total)

[-GGC,-4,N+M,1,2+M]

* Cast Entomb (don’t resolve)

[-BGGC,-4,N+M,1,2+M]

* Cast NC targeting Chains of Mephistopheles (don’t resolve)

[-BGGGC,-4,N+M,1,2+M]

* Cast DR

[B-GGGC,-4,N+M,1,3+M]

* Cast CR

[BBB-GGG,-4,N+M,1,4+M]

* *Special Cast*
* Cast Crop Rotation (draw trigger is generated)

[BBB-GGGG,-4,N+M+1,1,4+M+1]

* Respond to draw trigger by cracking LED for GGG (no lands in hand)

[BBB-G,-4,N+M+1,1,K+4+M+1]

* Resolve the Crop Rotation generated draw trigger as chains mill

[BBB-G,-4,N+M,0,K+5+M+1]

* Mill GB and resolve shuffle

[BBB-G,-4,N+M,K+5+M+1,0]

* Resolve Crop Rotation finding Twilight Mire

Filter B into GG

[BBG,-4,N+M,K+5+M,1]

* Resolve NC

[BBG,0,N+M,K+5+M,3]

* Resolve Entomb sending GB to grave

[BBG,0,N+M,K+5+M,5]

* Resolve GB shuffle

[BBG,0,N+M,K+10+M,0]

* Resolve N+M draw triggers

[BBG,0,0,0,0]

(empty state)

Notes:

K = the number of non-lands in hand at empty state including all combo pieces

M = the total number of lands in hand at empty state including Dakmor

N = can be up to M-1, and should be equal to K

You can alternate the crop rotation targets between twilight mire and any green source every other loop it only means you don’t net G in that iteration

You can use the same loop structure to cast instant speed payoff spells (e.g. Assassin’s Trophy) after generating infinite mana in the slot designated “*Special Cast*”

*This content was originally [posted on Reddit](https://old.reddit.com/r/CompetitiveEDH/comments/9rdzr7/gitrog_monster_titanless_combo_in_60_easy_steps/) by Noobzaurs.*
