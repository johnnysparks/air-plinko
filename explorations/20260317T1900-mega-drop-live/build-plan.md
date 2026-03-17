# Mega Drop Live — Build Plan

## Concept

A standard gravity plinko board augmented with computer vision and a combo-chasing scoring system. A single camera (board cam) feeds a Raspberry Pi running OpenCV. A large monitor overlays numbered target zones onto the live board view — hit them in sequence (1→2→3→4→5) to build combo multipliers. The physical build is intentionally simple — all complexity lives in software. No player cam needed; all gameplay runs through ball tracking.

## Overall Dimensions

| Dimension | Size | Notes |
|-----------|------|-------|
| Board width | 48" (4 ft) | Two-player side-by-side |
| Board height | 60" (5 ft) | Playable standing for kids & adults |
| Board depth | 4" | Ball clearance only (no air system) |
| Tilt angle | ~15° from vertical | Standard plinko tilt |
| Monitor | 32–43" TV | Mounted on stand beside the board |
| Total footprint | ~8 ft wide × 3 ft deep | Board + monitor + speaker stands |

---

## Architecture

### 1. Plinko Board (Physical)

The board is a simplified version of the Air Plinko base design — no air system, no flippers, no mechanical complexity.

- **Back panel:** 4×5 ft sheet of ¾" plywood, painted matte black (ideal for CV contrast)
- **Front panel:** 4×5 ft clear acrylic sheet (¼" thick)
- **Pegs:** ¾" wooden dowels, 3" long, drilled through acrylic into plywood. Offset grid pattern, 6" spacing. Painted white or neon for camera visibility.
- **Edge rails:** 1×4 lumber on all four sides, sandwiched between panels
- **Drop slots:** Top edge has 5 evenly spaced ball-drop notches (3" wide each), allowing players to choose their drop position
- **Scoring zones:** Bottom of board divided into 7 channels by short vertical dividers (1×2 lumber, 4" tall):

```
| 10 | 25 | 50 | 100 | 50 | 25 | 10 |
```

- **Ball catch trays:** Each scoring channel has a small tray/pocket that holds the ball visibly for 2-3 seconds (so the camera can confirm the score), then a hinged flap releases it to the return chute
- **Ball return:** Gravity chute behind the board, angled to a collection bin at the base

#### Peg Layout

Standard offset plinko grid:
- 8 rows of pegs
- Odd rows: 7 pegs (centered)
- Even rows: 6 pegs (offset by half-spacing)
- Total: 52 pegs
- All pegs painted bright white for maximum contrast against matte black background

### 2. Tilt Frame (Reusable)

- **Rear legs (×2):** 2×4 lumber, hinged at top, fold flat for transport
- **Cross brace:** Horizontal 2×4 between legs at 24" height
- **Angle chain:** Sets 15° tilt, prevents splaying
- **Rubber feet:** Prevents sliding on gym floors / concrete
- **Side handles (×2):** Heavy-duty gate handles for two-person carry
- **Wing nut joints:** Tool-free setup/teardown at all break-down points

### 3. Camera System

#### Board Cam (single camera — no player cam needed)
- **Hardware:** USB webcam, 1080p, wide-angle (120°+ FOV recommended)
- **Mount position:** Top-center of the board, clamped to the top edge rail, angled down at the playing field through the acrylic
- **Alternative mount:** Side-mount on a short gooseneck arm if top-mount creates parallax issues
- **Purpose:** Tracks colored ball positions in real-time via HSV color segmentation. Ball position is checked against combo target zones every frame.
- **Key requirement:** Must see the full playing field including all 7 scoring zones
- **Lighting note:** Board cam needs consistent lighting. A strip of USB-powered LED tape along the top inside edge (behind acrylic) provides even illumination and looks cool

#### Camera Mounting
- 3D-printed or wood bracket, clamped with a C-clamp or bolted to the edge rail
- Single USB connection to the Raspberry Pi (USB 2.0 sufficient for 30fps)

### 4. Display System

#### Monitor
- **Size:** 32–43" TV (whatever's available — thrift store find works great)
- **Mount:** TV stand or wall-mount bracket bolted to a vertical 2×4 post beside the board
- **Connection:** HDMI from Raspberry Pi
- **Orientation:** Landscape, angled slightly toward the crowd
- **Brightness:** Outdoor-rated or high-brightness preferred if the carnival is outdoors. Shade canopy recommended.

#### Speakers
- **Type:** Powered bookshelf speakers or a single Bluetooth party speaker
- **Volume:** Needs to cut through carnival noise — 20W+ minimum
- **Connection:** 3.5mm aux from Raspberry Pi or Bluetooth
- **Content:** Sound effects, announcer clips, background music, crowd reactions

#### Monitor Display Layout

The monitor shows the live board cam feed at nearly full-screen, with combo target zones overlaid directly on the playing field. The display IS the game board — not a sidebar.

```
┌─────────────────────────────────────────────┐
│  MEGA DROP LIVE        COMBO: --    HI: 750 │
│ ┌─────────────────────────────────────────┐ │
│ │ [1] [2] [3] [4] [5]   <- drop slots     │ │
│ │    ·  ·  ·  ·  ·  ·  ·  ·  ·  ·        │ │
│ │  (①)  ·  ·  ·  ·  ·  ·  ·  ·           │ │
│ │    ·  ·  ·  ·  ·  ·  ·  ·  ·  ·        │ │
│ │       ·  ·  ·(②) ·  ·  ·  ·  ·         │ │
│ │    ·  ·  ·  ·  ·  ·  ·  ·  ·  ·        │ │
│ │    ·  ·  ·  ·  ·  ·  (③) ·  ·          │ │
│ │    ·  ·  ·  ·  ·  ·  ·  ·  ·  ·        │ │
│ │       ·(④) ·  ·  ·  ·  ·  ·  ·         │ │
│ │    ·  ·  ·  ·  ·  ·  ·  ·  ·  ·        │ │
│ │    |10 |25 |50 |(⑤)00|50 |25 |10 |      │ │
│ └─────────────────────────────────────────┘ │
│                                             │
│  CHAIN: ①✓ ②✓ ③? ④  ⑤     MULTI: 2×      │
│  🔴 RED: 175              🔵 BLUE: 230     │
│         DAILY LEADERBOARD: 1. Max 750       │
└─────────────────────────────────────────────┘

① = green (hit)  ② = green (hit)  ③ = pulsing yellow (next target)
④ = dim (waiting)  ⑤ = dim (waiting)
```

**Key display states:**
- **Pre-drop:** All 5 zones visible, numbered, pulsing gently. Zone 1 pulses brightest ("start here"). Faint ghost-path lines show approximate ball trajectories from each drop slot.
- **During drop:** Active zone (next in sequence) pulses yellow. Hit zones turn solid green with a burst animation. Ball has a glowing trail. Combo counter updates live.
- **Score moment:** Final multiplier math animates: "50 × 3 = 150!" Perfect chains trigger full-screen gold explosion.
- **Replay:** 3-second slow-mo replay with zones lighting up in sequence again.

### 5. Compute System

#### Raspberry Pi 4 (4GB or 8GB)
- **OS:** Raspberry Pi OS Lite + Chromium kiosk mode
- **Software stack:**
  - Python 3 + OpenCV: Ball tracking pipeline + combo zone hit detection
  - Combo Zone Engine: Generates randomized target layouts, checks ball-in-zone collisions, manages chain state
  - WebSocket server (Python asyncio): Bridges CV data + combo state to the browser
  - Chromium in kiosk mode: Full-screen game display (HTML5 Canvas + Web Audio)
- **Mount:** Velcroed or zip-tied to the back of the board in a small ventilated enclosure
- **Power:** USB-C, 5V/3A — runs from same power strip as the monitor
- **SD Card:** 32GB+ with pre-built OS image. Entire setup is: insert SD card, plug in power + HDMI + 1× USB camera. Boot time ~30 seconds.
- **Backup:** Spare SD card with identical image in the parts bin

#### Software Architecture

```
Board Cam (USB) ──→ OpenCV HSV Tracking ──→ Ball position (x,y,color)
                                                    │
                                          Combo Zone Engine
                                          • generates target layout
                                          • ball-in-zone collision
                                          • chain state (0/5 → 5/5)
                                          • multiplier calculation
                                                    │
                                              WebSocket Server
                                              (ball pos + zone state
                                               + chain progress)
                                                    │
                                              Browser Display
                                              (Canvas + Audio)
                                                    │
                                              HDMI → Monitor
                                              3.5mm → Speakers
```

### 6. Ball System

- **Balls:** Standard 2.75" whiffle balls — 6 red, 6 blue (12 total)
- **Why whiffle balls:** Lightweight (camera tracks them well at slow plinko speed), brightly colored (easy HSV segmentation against black background), cheap to replace
- **Ball prep:** Use solid-color balls (not striped). If only striped available, spray paint them solid red/blue. Matte finish reduces glare for the camera.
- **Ball return:** Gravity chute behind the board dumps into a divided collection bin. Players grab their next ball from the bin. No automation needed.

### 7. Lighting

- **LED strip (interior):** 12V USB-powered white LED tape along the inside top edge of the board, behind the acrylic. Provides consistent illumination for the board cam and makes the pegs glow.
- **LED strip (exterior, optional):** RGB LED strip around the monitor frame. Can be synced to game events via the Pi (scoring = flash, high score = rainbow cycle). Uses a simple USB LED controller.
- **Ambient:** If outdoors, a pop-up canopy over the booth reduces sun glare on both the acrylic and the monitor.

---

## Materials List

### Board & Frame
| Item | Qty | Est. Cost |
|------|-----|-----------|
| ¾" plywood sheet (4×5 cut) | 1 | $35 |
| ¼" clear acrylic sheet (4×5 cut) | 1 | $90 |
| 1×4 lumber (edge rails, 18 lin. ft) | 3 (8ft) | $18 |
| ¾" wooden dowels (36" length) — pegs | 10 | $20 |
| 1×2 lumber (scoring dividers) | 1 (8ft) | $4 |
| 2×4 lumber (frame/legs) | 2 (8ft) | $12 |
| Matte black spray paint (back panel) | 2 cans | $10 |
| White spray paint (pegs) | 1 can | $5 |

### Hardware
| Item | Qty | Est. Cost |
|------|-----|-----------|
| Bolts, nuts, washers | — | $10 |
| Wood screws (assorted) | 1 box | $8 |
| Hinges (frame legs) | 2 | $8 |
| Chain (angle limiter) | 1 | $8 |
| Heavy-duty handles | 2 | $12 |
| Wing nuts + carriage bolts | 1 set | $15 |
| Rubber feet | 4 | $6 |

### Tech System
| Item | Qty | Est. Cost |
|------|-----|-----------|
| Raspberry Pi 4 (4GB) | 1 | $55 |
| MicroSD card (32GB) | 2 | $14 |
| USB-C power supply (5V/3A) | 1 | $10 |
| USB webcam 1080p (board cam) | 1 | $25 |
| Micro-HDMI to HDMI cable | 1 | $8 |
| USB LED strip (white, interior) | 1 | $8 |
| 3.5mm aux cable | 1 | $4 |
| Power strip (6-outlet) | 1 | $10 |
| Cable ties / velcro wraps | 1 pack | $5 |

### Display & Audio
| Item | Qty | Est. Cost |
|------|-----|-----------|
| 32" TV (thrift/borrowed) | 1 | $0–60 |
| TV stand or mount bracket | 1 | $20 |
| Powered speakers (20W+) | 1 pair | $25 |
| 2×4 post for monitor mount | 1 | $6 |

### Game Pieces
| Item | Qty | Est. Cost |
|------|-----|-----------|
| Whiffle balls (red, solid color) | 6 | $6 |
| Whiffle balls (blue, solid color) | 6 | $6 |
| Red + blue spray paint (if needed) | 2 cans | $10 |
| Scoring zone vinyl numbers | 1 sheet | $5 |

### **Estimated Total: $335–465**
(Range depends on TV — thrift find vs new budget model. ~$15 less than original concept due to dropping the player cam.)

---

## Build Sequence

### Phase 1: Board Build (Weekend 1, Day 1)
1. Cut plywood to 48×60"
2. Paint back panel matte black (2 coats, let dry overnight between coats)
3. Cut edge rails from 1×4, dry-fit to plywood edges
4. Mark peg grid on plywood: 8 rows, offset pattern, 6" spacing
5. Drill peg holes (¾" bit)
6. Cut dowels to 3" lengths (52 pegs). Paint white.
7. Insert and glue pegs into plywood
8. Attach edge rails with screws (forms the box)
9. Cut 6 scoring dividers from 1×2, 4" tall. Attach at bottom, spacing to create 7 channels

### Phase 2: Frame & Enclosure (Weekend 1, Day 2)
1. Build A-frame legs from 2×4, attach with hinges and carriage bolts
2. Install angle-limiting chain
3. Mount side handles
4. Label all modular joints (A1, A2, etc.)
5. Cut 5 ball-drop notches in top edge rail (3" wide, 1" deep)
6. Build ball return chute: angled trough behind back panel, dumps to collection bin
7. Drill acrylic for peg pass-throughs (match plywood holes exactly)
8. Mount acrylic front panel — seal all edges
9. Test: drop 12 balls, confirm all navigate to scoring zones and return cleanly

### Phase 3: Tech Integration (Weekend 2, Day 1)
1. Flash Raspberry Pi SD card with pre-built OS image
2. Mount board cam: bracket on top edge rail, angled down at playing field
3. Install LED strip inside top edge, behind acrylic
4. Connect: Pi ← USB cam, Pi → HDMI → monitor, Pi → aux → speakers
6. Mount Pi enclosure on back of board (ventilated, zip-tied)
7. Route all cables cleanly along the back with cable ties
8. Power test: single power strip powers Pi + monitor + speakers + LED strip

### Phase 4: Software Calibration (Weekend 2, Day 2)
1. Boot Pi, launch calibration mode
2. Board cam calibration: adjust HSV thresholds for red and blue balls under actual lighting
3. Map pixel coordinates to scoring zones (one-time calibration by dropping a ball in each zone)
4. Map pixel coordinates to the full playing field grid (defines the region where combo target zones can be placed)
5. Test combo zone generation: verify zones appear at valid, reachable positions within the peg field
6. Test collision detection: drop balls through known target zones, confirm hit detection registers accurately
7. Tune hitbox sizes for Easy/Medium/Hard difficulty modes
8. Sound check: verify speaker volume cuts through ambient noise
9. Full playtest: 10 rounds, both modes (solo and versus), all difficulty levels
10. Create spare SD card image (identical backup)

### Phase 5: Game Day Prep
1. Transport: Board + legs (folded) + monitor + speaker bag + Pi kit box
2. Assembly: unfold legs → stand board → plug in power strip → connect HDMI/USB/aux → boot
3. Target setup time: 15 minutes
4. Calibration check: run 2-3 test drops, confirm tracking
5. Print and post: rules sign, privacy notice (no images stored), leaderboard reset

---

## Software Notes (for the dev-inclined dad)

### Ball Tracking (OpenCV)
- Convert frame to HSV color space
- Threshold for red hue range (0-10, 170-180) and blue hue range (100-130)
- Contour detection → centroid = ball position
- Kalman filter for smooth tracking through brief occlusions behind pegs
- Score detection: ball centroid enters a scoring zone polygon → trigger score event
- Ball position published at 30 FPS to the combo zone engine and WebSocket

### Combo Zone Engine (Python)
The core gameplay logic. Runs alongside the CV pipeline.

- **Zone generation:** Before each drop, generate N target zones (3 for Easy, 4 for Medium, 5 for Hard). Each zone is a circular region defined by (x, y, radius) in board-pixel coordinates. Zones are placed within the peg field bounds, vertically distributed (zone 1 near top, zone N near bottom), with horizontal randomization. Constraint: zones must not overlap and must be reachable by a ball (not placed directly on a peg).
- **Collision detection:** Each frame, check if ball centroid is within any zone's radius. If ball enters zone K:
  - If K == next_expected_zone: **HIT** — increment chain, advance next_expected_zone, fire hit event
  - If K != next_expected_zone: **WRONG ORDER** — fire miss event (visual/audio feedback), but do NOT break the chain. Player can still hit the correct zone later.
  - If ball has already passed zone K vertically (below it): zone becomes unreachable, mark as missed
- **Chain state:** Tracks current chain length (0 to N). Published to browser every frame.
- **Multiplier math:** chain 0 = 1×, chain 1 = 1.5×, chain 2 = 2×, chain 3 = 3×, chain 4 = 4×, chain 5 (perfect) = 5× + 200 bonus
- **Ghost paths (pre-drop):** During the "Read the Board" phase, simulate 50 random ball drops from each of the 5 drop slots using a simplified peg-bounce model. Display the resulting probability clouds as faint path lines on the display. These are approximate — just enough to help the player pick a drop slot, not enough to guarantee anything.
- **Difficulty scaling:** Volunteer presses a key (1/2/3) or the system auto-detects based on player height (short = Easy, tall = Hard). Affects zone count and hitbox radius:
  - Easy: 3 zones, radius = 45px (~3" on board)
  - Medium: 4 zones, radius = 35px (~2.5" on board)
  - Hard: 5 zones, radius = 25px (~1.75" on board)

### Display (Browser)
- HTML5 Canvas for real-time rendering (ball trails, combo zone overlays, chain effects)
- Web Audio API for layered sound (background music + SFX + announcer)
- WebSocket client receives ball position + combo zone state + chain progress at 30 FPS
- Zone rendering: numbered circles overlaid on the live camera feed. Green = hit, pulsing yellow = next target, dim gray = waiting, red flash = wrong order
- Announcer: pre-recorded clips triggered by combo events
- Ghost path rendering: semi-transparent gradient lines from each drop slot, showing approximate ball trajectories
- All assets preloaded at boot — no internet required during operation

### Announcer Clip List (record these with any enthusiastic friend)

**Setup & attract:**
- "Step right up to MEGA DROP LIVE!"
- "Read the board... choose your slot... chase the chain!"
- "New targets! Study the board!"

**During drop — chain building:**
- "Here... we... GO!"
- "Zone one — GOT IT!"
- "Two for two! Keep it going!"
- "Three in a row! The crowd is ON THEIR FEET!"
- "FOUR! One more for the PERFECT CHAIN!"
- "FIVE! FIVE! FIVE! PERFECT CHAIN! UNBELIEVABLE!"

**During drop — misses and near-misses:**
- "OHHH! Right past zone two!"
- "So close! That was INCHES from the chain!"
- "The pegs said NO!"
- "Tough bounce... tough bounce..."

**Score reveals:**
- "TEN POINTS!" / "TWENTY-FIVE!" / "FIFTY!" / "ONE HUNDRED! JACKPOT!"
- "Fifty times THREE — that's a hundred fifty!"
- "ONE HUNDRED times FIVE — FIVE HUNDRED POINTS! ARE YOU KIDDING ME?!"
- "NEW HIGH SCORE!"
- "What a chain! Let's see that replay!"

**Two-player:**
- "Red hits zone three! Blue still stuck on two!"
- "It's a CHAIN RACE!"
- "Blue with the perfect chain — can Red answer?!"

---

## Open Questions
- [ ] Raspberry Pi availability (supply chain) — alternatives: old laptop, Intel NUC, Orange Pi
- [ ] Outdoor sun visibility on TV — may need canopy or high-brightness display
- [ ] Pre-record announcer clips or use TTS? (Pre-recorded = more energy, TTS = more variety)
- [ ] Tournament mode logistics — how to manage brackets across a full carnival day
- [ ] Power requirements: Pi (15W) + TV (50-80W) + speakers (20W) + LED (5W) ≈ 120W total — standard outlet sufficient
- [ ] Ghost path accuracy: how many simulations needed for useful-but-not-spoiling path hints? 50 might be too few or too many — needs playtesting
- [ ] Zone placement algorithm: need to ensure generated layouts are always "fair" — at least one drop slot should have a reasonable chance of hitting zones 1→2→3 in sequence. Bad RNG could create impossible layouts.
- [ ] Hitbox tuning: the "right" radius for each difficulty needs real-world testing. Too generous = everyone gets perfect chains (boring). Too tight = nobody chains past 2 (frustrating). Target: ~5% perfect chain rate on Hard, ~30% on Easy.
