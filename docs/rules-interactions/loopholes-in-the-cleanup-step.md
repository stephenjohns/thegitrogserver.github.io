---
layout: default
title: Loopholes in the Cleanup Step
nav_order: 1
parent: Rules Interactions
---

# Loopholes in the Cleanup Step - A Niche Rules Interaction

This investigation started with a spontaneous thought - Is it possible to have your opponent cast silence on your turn, then proceed to cast a spell? Turns out, the answer is yes - and it's more relevant than you think!

## Rules Background

Let's start by looking at the relevant rules surrounding the cleanup step:

> 514 Cleanup Step
> 
> 514.1. First, if the active player’s hand contains more cards than their maximum hand size (normally seven), they discard enough cards to reduce their hand size to that number. This turn-based action doesn’t use the stack.
> 
> 514.2. Second, the following actions happen simultaneously: all damage marked on permanents (including phased-out permanents) is removed and all “until end of turn” and “this turn” effects end. This turn-based action doesn’t use the stack.
> 
> 514.3. Normally, no player receives priority during the cleanup step, so no spells can be cast and no abilities can be activated. However, this rule is subject to the following exception:
> 
>> 514.3a At this point, the game checks to see if any state-based actions would be performed and/or any triggered abilities are waiting to be put onto the stack (including those that trigger “at the beginning of the next cleanup step”). If so, those state-based actions are performed, then those triggered abilities are put on the stack, then the active player gets priority. Players may cast spells and activate abilities. Once the stack is empty and all players pass in succession, another cleanup step begins.

Simplified, it means that discarding to hand size and Until EoT effects wearing off happen before any priority is created in the Cleanup step, and priority can be created in the cleanup step if Triggered abilities have to be put on the stack or if State Based Actions are performed (eg a creature dying to having 0 or less toughness).

## Creating Priority in the Cleanup Step

Lets look at a few prominent effects that can create priority in the cleanup step.

### Necropotence

Necropotence creates a triggered ability when you discard cards. Commonly, when you use Necropotence and go to 8+ cards in hand, you discard down to hand size in the cleanup step, and you get triggers making you exile the discarded cards (Planar Void does a similar thing). Players get priority here and you can even do things like instant speed reanimating one of the discarded cards before the exile trigger resolves.

### Necromancy

Speaking of instant speed reanimation, Necromancy, when cast as an instant, creates a trigger on the cleanup step making you sacrifice the reanimated creature. For something like Protean Hulk, this is great, and you frequently cast Necromancy as an instant for this effect.

### The Gitrog Monster

Gitrog creates a triggered ability when lands are put into your graveyard. During your cleanup step, if you discard lands to hand size, you create a triggered ability from Gitrog making you draw cards (and cycle through more cleanup steps, since you go back above 7 cards in hand). This is sometimes used in the deck as a way to combo with Dakmor Salvage, but I won't go into detail here.

### State-Based Actions

I actually couldn't think of many relevant scenarios surrounding SBAs here. But a pretty simple illustrative example is this:

I have a 2/2 Grizzly Bears. I cast Giant Growth on it, giving it +3/+3 until end of turn. I then enchant it with Dead Weight, an aura giving -2/-2. In the cleanup step, the Giant Growth wears off, and Grizzly Bears is now 0/0. State-based actions are checked, and it dies as a result. This actually leaves players with priority even though nothing was placed on the stack.

If you can think of a relevant and common enough scenario where this happens, please share it in the comments!

## Bringing It Together - Applying the Rules

Here are a few illustrative examples on how we can apply this rule in cEDH:

## Silence

Silence is a pretty common until EoT effect and normally it's treated as being a hard stop on the turn. However, we can do some skirting around silence like so:

Example I: I attack with Zur the Enchanter and get Necropotence out of my deck. I activate Necropotence for 20, and my opponent casts silence to keep me from winning this turn. In my cleanup step, I discard down to 7 cards - eg. Shimmer Myr, Isochron Scepter, Dramatic Reversal, Aetherflux Reservoir, and some mana rocks - basically a very simple shimmer win. Normally, you'd be expected to exile your discarded cards and pass the turn. However, in the cleanup step, you actually can cast spells, as Silence has worn off. Therefore, you can avoid passing turn and letting your opponent untap with their counterspell mana, and combo off in your own cleanup step.

Example II: On my opponent's turn, they cast silence, which resolves, normally locking me out of interaction. They then play entomb for Protean Hulk. On their end step, they cast a Necromancy at instant speed for Protean Hulk. In their cleanup step, Necromancy triggers, prompting them to sacrifice hulk. At this moment, silence has worn off. I can now respond to the Necromancy trigger with a Swords to Plowshares or a Chain of Vapor on Hulk. I can even cast a Stifle on the Protean Hulk trigger after letting it die.
Angel's Grace

This example actually uses State-Based Actions as a way to create priority in the cleanup step, and is less deliberate than the others.

Example III: You're playing a deck with necromancy and hulk, but are shut down by your Tymna Kraum opponent who has a Rest in Peace and Grafdigger's Cage in play. On their turn, the Tymna Kraum player casts Angel's Grace + Ad Nauseam, but fails to win through everyone's interaction. In their cleanup step, Angel's Grace wears off. State-Based Actions are checked, and that player loses the game to having a negative life total. Priority exists in the cleanup step, and you can now cast Entomb -> Necromancy on their cleanup step with the hate pieces gone, before your next opponent can untap and have mana for counterspells. Since this creates multiple cleanup steps, Necromancy should sacrifice on the same turn.
Avenues for Exploration

I gave some thought to Yawgmoth's Will, but creating priority in the cleanup step became problematic as you discard to hand size prior to the exile effect wearing off. I also wanted to think up more examples of using SBAs for the priority creation effect, and look at more Until EoT effects to get around.

*This content was originally [posted on Reddit](https://old.reddit.com/r/CompetitiveEDH/comments/9g3vg0/loopholes_in_the_cleanup_step_a_niche_rules/) by guyonearth.*
