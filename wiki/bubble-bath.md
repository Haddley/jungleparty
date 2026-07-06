# Bubble Bath

**Category: Luck** · **Controls: hold the red Buzz! button**. One of the [starter six](minigames.md) deep pages. Four [monkeys](monkeys.md) share a jungle pool with a dozing gorilla; hold the buzzer to blow bubbles and rack up points, release before he wakes or lose everything you haven't banked. Rules below come from the [manual](sources/us-instruction-manual.md), verified and enriched against the [longplay](sources/full-longplay.md) chapter at 0:04:48 ([watch](https://www.youtube.com/watch?v=dZEJTdSRqrY&t=288s)) — an instruction video followed by one full round (three human players: Blue, Orange, Green).

## Rules and scoring (as observed)

- **Hold Buzz! to blow bubbles.** While held, a live "streak" counter under your banked score ticks upward and a mound of white foam grows in front of your monkey.
- **Release to bank.** On release the streak transfers into your banked total. Banked totals never decrease — confirmed on video (Orange kept 0415 through two catches).
- **Get caught, lose the streak.** If the gorilla wakes while you are still holding, your live streak drains to zero in under a second (digits flash as they count down) and is lost. Only the unbanked streak is forfeited; there is no deduction from the bank. The gorilla rears up and slams both arms down, dunking every still-holding monkey face-first (cartoon impact stars along his arms). Dunked monkeys resurface after roughly 2 seconds.
- **Point rate ramps.** Early holds accrued at roughly 10–15 points/second; later, sustained holds built streaks of 500–600 in under ten seconds (~60–75 points/second). The rate clearly accelerates the longer a hold is sustained (and/or rises as the round progresses) — the risk/reward core of the game.
- **Round length ≈ 120 seconds** of play (HUD appears ~6s after the intro pan; the finale triggers about two minutes later). A leaf-shaped dial at top-centre is the round timer.
- **Win condition: highest banked total when time expires.** Observed totals near the end: Orange ~3175, Blue 2396, Green 2270.

The manual's summary — hold to make bubbles, release before the gorilla wakes or he hits you on the head — holds up, with one refinement: the "bonk" costs you your unbanked streak plus ~2 seconds of downtime, nothing more.

## Scene

A round jungle lagoon serves as the "bath", ringed by mossy rocks with several waterfalls cascading down ochre cliffs behind it. Dense oversized leaves frame the left and right screen edges. The camera is a fixed frontal shot, roughly water level, pulling back to a wide view for the finale.

The gorilla lies face-down across a rock ledge at the back-centre of the pool, arms spread wide along the banks to either side — his body visually splits the pool in half. The monkeys sit chest-deep in the water facing the camera, two per side of the gorilla; in the 4-player instruction video the left-to-right order is **Blue, Orange, gorilla, Green, Yellow** (in the observed 3-player round Yellow's spot is empty). Each monkey wears a swim cap and goggles in its player colour.

Comedic prop: a **yellow rubber duck** drifts around the foreground and swaps hats as the round progresses (bare, then a little safari/pith hat, and other headgear) — pure set dressing.

The finale is the punchline: the gorilla stands up in the middle of the pool revealing his pale belly, strikes a relaxed hands-behind-head pose, and bubbles fizz up around *him* — the game's ESRB "crude humor" moment. The HUD disappears, the camera pulls wide, and a leaf-wipe transition ends the game (the winner podium falls outside this clip).

## The gorilla's tell and timing

- **Asleep**: lying flat, Z glyphs floating up, with an occasional exaggerated open-mouth snore. Safe to hold.
- **Wake events are random**, observed at roughly 10–25 second intervals across the round (events near clip marks 0:44, 1:03, 1:23, 2:13, 2:17).
- **Warning window ≈ 1.0–1.5 seconds.** Frame-stepping a wake at 5 fps: first stir (head lifts, Z's vanish) → arms raised high ≈ 0.4s → full double-arm slam onto the water ≈ 1.4s after the first stir. A player watching for the stir has about one second to release.
- **Harmless wakes happen.** In one event nobody was holding when he woke; he sat up, peered at the water, had a big stretch and settled back down — no slam. Players even resumed holding while he was still upright, without penalty. The punishment is tied to the slam moment, not to him merely being awake.

## Monkey animation states

- **Idle** — bobbing chest-deep, arms loose, gentle sway (looping, ~1–2s cycle).
- **Blowing bubbles** — face lowered to the water, cheeks working, white foam mound growing in front; sustained for as long as the button is held (holds of 5–15s observed).
- **Release / "wasn't me"** — arms shoot up out of the water in an innocent hands-up pose when the gorilla stirs (~1s).
- **Caught / dunked** — shoved underwater face-first by the arm slam, impact stars, ~2 seconds submerged before resurfacing.
- **Finale** — all monkeys idle and watch the gorilla stand; celebration/mourn poses (see [monkeys](monkeys.md) state list) presumably follow on the results screen not captured here.

## HUD

Player panels sit along the top of the screen, one per active player, colour-coded (dark blue, orange, green in this round). Each panel is a rounded rectangular nameplate in the player colour: a circular monkey-face portrait on the left, the player name ("BLUE", "ORANGE", "GREEN") in white capitals beside it. Below the nameplate are two white pill-shaped counter boxes with dark four-digit, leading-zero readouts: the **top box is the banked total**, the **bottom box the live bubble streak**, which visibly counts down as it drains when caught. Centre-top between the panels sits the **leaf dial round timer**: a stylised leaf with a red-tipped needle that sweeps as time passes; the leaf is green early, turns orange past the midpoint, and is red and curling by the final stretch.

## Audio (inferred from visuals)

No audio was analysed; from the visuals and the [presentation](presentation.md) research the expected cues are: waterfall/jungle ambience throughout; loud comedy **snoring** synced to the Z glyphs; a wet **bubbling/raspberry** loop while a streak is building; a roar-plus-splash and cartoon **bonk** on the arm slam; a monkey **screech** from each dunked player; a rising fizz for the finale belly-bubble gag; likely a ticking or musical intensification as the leaf timer reddens.

## Recreation notes

Concrete parameters for a web recreation (tuned to the observed round):

- **Round length**: 120 000 ms. Timer dial: green → orange at ~50%, red at ~85%.
- **Scoring while holding**: start at 15 pts/s and ramp linearly to 75 pts/s over ~6 s of continuous hold; reset the ramp on every release or catch. (Simplest faithful alternative: flat 25 pts/s early round, 60 pts/s in the second half.)
- **Banking**: on release, transfer streak → bank with a fast count-up animation (~500 ms). Bank is immutable.
- **Gorilla sleep scheduler**: next wake at random uniform 8–20 s after he settles; guarantee 6–10 wakes per round.
- **Warning window**: 1200 ms from stir cue (head lift, snore SFX stops, audio gasp) to slam impact; releases registered before impact keep the streak safe.
- **Penalty on catch**: streak drains to 0 over ~700 ms with red flashing digits; caught player locked out (dunked) for 2000 ms.
- **Harmless-wake variant**: if nobody is holding at wake time, play a stretch animation instead of the slam; allow re-holding immediately (matches footage).
- **Props/polish**: rubber duck drifting with escalating hats; Z glyphs; impact stars on the slam; belly-bubble finale before results.

Observations above are from the longplay chapter at 0:04:48; frame notes were taken from a ~2m46s capture and no imagery is reproduced here.
