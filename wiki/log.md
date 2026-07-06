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
