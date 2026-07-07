# Elephant Baseball

**Category: Skill** · **Controls: Buzz! button** · Longplay chapter 0:31:28 ([watch](https://www.youtube.com/watch?v=dZEJTdSRqrY&t=1888s)). Not yet recreated; core rule from the catalog, details pending video.

Timing-based batting: an elephant pitches (presumably trunk-launched), and players press Buzz! with timing to bat. Also one of the ten [single-player games](minigames.md#single-player-exclusives) list, so a solo scoring variant exists.

## What the sources say

- [Catalog](minigames.md): "An elephant pitches; press with timing to bat" (not marked inferred).
- The **elephant pitcher** is listed in the NPC supporting cast in [monkeys](monkeys.md).
- Explicitly noted as *not sighted* in the [launch trailer](sources/launch-trailer.md).
- German Wikipedia category: **Skill**.

## Rules (reported / *(inferred)* where noted)

- The elephant winds up and pitches; each batter presses Buzz! as the ball arrives. Timing quality presumably grades the hit (foul / hit / home run) *(inferred)*.
- Unknown: whether monkeys bat simultaneously in lanes or take turns; points per hit; number of pitches *(all inferred territory)*.
- Solo variant exists (single-player list), suggesting score-per-pitch structure rather than head-to-head.

## Verification targets for a video pass

Turn order vs. simultaneous batting, timing window size, hit grading, pitch count, whether pitch speed varies (the elephant's tell).

## Recreation sketch (phone-buzzer fit: excellent)

- Timing-press on RED is the most latency-sensitive shape we ship; mitigate like [Simian Shootout](simian-shootout.md) (host-side timestamps, generous ±150 ms grading bands).
- Simultaneous lanes keep everyone engaged: one pitch, four ghost balls, each phone judges its own swing.
- Parameter sketch: 10 pitches; grading perfect ±60 ms = 300 (home run), good ±150 ms = 100, else whiff; occasional slow-ball tease (elephant wiggles its trunk longer) to punish rhythm-guessing.
- New elephant SVG; batter uses a `whack`-pose variant with a bat instead of a mallet.

Back to the [catalog](minigames.md).
