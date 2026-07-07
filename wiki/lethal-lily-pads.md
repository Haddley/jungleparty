# Lethal Lily Pads

**Category: Accuracy** · **Controls: Buzz! button** · Longplay chapter 0:54:32 ([watch](https://www.youtube.com/watch?v=dZEJTdSRqrY&t=3272s)). Not yet recreated; described by a launch review and clearly sighted in the trailer.

Coconut artillery on a pond: knock the other monkeys off their lily pads. The best-documented of the throwing games after [Island War](island-war.md), thanks to a two-second trailer shot that pins down the staging.

## What the sources say

- [Kikizo](sources/reviews.md) describes knocking opponents off lily pads with coconuts.
- The [launch trailer](sources/launch-trailer.md) (0:22–0:25) shows the game **top-down**: a pond with three small islands and lily pads, **each monkey with a coloured aiming arrow**, and a leaf-shaped timer dial at the bottom — directly confirming per-player sweep arrows (the [Island War](island-war.md) mechanic) and the leaf timer from [Bubble Bath](bubble-bath.md)'s HUD.
- German Wikipedia category: **Accuracy**.

## Rules (reported + trailer-observed, details *(inferred)*)

- Each monkey floats on a lily pad; coloured sweep arrows aim coconut throws (two-press lock-then-power cycle assumed from Island War *(inferred but strongly implied by the arrows)*).
- A hit knocks the target off (into the water) — respawn vs. elimination unverified; the "lethal" name and Accuracy category suggest knock-offs score points and victims respawn after a dunk *(inferred)*.
- Timer dial visible in the trailer → fixed-length round, not last-monkey-standing.

## Verification targets for a video pass

Hit → knock-off behaviour (respawn time, point value), whether pads drift, whether you can dodge (move pads), island props' role.

## Recreation sketch (phone-buzzer fit: excellent)

- Top-down staging is a refreshing camera change for our TV stage, and the shared `sweepAim` helper (see [Island War](island-war.md)) covers the input.
- Water dunk reuses splash particles from Bubble Bath; dunked monkey plays `flat`-then-respawn.
- Parameter sketch: 45 s; +150 per knock-off; victim respawns after 2.5 s (invulnerable 1 s); throw cycle ~3 s; leaf timer dial on the TV as a nod to the original HUD.

Back to the [catalog](minigames.md).
