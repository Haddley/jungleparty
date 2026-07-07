# Splat

**Category: Accuracy** · **Controls: Buzz! button** · Longplay chapter 1:37:36 ([watch](https://www.youtube.com/watch?v=dZEJTdSRqrY&t=5856s)). Not yet recreated; rules from a detailed review.

Paintball target practice on the gorilla: throw paintballs at him, best splats win. The put-upon gorilla host — manual narrator, [Bubble Bath](bubble-bath.md) sleeper, [Simian Shootout](simian-shootout.md) referee — here becomes the literal target ([monkeys](monkeys.md) NPC list notes him as "paintball target in Splat").

## What the sources say

- [Wilcox Arcade](sources/reviews.md) documents the rules: throw paintballs at the gorilla; best splats win.
- German Wikipedia category: **Accuracy**.

## Rules (reported / *(inferred)* where noted)

- Players lob paintballs at the gorilla; scoring by "best splats" suggests placement quality (bullseye zones on the gorilla, or splat coverage) rather than raw hit count *(interpretation of the review's phrasing)*.
- Aiming is presumably the [Island War](island-war.md) sweep-arrow (two-press lock-then-power), the series' verified aiming grammar *(inferred)*.
- Whether the gorilla moves/dodges — which would justify the Accuracy tag — is unverified *(inferred: probably ambles about)*.

## Verification targets for a video pass

The aiming mechanic, gorilla movement pattern, zone values vs. coverage scoring, ammo/cooldown, his reaction animations (the comedy payload).

## Recreation sketch (phone-buzzer fit: excellent)

- Reuses the shared `sweepAim` helper (see [Island War](island-war.md)) with the gorilla ambling on a slow patrol; splats persist on him as coloured blotches in each player's colour — the scoreboard is literally worn by the target.
- Zone scoring: belly 50, chest 100, face 300 (he blocks his face more often as the round progresses — difficulty ramp with personality).
- His mood escalates through the round: `calm` → `stir` → `awake` rig moods as he gets increasingly painted; final scoreboard shows him fully speckled.
- Parameter sketch: 45 s; throw cycle ~2.5 s; face-block windows grow from 20 % to 60 % duty cycle.

Back to the [catalog](minigames.md).
