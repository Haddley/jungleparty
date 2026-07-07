# Freefall

**Category: Luck & tactics** · **Controls: colour buttons** · Longplay chapter 0:33:44 ([watch](https://www.youtube.com/watch?v=dZEJTdSRqrY&t=2024s)). Not yet recreated; unusually well documented for a non-starter game.

Skydiving hot-potato with an anvil: the monkeys fall together, one holds an anvil that earns points, and passing it works like [Monkey Bomb](monkey-bomb.md) — but the deadline is the **ground**, not a fuse. Whoever holds the anvil at landing gets flattened.

## What the sources say

- [IGN](sources/reviews.md) cites Freefall (alongside [Lion Taming](lion-taming.md)) as an example of the game's risk/reward design thread.
- [Catalog](minigames.md): "Skydiving hot-potato with an anvil: holding scores, pass it by pressing a monkey's colour; holder at the ground gets flattened" (assembled from review fragments; not marked inferred).
- German Wikipedia category: **Luck & tactics** — same as Monkey Bomb, confirming the shared design family.

## Rules (reported / *(inferred)* where noted)

- All four monkeys freefall; the anvil holder accrues points over time.
- Press another monkey's colour button to throw them the anvil (identical pass grammar to Monkey Bomb's verified rules).
- The visible, shared deadline (approaching ground) replaces Monkey Bomb's hidden fuse — this flips the tactics: everyone can see how much time is left, so late-game passes become frantic *(dynamic inferred, deadline visibility confirmed by the premise)*.
- Landing holder is flattened (the rig's `flat` state); penalty size unverified *(Monkey Bomb's −100 + round points is the likely template)*.

## Verification targets for a video pass

Fall duration, pass flight time (can you be "passed to" too late to re-pass?), landing penalty, whether multiple drops occur per game, scoring rate while holding.

## Recreation sketch (phone-buzzer fit: excellent)

- Direct variant of our shipped Monkey Bomb module: swap the fuse timer for a visible altitude meter, background scrolls upward (clouds, birds), landing = `flat` pose + dust.
- The visible deadline is the design twist worth preserving: show altitude on both TV and phone prompt ("1200 m…").
- Parameter sketch: 5 drops of ~15 s; ~50 pts/s held; flight 0.6 s; landing −100 and lose round points; last-second passes (<1 s to ground) still legal — chaos is the point.

Back to the [catalog](minigames.md).
