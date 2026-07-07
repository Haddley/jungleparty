# Balloon Battle

**Category: Accuracy** · **Controls: Buzz! button** · Longplay chapter 0:01:15 ([watch](https://www.youtube.com/watch?v=dZEJTdSRqrY&t=75s)). Not yet recreated; no frame-analysis pass yet, so everything beyond the catalog line is *(inferred)*.

The first game alphabetically and therefore the first chapter of the [longplay](sources/full-longplay.md). A balloon-popping/shooting contest: players time Buzz! presses to burst balloons *(partly inferred)* — the [catalog](minigames.md) line comes from name, category, and fragments; no source gives the full rules.

## What the sources say

- [2009 Wikipedia game list](sources/wikipedia.md): the name and its presence in the EU 40; German Wikipedia supplies the **Accuracy** category.
- Not among the [manual](sources/us-instruction-manual.md)'s five documented rule sets; not sighted in the [launch trailer](sources/launch-trailer.md).

## Rules *(inferred)*

- Balloons drift or rise through the scene; each player pops balloons by pressing Buzz! with timing (an aiming sweep or a reticle pass is the likely mechanic, by analogy with the confirmed sweep-arrow mechanic of [Island War](island-war.md)).
- Accuracy category suggests scored hits rather than a race; likely points per balloon, possibly value-tiered balloons (compare the 100/50/25/10 point balloons seen in [Monkey Catapult](monkey-catapult.md)'s trailer shot).

## Verification targets for a video pass

Watch the chapter for: whether balloons are shared or per-player, what the Buzz! press actually does (fire vs. lock aim), balloon point values, round length, and the miss penalty.

## Recreation sketch (phone-buzzer fit: good)

- A sweeping reticle per player (auto-oscillating) with RED to fire maps cleanly to one-button play.
- Shared balloon field with first-hit-claims scoring would create the party-game contention our host-authoritative loop handles well (single source of truth in the host `tick`).
- Parameter sketch: 45 s round, balloons spawn every 1–2 s, values 25–100 by size (small = high), reload lockout ~0.8 s per shot.

Back to the [catalog](minigames.md).
