---
layout: default
title: Cleanup Step Sculpt Analysis of Failure States
parent: Mathematical Proofs
nav_order: 2
---

# Cleanup Step Sculpt: Analysis of Failure States

Someone was talking about almost getting stuck during an end step sculpt and asked what all of the possible failure states were. I tried to distill it to the essential details, but there is still a lot.

## About

Since the cleanup step sculpt is based on passive discarding, there are situations that can cause it to get stuck and prevent the seemingly endless chain of cleanup steps. This analysis examines those failure conditions and how to avoid them. I am not considering things like sylvan safekeeper here. Although land sacrificers can get you out of a tight spot and should be used if available, they are a finite resource so they are not dependable when discussing potentially unbounded iterations.

## Theoretical Failure States

Cleanup step sculpting is not inevitable, so if you get infinitely unlucky, you could theoretically carry on forever without accomplishing anything. There are two forms of this:

1. Shuffler is dredged early enough that no progress is made. If the shuffler appears before any lands, you will not even have a chance at accomplishing anything. You would just mill into it and shuffle again.

2. Bonus draw trigger always nets some useless card. Another way of stating the same situation is you always dredge the cards you want, so although you are generating additional draws and moving through the deck, you just filter through the same unwanted things.

3. The theoretical failure states are unavoidable. They do not stop the chain, but could cause issues if you do not get to a winning state.

## Concrete Failure States

These all essentially come down to being unable to dredge because you run out of deck and the shuffler is somewhere awkward. Let's get more specific:

1. The last shuffler is in hand.

    1. Shuffler drawn early in the deck: It may seem convenient to keep the shuffler in hand since it helps reduce the impact of early shuffle with no progress, but it can become perilous as the deck starts to run out. I have determined that it is unsafe to have a shuffler in hand if the deck is odd and has fewer than 3 lands remaining or if the deck is even as has fewer than 4 lands remaining. Since it is difficult to control whether the deck is even or odd, you really need to discard the shuffler when there are fewer than 4 lands in the deck.

        * Demonstration for why 3 lands could fail in an even deck: [LL] /X/ L: Dredge two lands, draw a nonland, discard shuffler and Dakmor. Cannot dredge a deck with just one card, so you must shuffle Dakmor into the deck. If the drawn card was a land, you could draw either before or after the shuffle with no problem. Therefore, having 4 lands remaining in deck prevents you from getting stuck. Of course, if the lands were not concentrated at the end, there would be plenty of room to dredge while discarding the shuffler, this is simply a worst case scenario.

    2. Shuffler drawn late in the deck: The above strategy (1A) works in almost every case because you will only draw a shuffler if Dakmor dredged a land, and that means you can discard the shuffler and Dakmor at the same time. It does not work if you drew the shuffler at the end of the deck with either 1 or 0 cards remaining, because that would prevent the dredge and force you to shuffle Dakmor into the deck. This is avoided if you have 1 additional land in hand. One final sneaky case that causes the same problem is if there are 2 cards remaining and at least one of them is a land. This is a problem because if you stack the triggers to dredge before shuffling (to prevent shuffling Dakmor away), you will dredge the land(s) and get another trigger on an empty deck, causing you to lose. It is avoided in the same way, just discard a different land instead of Dakmor.

2. Shuffler is the last and only card in the deck. This is the awkward case where one of following two things happened: 1. There were 3 cards in the deck and Dakmor dredged 0 lands, leaving the shuffler as the last card and cannot be dredged. 2. There were 4 cards in the deck, Dakmor dredged a land, and you drew something, again leaving the shuffler as the last card. The strategy here is essentially to prevent the situation from coming up, but gets complicated because there are a few variables to consider.

    1. Full reset: The worst possible scenario is when only the shuffler remains in the deck. This extreme situation would require a spare land to get to the shuffler and then a fetch (Crop Rotation) to get back to 8 cards. Therefore, you are always safe to continue if you have Crop Rotation and an extra land. The remaining entries are a list of special cases that do not require Crop Rotation and reduce the chance of this extreme case.

    2. Landless even: If there are no lands in the deck, you can just dredge through and there are no problems. Related to this concept, if you mill the last land in the deck and resolving the draw would make the deck odd, if possible, dredge Golgari Grave Troll instead to prevent the deck from becomming odd.
    
    3. Safe gamble: If there are 3 cards in the deck and at least one is a land, it is safe to dredge. You will either dredge the shuffler in the first two cards or get a draw trigger and draw the shuffler anyway, which is then solved by 1 spare land.
    
    4. Substitute dredging: By discarding one spare land, you can dredge something else to avoid the problems at the end of the deck. These include Life from the Loam when there are either 3 nonlands or 4 cards where at least one is a land and similarly Golgari Grave Troll when there are 6 or 7 cards remaining and at least one is a land. (There is no need to substitute Golgari Grave Troll on 6 cards if there are no lands because of 2B. There is also no need to substitute Life from the Loam on 3 cards if there are lands because of 2C.)

## Conclusion

Since you cannot guarantee to have spare lands and fetches available, the concrete failure states are also not fully preventable, but can be reduced with strategic play. My recommendation is to stockpile lands, ideally non-green non-fetch lands because crop rotation likes to fetch green lands. The target hand would be:
* Dakmor Salvage (to continue the chain)

* Oblivion Crown (the goal is to cast this for active discarding)

* Dark Ritual (to cast Oblivion Crown)

* Crop Rotation (green mana allows you to fetch and restart the chain even if you end up with 7 cards in hand. If you have spare life, rotate into green fetch lands for extra insurance)

* 4 lands (spare lands are needed for several tough situations)

Then dredge chain +2 to 10 cards so you can cast Dark Ritual and Oblivion Crown

As always, let me know if I have missed anything important or if you have other questions or suggestions.

*This was originally [posted](https://old.reddit.com/r/CompetitiveEDH/comments/bgk4q9/the_gitrog_monster_cleanup_step_sculpt_analysis/) on Reddit by mazeTemporal.*
