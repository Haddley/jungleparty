# Ingestion log

Append-only. Newest entries last.

## 2026-07-06 — Wiki created; text sources ingested

Scaffolded the wiki and ingested the initial research sweep for the recreation project:

- [sources/us-instruction-manual](sources/us-instruction-manual.md) — archive.org OCR of the US PS2 manual (primary source: menus, buzzer controls, pause combo, official rules for Bubble Bath, Jungle Hurdles, Keep It Up, Island War, Monkey Bomb, credits).
- [sources/wikipedia](sources/wikipedia.md) — EN current + 2009 revision (official 40+10 game lists) + DE (categories).
- [sources/reviews](sources/reviews.md) — IGN, Wilcox Arcade, Kikizo, NoobFeed, SMH, Common Sense Media, Rory's Retrospectives.
- [sources/misc](sources/misc.md) — speedrun.com, PCSX2 wiki, PSP/PS3 version pointers.
- [sources/launch-trailer](sources/launch-trailer.md) + [sources/full-longplay](sources/full-longplay.md) + [sources/instruction-videos](sources/instruction-videos.md) — video sources registered; longplay chapter timestamps extracted (41 chapters, all 40 games); trailer identified as the **2010 PSN/PSP version** launch trailer, not PS2 2006.

Concept pages created: [game-overview](game-overview.md), [game-structure](game-structure.md), [buzz-controller](buzz-controller.md), [monkeys](monkeys.md), [minigames](minigames.md) (full catalog with longplay timestamps), [presentation](presentation.md).

Open items: EU vs US session-length counts; PS3 5-game list; ~12 catalog rules still marked *(inferred)*.

## 2026-07-06 — Frame-by-frame video analysis of the starter six + trailer

Downloaded the trailer and six longplay chapter segments to the session scratchpad, frame-stepped them with ffmpeg (transient frames, deleted after analysis; nothing stored in the repo), and wrote the six deep mini-game pages plus trailer notes:

- [bubble-bath](bubble-bath.md) — rule refinement: catches drain only the live streak (bank never drops), ~2s dunk lockout; score rate ramps ~15→75 pts/s; gorilla wakes every ~10–25s with a ~1.0–1.5s stir warning; original round ~120s.
- [jungle-hurdles](jungle-hurdles.md) — structural finding: hurdle waves are **shared** (four identical same-colour hurdles per wave, ~2s apart); banana skins are solo per-lane extras; true first-to-finish race (~200 units, ~35s); sprawl ~1.0–1.5s; "PERFECT" popups for late, well-timed jumps.
- [monkey-bomb](monkey-bomb.md) — 6 bombs per game; hidden fuse ~8–12s; ~55–60 pts/s held; totals clamp at 0; previous loser starts the next bomb; immediate pass-backs legal.
- [simian-shootout](simian-shootout.md) — structural finding: strictly **1v1 round-robin duels** with a gorilla referee (lollipop-buzzer signal after a 3–5s tease); +1000 per duel win; a false start hands the duel to the opponent.
- [totem-poles](totem-poles.md) — 40 heads per pole at 100 pts/chop, identical stacks for all players; finish bonuses 1st +2000 / 2nd +1000; wrong press costs time only; 45s dial.
- [whack-a-squirrel](whack-a-squirrel.md) — four shared colour-ringed holes in one stump; one squirrel at a time (up ~2–3s, spawns ~3–5s apart); flat +100 per whack; wrong press = whiffed swing, no score loss; ~120s round.
- [sources/launch-trailer](sources/launch-trailer.md) — full shot-by-shot + art direction notes; 12 of the PSP version's 15 games identified; PSP UI uses PlayStation face-button icons (the PS2 buzzer-colour scheme remains our model).

Concept pages updated with findings; [recreation-notes](recreation-notes.md) created recording all original→web parameter mappings and pacing deviations. All six game modules in `buzzjungleparty.html` corrected to match (Jungle Hurdles and Simian Shootout were structurally rewritten).

## 2026-07-06 — Recreation built and verified end-to-end

