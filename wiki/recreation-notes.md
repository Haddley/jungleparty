# Recreation notes

How `buzzjungleparty.html` maps the original game to the web, and where it deliberately deviates. Architecture blueprint: `~/Documents/GitHub/games/boggleparty.html` (PeerJS phone-controller party game).

## Asset policy

**Nothing in this project is copied from the original game.** All art is original SVG/CSS (one monkey rig recoloured four ways, emoji for props); all music and SFX are synthesized at runtime with the Web Audio API; announcer lines are original text in the register described in [presentation](presentation.md). The wiki documents the original in words and links to public videos — no frames, sprites, or audio rips are stored. Video analysis used transient scratchpad frames that were deleted after the written notes were made.

## Architecture (inherited from the blueprint)

- Single self-contained HTML file; CDN deps: PeerJS 1.5.4, qrcode-generator 1.4.4.
- Host-authoritative WebRTC: the TV screen claims peer ID `BZJP-<4-letter code>`; phones join by code or QR (`?room=CODE`). JSON messages: `join`, `buzz {btn,down}`, `ctl`; host pushes per-player `state`.
- The first phone to join is the **captain** (👑) and drives flow (length select, next game, play again) — mirroring the blueprint's TV-host pattern.
- During play the host pushes controller state every 200ms and the phone patches its DOM in place, so held buttons (Bubble Bath) survive updates.

## The phone as Buzz! controller

Per [buzz-controller](buzz-controller.md): full-screen handset — big red dome (top ~40%), then the blue/orange/green/yellow stack. Buttons depress, vibrate (`navigator.vibrate`), and are enabled per mini-game (e.g. only colours in [Totem Poles](totem-poles.md), only red in [Bubble Bath](bubble-bath.md), other monkeys' colours — labelled with their names — when you hold the bomb in [Monkey Bomb](monkey-bomb.md)). A prompt strip above the buzzer carries the per-game instruction. Note the PS2 buzzer is our model; the PSP/PSN version seen in the [trailer](sources/launch-trailer.md) used PlayStation face-button icons instead.

## Session flow vs the original

| Original | Recreation |
|---|---|
| Up to 4 buzzers, monkeys Blue/Orange/Green/Yellow | Same; colour assigned by join order |
| Length: Short/Medium/Long/Marathon (10/15/20/25 US or 5/10/20/40 EU) | Short/Medium/Long = 4/6/8 rounds from the [starter-six](#starter-six) pool |
| Narrated instruction video, Buzz! skips | Instruction card + optional Web Speech announcer, red button skips |
| Bananas by placement across the session | Same: 4/3/2/1 per game |
| Winner ceremony, Hall of Fame | Podium + fireworks; no persistent leaderboard (yet) |
| Standard/Custom start, costumes, practice | Not implemented (Quick-Start flow only) |

## Starter six

Chosen for documentation quality + full controller coverage. Parameters come from the per-game wiki pages (each verified frame-by-frame against the [longplay](sources/full-longplay.md)); deviations are for phone-tap pacing:

| Game | Fidelity notes |
|---|---|
| [Bubble Bath](bubble-bath.md) | Ramping 15→75 pts/s, ~1.2s stir warning, catch drains streak only. Round 45s vs original ~120s. |
| [Simian Shootout](simian-shootout.md) | Quick-draw duels, false-start penalty. Structure verified from video. |
| [Whack A Squirrel](whack-a-squirrel.md) | Four shared colour holes, +100/whack, whiff = time cost only. 45s vs original ~120s; spawn gaps compressed ~3–5s → 2–3.5s. |
| [Monkey Bomb](monkey-bomb.md) | Faithful: 6 bombs, hidden 8–12s fuse, ~55 pts/s, clamp at 0, loser starts next bomb. |
| [Jungle Hurdles](jungle-hurdles.md) | Faithful: shared colour waves every ~2s, solo banana skins on red, ~1.3s sprawl, first over 200 units. |
| [Totem Poles](totem-poles.md) | Identical stacks, 100/chop, +2000/+1000 finish bonuses. 22 heads vs original 40 (phone taps are slower than buzzer presses). |

## Known gaps / future work

- Remaining 34 catalog games ([minigames](minigames.md)) — the module interface (`start/tick/onBuzz/ctrl/tv/end`) is designed for them.
- Costume editor, practice mode, persistent Hall of Fame.
- Dedicated spectator/scoreboard join (protocol supports viewers; no UI button).
