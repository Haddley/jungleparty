# Crazy Climbers

**Category: Speed** · **Controls: Buzz! button** · Longplay chapter 0:17:45 ([watch](https://www.youtube.com/watch?v=dZEJTdSRqrY&t=1065s)). Not yet recreated; rules *(partly inferred)*.

A climbing race up the trees — mash (or rhythm-press) Buzz! to climb *(partly inferred)*.

## What the sources say

- [2009 Wikipedia list](sources/wikipedia.md) for the name; German Wikipedia for the **Speed** category.
- The [launch trailer](sources/launch-trailer.md) (0:28–0:29) shows an unidentified climbing round — monkeys racing up ropes/vines beneath four giant carved stone monkey-head idols. The trailer notes could not confidently match it to a catalog name; Crazy Climbers is the strongest candidate alongside a Totem Poles stretch.

## Rules *(partly inferred)*

- First monkey to the top wins; the open question is the input verb: pure mash, alternating rhythm, or timed presses (release-and-press windows). The Speed category suggests mash or near-mash.
- Possible hazards on the way up (falling objects, slips) are unverified *(inferred — party-game convention)*.

## Verification targets for a video pass

The press mechanic (mash vs. timing — critical for recreation feel), climb duration, hazards, rubber-banding, and whether the idol-climb trailer shot is in fact this game.

## Recreation sketch (phone-buzzer fit: good, with a caveat)

- Buzzer mash maps to RED mash, but raw mash rate over PeerJS (~200 ms state pushes, per-event buzz messages) favours **timed presses** over pure mash: e.g. alternating "press exactly when your monkey's hand glows" beats spam and is latency-tolerant.
- Reuses the `run`/`hold` rig poses rotated vertically; vines from the scenery vocabulary.
- Parameter sketch: 30 m climb, each valid press +1 m, mistimed press slides −0.5 m, first to top +1000, others by height.

Back to the [catalog](minigames.md).