`buzzjungleparty.html` completed: PeerJS TV-host + phone-buzzer architecture, original SVG monkey rig, synthesized jungle music/SFX, six mini-game modules, banana standings, podium ceremony. Verified with a Playwright run driving one TV window plus three phone windows through a full 4-round party to the podium (join by room code, instruction cards, all input paths, placements, bananas, ceremony) with zero page errors; TV and controller screenshots reviewed at every phase. Wiki link lint: 22 pages, all links resolve, all reachable from [index](index.md). Downloaded footage deleted from the scratchpad per the [asset policy](recreation-notes.md#asset-policy).

## 2026-07-06 — Sprite & animation overhaul (rig v2)

Full visual upgrade of `buzzjungleparty.html`, all original SVG/CSS per the asset policy:

- **Monkey rig v2** — gradient-shaded fur (shared `<defs>` gradients injected once at boot so per-frame string rebuilds never churn IDs), hands with palms, feet with toes, tail tuft, hair tuft, inner ears, expressive brows (raised/determined/sad), drifting pupils with catchlights, breathing, deterministic ear-twitch/blink cycles. Pose upgrades: cheer (open grin + teeth + tongue + orbiting sparkles), mourn (drooped ears, animated tears), bonked (head lump + orbiting stars), run (gallop lean, ears back, speed lines), hold (worry brows + sweat drop), zap (jagged bolts, standing hair, cartoon skeleton flicker), flat (popped eyes, dust puffs). New poses: **blow** (puffed cheeks, for Bubble Bath), **throw** (Monkey Bomb pass, Totem chop), **whack** (mallet raised overhead).
- **Supporting cast** — gorilla: gradient body, brow ridge, inflating snot bubble (doze), widening peek eye + "?" (stir), ear steam + zigzag teeth (awake), glossy paddle. Squirrel: fluffier tail, ear tufts, darting pupils, new *bonked* mode (X eyes, tongue, stars). Bomb: rising fuse smoke. Explosion: smoke ring + flying debris + white-hot core.
- **Scenery** — day: two butterflies on flutter paths, toucan flyby, perched parrot with head-bob (all CSS-keyframe, outside the per-frame repaint); night: pulsing glow mushrooms; both: swaying foreground canopy leaves in the stage corners (validates the "environments feel alive" note in [presentation](presentation.md)).
- **Per-game juice** — Whack: mallet swing + POW! star + dazed squirrel sinking back. Bubble Bath: rubber duck, steam wisps. Hurdles: banana-peel sprite (was emoji), breakable finish tape. Shootout: winner star-burst, rolling tumbleweed during the tease. Monkey Bomb: scorch mark under the blast. Totem: flying wood chips, wobble grows as the pole shrinks, glow on the last three heads. Results/podium: falling confetti; the phone buzzer's mini monkey now cheers/mourns with your placement.

Verified with a pose-sheet screenshot (11 poses × 4 colours + full supporting cast at two animation phases) and a full 6-round Playwright party (TV + 2 phones) exercising every game's new effects — zero page errors. Updated [monkeys](monkeys.md).

## 2026-07-06 — Every game documented: 36 new per-game pages

The catalog's remaining games — 34 multiplayer plus the 2 single-player exclusives — now each have their own page, completing per-game coverage of all 40+2. No new sources were ingested; each page digests everything already on file (manual rule sets, review fragments, trailer sightings, longplay chapter links, NPC/presentation cross-references) into a fixed shape: sourced facts up top, rules with *(inferred)* marking, **verification targets** for a future frame-analysis pass, and a phone-buzzer recreation sketch with candidate parameters.

Notable syntheses: [island-war](island-war.md) documents the manual-verified two-press sweep-aim mechanic as the shared grammar for all six throwing games; [freefall](freefall.md) and [monkey-slide](monkey-slide.md) are placed in the Monkey Bomb hot-potato family; [lion-taming](lion-taming.md)/[crazy-croc](crazy-croc.md)/[ostrich-eggs](ostrich-eggs.md) form the push-your-luck family descended from Bubble Bath's verified rules; trailer shots pinned staging for [lethal-lily-pads](lethal-lily-pads.md), [monkey-catapult](monkey-catapult.md), [primate-penalties](primate-penalties.md), [rocket-riders](rocket-riders.md), [odd-one-out](odd-one-out.md) and (tentatively) [crate-surprise](crate-surprise.md). The three near-unknowns — [deadly-dynamite](deadly-dynamite.md), [run-around](run-around.md), [whackers-revenge](whackers-revenge.md) — are flagged as top priorities for the next video pass.

[minigames](minigames.md) now links every row to its page; [index](index.md) gains a grouped listing of all game pages; [sources/full-longplay](sources/full-longplay.md) note updated. Open items unchanged: EU vs US session-length counts; PS3 5-game list; single-player footage needed for the two exclusives.

## 2026-07-06 — Animation system v3 (pose blending) and audio v2

**Animation.** The rig now blends between poses instead of snapping — the recreation's answer to the original's praised "seamless transitions" ([monkeys](monkeys.md)). `monkeySVG` was split into pose targets → spring → renderer: every limb control point, the tail (8 blended coordinates), squash, rotation and brows are eased by a slightly underdamped spring (natural anticipation/overshoot — a flattened monkey now *splats*, a landing jump squashes), while fast cycles (gallop, cheer wave, zap vibration) ride on an additive channel after the spring so easing never damps them. Per-entity state keyed by player id, cleared each mini-game. Specific fixes from playtest feedback: the **run cycle** is a true alternating gait (antiphase legs, per-leg foot lift on the forward swing, counter-swinging arms, double-frequency footfall bounce with stride squash); Jungle Hurdles gained a dedicated **jump pose** (tucked knees, flung arms, stretched body) with a real half-lane arc and take-off dust; the **squirrel** now bobs, leans, cocks its head, fidgets its paws and taunts (squint + tongue) on a ~2.6 s cycle, and pops up with ease-out-back overshoot; the **gorilla** got the same spring treatment plus a furious alternating **chest-beat** when awake, an eye-rub while stirring, knuckle-rock at idle, and an arm-tracked paddle — his Bubble Bath wake now visibly lunges, with a splash row across the tub.

**Audio.** SFX vocabulary v2: layered, characterful synthesis (detuned saw buzz, vibrato boing, wet splat sweep, crackling zap, multi-syllable monkey hoot, wood-block ticks, drum-roll for the countdown) plus a slapback echo bus per output (music/SFX, so mute toggles still apply) for jungle space. Music v2: a shared percussion kit (kick, djembe low/slap, shaker, tambourine, clave, tom, block), two-bar 32-step patterns with bass lines, marimba leads with echo, velocity accents, a 3-2 clave in the lobby, and a low breathy "chant" pad on downbeats — matching the "driving jungle rhythms, heavy chanting" note in [presentation](presentation.md). Urgent mode swaps shaker→tambourine 16ths and pushes the lead up an octave.

Verified: pose sheet re-render, a full 6-round two-phone Playwright party across all six games (zero page errors), and a runtime audio smoke test exercising every SFX, drum, chant and all steps of all four music tracks.
