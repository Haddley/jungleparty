# The monkeys

The four player characters. Sources: [Wikipedia](sources/wikipedia.md), [IGN / Rory's / Common Sense Media reviews](sources/reviews.md), [manual](sources/us-instruction-manual.md).

- Named after and coloured exactly as the controller's colour buttons: **Blue, Orange, Green, Yellow** ("imaginatively named… surprisingly coloured orange, blue, yellow and green" — Rory's). Player identity = button colour = monkey colour; the [announcer](presentation.md#announcer) addresses players by colour name ("Keep at it, Blue!", "Blue, we will mourn you").
- In Standard multiplayer you pick your monkey by **seated position**; in Quick Start by pressing your colour button.
- **Costumes**: an editor with separate head / body / legs items (blue/orange select slot, green/yellow scroll, Buzz! accepts); more items unlock through play, including Bronze, Silver and Gold outfits for high scores.

## Animation character

Reviewers repeatedly single out the animation: the monkeys are "adorably animated" with **seamless transitions** — a monkey clapping in approval blends back into the same idle a just-zapped monkey returns to (IGN). They screech frantically, celebrate, mourn, and absorb endless slapstick: bonked on the head, flattened by anvils, zapped by electricity, blown up by bombs, always intact next round (the E10+ "mild cartoon violence").

State list observed/reported (recreation rig targets): **idle, run, celebrate, mourn, bonked, flattened, zapped**, plus per-game actions (blow bubbles, throw, whack).

## Supporting cast (NPCs)

- The **gorilla** — jungle host and manual narrator; dozes in the [Bubble Bath](bubble-bath.md) hot tub; paintball target in Splat.
- Lion (Lion Taming), crocodile (Crazy Croc), ostrich (Ostrich Eggs), hippos in outfits — one in a coconut bikini, one in a cowboy hat (Hippo Splash), elephant pitcher (Elephant Baseball), squirrels ([Whack A Squirrel](whack-a-squirrel.md)), turtles (Turtle Shoot).

## In the recreation

One original SVG monkey rig, recoloured four ways; CSS/JS animation states matching the list above. No art from the original game is copied — the rig is our own cartoon monkey informed by written descriptions. See [recreation-notes](recreation-notes.md).

Rig v2 (2026-07-06): gradient-shaded fur from shared SVG `<defs>` (injected once at boot; per-frame SVG string rebuilds reference stable gradient IDs), hands/feet with palms and toes, expressive brow states, drifting pupils, breathing, deterministic blink and ear-twitch cycles keyed off the game clock. Pose set grew to eleven: **idle, cheer, mourn, bonked, run, hold, blow, zap, flat, throw, whack** — covering the observed states plus the per-game actions (blow bubbles for [Bubble Bath](bubble-bath.md), throw for [Monkey Bomb](monkey-bomb.md), mallet raise for [Whack A Squirrel](whack-a-squirrel.md)). Slapstick reads bigger: the zap pose flickers a cartoon skeleton, bonked grows a head lump under orbiting stars, mourn sheds animated tears — matching the "endless slapstick, always intact next round" character noted above.
