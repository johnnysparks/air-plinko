# Mega Drop Live

## The Pitch

A plinko board where the screen IS the game board. A camera tracks your ball in real-time while the monitor overlays numbered target zones onto the playing field. Hit targets in sequence — 1, 2, 3 — and your combo multiplier climbs. Miss the order and you're back to 1×. Every single bounce matters. The crowd watches the combo chain build on the big screen and loses their minds on a 5× streak.

The physical build is dead simple (wood + pegs + gravity). The software turns every random plinko bounce into a skill-based combo puzzle. Every kid leans in, holds their breath, and screams when the chain hits.

## How It Works

### The Setup

A 4×5 ft tilted plinko board. Clear acrylic front. Colored balls (red vs blue). Standard peg grid. Seven scoring zones at the bottom. Nothing mechanically fancy — this is a gravity game.

Next to the board: a 32"+ TV monitor on a stand, angled so the crowd can watch. Powered speakers flanking the monitor. A Raspberry Pi 4 tucked behind the board running OpenCV + a web-based display.

One camera:
- **Board Cam** — USB webcam mounted above or beside the board, watching the playing field through the acrylic. Tracks colored ball positions using HSV color detection. This is the only camera needed — all gameplay runs through ball tracking.

### The Combo Catcher System

Before each drop, the screen overlays **5 numbered target zones** across the peg field. These are circular regions scattered from top to bottom of the board, numbered 1 through 5. The ball must pass through them **in order** to build a combo chain.

```
Drop slots:   [ 1 ] [ 2 ] [ 3 ] [ 4 ] [ 5 ]
              ·  ·  ·  ·  ·  ·  ·  ·  ·  ·
           ①   ·  ·  ·  ·  ·  ·  ·  ·  ·
              ·  ·  ·  ·  ·  ·  ·  ·  ·  ·
                 ·  ·  · ②·  ·  ·  ·  ·
              ·  ·  ·  ·  ·  ·  ·  ·  ·  ·
           ·  ·  ·  ·  ·  ·  ·  ③  ·  ·
              ·  ·  ·  ·  ·  ·  ·  ·  ·  ·
                 · ④·  ·  ·  ·  ·  ·  ·
              ·  ·  ·  ·  ·  ·  ·  ·  ·  ·
              |10 |25 |50 |⑤00|50 |25 |10 |
```

- **Hit zone 1 first?** It lights up green on screen. Zone 2 starts pulsing — "this one's next."
- **Hit zone 2 after 1?** Chain continues. Combo counter shows 2×. Zone 3 pulses.
- **Hit zone 3 out of order (before 2)?** Nothing happens — zone 3 stays dark. You need 2 first.
- **Complete the full 1→2→3→4→5 chain?** 5× multiplier on your landing zone score. Screen explodes.

The target layout **randomizes every drop**. Sometimes the chain flows naturally left-to-right down the board. Sometimes it zigzags. Sometimes zone 1 is on the far right and zone 2 is on the far left — good luck threading that needle. The player reads the pattern, chooses a drop slot, and prays to the peg gods.

### Gameplay Flow

1. **ATTRACT MODE** — Between rounds, the monitor shows a flashy attract screen: "STEP UP TO MEGA DROP LIVE!", highlight reel of the day's best combo chains, current leaderboard. Speakers pump arcade music. The attract screen shows a demo drop with the combo system so kids in line already understand it.

2. **PLAYER UP** — Player steps to the board. Monitor switches to the augmented board view: the live camera feed of the peg field with the 5 target zones overlaid. The player can see exactly where zones 1 through 5 are placed before they drop.

3. **READ THE BOARD** — 5-second countdown while the player studies the target layout. Which drop slot gives the best chance of threading zones 1→2→3→4→5? This is the strategy moment. The screen shows faint path predictions — ghost lines showing roughly where a ball dropped from each slot tends to travel. Not exact (plinko is chaos), but directional hints.

4. **THE DROP** — Player drops the ball. Board cam tracks it in real-time. Monitor shows the augmented view:
   - Ball gets a glowing trail effect (fire for red, ice for blue)
   - When the ball enters a target zone in the correct sequence: **BOOM** — the zone explodes with light, combo counter ticks up, crowd roar sound, zone turns solid green
   - When the ball passes near a zone but misses: the zone flickers and the announcer winces — "OHHH, just missed zone 3!"
   - When the ball enters a zone out of order: zone flashes red briefly, buzzer sound — crowd groans
   - Music intensifies with each combo link: quiet at 0×, building at 2×, absolutely pumping at 4×
   - AI announcer calls the chain: "ZONE ONE — GOT IT! ZONE TWO — YES! HEADING FOR THREE... COME ON... COME ONNNN..."

