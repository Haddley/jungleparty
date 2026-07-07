# Keep It Up

**Category: Skill** · **Controls: Buzz! button** · Longplay chapter 0:52:24 ([watch](https://www.youtube.com/watch?v=dZEJTdSRqrY&t=3144s)). Not yet recreated; one of only five games with **official manual rules**.

Keepy-uppy with a risk twist: Buzz! throws the ball up, Buzz! again keeps it airborne — and **the longer you wait to hit it, the more points you score**. Miss, and Buzz! relaunches. A pure distillation of the game's push-your-luck design thread into a single button.

## What the sources say

- The [US manual](sources/us-instruction-manual.md) documents the full rules (one of its five official rule sets): throw up, timed hits keep it up, later hits score more, relaunch on miss.
- German Wikipedia category: **Skill**.

## Rules (manual-verified core, details *(inferred)*)

- First Buzz! launches your ball; subsequent presses must connect as the ball falls.
- Points per hit scale with how late (low) you let the ball drop before hitting — brushing the ground is maximum value, mistiming means a miss.
- A miss costs time only (relaunch); whether it also breaks a multiplier is unverified *(inferred: probably not — the manual mentions no combo)*.
- Presumably simultaneous play in four lanes for a fixed round; highest total wins *(structure inferred)*.

## Verification targets for a video pass

Ball fall speed and rhythm, the scoring curve vs. hit height, miss recovery time, round length, any ball-type variations.

## Recreation sketch (phone-buzzer fit: excellent)

- One-button timing with a *visible* risk dial — the ball's height IS the UI, which reads perfectly on a TV at a distance.
- Host simulates each ball ballistically in `tick`; a press connects if the ball is below a strike ceiling; score = f(height): e.g. 10 pts at apex-adjacent, 100 pts in the last 15 % before ground.
- Latency mitigation: judge presses against host ball position at receive time minus half RTT (same approach as Simian Shootout's reaction times).
- Parameter sketch: 45 s; bounce cycle ~1.8 s; miss = 1.2 s fumble + relaunch; ball trail turns gold in the high-value band so the gamble is legible.

Back to the [catalog](minigames.md).
