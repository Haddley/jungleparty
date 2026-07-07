# High Voltage Voting

**Category: Speed** · **Controls: colour buttons** · Longplay chapter 0:41:42 ([watch](https://www.youtube.com/watch?v=dZEJTdSRqrY&t=2502s)). Not yet recreated; the core twist is reported by a review.

Fastest-finger rounds where the **winner chooses a victim**: each round's quickest player picks which monkey gets zapped — the game's most social/vindictive design, and the origin of the electrocution slapstick our rig's `zap` pose recreates (skeleton flash and all).

## What the sources say

- [Rory's Retrospectives](sources/reviews.md) documents the winner-picks-victim rule.
- [Catalog](minigames.md): "Fastest-finger rounds; each round's winner chooses which monkey gets zapped/loses a life."
- The announcer's mock-mournful line "Blue, we will mourn you" quoted in [monkeys](monkeys.md) fits this game's elimination framing.
- German Wikipedia category: **Speed**.

## Rules (reported / *(inferred)* where noted)

- Each round poses a fastest-finger challenge (exact stimulus unverified — likely a colour or signal prompt *(inferred)*).
- The round winner then presses a colour button to choose which opponent gets electrocuted.
- Zapped monkeys lose a life (the catalog's "loses a life" phrasing suggests elimination stakes: last monkey standing wins) *(structure partly inferred)*.

## Verification targets for a video pass

The fastest-finger stimulus, lives per player, whether eliminated players keep playing rounds (kingmaker role), self-zap legality, tiebreaks.

## Recreation sketch (phone-buzzer fit: excellent)

- Two-phase round loop maps directly onto our `ctrl()` per-player button maps: phase 1 all players race (RED on signal — reuse Simian Shootout's tease/draw timing), phase 2 only the winner's phone enables opponents' colours (exactly like Monkey Bomb's pass buttons, labels = names).
- Elimination needs care in a 2-player party: give 3 lives each and convert to placement by survival order + lives remaining.
- Parameter sketch: tease 2–4 s, false start = you're zappable but round rethrown; zap costs 1 life; `zap` pose 1.5 s; announcer line on each elimination.

Back to the [catalog](minigames.md).
