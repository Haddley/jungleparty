# Door Running

**Category: Luck** · **Controls: colour buttons** · Longplay chapter 0:29:53 ([watch](https://www.youtube.com/watch?v=dZEJTdSRqrY&t=1793s)). Not yet recreated; rules *(inferred)*.

A choose-your-door luck game: pick among doors, some safe, some booby-trapped *(inferred)*. Notable trivia: the [instruction-videos compilation](sources/instruction-videos.md) uploader notes a **beta variant of the Door Running instruction video exists** — one of only two games with known beta instruction movies (the other is [Odd One Out](odd-one-out.md)), hinting its rules changed during development.

## What the sources say

- [2009 Wikipedia list](sources/wikipedia.md) for the name; German Wikipedia for the **Luck** category; colour-button controls from the catalog.
- Beta instruction video variant noted in [instruction-videos](sources/instruction-videos.md).

## Rules *(inferred)*

- Each round offers a row of colour-marked doors; players choose with the colour buttons, monkeys run at their chosen door.
- Safe doors open (points or progress); booby-trapped doors deliver slapstick — a classic set-up for the rig's `bonked`/`flat` states.
- "Running" suggests the choice happens at speed — perhaps repeated waves of doors mid-run, making it a luck-driven cousin of [Jungle Hurdles](jungle-hurdles.md).

## Verification targets for a video pass

Door count per wave, single choice vs. repeated waves, trap penalty, whether any tell distinguishes safe doors, what the beta variant changed.

## Recreation sketch (phone-buzzer fit: excellent)

- Wave-based structure fits our shipped Jungle Hurdles module: shared waves of four doors, each player commits a colour before impact.
- Luck twist vs. Hurdles' skill: the correct door is random per player rather than signposted; safe = keep running, trap = 1.3 s sprawl (identical timing constants to Hurdles for consistency).
- Parameter sketch: door wave every ~3 s, 2-of-4 doors trapped, finish by distance at 45 s.

Back to the [catalog](minigames.md).
