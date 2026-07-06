# Monkey Bomb

Category: **Luck & tactics**. Controls: the **four colour buttons** (blue, orange, green, yellow) — no Buzz! button. A bomb with a hidden-length fuse is hot-potatoed among the [monkeys](monkeys.md): holding it earns points at a steady tick, and pressing a colour button throws it to that monkey (green button → green monkey). Whoever is holding it at the bang forfeits everything earned that round **and** loses 100 from their total. One of the six games in the [minigames](minigames.md) catalog's starter set with a deep page.

Sources: [manual](sources/us-instruction-manual.md) for the stated rules; all observations below are from the [longplay](sources/full-longplay.md), chapter 1:00:03 ([watch](https://www.youtube.com/watch?v=dZEJTdSRqrY&t=3603s)) — an instruction video followed by one full 3-player game (Blue, Orange, Green; no Yellow this session).

## Rules & scoring as observed

- **A game is six bombs (rounds).** Each round is announced with letters flying in across the playfield: "FIRST BOMB" for round 1, then "BOMB 2" … "BOMB 6". In the observed game each of the three players got blown up exactly twice (Orange, Green, Blue, Orange, Green, Blue) — likely luck, but suspiciously tidy.
- **Holding accrues points** into a per-round counter (the lower box of your HUD panel). Measured tick rates varied between ~50 and ~75 points/second across holds (rolling-digit blur makes exact reads hard); whole-round sums divided by fuse time give a consistent **~55–60 points/second average**.
- **Passing**: press the colour button of a target monkey; the holder throws immediately. The bomb arcs across with a smoke trail (~0.5–1 s flight). **No minimum hold observed** — holds as short as ~1 s occurred, and **immediate pass-backs are allowed**: in bomb 3, Blue → Orange → straight back to Blue, where it exploded essentially on arrival. Points already accrued are kept when you throw; you can accrue in several separate holds within one round and they accumulate in the same round counter.
- **Explosion settlement**: every survivor's round counter rolls down to 0000 while their total rolls up by the same amount (banked). The victim's round counter rolls down to nothing (forfeited) and their total rolls **down 100**. Totals are **clamped at zero**: Orange (total 0) and Green (total 37) both showed 0000 after losing, never negative.
- **Next round's first holder appears to be the previous round's loser** — held in all five observable handovers (Orange lost bomb 1 and started bomb 2, etc.). Round 1 started with Blue (player 1?).
- Final scores of the observed game: Orange 988, Green 746, Blue 635 — despite Orange having been the first casualty and sitting on 0 after two rounds, so the −100 penalty is far from decisive.

## Scene

Side-on, fixed camera. A swampy jungle: misty teal water and giant buttress-rooted trees in the background, hanging vines, and a single long **moss-covered branch/log spanning the whole screen** on which the monkeys stand — left, centre, right for three players (the instruction video shows four across). No movement along the branch; monkeys stay on their spots and only lean/reach to throw and catch. The instruction video plays inside the standard bamboo-framed screen with a wooden "MONKEY BOMB" nameplate over the leaf-pattern backdrop.

## Animations

- **Holding**: the bomb is a black sphere clutched at the belly, with a fizzing dark smoke/spark plume streaming sideways off the fuse — the plume is large and constant, an obvious "who has it" marker readable from the HUD-height framing.
- **Idle (not holding)**: standard nervous idle, arms on the branch, watching.
- **Throw / catch**: quick raise-and-lob; the receiver reaches up to catch. Flight ~0.5–1 s with a smoke trail arc.
- **Explosion**: a large orange-and-black fireball erupts at the holder's position (roughly one monkey wide, taller than the monkeys). The victim is **blackened/charred** and flung — seen thrown into the air with arms up, or left dazed and sooty on the branch; neighbours flinch and get knocked flat by the shockwave (in bomb 6's aftermath the non-victim Orange was lying flat on the branch beside charred Blue). Soot persists through the settlement pause, then everyone is intact for the next round.
- **Winner**: after bomb 6 the camera cuts to the winning monkey alone on the branch, jumping with an arm raised.
- **Pacing**: explosion + score-settlement + "BOMB n" letters takes ~5–7 s between rounds.

## Fuse behaviour

There is **no visible timer or fuse-length indicator** — only the constant smoke plume, which does not visibly shorten or intensify (nothing telegraphs the bang). Estimated fuse durations across the six rounds, from round-start/explosion timings and from banked-points sums: roughly **8–12 seconds** (bomb 1 ≈ 11–12 s, bomb 3 ≈ 8–9 s, others in between). Consistent with a random draw in that range.

## HUD / score display

Panels across the top, one per active player (three this session; four in the instruction video), in the player's colour with the monkey's face in a colour-ringed circle and the colour name (BLUE / ORANGE / GREEN). Each panel has **two four-digit odometer-style boxes**: top = banked total, bottom = current bomb's accrual, ticking live while that player holds. At the explosion the digits **roll mechanically** — round counters spin down as totals spin up (or down 100 for the victim) — a satisfying slot-machine settlement over ~1–2 s.

## Recreation notes

Parameters for a faithful re-implementation:

| Parameter | Value |
|---|---|
| Players | 2–4 monkeys on a branch, side view |
| Rounds per game | 6 ("FIRST BOMB", then "BOMB 2"…"BOMB 6") |
| Fuse | random ~8–12 s, hidden; no visual countdown |
| Hold scoring | ~60 pts/s (observed 50–75; average ~55–60) into a round counter |
| Pass | colour button → throw to that monkey; flight ~0.6 s; any target, pass-backs allowed |
| Pass lockout | none observed above ~1 s holds; suggest ~300–500 ms catch animation lockout to prevent instant ping-pong |
| Explosion settlement | survivors bank round counter into total; victim forfeits round counter and total −100, clamped at ≥ 0 |
| Next first holder | previous round's loser (round 1: player 1) |
| Inter-round pause | ~5–7 s (blast, rolling-digit settlement, next-round letters) |
| Animations needed | hold-with-smoking-bomb, throw, catch, fireball, charred/flung victim, flinching neighbours, winner celebration |

Design notes: the tension is entirely in the hidden fuse — the HUD's live tick makes greed legible (everyone can watch your counter climb), and the rolling-digit settlement is the payoff moment worth recreating. The −100 penalty is small next to a good round's ~300–400 points, so the real loss is the forfeited round counter; a player who hoards for 5+ seconds risks proportionally more.
