# Jungle Hurdles

**Category:** Skill · **Controls:** all five buttons — the four colour buttons (blue, orange, green, yellow) to leap the matching coloured hurdles, and the big red Buzz! buzzer to leap banana skins. One of the few games in [minigames](minigames.md) that uses the entire [buzz-controller](buzz-controller.md).

A four-lane sprint down a jungle running track. Waves of coloured hurdles sweep in from the right; press the button that matches the hurdle's colour to jump it, and press Buzz! (red) when a banana skin lies in your lane — or your monkey slips flat on its face and the others pull ahead. First across the finish line wins.

All observations below are from the [longplay](sources/full-longplay.md), chapter 0:51:07 ([watch from 0:51:07](https://www.youtube.com/watch?v=dZEJTdSRqrY&t=3067s)): the in-game instruction video (~28 s) followed by one full four-player round (~37 s). Rules cross-checked against the [manual](sources/us-instruction-manual.md).

## Rules and scoring

- **Race format, first to finish.** This is a genuine point-to-point race, not a distance-in-fixed-time game. The track has a bunting-and-white-line start gate and an identical finish gate; roadside signposts count *down* the remaining distance (160 → 140 → 120 → 100 → 80 → 60 → 40 → 20 → finish, implying a ~200-unit course). The round ends shortly after the field crosses the line, with a leaf-wipe transition.
- **Hurdle waves are shared, one hurdle per lane.** Every hurdle wave is monochrome: four identical hurdles of the same colour, one in each lane, staggered in a shallow diagonal (matching the track's perspective). All four players therefore answer the same colour at almost the same moment — the game tests everyone on the same prompt, per-lane collision but shared colour.
- **Correct press = jump.** The monkey vaults the hurdle. A well-timed press earns a **"PERFECT"** popup under that monkey (seen repeatedly for the leaders); PERFECT jumps appear to carry no speed loss, and the leaders who string PERFECTs together steadily pull away.
- **Wrong or missed press = fall.** The monkey crashes and sprawls face-down flat on the track (observed on the trailing green monkey at the 80-marker: upright one second, flat the next, running again the next), costing roughly 1–1.5 s before it picks itself up — several body-lengths against runners who cleared the wave.
- **Banana skins are per-lane, red-button obstacles.** Unlike hurdles they do not come in waves: a single skin lies flat in one lane (occasionally shown with a small red marker above it, echoing the red buzzer). Press Buzz! to hop it; failing to means a slip with the same face-plant penalty (per the manual: "press Buzz! to leap banana skins or you slip over").
- **Scoring** follows the game's standard convention: bananas awarded by finishing position on the results screen (the clip's leaf-wipe cuts before the podium, so exact banana counts were not observable here).

## Scene and camera

- **View:** side-on with a slight top-down tilt, monkeys running left to right. The camera scrolls continuously rightward, keeping the main pack in the left-to-centre third of the screen. Notably the camera does *not* chase the leader — in this round the yellow monkey led off-screen right for the whole race and only reappeared standing celebrating just past the finish line as the camera caught up.
- **Track:** four parallel grassy lanes separated by worn dirt ridges, dotted with pale flower clusters. Dense jungle dressing above and below the track: pink blossom trees, fallen logs, red spiky plants, rocks, waterfalls, a tent; black silhouetted spectator monkeys occasionally bob through the foreground foliage at the bottom edge.
- **Start/finish:** a white line across all lanes under strings of multicoloured bunting on poles. At the start an **orangutan starter** stands bottom-right holding a red, buzzer-shaped air horn and calls the race off with big "READY" then "GO!" text cards.
- **Look-ahead:** a hurdle wave becomes visible entering the right edge roughly 1.5–2 s before it reaches the pack — about half a screen of warning. Typically one wave is on screen ahead of the runners at any time (occasionally the previous wave is still exiting behind them).
- **Obstacle frequency:** waves arrive steadily about every 2 s. Colours observed across the round, in no fixed rotation: blue, green, orange, yellow, orange, blue, yellow(+banana), blue, green, yellow(+banana), orange, blue, green, yellow, blue — i.e. all four colours drawn apparently at random, with banana skins interleaved as solo extras every few waves.

## Monkeys and animations

- The four racers are the standard player monkeys in blue, yellow, orange and green shirts. Before "READY", floating colour name-plates ("BLUE", "ORANGE", "GREEN", …) tag each lane.
- **Run:** a bounding four-limbed gallop, dust/flower puffs kicked up behind.
- **Jump:** a big forward vault with limbs stretched, lasting roughly 0.5–0.8 s, landing back into the run without pause; "PERFECT" flashes beneath on a well-timed clear.
- **Fall/slip:** a face-first sprawl, the monkey lying flat prone on the track for about a second before scrambling up — the visible mechanism by which gaps open up.
- **Finish:** finished monkeys stop just past the line and celebrate (jumping with arms raised) while stragglers run in behind them.

## HUD

Essentially diegetic — there is no overlay score bar:

- Lane name-plates in player colours shown only during the pre-race line-up.
- "READY" / "GO!" start cards with the orangutan starter.
- "PERFECT" text popups under monkeys for well-timed jumps.
- Blue roadside signposts counting down the distance remaining (…160, 140, 120, 100, 80, 60, 40, 20) — these double as the only progress indicator.
- Relative standing is read directly from monkey positions on screen; a far-ahead leader simply leaves the frame.

## Results

The captured clip ends on the leaf-wipe immediately after the finish, before the results screen. Observable finishing order in this round: yellow (off-screen leader, first), blue, orange, green (the green monkey, who fell at least once, trailed throughout). Banana awards by placement are presumed per the game's standard results presentation (see [minigames](minigames.md)).

## Recreation notes

Concrete parameters estimated from the footage (PAL longplay, values ± ~20%):

- **Race length:** ~200 distance units (signposts every 20 units), ~35 s from "GO!" to the pack crossing the line at base pace.
- **Scroll speed:** camera/background moves ~1/3 screen width per second (≈160 px/s at 480 px frame width); one screen ≈ 3 s of travel; ~5.7 distance units/s (20-unit signpost interval passes every ~3.5 s).
- **Obstacle interval:** one monochrome 4-lane hurdle wave every ~2.0 s (roughly one wave per 12 distance units); banana skins as solo per-lane extras every 3–5 waves.
- **Reaction window:** ~1.5–2 s from a wave entering the right edge to contact; grade the press — a press inside roughly the last 300–500 ms before contact reads as "PERFECT", earlier correct presses still clear the hurdle without the popup.
- **Stumble penalty:** ~1.0–1.5 s prone plus re-acceleration; net loss vs. a clean runner ≈ 8–12 distance units per fall, which matches the on-screen gaps.
- **Jump:** ~0.5–0.8 s airborne, no speed loss on a clean clear.
- **Wave stagger:** offset the four lanes' hurdles by a small per-lane x-offset (a shallow diagonal, ~50–100 ms lane-to-lane) purely as a perspective touch; colour is identical across the wave.
- **Camera rule:** follow the median/rear pack, clamp so trailing players stay on screen; let a runaway leader exit frame right and re-enter at the finish.
