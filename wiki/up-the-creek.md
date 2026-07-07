# Up The Creek

**Category: Accuracy** · **Controls: Buzz! button** · Longplay chapter 1:41:55 ([watch](https://www.youtube.com/watch?v=dZEJTdSRqrY&t=6115s)). Not yet recreated; rules *(inferred)*.

River-float coconut warfare *(inferred)*: the moving-water entry in the coconut-artillery family ([Island War](island-war.md), [Lethal Lily Pads](lethal-lily-pads.md), [Bridge Out](bridge-out.md)).

## What the sources say

- [2009 Wikipedia list](sources/wikipedia.md) for the name; German Wikipedia for the **Accuracy** category.
- The river diorama is listed among the game's settings in [presentation](presentation.md) ("hot-tub clearing, four-lane running track, night-time campfire, **river**, treetops, small islands, savannah") — this game is the likely river tenant.
- No manual rules, review description, or trailer sighting.

## Rules *(inferred)*

- Monkeys float downstream (rafts, logs, or inner tubes) while lobbing coconuts at each other — the drifting platforms are what would make this the *hard* aiming game, justifying a separate catalog slot from Island War's static islands.
- Sweep-arrow aiming assumed (the verified series grammar); moving shooter + moving target = lead-the-shot gameplay.
- Hits presumably dunk or stun; score by hits landed over the float *(inferred)*.

## Verification targets for a video pass

Whether players drift on a shared current or steer, the aiming mechanic under motion, hit effects, obstacles in the river (rocks, branches), round length vs. river length.

## Recreation sketch (phone-buzzer fit: good)

- Side-scrolling river with all four monkeys drifting at slightly different speeds; the shared `sweepAim` helper fires across lanes; leading a bobbing target is the skill.
- Scenery writes itself from our existing vocabulary (water shimmer from Bubble Bath, palms, ferns) plus a scrolling bank.
- Parameter sketch: 50 s float; +100 per hit (1 s dunk for the victim); bob amplitude grows in "rapids" segments mid-round for a difficulty wave; drift shuffle each 10 s so no one camps a firing angle.

Back to the [catalog](minigames.md).
