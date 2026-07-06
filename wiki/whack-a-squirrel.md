# Whack A Squirrel

Category: **Speed**. Controls: the **four colour buttons** (blue, orange, green, yellow) — no Buzz! button. Competitive whack-a-mole: squirrels pop out of four colour-ringed holes in a tree stump, and the first [monkey](monkeys.md) to press the button matching the hole's colour swings its mallet and takes the points. Every player can go for every squirrel — there are no per-player holes, only per-colour ones. One of the games in the [minigames](minigames.md) catalog; general reception of the minigame set is covered in [reviews](sources/reviews.md).

Sources: all observations below are from the [longplay](sources/full-longplay.md), chapter 1:44:33 ([watch](https://www.youtube.com/watch?v=dZEJTdSRqrY&t=6273s)) — an instruction video followed by one full 3-player round (Blue, Orange, Green; no Yellow this session; the instruction video shows the 4-player layout).

## Rules & scoring as observed

- **One round, one shared board.** "READY" then "GO!" letters appear over the stump; the first squirrel pops the moment GO! lands.
- **Four holes, colour-coded** with a blue, orange, green and yellow ring — the four buzzer colours, **not** the four players. All four colours are present even in this 3-player session (squirrels still use the yellow hole with nobody named Yellow playing).
- **A squirrel pops from one hole at a time** (never two simultaneously in the observed round). Press the colour of its hole; the fastest presser's monkey lunges and whacks it.
- **+100 points per whack**, credited with a rolling odometer count-up. Every score change in the round was exactly +100.
- **No point penalty observed**: all three scores were strictly non-decreasing (Blue 0→1400, Orange 0→800, Green 0→600). A wrong or late press appears to cost only time — monkeys were seen slamming the mallet onto empty stump (a whiff animation) while a rival scored.
- **Timer, not target score**: the round runs on the leaf timer (below) for roughly **two minutes**; highest total wins. Final scores of the observed round: Blue 1400, Orange 800, Green 600 — 2800 points total, i.e. 28 whacks, averaging one squirrel every ~4.3 s.

## Scene

A round jungle clearing carpeted in grass and ringed with clusters of pale-yellow mushrooms/toadstools. In the centre stands a single **broad, flat-topped tree stump** with the four ringed holes cut into its top. The monkeys kneel around the stump, one per side, each gripping a **barrel mallet** — a dark wooden keg on a stick, comically oversized. The camera sits at a low three-quarter angle and **slowly orbits the stump** throughout the round, so the colour rings drift around the screen (players key off colour, not position). The instruction video plays inside the standard bamboo-framed screen with a wooden "WHACK A SQUIRREL" nameplate over the leaf-pattern backdrop.

The squirrel is a small brown rodent with a lighter tan muzzle and belly, perky ears and a big bushy dark-brown tail; it pops up chest-high out of a hole and looks around cheekily until it is flattened or retreats.

## Timings

- **Round length**: GO! at ~0:41 of the clip, final whistle at ~2:43 — about **120 seconds** of play.
- **First squirrel**: up at GO!, whacked within ~1 s (Blue's counter was already rolling to 0100 one second after GO!).
- **Post-whack lingering**: the flattened squirrel stays visible in the hole for ~1–2 s before sinking away.
- **Spawn cadence**: next squirrel up roughly 3–4 s after the previous one appeared (a second whack was banked ~4 s after the first); the 28-whacks-in-120-s total corroborates a ~3–5 s spawn interval.
- **Up-duration if ignored**: hard to isolate — squirrels in this round were almost always whacked within ~1–2 s; they appear to stay up on the order of 2–3 s before ducking back down.

## Animations

- **Pop**: the squirrel springs up out of a hole facing outward, upright, tail flicking.
- **Whack**: the scoring monkey lunges across/around the stump and slams its barrel mallet down; the squirrel is **squashed into a flattened brown lump** in the hole before sliding out of sight.
- **Whiff**: a monkey can be seen bringing the mallet down on the bare stump when it loses the race — recovery from the swing is the effective penalty.
- **Idle**: the non-swinging monkeys hover around their side of the stump, mallets shouldered, fidgeting.
- **Round end**: HUD clears and the camera pulls back — the winner (Blue) throws both arms up bouncing beside the stump while the losers slump face-down, heads buried in the grass like ostriches. Then the leaf-curtain transition wipes the scene.

## HUD / score display

One panel per active player pinned to a screen corner (three this session, four in the instruction video): the monkey's face in a colour-ringed circle, the colour name on a coloured banner (BLUE / ORANGE / GREEN), and a **four-digit odometer-style score box** whose digits roll mechanically on every +100 (a mid-roll "0092" is readable in the footage). The panel of whoever just scored briefly **enlarges with a dashed highlight ring** around the face icon. Bottom-centre sits the round timer: a **leaf-shaped dial with a red-tipped needle** that starts green and **fills orange** as time drains — fully orange just before the finish.

## Recreation notes

Parameters for a faithful re-implementation:

| Parameter | Value |
|---|---|
| Players | 2–4 monkeys around a central stump; camera slowly orbiting |
| Holes | 4, colour-ringed blue/orange/green/yellow (always all four, regardless of player count) |
| Round length | ~120 s, shown on a green→orange leaf dial |
| Spawns | one squirrel at a time, random hole; interval ~3–5 s (≈28 spawns/round observed) |
| Up-duration | ~2–3 s, then the squirrel retreats unwhacked |
| Input | first player to press the colour matching the occupied hole wins the whack |
| Points per whack | +100, rolling-digit credit |
| Wrong/late press | no point deduction; suggest a short swing-and-recover lockout (~0.5–1 s) as the observed effective penalty |
| Post-whack | squirrel flattens in the hole ~1–2 s; brief scorer-panel highlight |
| Animations needed | squirrel pop/flatten/retreat, monkey lunge-and-slam, whiff on bare stump, winner celebration, losers face-planted |

Design notes: with only +100 flat scoring and no deductions, the entire game is a reaction-time race — the colour-to-button mapping is the only cognitive load, and the orbiting camera keeps it honest by preventing players from parking on a screen position. The whiff lockout matters: without it, mashing all four colours would dominate, so a wrong press must eat the swing animation before the player can contest the next squirrel.
