# The Buzz! controller

The wired quiz-show-style handset shipped with the Buzz! series and used by every Buzz! Junior game. Sources: [US manual](sources/us-instruction-manual.md#hardware-and-controls), [Buzz! series Wikipedia](sources/wikipedia.md), [SMH and Wilcox reviews](sources/reviews.md).

## Layout

- **Top: one large round red "Buzz!" button** — the dome buzzer ("a red Temptation-style buzzer on top", SMH). Confirm/act/mash button.
- **Below it, a vertical column of four smaller rounded-rectangular colour buttons, top to bottom: Blue, Orange, Green, Yellow.** Order corroborated by Wilcox's two-thumb technique (left thumb covers the upper pair blue+orange, right thumb the lower pair green+yellow).
- Four handsets, their cables merging into a **single USB plug**; PS2/PS3 USB port. A later wireless variant uses a USB dongle.

## Menu conventions

Established by the manual and consistent game-wide:

- **Blue / orange scroll** lists (languages, letters, mini-games, leaderboards); **Buzz! confirms**.
- Menu options are colour-coded so each of four choices maps to one colour button (e.g. main menu, session length).
- Costume editor: blue/orange pick the body slot, green/yellow scroll items, Buzz! accepts.
- Pause: hold all four colours together.

## Player identity

Button colours are the player identities: the four [monkeys](monkeys.md) are literally named Blue, Orange, Green and Yellow. Pressing "the green button" always means acting on/as the green monkey (see [Monkey Bomb](monkey-bomb.md)).

## In the recreation: the phone as buzzer

The phone controller screen is a full-screen original rendering of this layout — big red dome (~top 40%), then the blue/orange/green/yellow stack — tinted with the player's monkey colour, with a one-line prompt area for per-game instructions ("HOLD to blow bubbles!"). Buttons depress visually, glow, and fire `navigator.vibrate` on press; per-mini-game config enables only the buttons that game uses. Menu conventions carry over (blue/orange scroll, red confirms). See [recreation-notes](recreation-notes.md).
