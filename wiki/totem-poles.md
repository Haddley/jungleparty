# Totem Poles

Category: **Speed**. Controls: the **four colour buttons** (blue, orange, green, yellow) — no Buzz! button. Each [monkey](monkeys.md) stands at the foot of a towering totem pole of coloured tiki heads and must hammer the stack away **from the bottom**: press the colour button matching the current bottom head and the monkey whacks it out with a mallet, dropping the pole one notch. Finish your whole pole before the round timer runs out — first to demolish theirs takes the biggest bonus. One of the games in the [minigames](minigames.md) catalog.

Sources: all observations are from the [longplay](sources/full-longplay.md), chapter 1:40:31 ([watch](https://www.youtube.com/watch?v=dZEJTdSRqrY&t=6031s)) — an instruction video followed by one full 3-player round (Blue, Orange, Green; no Yellow this session). See also [reviews](sources/reviews.md).

## Rules & scoring as observed

- **One round per game**, on a shared countdown timer (a needle dial in the centre of the HUD sweeping from green to red; the observed round ran ~45 seconds of play after a "READY" intro).
- **Chop from the bottom** (confirmed): the target is always the lowest head on your own pole. A correct press knocks it out sideways and the whole stack drops down one place. There is no way to hit any other head.
- **Stack height: 40 coloured heads per pole.** Every chop is worth **100 points**, and both players who finished did so on a base score of exactly 4000 before their bonus. Topping each pole is a **grey stone cap head** that is never chopped — it settles on the ground as a little moai-style statue when the 40th head goes, marking a finished player.
- **Identical stacks**: at the starting whistle all poles show the same head sequence, so the race is fair; the sequences diverge on screen only because players chop at different speeds. The pole is far taller than the screen — upcoming heads scroll down from above as you work.
- **Finish bonuses**: "1ST" flashes over the first player to demolish their pole, with a floating "+2000" (Green: 4000 → 6000). The second finisher gets "2ND" and **+1000** (Blue: 4000 → 5000). Anyone still chopping at the whistle simply keeps their chop score (Orange ended on 3400 with about six heads still stacked). A 3rd-place bonus presumably exists in 4-player games but was not observed.
- **Wrong presses**: no penalty was directly caught at the sampled frame rate; no counter ever rolled backwards, so the cost appears to be time only — a fumbled swing/recovery animation rather than lost points.
- Final scores of the observed round: Green 6000, Blue 5000, Orange 3400.

## Scene

Side-on, fixed camera, and unusually for this game it is **night**. A jungle clearing on a grassy cliff-edge ledge, lit by glowing firefly jars hanging from the branches, with vines and dark foliage behind. Two to four totem poles descend from above the top of the screen, one per monkey, each pole standing on a small drum-like base; a spare tree-stump drum sits at the right edge. Each monkey stands beside its pole wielding a wooden mallet. The round opens with a big orange orangutan looming into the foreground to slam a giant red buzzer as "READY" letters fly in.

The heads are chunky carved tiki faces in the four buzzer colours, with several sculpt variants per colour — bug-eyed angry orange faces with heavy brows, slat-mouthed orange "crate" faces, blue frowners baring teeth, yellow grinners, green grimacers — stacked cheek-to-jowl so the pole reads as a wall of expressions. The instruction video plays inside the standard bamboo-framed screen with a wooden "TOTEM POLES" nameplate over the leaf-pattern backdrop, demonstrating a 4-player race.

## Chop animation

On a correct press the monkey rears back and swings the mallet into the bottom head, which **shoots out sideways** (left or right, varying) with a squashed motion-blur streak before vanishing; the stack thumps down one notch in the same beat. The cycle is fast — the winner averaged about **1.3 chops per second** over the whole round (40 heads in ~30 s), so the swing-and-drop loop must resolve in well under a second. When the last coloured head goes, the grey cap drops to the ground as a statue and the monkey turns to celebrate, mallet held high, while the others keep hammering.

## HUD / progress display

Wooden panels along the bottom edge, one per active player (three this session; four in the instruction video): the monkey's face in a colour-ringed circle, the colour name (BLUE / ORANGE / GREEN), and a **four-digit odometer-style counter** that rolls up 100 per chop — mid-roll frames show values like 3097 or 2499 blurring between hundreds. Between the panels sits the **round-timer dial**, a leaf-shaped gauge whose needle sweeps from the green zone at the start to red at the whistle. There is no explicit "heads remaining" readout; progress is read from the pole itself and the counter.

## Results

Placement text ("1ST", "2ND") flashes in situ over each finishing player, followed by the floating bonus figure ("2000" bursting into drifting digits). When the timer expires the HUD fades, unfinished poles simply stop, and losers slump while finishers keep celebrating beside their statues. The scene fades to a winner cutscene: the champion monkey alone in the clearing, hopping and brandishing the mallet next to a repainted, player-coloured version of the stone tiki statue.

## Recreation notes

Parameters for a faithful re-implementation:

| Parameter | Value |
|---|---|
| Players | 2–4 monkeys, side view, one pole each |
| Stack | 40 coloured heads + 1 grey non-choppable cap; identical random sequence for all players |
| Head colours | the 4 buzzer colours, uniformly mixed; 2–3 face variants per colour for visual texture |
| Round timer | ~45 s fixed, shown as a green-to-red needle dial |
| Correct press | bottom head flies out sideways, stack drops; ~300–500 ms swing cycle (winner sustained ~1.3 chops/s, so allow bursts near 2/s) |
| Wrong press | no point loss; time penalty only — suggest a ~500–800 ms fumble/stun lockout (not directly measured) |
| Scoring | 100 pts per head; finish bonuses +2000 / +1000 (suggest +500 for 3rd); non-finishers keep chop score |
| Expected round | strong player finishes in ~30 s; weaker players clear ~30–35 heads by the whistle |
| Animations needed | mallet swing, head knock-out with motion streak, stack drop, cap-statue settle, fumble, celebration, dejected idle, winner cutscene |

Design notes: the game is a pure reaction chain — read the bottom head, press, re-read — and its feel depends on the stack drop being instant and rhythmic. Tuning matters most in two places: the wrong-press lockout (long enough that mashing all four buttons is slower than reading) and the finish bonuses, which are big enough (half a finished pole's base score) that placement, not raw chop count, decides the round.
