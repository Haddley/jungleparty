# Ostrich Eggs

**Category: Luck** · **Controls: Buzz! button** · Longplay chapter 1:14:07 ([watch](https://www.youtube.com/watch?v=dZEJTdSRqrY&t=4447s)). Not yet recreated; core rule from a review.

Grandmother's-footsteps with an ostrich: creep toward her egg while she isn't looking, **freeze when her head pops up**. Also on the ten-game [single-player list](minigames.md#single-player-exclusives) (as "Ostrich Egg").

## What the sources say

- [Common Sense Media](sources/reviews.md) documents the creep-and-freeze rule.
- [Catalog](minigames.md): "Creep toward the ostrich's egg while she isn't looking; freeze when her head pops up."
- The ostrich is in the NPC cast list in [monkeys](monkeys.md). Noted as *not sighted* in the [launch trailer](sources/launch-trailer.md).
- German Wikipedia category: **Luck**.

## Rules (reported / *(inferred)* where noted)

- The ostrich's head is down (in the sand, presumably — the classic gag); monkeys creep toward the egg. Input is most likely **hold Buzz! to creep, release to freeze** *(input verb inferred; could also be press-repeatedly)*.
- When her head pops up, any monkey still moving is punished — sent back to the start, or bonked *(penalty unverified)*.
- First to reach the egg wins (or steals it and must return? *(speculative)*). Luck category reflects the random look-up timing.

## Verification targets for a video pass

The creep input, penalty (restart vs. stun vs. distance loss), the ostrich's tell before looking, whether reaching the egg ends the round or scores and resets.

## Recreation sketch (phone-buzzer fit: excellent)

- Grandmother's footsteps is the archetypal shared-threat hold-release game: our Bubble Bath scheduler (random threat windows + tell) drives it directly, but with **distance instead of points** — a genuinely different feel from the score-streak games.
- Monkeys use `run` while held, freeze-frame idle on release, `bonked` + slide-back on getting caught.
- Parameter sketch: track 100 units; creep 8 units/s; look-ups every 4–10 s with a 0.9 s tell (head shake before rising); caught = sent back 30 units (not to zero — keeps hope alive); first to the egg +1000, others by distance.

Back to the [catalog](minigames.md).
