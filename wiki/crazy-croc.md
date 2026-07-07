# Crazy Croc

**Category: Speed** · **Controls: Buzz! button** · Longplay chapter 0:19:45 ([watch](https://www.youtube.com/watch?v=dZEJTdSRqrY&t=1185s)). Not yet recreated; core rule reported by a review.

Push-your-luck with a crocodile: put your head inside its jaws, stay as long as you dare for points, and pull out before the snap. The crocodile sibling of [Lion Taming](lion-taming.md) — the game clearly liked this design enough to build it twice (IGN's noted risk/reward thread).

## What the sources say

- [NoobFeed](sources/reviews.md) describes Crazy Croc: head inside a crocodile's jaws, stay long for points, pull out before the snap.
- The crocodile is listed among the NPC supporting cast in [monkeys](monkeys.md).
- German Wikipedia category: **Speed** (reaction to the snap tell, presumably).

## Rules (reported / *(inferred)* where noted)

- Hold (or stay in — the exact input is unverified: hold-to-stay like [Bubble Bath](bubble-bath.md), or press-to-withdraw) while your monkey's head is in the croc's mouth; points accrue over time.
- The croc telegraphs, then snaps; monkeys still inside get chomped — cost unverified: streak loss, point deduction, or time-out *(inferred: streak loss, by analogy with Bubble Bath's verified rule)*.
- Whether all four monkeys share one croc or have one each is unverified *(a croc each is more likely given lanes in similar games)*.

## Verification targets for a video pass

Input verb (hold vs. press-out), shared vs. per-player croc, snap tell duration, penalty, score rate, round length.

## Recreation sketch (phone-buzzer fit: excellent)

- Identical control shape to our shipped Bubble Bath module (hold RED, watch the tell, release) — a re-skin with different pacing: croc tells should be **shorter and sharper** than the gorilla's ~1.2 s stir to differentiate the two.
- Parameter sketch: 45 s round, ~8–20 s between snaps, 0.6–0.9 s tell, streak-only loss + 2 s recovery, score ramp 20→80 pts/s.
- New croc SVG needed (jaw hinge = one rotating group); monkey uses `hold`/`bonked` poses.

Back to the [catalog](minigames.md).
