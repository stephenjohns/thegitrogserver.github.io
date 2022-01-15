---
layout: default
title: Proof of Determinacy
parent: Mathematical Proofs
nav_order: 3
---

# Proof of Determinacy for The Gitrog Monster Combo

## Algorithm
```
  While draw triggers < number of cards in deck:
  - Discard lands such that lands in deck + grave >= 3, putting triggers on stack
  - Dredge until you find K, putting all draw triggers on stack
  - If you did not find K (deck was odd and K was last card):
  - -  Draw one card then discard K
  - Put shuffle trigger on stack
  - While cards in deck >= 3:
  - -  Dredge
  - -  If a land flipped, draw 1 card
  - Shuffle deck
  Draw deck, you are finished
```
Notes for Algorithm
* This WILL NOT WORK for Chains of Mephistopheles. Since you cannot perform stack manipulation, it just leaves determinacy to fate.
* Using Kozilek and Ulamog is not a problem, the section of deck between them can be treated as either before K (because it is before the second one) or after K (because it is after the first one).

## Proof

Assume that you have Dakmor Salvage in hand and The Gitrog Monster and Putrid Imp in play.

Definitions
```
  L => Land
  K => Kozilek (or Ulamog, only 1 in the deck)
  X => some non-L non-K card
  N => number of X in deck
  T => 'draw a card' trigger (from dredging a land)
```

Proving this combo to be determinate requires:
1. Each state finds K, either drawn or milled, such that the combo can continue
2. Each state increases number of draw triggers, reduces number of nonlands in deck, or leads unidirectionally towards a state which does so

Deck is Even:
```
  K can be found (just dredge right to it)
  T increases by >= 1 if any L before K
  T increases by >= 1 if at least three L after K
  (worst case: deck ends with XL LL causing one L draw. That L will increase T 
     by 1 on the next cycle)
```

Deck is Odd:
```
  If K is last card:
    T increases by >= 2 if at least 3 L before K
    T decreases by 1 to draw K
  If K is not last card:
    Same as Even
```

Special Case:
```
  Lands drawn in previous cycles will not cause the change of T
    for two consecutive cycles to be <= zero
  Even:
    T increases by >= 0 for any number of L
  Odd:
    If K is last card:
      T >= ceiling(number of L / 2) - 1
      T < 0 for number of L = 0
      If number of L = 0, T increased by 3 on previous cycle, a net gain of 2
    If K is not last card:
      Same as Even
   In all special cases, where T <= 0, no lands were drawn,
     so special cases of T <= 0 never chain into themselves
```

*This was originally [posted](https://old.reddit.com/r/CompetitiveEDH/comments/4fbhk1/proof_of_determinacy_for_the_gitrog_monster_combo/) on Reddit by mazeTemporal.*
