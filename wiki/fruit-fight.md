# Fruit Fight

**Category: Skill** · **Controls: Buzz! button** · Longplay chapter 0:37:55 ([watch](https://www.youtube.com/watch?v=dZEJTdSRqrY&t=2275s)). Not yet recreated; rules *(inferred)*.

A fruit battle — hurl fruit at the other monkeys *(inferred)*. One of the artillery/throwing family, distinguished from the coconut games by (presumably) softer, splattier ammunition.

## What the sources say

- [2009 Wikipedia list](sources/wikipedia.md) for the name; German Wikipedia for the **Skill** category.
- No manual rules, review description, or trailer sighting. The catalog line is inferred from the name.

## Rules *(inferred)*

- Monkeys pelt each other with fruit; Buzz! presses throw, most likely via the series' sweep-aim mechanic (see [Island War](island-war.md)'s verified arrow: first press locks direction, second sets power) or a simpler timing press if targets move through a fixed arc.
- Skill category (not Accuracy — unlike Island War/Lily Pads) hints the challenge is timing or dodging rather than aiming *(reading the category tea-leaves; verify)*.
- Hits presumably score and/or stun the target (splat + `bonked` state).

## Verification targets for a video pass

Aim mechanic, whether players can dodge, hit effects (score vs. stun vs. knockout), ammo variety, round length.

## Recreation sketch (phone-buzzer fit: good)

- If timing-based: RED throws at the monkey your auto-swinging aim line currently crosses — one-button chaos that suits phones.
- Splat effects reuse our `S.splat()` SFX and burst visuals; fruit projectiles are trivial SVG (banana, mango, melon slice).
- Parameter sketch: 45 s brawl; +100 per hit, hit monkey stunned 1 s (`bonked`); throw cooldown 1.5 s; friendly-fire only (no NPC targets) keeps it a pure four-way melee.

Back to the [catalog](minigames.md).
