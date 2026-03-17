# DROP ZONE EXPRESS

## The Problem This Solves

You've got 200 kids in line and two dads running the booth. Every second between players is a kid shifting weight, a parent checking their phone, a line that isn't moving. The game needs to eat players like a machine — fun in, memories out, NEXT.

**This concept is designed operations-first.** The game is rad, but more importantly: it sets up in 8 minutes, turns over players in 10 seconds, and tears down in 6.

## The Pitch

*"Step up! Grab the handle! DROP — BOUNCE — SCORE — NEXT!"*

No rules explanation. No complicated setup between turns. You walk up, you see what to do, you do it, you scream, you leave grinning. The line never stops.

## Concept

A 4ft × 5ft tilted plinko board with a **conveyor-style player rotation system**. Three drop slots across the top. One pull handle per slot. Yank the handle, ball drops, chaos ensues, ball lands in a scoring bucket, score lights up on a big LED number board overhead. **Total interaction time per player: 12–15 seconds.**

But here's the trick: **three kids play simultaneously.** Each kid gets ONE drop slot (left, center, right). They step up together, drop together (on a countdown), watch their balls bounce, see their scores, and cycle out while the next three step up. The line moves in threes.

## Gameplay

### The Flow (Per Wave)

1. **LOAD** (3 sec) — Three kids step to their stations. Ball is already sitting in the drop slot from the auto-reload
2. **COUNTDOWN** (3 sec) — LED board flashes 3... 2... 1... DROP! (with crowd-hyping sound effects)
3. **CHAOS** (5 sec) — All three balls cascade through the peg field simultaneously. Balls bounce off each other. Crowd goes wild
4. **SCORE** (2 sec) — Balls land in scoring buckets. Three scores flash on the overhead LED board
5. **CYCLE** (2 sec) — Kids step aside, next three step up. Balls auto-return to drop slots via gravity chute

**Total wave time: ~15 seconds**
**Throughput: 12 kids per minute. 720 kids per hour.**

That line is MOVING.

### Drop Mechanics

Each drop slot has a **pull-and-release handle** — a spring-loaded gate that holds the ball. Kid yanks the handle down, gate opens, ball drops. Satisfying mechanical CLUNK. The handle resets automatically.

No pinball plungers. No stomp pads. No aiming. The beauty is the SIMPLICITY. Pull handle. Ball drops. Plinko does the rest.

### The Peg Field

- Classic offset peg grid: 8 columns × 10 rows
- 3D-printed mushroom-cap pegs in alternating neon green and hot pink
- Pegs mounted through the plywood back, secured with a washer and nut from behind
- **Ball interaction zones**: Where three balls can collide mid-field for extra chaos
- A few **SPINNER PEGS** — 3D-printed helicopter rotors on a bearing that spin when hit, deflecting balls unpredictably. Three spinners placed at choke points in the mid-field

### Scoring Buckets (Bottom)

| Zone | Points | Width | Color |
|------|--------|-------|-------|
| JACKPOT | 1000 | 2.5" | Gold, lit LED strip |
| HIGH × 2 | 500 | 3" | Red |
| MID × 2 | 200 | 4" | Blue |
| LOW × 2 | 100 | 5" | Green |
| GUTTER × 2 | 0 | Edge gaps | Black |

Nine buckets total across the 48" width. The JACKPOT is dead center and barely wider than the ball. When a ball hits it — **AIRHORN. LED FLASH. The crowd knows.**

### Score Display

Overhead LED number board (battery-powered, Arduino + 7-segment displays). Three scores displayed side by side. Resets automatically after each wave. **The operator doesn't touch anything.**

Optional: a running "HIGH SCORE OF THE DAY" display. Kids will talk about beating the high score all week.

## What Makes It Special

1. **THREE SIMULTANEOUS PLAYERS** — The line moves 3× faster than any single-player game. This is the #1 feature
2. **ZERO EXPLANATION NEEDED** — Pull the handle. That's it. A 5-year-old figures it out by watching the kid before them. Kindergarteners to 5th graders, no onboarding
3. **BALL COLLISIONS** — Three balls in the peg field at once means they smash into each other mid-cascade. Unpredictable. A kid's ball can knock another kid's ball into the jackpot. Instant drama. Instant stories
4. **SELF-RESETTING** — Gravity-fed ball return. Balls land in buckets, roll through rear chute, drop back into the three top slots. The operator's only job is vibes and crowd control
5. **SPINNER PEGS** — The rotating pegs add a skill-vs-luck wildcard. Does the spinner deflect your ball to glory or gutter? Nobody knows until it hits
6. **THE COUNTDOWN** — "3... 2... 1... DROP!" creates a shared moment. The crowd counts along. Every wave is a mini-event
7. **SCOREBOARD DRAMA** — Public scores visible to the whole line. Kids cheer. Kids groan. Rivalries form between strangers in 15 seconds

## Line Management Design

The game's physical layout is designed to manage the line:

- **Queue rails** (rope + stanchion or PVC pipe rails) feed directly to the three stations
- **"ON DECK" marks** on the ground — next three kids stand on painted footprints so they're ready to step up instantly
- **EXIT LANE** — one-way path to the right so exiting players don't collide with the line
- **SPECTATOR ZONE** — the acrylic front panel faces outward toward the line, so everyone waiting can see the ball chaos. The line IS the audience

## Operator Role

One person. That's it. Their job:

1. Vibe. Hype the countdown. "WHO'S READY?! THREE... TWO... ONE..."
2. Make sure the next three kids step up (the ON DECK marks handle this)
3. Handle any ball jams (rare — gravity does the work, but have a dowel poker handy)
4. Swap batteries on the scoreboard once mid-event (if running 4+ hours)

**The second dad?** He's free to run the prize table, take photos, or just enjoy the carnival. This game runs itself.

## Vibe

Think: **airport baggage claim meets The Price Is Right**. Efficient, relentless, hypnotic. The mechanical rhythm of load-countdown-drop-score-cycle becomes a heartbeat. Kids in line unconsciously sync to it. The energy builds. Every wave gets louder.

It's not the most complex game. It's not the most physical. But it's the one that processes the most kids, creates the most shared moments, and never stops moving. On carnival day, when the line stretches past the face painting booth — this is the game that handles it.
