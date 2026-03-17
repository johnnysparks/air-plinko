# Stomp Rockets Plinko — Build Plan

## Overall Dimensions

| Dimension | Size | Notes |
|-----------|------|-------|
| Board width | 48" (4 ft) | 7 scoring buckets + 2 gutters across |
| Board height | 72" (6 ft) | Tall enough for epic peg runs |
| Board depth (gap) | 4" | Whiffle ball (2.75") + bounce clearance |
| Tilt angle | ~25° from vertical | Steep enough for ball speed, shallow enough for stomped launches to reach the top |
| Peak height (top of board) | ~84" (7 ft) | Top of board when tilted on frame |
| Bottom of board height | ~24" off ground | Low enough for small kids to see |
| Stomp pad distance | 36" in front of board | Room for full jumping stomps |
| Total footprint | ~48"W × 60"D × 84"H | Includes stomp zone |

---

## Architecture

### 1. Plinko Board

#### Back Panel
- 4×6 ft sheet of ¾" plywood
- Painted matte black with neon accent stripes (pink, green, yellow)
- Peg holes drilled in offset grid pattern: 8" horizontal spacing, 6" vertical spacing, offset every other row
- ~60 peg positions total

#### Front Panel
- 4×6 ft clear acrylic sheet (¼" thick, shatter-resistant)
- Mounted with bolts through spacer pegs
- Hinged at top for ball jam access (piano hinge)

#### Pegs
- 3D-printed mushroom-cap pegs: 1.5" diameter cap, ¾" stem, 3" long
- Stem inserts into drilled hole in plywood, friction-fit + dab of wood glue
- Printed in 4 neon colors (15 each): hot pink, electric green, yellow, cyan
- Mushroom cap shape gives satisfying deflection and visual pop

#### Edge Rails
- 1×4 lumber on all four sides between plywood and acrylic
- 4" depth = ball gap
- Bottom rail has 9 slots cut into it for scoring buckets and gutters

### 2. Scoring Buckets (Bottom of Board)

- 9 channels cut through the bottom edge rail
- Layout (left to right): GUTTER | 50 | 100 | 200 | **500** | 200 | 100 | 50 | GUTTER
- Channel widths: gutters 2", outers 6", mids 5", inners 4", center 3"
- Each channel has a painted backplate with the point value in large reflective vinyl numbers
- Bucket channels angle backward through the board into collection tubes

#### Sound triggers (optional but awesome)
- Piezo sensors or simple lever switches at the bottom of each bucket channel
- Wired to a small Arduino + speaker module mounted behind the board
- CENTER 500: victory siren clip
- GUTTER: sad trombone WAH WAH WAH
- All others: satisfying "ding" at different pitches
- DRY FIRE (stomp with no ball): whoopee cushion sound from stomp pad speaker

### 3. Support Frame

- **A-frame design:** Two sets of 2×4 legs, bolted to back of board
- **Front legs (×2):** Angled forward, feet land ~36" in front of board bottom — creates the tilt
- **Rear legs (×2):** Straight down from board back, adjustable chain for angle fine-tuning
- **Cross braces:** Horizontal 2×4 between each leg pair at mid-height
- **Break-down joints:** Carriage bolts + wing nuts at all connections
- **Rubber feet** on all four contact points
- **Side handles (×2):** Mounted on board edges for two-person carry

### 4. Stomp Launch System (×2)

#### Stomp Pad
- **Base:** 18"×18" plywood platform, ¾" thick
- **Bladder:** Heavy-duty rubber exercise ball bladder OR custom-sewn vinyl bladder, ~14" diameter, 4" inflated height
- **Mounting:** Bladder sits in a recessed pocket in the platform, covered with a ¼" rubber mat for grip and durability
- **Air outlet:** Barbed fitting epoxied into bladder, connects to 1" ID flexible hose
- **Anti-slip:** Rubber mat on top, rubber feet on bottom. This thing cannot slide.
- **Durability:** The bladder is the wear item. Keep 2 spares. Takes 3 minutes to swap.

#### Air Hose
- 1" ID flexible vinyl tubing, ~4 ft length
- Connects stomp pad to launch tube
- Slight upward routing to prevent ball backflow

#### Launch Tube
- 1.5" ID PVC pipe, 18" long
- Mounted at ~60° angle on the bottom edge of the plinko board
- Ball sits at the bottom of the tube, held by gravity
- Air burst from stomp pad shoots ball up the tube into the playing field
- Exit point is at the bottom of the board — ball enters the peg field and travels upward based on stomp force

#### Ball Magazine
- Gravity-fed hopper mounted above the launch tube entry point
- Made from 4" PVC pipe, 18" tall, holds 10 balls in a stack
- Ball-release gate at the bottom: simple spring-loaded flap that opens when launch tube is empty (ball weight pushes it open) and closes when launch tube has a ball
- Magazine is clear/translucent so players can see remaining balls

### 5. Ball Collection & Return

- **Bucket exits:** Each scoring bucket channel angles backward through the board at ~30°
- **Rear chute:** Behind the board, a wide angled chute (plywood, painted smooth) collects all balls from all bucket channels
- **Center divider:** Splits balls to left/right player collection
- **Return tubes:** 3" PVC, gravity-fed from rear chute back to each player's magazine
- **Flow:** Score bucket → rear chute → divider → return tube → magazine top
- **Gutter returns:** Same path, just no points

---

## Materials List

### Lumber & Sheet
| Item | Qty | Est. Cost |
|------|-----|-----------|
| ¾" plywood sheet (4×6 cut) | 1 | $45 |
| ¼" clear acrylic sheet (4×6 cut) | 1 | $100–140 |
| 1×4 lumber (edge rails, 20 lin. ft) | 3 (8ft) | $18 |
| 2×4 lumber (frame/legs, 32 lin. ft) | 4 (8ft) | $24 |
| Scrap plywood for stomp pads, chutes | — | $15 |

### 3D Printed Parts
| Item | Qty | Est. Cost (filament) |
|------|-----|-----------|
| Mushroom-cap pegs (4 colors) | 60 | $15 |
| Ball magazine release gates | 2 | $3 |
| Scoring bucket dividers | 8 | $5 |

### Hardware
| Item | Qty | Est. Cost |
|------|-----|-----------|
| Piano hinge (48" for acrylic lid) | 1 | $10 |
| Carriage bolts + wing nuts | 1 set | $15 |
| Wood screws (assorted) | 1 box | $8 |
| Hinges (for frame legs) | 4 | $16 |
| Chain (angle limiter) | 2 | $10 |
| Heavy-duty handles | 2 | $12 |
| Rubber feet caps | 4 | $6 |
| Barbed hose fittings | 4 | $8 |

### Launch System
| Item | Qty | Est. Cost |
|------|-----|-----------|
| Heavy-duty rubber bladders | 4 (2 active + 2 spare) | $20 |
| 1" ID vinyl tubing (per foot) | 10 ft | $8 |
| 1.5" PVC pipe (launch tubes) | 4 ft | $4 |
| 4" clear PVC pipe (magazines) | 3 ft | $12 |
| ¼" rubber mat (stomp pad surface) | 2 sq ft | $8 |
| Rubber sheet for pad bottoms | 2 sq ft | $6 |

### Ball Return
| Item | Qty | Est. Cost |
|------|-----|-----------|
| 3" PVC pipe (return tubes) | 8 ft | $10 |
| PVC elbows and fittings | 6 | $12 |

### Game Pieces & Finish
| Item | Qty | Est. Cost |
|------|-----|-----------|
| Whiffle balls (neon, 2 colors) | 24 pack | $12 |
| Neon spray paint (4 colors) | 4 cans | $20 |
| Reflective vinyl numbers/letters | 1 roll | $8 |
| LED strip (optional — backlight the pegs) | 1 (16ft) | $15 |

### Sound System (Optional)
| Item | Qty | Est. Cost |
|------|-----|-----------|
| Arduino Nano | 1 | $8 |
| Piezo sensors | 9 | $10 |
| Small powered speaker | 1 | $12 |
| Wiring / breadboard | — | $5 |

### **Estimated Total: $400–500** (without sound: $360–440)

---

## Build Sequence

### Phase 1: Board & Frame (Weekend 1, Day 1)
1. Cut plywood to 48×72"
2. Sand and paint matte black. Add neon racing stripes while paint is wet (tape + spray)
3. Mark and drill peg holes — offset grid, 8"H × 6"V spacing, ~60 holes
4. Cut edge rails from 1×4, attach to plywood (forms 4" deep box)
5. Cut 9 scoring channels into the bottom edge rail
6. Build A-frame legs from 2×4, attach with carriage bolts + wing nuts
7. Test stand-up — verify tilt angle, stability

### Phase 2: Pegs & Scoring (Weekend 1, Day 2)
1. 3D print mushroom-cap pegs (can run overnight in batches of 15)
2. Insert and glue pegs into board holes
3. Build scoring bucket channel dividers, install in bottom rail slots
4. Paint point values on bucket backplates with reflective vinyl
5. Build rear collection chute from scrap plywood
6. Install center divider in rear chute
7. Dry-test: drop balls from top, verify they cascade cleanly to buckets

### Phase 3: Launch System (Weekend 2, Day 1)
1. Build stomp pad platforms (cut plywood, route bladder pocket, add rubber surfaces)
2. Install barbed fittings in bladders
3. Cut and connect vinyl air hoses
4. Mount launch tubes (1.5" PVC) at bottom of board at 60° angle
5. Build ball magazines from 4" clear PVC, mount above launch tube entries
6. 3D print and install ball release gates
7. Test: stomp → air burst → ball launches into field. Tune bladder size and hose length for good response

### Phase 4: Ball Return & Finish (Weekend 2, Day 2)
1. Route 3" PVC return tubes from rear chute to magazine tops
2. Test full cycle: stomp → launch → cascade → bucket → return → magazine
3. Drill acrylic for peg pass-throughs and edge bolt holes
4. Mount acrylic front panel with piano hinge at top
5. Seal all edges — no ball escapes
6. Add LED backlighting (optional: run strip behind pegs for neon glow)
7. Install sound system if desired (Arduino + sensors + speaker)
8. Full playtesting — 45-second timed rounds, verify ball flow, stomp response, scoring

---

## Open Questions
- [ ] Bladder durability under heavy stomping — may need reinforced seams or commercial stomp rocket replacement bladders
- [ ] Optimal launch tube angle vs stomp force — needs prototyping (try 45°, 60°, 75°)
- [ ] Ball magazine auto-feed reliability — the release gate is the trickiest mechanical part
- [ ] Sound system scope — full Arduino rig or just a Bluetooth speaker with manual sound effects?
- [ ] Whether to allow JUMPING stomps (more force, more fun, more wear) or just standing stomps
- [ ] LED power source — battery pack or extension cord?
