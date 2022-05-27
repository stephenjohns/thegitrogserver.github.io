---
layout: default
title: Drawing the Library
nav_order: 1
grand_parent: Budget
parent: Budget Loops
---

# Drawing the Library

This Dakmor loop is a little different than the [standard](../../fundamental-loops/drawing-the-library.md) because this loop assumes the deck has Gaea’s Blessing as its only shuffler, meaning that this loop is non-deterministic and also fallible if missequenced.

The requirements and procedure are identical to the standard "Drawing the Library" loop, but it is important to not resolve the Gitrog’s draw triggers until you have more triggers than cards in Library since Gaea’s Blessing can’t be discarded to shuffle if you unintentionally draw it.

An interesting caveät here is that, since you must wait until you have >=N, where N is cards in Library, draw triggers on the stack, you cannot guarantee that you will have exactly N draw triggers. It is likely that you will have >N triggers, meaning that budget lists not playing a titan shuffle effect must always assume they’ll have to win at instant speed. For this reason the titanless lists play Emergence Zone
