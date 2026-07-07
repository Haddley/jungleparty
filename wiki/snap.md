# Snap

**Category: Speed** · **Controls: Buzz! button** · Longplay chapter 1:34:54 ([watch](https://www.youtube.com/watch?v=dZEJTdSRqrY&t=5694s)). Not yet recreated; rules *(partly inferred)*.

The card game Snap: cards flip, and when two match, buzz first *(partly inferred)*. Alongside [Simian Shootout](simian-shootout.md), the purest reaction test in the catalog — but with a *decision* attached (is it actually a match?), which is what separates it from a raw quick-draw.

## What the sources say

- [Catalog](minigames.md): "Card game Snap: buzz first when cards match *(partly inferred)*."
- [2009 Wikipedia list](sources/wikipedia.md) for the name; German Wikipedia for the **Speed** category.
- Card assets exist in the game ([Card Counting](card-counting.md)'s oversized fruit cards, per the trailer) and are presumably shared.

## Rules *(partly inferred)*

- Cards flip in sequence (one growing pile, or two side-by-side piles — unverified); when consecutive/facing cards match, the first Buzz! wins the round or the pile.
- **False snaps must be punished** — otherwise mashing dominates — likely a lockout or point loss *(inferred; the false-start rule in Simian Shootout, verified, is the in-house pattern)*.
- Rounds until a card budget or timer expires *(inferred)*.

## Verification targets for a video pass

One pile vs. two, flip cadence, match frequency, points per snap, and the false-snap penalty (the key parameter).

## Recreation sketch (phone-buzzer fit: excellent)

- Shared-screen reaction with a cognitive gate ports directly: TV flips cards on a rhythm; all REDs enabled; first correct press takes the points, wrong-press lockout deters mashing.
- Latency fairness: award by host receive-time minus half RTT per player (identical approach to Simian Shootout's ms display — showing reaction times is half the fun).
- Parameter sketch: 45 s; flip every 1.1 s; match probability ~22 %; snap +150; false snap = 2 s lockout with the `bonked` pose on the TV; near-miss art (banana vs. banana-bunch) in later rounds.

Back to the [catalog](minigames.md).
