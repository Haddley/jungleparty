# Monkey Bongo

**Category: Skill** · **Controls: Buzz! button** · Longplay chapter 1:02:30 ([watch](https://www.youtube.com/watch?v=dZEJTdSRqrY&t=3750s)). Not yet recreated; rules *(partly inferred)*.

A drumming rhythm game *(partly inferred)* — one of the game's two rhythm entries (with [Rain Dance](rain-dance.md)), fitting the soundtrack's "driving jungle rhythms, heavy chanting" ([presentation](presentation.md)).

## What the sources say

- [2009 Wikipedia list](sources/wikipedia.md) for the name; German Wikipedia for the **Skill** category.
- No manual rules, review description, or trailer sighting; the catalog line is inferred from the name and category.

## Rules *(partly inferred)*

- Monkeys drum bongos; presses must land on beats. Whether the pattern is call-and-response (watch the lead, repeat it) or continuous scrolling-cue play (like [Rain Dance](rain-dance.md)'s confirmed scrolling icons) is unknown.
- Single-button controls mean rhythm accuracy, not drum choice, is the skill *(safe inference from the controls column)*.

## Verification targets for a video pass

Call-and-response vs. scrolling cues, tempo range, scoring per hit vs. combo, miss penalty, how it differs from Rain Dance (they must play differently to justify both existing).

## Recreation sketch (phone-buzzer fit: good)

- Rhythm on RED synced to our Web-Audio step sequencer: the host already runs `MTRACKS` on a beat grid, so cue times can literally be sequencer steps — music and judgment can't drift apart.
- Latency is the enemy; judge with wide bands (±120 ms perfect, ±250 ms good) and let the TV pulse on every beat so players lock to sight + sound.
- Parameter sketch: 40 s track at ~100 BPM; cued beats only (not every beat); perfect 100 / good 50 / miss breaks a small ×1–×4 combo.
- Differentiate from Rain Dance by making this **call-and-response**: gorilla drums a 3–5 note phrase, players echo it.

Back to the [catalog](minigames.md).
