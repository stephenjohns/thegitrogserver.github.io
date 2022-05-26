---
layout: default
title: What is "The Gamestate"?
nav_order: 2
parent: Rules Interactions
---

Whenever you’re doing a non-deterministic loop, you need to be very careful of this specific section in [MTR4.4](https://blogs.magicjudges.org/rules/mtr4-4/):
> Non-deterministic loops may not be shortcut. A player attempting to execute a nondeterministic loop must stop if at any point during the process a previous game state is reached again.

That’s great let’s just check [Yawgatog](https://yawgatog.com/resources/magic-rules) really fast—control-F "game state"—hmm 18 results and not one of them even defines what the "game state" even *is*. Is it just cards on the battlefield? Surely not. Obviously cards in the graveyard count. And I’m sure cards in exile have to count too right? Ok well what about cards on the stack? Do those count? How about cards in your hand? Or cards in a hidden zone? Does the command zone count as part of the game state? If you have a Wishboard then does your Sideboard count as part of the gamestate?

Nobody fucking knows. And no, I’m not kidding.

On 2019-04-26T14:14EST I sent Nik Zitomer, the head L3 in charge of all Magic tournaments in the Southeast USA, an email asking several questions about the legality of clean-up step interactions that were first outlined by guyonearth in 2018. Nik has been head judge at several Pro Tours, Grands Prix, Magifests, and StarCityGames Opens. He’s a big fucking deal and his opinion matters in the world of Magic.

> Hey it's KJ! I'm from the other side of Chattanooga. I was in your judge class for the SE, talked to you on Facebook, you approved my account on here, etc. My Facebook got deactivated because I used a disposable email address to make it. (I've never had a FB before and made one just to be in your class). Unlucky. Anyway I need your advice when you get the chance :)
> 
> I'm part of a decent sized, online, competitive EDH community. Think of it like singleton Vintage. We sometimes have community tournaments which we (try to) keep a CREL policy on. Most of the players have a good grasp of MTG so there are rarely ever problems with interaction. If we have any we always use the IRC chat for help. But there is a continued issue we have involving The Gitrog Monster that has almost become a meme. It boils down to a nondeterministic loop and MTR 4.4 (I think).
> 
> Basically the loop is this:
> - AP controls The Gitrog Monster
> - AP has 8 cards in hand, specifically including Dakmor Salvage
> - AP moves to End Step
> - On Clean-up AP discards Dakmor Salvage to hand size
> - The Gitrog Monster's triggered ability goes onto the stack
> - The Gitrog Monster's triggered ability resolves
> - AP replaces the draw with Dredge 2, getting back Dakmor Salvage
> - AP goes to a second Clean-up
> 
> I'm sure you see where this is going, but the goal of it is that once a land is milled off of Dredge 2, then an "extra" draw trigger is created; meaning that AP will now have 9 cards in hand. Kozilek, Butcher of Truth is played in this deck to assure that it can do this indefinitely. In this way, AP can filter through their deck to reach a particular hand, consisting of any 7 cards they want plus Dakmor Salvage. AP can then win from this position at instant speed during Clean-up by getting priority from The Gitrog Monster's trigger.
> 
> --
> 
> Because the combo is technically inëvitable (unlike, say 4 Horseman) our community has reached 5 different conclusions:
> 
> 1) This loop is legal. The game state is advancing because AP's hand, graveyard, and deck contents are changing.
> 
> 2) This loop is slowplay, and punishable.
> 
> 3) This loop is ultimately not punishable. Nothing about the loop itself violates the CR or the MTR, but once a state is reached twice (from Kozilek shuffle) where AP has The Gitrog Monster on the battlefield, 91 cards in Library, 8 cards in Hand, and 0 cards in the Graveyard/Exile, then the portion of MTR 4.4 that says "A player attempting to execute a nondeterministic loop must stop if at any point during the process a previous game state  is reached again. This happens most often in loops that involve shuffling a library." is met; meaning that the AP must stop the loop at that point.
> 
> 4) The loop itself is not punishable, but it is pointless to do since it will violate MTR 4.4 before the player wins; it is therefore slowplay to knowingly do something pointless, which is punishable.
> 
> 5) This is probably an illegal loop, but makes sense pragmatically, so it's fine.
> 
> --
> 
> I'm partial to position 3. But I'm clearly not an L2 nor is anyone else in the group. So in every game we've had, everyone involved adopted position 5. There were no hard feelings. Once the Gitrog player reached a state where they could loop Dakmor to the Clean-up hand-size check, the other 3 players in the pod simply conceded.
> 
> Now for my actual question: Obivously EDH isn't sanctioned but, what would your ruling be if you were perhaps at a GP side-event and there was a pod with someone unwilling to concede to this? Is the Gitrog player allowed to get a 10 minute extension to play this out because, technically the game state is advancing? How about a 45 minute extension? Or is the loop just flat-out not legal at a competitive enforcement level?
> 
> --
> 
> Also, what the hell is "game state"? I know we like to make fun of the rules that read "A player is someone playing the game", but also why is game state never actually defined in the CR? Do hidden zone changes count towards game state changes?
> 
> Thank you Nik. I know this is a lot. If I explained anything poorly and you need me to rephrase I'm more than willing to write it differently or talk about it verbally.
> 
> ~KJ

He replied

> Hey KJ!
> 
> Don’t worry about the email being long or complicated, it’s no big deal. Ultimately, even at MF’s Commander games are untimed. Given that the game state is advancing in these cases I wouldn’t issue slow play if somehow (please no) this were ever at Comp REL. It is a loop, imo, and one maintained by one player. I’d say to the player they can try to execute it a reasonable number of times (say... for 2 minutes), then they need to stop.
> 
> The simple answer is that really, like most things in commander, if you want to play this deck you should agree to how to handle it before the game begins. Just make a house rule.
> 
> As for what constitutes a game state: it’s all of the objects in play at the specific moment. It also includes status of those objects (attacking, exiled, etc.). I’d say objects in hidden zones are part of the game state, but not known to all players.
> 
> Hope this helps, and also please realize that it’s simply my take, others may have differing opinions.
> 
> Nik

So if you go to a major tournament in the Southeastern USA and Nik is in charge, then yeah you can clean-up step sculpt. (As long as your library doesn’t shuffle into the exact same order twice.)

But we have a problem here, of course. The CR takes time to define what "a [player](https://yawgatog.com/resources/magic-rules/#R102)" is but has not a shred of fucking insight into what constiutes the "game state". The legality of these kinds of interactions are *not* in the rules and as such the tournament legality is up to what the opinions of your head judge are.
