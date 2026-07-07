# Island War

**Category: Accuracy** · **Controls: Buzz! button ×2 (lock, then throw)** · Longplay chapter 0:48:29 ([watch](https://www.youtube.com/watch?v=dZEJTdSRqrY&t=2909s)). Not yet recreated; one of only five games with **official manual rules**.

Coconut artillery between islands, and the definitive statement of the series' **sweep-aim mechanic**: a red arrow sweeps left–right in front of your monkey; the first Buzz! press locks the direction (the arrow then grows in length), the second press throws — the arrow's length at release sets the distance. Every other throwing game in the catalog is assumed to derive from this verified core.

## What the sources say

- The [US manual](sources/us-instruction-manual.md) documents the full mechanic (one of its five official rule sets): "hurl coconuts at anything that moves", lock direction, arrow grows, second press sets distance.
- German Wikipedia category: **Accuracy**. The catalog controls column reads "Buzz! ×2".

## Rules (manual-verified core, targets *(inferred)*)

- Two-press throw cycle: press 1 stops the sweeping arrow (direction), the arrow starts growing; press 2 releases at the current length (power/distance).
- "Anything that moves" implies targets beyond rival monkeys — critters or drifting objects *(specifics unverified)*.
- Scoring per hit and round structure are unverified; islands suggest each monkey has home ground and lobs across water.

## Verification targets for a video pass

Sweep speed and growth rate, what the targets are and their values, splash/miss feedback, friendly-fire rules, round length.

## Recreation sketch (phone-buzzer fit: excellent — the template for all aiming games)

- The two-press cycle is ideal for phones: it's discrete (latency-tolerant) yet skillful. Implement once as a shared `sweepAim` helper and reuse for [Balloon Battle](balloon-battle.md), [Bridge Out](bridge-out.md), [Lethal Lily Pads](lethal-lily-pads.md), [Splat](splat.md), [Up The Creek](up-the-creek.md).
- Host animates the arrow in `tick`; phone RED does lock/throw alternately; phone prompt mirrors the state ("Stop the arrow!" → "Set the power!").
- Parameter sketch: sweep 1.2 s per arc, growth 0–100 % over 1.5 s, coconut flight with arc + splash, +100 monkey hit (1 s `bonked` stun), +50 moving critter, 45 s round.

Back to the [catalog](minigames.md).
