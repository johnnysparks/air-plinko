# Mega Drop Live

## The Pitch

A plinko board that thinks it's a live game show broadcast. Two cameras and a big-screen monitor transform a simple peg board into an ESPN-style spectacle — real-time ball tracking, pose-activated power-ups, AI play-by-play announcer, instant replays, and a daily leaderboard. The physical build is dead simple (wood + pegs + gravity). All the magic is software running on a Raspberry Pi.

Every drop feels like being on TV. Every kid walks away saying "did you SEE that?"

## How It Works

### The Setup

A 4×5 ft tilted plinko board. Clear acrylic front. Colored balls (red vs blue). Standard peg grid. Five scoring zones at the bottom. Nothing mechanically fancy — this is a gravity game.

Next to the board: a 32"+ TV monitor on a stand, angled so the crowd can watch. Powered speakers flanking the monitor. A Raspberry Pi 4 tucked behind the board running OpenCV + a web-based display.

Two cameras:
1. **Board Cam** — USB webcam mounted above or beside the board, watching the playing field through the acrylic. Tracks colored ball positions using HSV color detection.
2. **Player Cam** — Second webcam on top of the monitor, facing the players. Detects body poses using MediaPipe/OpenPose for power-up activation.

### Gameplay Flow

1. **ATTRACT MODE** — Between rounds, the monitor shows a flashy attract screen: "STEP UP TO MEGA DROP LIVE!", highlight reel from the day's best drops, current leaderboard. Speakers pump arcade music.

2. **PLAYER UP** — Player steps to the board and the player cam detects them. Monitor switches to split-screen: live board view on the left, player silhouette with pose guide on the right. "CHOOSE YOUR POWER-UP!"

3. **POSE TO POWER** — Player strikes a pose detected by CV:
   - **Flexing arms** → **HEAVY BALL** — 2× multiplier on bottom zones
   - **T-Pose (arms out)** → **SCATTER SHOT** — Drop 3 balls at once
   - **Hands on head (crown pose)** → **CROWN ZONE** — Random zone becomes worth 200 pts for this drop
   - **No pose / timer expires** → **CLASSIC MODE** — Standard scoring, no modifiers

4. **THE DROP** — Player drops the ball. Board cam tracks it in real-time. Monitor shows the augmented view:
   - Ball gets a glowing trail effect (fire for red, ice for blue)
   - Pegs flash on the display when hit
   - Music intensifies as ball approaches high-value zones
   - AI announcer calls the action: "LEFT SIDE... BOUNCING RIGHT... HEADING FOR THE HUNDRED... OH! DEFLECTED!"

5. **SCORE** — Ball lands in a zone. Monitor explodes with effects. Speakers blast a crowd roar (big zone) or a sympathetic "awww" (gutter). Score tallies with slot-machine animation. If it's a new high score: strobe effects, victory fanfare, confetti animation.

6. **REPLAY** — Monitor auto-plays a 3-second slow-motion replay of the drop, ball trail and all. Crowd goes nuts.

7. **NEXT UP** — Score posts to the daily leaderboard. Next player steps up. Repeat.

### Two-Player Mode

Red vs Blue, simultaneous drops. Board cam tracks both colors independently. Monitor shows split-score display. The announcer plays favorites based on who's winning. "RED IS ON FIRE! BLUE, YOU GONNA TAKE THAT?"

### The Tech Stack

- **Raspberry Pi 4** (4GB+) — Runs everything
- **OpenCV** — Ball tracking via HSV color segmentation on the board cam feed
- **MediaPipe Pose** — Skeleton detection on the player cam for power-up poses
- **Web browser (Chromium kiosk)** — Full-screen display app with Canvas/WebGL effects
- **Python backend** — WebSocket bridge between CV pipeline and the browser display
- **Web Audio API** — Sound effects, announcer clips, dynamic music

### Why This Works at a Carnival

- **Physical build is trivial** — It's just a plinko board. Two dads, one weekend.
- **Tech setup is one-time** — Flash an SD card, plug in two USB webcams, HDMI to the monitor. Done.
- **Zero moving parts to break** — No servos, no air, no flippers. Gravity and software.
- **Volunteers just refill balls** — The game runs itself. No explanation needed.
- **The monitor IS the spectacle** — Kids who aren't playing stand around watching the screen like it's a Jumbotron. Builds a crowd. Crowds build lines. Lines build hype.
- **Scales to any skill level** — A 5-year-old drops a ball and gets an epic show. A 10-year-old strategizes power-ups. Both have the time of their lives.

## Modes

- **Solo** — Beat the leaderboard. Personal best chase.
- **Versus** — Red vs Blue. Head-to-head with announcer trash talk.
- **Co-op** — Same color. Combined score targets ("Can you beat 500 together?")
- **Tournament** — Bracket mode across the carnival day. Finals announced on the big screen.

## Vibe

Think: Japanese arcade game meets ESPN broadcast meets school carnival. Bright colors, loud sounds, over-the-top reactions. The physical game is humble. The digital layer makes it legendary.