5. **SCORE** — Ball lands in a scoring zone. Base points × combo multiplier = final score.
   - 0 combos: 1× (base score only — you just played regular plinko)
   - 1 combo (hit zone 1): 1.5×
   - 2 combo chain (1→2): 2×
   - 3 combo chain (1→2→3): 3×
   - 4 combo chain (1→2→3→4): 4×
   - **PERFECT CHAIN (1→2→3→4→5): 5× + bonus 200 points**
   - Screen shows the multiplier math: "50 × 3 = 150!" with escalating celebration effects
   - Perfect chain triggers: screen-wide gold explosion, victory fanfare, confetti, slow-motion replay, announcer loses their mind

6. **REPLAY** — Monitor auto-plays a 3-second slow-motion replay of the drop. The combo zones light up again in sequence as the ball passes through. This is the money shot — the crowd watches the chain build a second time.

7. **NEXT UP** — Score posts to the daily leaderboard. Target zones randomize for the next player. Repeat.

### Difficulty Modes

The target zone layout algorithm has three difficulty settings (controlled by a volunteer or auto-scaled by age/height detection):

- **Easy (K-2nd):** 3 target zones instead of 5. Zones are large (generous hitboxes). Zones flow in a natural top-to-bottom, left-to-right path. A lucky drop can hit all 3.
- **Medium (3rd-4th):** 4 target zones. Standard hitbox size. Some zigzag in the layout. Requires a smart drop position choice.
- **Hard (5th+ and adults):** 5 target zones. Smaller hitboxes. Aggressive zigzag layouts. A perfect chain is rare and genuinely impressive.

### Two-Player Mode

Red vs Blue, simultaneous drops. Both players see the SAME target layout — same zones, same sequence. Board cam tracks both colors independently. Who builds the longer chain? The announcer narrates the race: "RED HITS ZONE 2 — BLUE STILL STUCK ON ONE! OH WAIT, BLUE JUST NAILED TWO AND THREE BACK TO BACK!"

Split-score display shows both combo chains building side by side. The crowd picks sides.

### The Tech Stack

- **Raspberry Pi 4** (4GB+) — Runs everything
- **OpenCV** — Ball tracking via HSV color segmentation on the board cam feed
- **Web browser (Chromium kiosk)** — Full-screen display app with Canvas/WebGL effects
- **Python backend** — WebSocket bridge between CV pipeline and the browser display
- **Web Audio API** — Sound effects, announcer clips, dynamic music

### Why This Works at a Carnival

- **Physical build is trivial** — It's just a plinko board. Two dads, one weekend.
- **Tech setup is one-time** — Flash an SD card, plug in one USB webcam, HDMI to the monitor. Done.
- **Zero moving parts to break** — No servos, no air, no flippers. Gravity and software.
- **Volunteers just refill balls** — The game runs itself. No explanation needed.
- **The monitor IS the game** — Without the screen, it's just plinko. With the screen, every bounce is a cliffhanger. Kids not playing stand around watching the combo chains build like it's March Madness.
- **Scales to any skill level** — Easy mode for little kids (3 big zones, hard to miss). Hard mode for 5th graders who want to grind for a perfect chain. Both are screaming by the end.
- **Skill actually matters** — Reading the target layout and choosing the right drop slot is a real decision. Kids who study the board outperform kids who drop blind. But plinko chaos means upsets happen — the best-laid plans still bounce wrong sometimes.
- **Replay value is high** — Every drop has a different target layout. You can't memorize the board. Kids come back all day trying to hit a perfect chain.

## Modes

- **Solo** — Beat the leaderboard. Chase the perfect chain.
- **Versus** — Red vs Blue. Same target layout, race for the longer chain.
- **Co-op** — Same color. Player 1 drops, trying for zones 1-3. Player 2 drops a second ball, trying for zones 3-5. Combined chain = combined score.
- **Tournament** — Bracket mode across the carnival day. Finals announced on the big screen.
- **Frenzy Round** — Every 30 minutes, a special round where the target zones MOVE slowly across the board during the drop. The announcer hypes it: "IT'S FRENZY TIME!" Crowd gathers.

## Vibe

Think: Japanese arcade game meets ESPN broadcast meets school carnival. The screen isn't showing you a replay of what happened — it's showing you a game that's happening RIGHT NOW on the board. Every bounce either builds the chain or breaks it. The crowd reads the screen, holds their breath, and erupts. The physical game is humble. The digital layer turns it into a combo-chasing skill game that happens to use gravity as its physics engine.
