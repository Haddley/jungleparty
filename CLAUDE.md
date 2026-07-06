# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## What this is

A browser recreation of the PS2 party game **Buzz! Junior: Jungle Party** (Magenta Software / SCEE, 2006) where mobile phones act as Buzz!-style buzzer controllers. Two deliverables:

- `buzzjungleparty.html` — the entire game: one self-contained file, no build step. CDN deps only (PeerJS 1.5.4, qrcode-generator 1.4.4).
- `wiki/` — the research wiki behind every design decision (LLM Wiki pattern).

Architecture is modelled on `~/Documents/GitHub/games/boggleparty.html`; sibling games there (`familytrivia.html`, `pit.html`) use the same patterns.

## Asset policy (hard constraint)

**No copyrighted material from the original game may be stored in this repo** — no sprites, video frames, screenshots, music, or sound-effect rips. All art is original inline SVG/CSS; all audio is synthesized at runtime via the Web Audio API. Research documents the original in *written descriptions* with links/timestamps to public sources. Do not add extracted game assets, even "for reference". Transient analysis frames belong in the session scratchpad and must be deleted after notes are written.

## Commands

- Serve: `python3 -m http.server 8471` → `http://localhost:8471/buzzjungleparty.html`
- Syntax-check the inline script (no bundler, so do this after edits):
  `python3 -c "import re;open('/tmp/check.js','w').write(re.findall(r'<script>(.*?)</script>',open('buzzjungleparty.html').read(),re.S)[-1])" && node --check /tmp/check.js`
- E2E (no local node_modules — reuses Playwright from the games repo): run a script importing `/Users/neilhaddley/Documents/GitHub/games/node_modules/playwright/index.mjs`; drive one 1280×720 "TV" page (click `button.host`, read the room code from `.roomtag`) plus 390×780 phone pages (fill `#fname`/`#fcode`, click `button.join`), then dispatch `pointerdown`/`pointerup` on `#btn-red`/`#btn-<colour>`. Host internals are inspectable from the TV page via `window.H` (e.g. `H.phase`, `H.players`). A reference script lives in the session scratchpad as `e2e.mjs`.
- Manual multiplayer test: one browser window as TV host + 2–4 phone-sized windows (DevTools device mode) joining with the room code. PeerJS uses the public cloud broker, so internet is required even for localhost testing.

## Game architecture (`buzzjungleparty.html`)

One `<script>`, sectioned by banner comments, rendered into `#app` as template-literal HTML (blueprint pattern):

- **Roles**: the TV screen is the authoritative host (PeerJS ID `BZJP-<4-letter room code>` — deterministic, so phones join by code alone; QR encodes `?room=CODE`). Phones are controllers. The **first phone to join is the "captain"** and drives flow via `ctl` messages (start + length select, next game, play again).
- **Protocol** (JSON over PeerJS DataConnection): controller→host `{type:'join',name}`, `{type:'buzz',btn:'red'|'blue'|'orange'|'green'|'yellow',down:bool}` (down/up split matters — Bubble Bath holds), `{type:'ctl',action}`; host→controller `{type:'state',...}` with per-player fields from `stateFor(pid)` (phase, `buttons` enable-map, `prompt`, `me`, `results`).
- **Host state machine** `H.phase`: `lobby → (instruct → countdown → playing → miniresults) ×rounds → podium`. `hostPlay()` runs a rAF loop: calls the mini-game's `tick`, repaints the TV stage (`tvPatchGame`), and pushes controller state every 200ms. Controllers **patch in place** during `playing` (`patchBuzzer`) so a held button's DOM element survives updates — don't replace buzzer innerHTML mid-game.
- **Mini-games** live in the `GAMES` registry; each is `{name, short, desc, how, voice, start(ctx)→st, tick(st,dt)→done, onBuzz(st,player,btn,down), ctrl(st,player)→{buttons,prompt}, tv(st)→html, end(st)→placements}`. Add a game = add a registry entry; session flow, banana scoring (4/3/2/1 by placement via `BANANAS`), instruction cards and results screens are generic. Gameplay parameters come from the wiki page for that game — cite it in a comment (see existing modules).
- **Players are the four monkeys** Blue/Orange/Green/Yellow (`COLORS`, join order = colour); max 4; reconnect-by-name reclaims a slot. `monkeySVG(colorId,pose)` is the single original monkey rig (poses: idle/cheer/mourn/bonked/run/hold/zap/flat).
- **Audio**: all synthesized — `tone()`/`noise()` primitives, `S.*` SFX vocabulary, `MTRACKS` step-sequencer (per-screen tracks, `setMusic(track,urgent)`), lazy AudioContext unlock on first pointerdown, toggles persisted in localStorage. Optional Web Speech announcer via `say()`.

## The wiki (`wiki/`)

LLM Wiki per https://haddley.github.io/posts/LLM-Wiki/, plain style: no YAML frontmatter, no `[[wikilinks]]`; kebab-case filenames, single `# Title` H1, relative links (`[x](page.md)`, `../page.md` from `sources/`).

- `wiki/index.md` — master catalog; every page must be reachable from it.
- `wiki/log.md` — append-only dated log (`## YYYY-MM-DD — title`, newest last).
- `wiki/sources/<name>.md` — one page per ingested source, opening with "Reviewed YYYY-MM-DD" and a what/where/licence note.
- `wiki/<concept>.md` — one topic per file. Per-mini-game pages carry the verified rules and the recreation parameter tables the code cites.

Ingest workflow for a new source: read it → write/update its `sources/` page → update `index.md` → update affected concept pages → append to `log.md`. Facts carry citations; rules not yet verified on video are marked *(inferred)*. `wiki/minigames.md` is the full 40+2 catalog with longplay timestamps; `wiki/recreation-notes.md` records original→web deviations (round lengths compressed for phone-tap pacing, etc.).
