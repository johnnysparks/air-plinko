# Flipper Frenzy — Build Plan

## Concept
Portable pinball/plinko riot built on hardware-store pegboard. Up to 6 balls cascade simultaneously through static pegs, SPINNER pegs (rotating windmills that redirect subsequent balls), and CHIME pegs (aluminum tubes that create melodies). Two players each control dual flippers (left + right hand). A WARP ZONE tunnel through the center divider sends balls between player sides. Auto-feed magazine drops a new ball every ~5 seconds. Entire game packs into two flat bundles + a duffel bag. Zero tools to assemble. ~33 lbs total.

## Overall Dimensions

| Dimension | Size | Notes |
|-----------|------|-------|
| Width | 48" (4 ft) | Two-player side-by-side |
| Height | 60" (5 ft) | Playable standing for kids & adults |
| Depth (gap) | 4" | Whiffle ball (2.75") + peg/spinner clearance |
| Tilt angle | ~20° from vertical | Balls roll down, flippers launch up |
| Frame footprint | 48"W x 24"D x 65"H | PVC frame with rear legs + top magazine |
| Transport: panel bundle | 48" x 60" x 1" | Pegboard + polycarbonate rubber-banded |
| Transport: frame kit | 36" x 14" x 10" duffel | Everything else |

---

## Architecture

### 1. Frame — PVC Snap-Together Skeleton

**Pipes:** 3/4" Schedule 40 PVC conduit, cut to length:
- 2x vertical uprights: 65" (front face, left & right — 3" taller than Flipper Plinko for magazine mount)
- 2x horizontal crossbars: 48" (top & bottom of playing field)
- 1x magazine crossbar: 48" (across top, 3" above main crossbar — supports ball magazine)
- 2x rear legs: 48" (angled back for tilt)
- 2x rear cross-braces: 46" (lateral stability between rear legs)
- 2x diagonal braces: 24" (connect uprights to rear legs at top)

**3D-Printed Connectors (PETG):**
- 4x corner joints (90-degree elbow with channel rail for panels)
- 2x top T-joints (upright-to-crossbar-to-diagonal)
- 2x magazine bracket joints (extend uprights above crossbar, hold magazine rail)
- 2x bottom T-joints (upright-to-crossbar-to-rear-leg)
- 2x rear leg feet (with rubber bumper recess)
- 2x rear brace clips (snap onto rear legs at 24" height)

**Assembly:** All joints are friction-fit with a 3D-printed retaining clip that snaps over the joint to lock it. No glue, no screws. Pull the clip to disassemble.

**Channel Rails:** Each corner joint includes an integrated channel (slot) that accepts the pegboard and polycarbonate panels. Panels slide in from the top.

### 2. Playing Surface — Standard Pegboard

- **Material:** 1/4" tempered hardboard pegboard, 48" x 60" (cut from standard 4x8 sheet)
- **Hole pattern:** Standard 1" center-to-center, 1/4" holes
- **Weight:** ~8 lbs
- **Finish:** Spray painted matte black (neon pegs + spinners pop against dark background)
- **Mounting:** Slides into channel rails on the PVC frame
- **Center divider hole:** One 3.5" diameter hole drilled at board center (24" from each side, 30" up from bottom) for the Warp Zone tunnel

### 3. Front Panel — Clear Polycarbonate

- **Material:** 1/8" clear polycarbonate (Lexan), 48" x 60"
- **Weight:** ~10 lbs
- **Mounting:** Slides into front channel rails on same corner joints
- **Gap:** 4" between pegboard and polycarbonate (set by connector depth)
- **Access:** Slides out the top for peg reconfiguration

### 4. Static Pegs (3D Printed)

- **Quantity:** ~40 pegs in offset rows
- **Design:** Mushroom-cap peg with a 1/4" post that press-fits into pegboard holes. Cap diameter: 1.5". Post length: 1"
- **Material:** PETG (tough, slight flex)
- **Colors:** Neon green, neon orange, neon pink, neon blue — alternating rows
- **Layout:** Offset grid, 3" horizontal spacing, 4" vertical spacing, starting 14" from bottom (above flipper zone), ending 8" below top (below magazine feed zone)

### 5. Spinner Pegs (3D Printed — THE KEY INNOVATION)

- **Quantity:** 20 spinners, distributed evenly through the peg field
- **Design:** Four-armed windmill/pinwheel on a central axle. Each arm is 1.25" long, 0.5" wide, with a slight cup to catch ball impacts. Total diameter: 3".
- **Axle:** 1/4" steel pin (cut from nail or rod) press-fit through the windmill hub. Pin passes through the pegboard hole and is retained by a 3D-printed backing washer on the rear.
- **Bearing:** Miniature skateboard bearing (608ZZ, 8mm bore) pressed into the windmill hub. Axle pin passes through the bearing. Spins freely with near-zero friction.
- **Colors:** Bright yellow PETG — visually distinct from static pegs
- **Behavior:** Ball strikes one arm, spinner rotates 60-120 degrees. The repositioned arms redirect the NEXT ball that passes through at a different angle. After 3-4 ball impacts, the spinner has rotated enough to create a completely different ball path through that zone.
- **Mounting:** Same pegboard hole as static pegs. Pin press-fits. Pull from the back to remove/replace.
- **Placement:** Staggered through the mid-field zone (rows 3-8 of 10 peg rows). Concentrated in the center where ball traffic is highest. Never adjacent to another spinner (minimum 2 static pegs between spinners).

### 6. Chime Pegs (Aluminum Tubes — THE SOUND)

- **Quantity:** 12 chime tubes
- **Material:** 3/8" diameter aluminum tube (from wind chime stock or hobby shop), cut to lengths:
  - Top row (2 tubes): 6" — highest pitch
  - Upper-mid row (3 tubes): 5" — high-mid pitch
  - Lower-mid row (3 tubes): 4" — low-mid pitch
  - Bottom row (4 tubes): 3" — lowest pitch
- **Mounting:** Each tube hangs vertically behind the pegboard, positioned directly behind a static peg. A 3D-printed clip hooks onto the pegboard from the rear, holds the tube suspended with 1/4" of clearance. When a ball hits the peg, the peg vibrates through the pegboard and strikes the tube.
- **Alternate mounting:** Tube passes through a slightly enlarged pegboard hole (drill to 3/8") with the tube end flush with the peg face. Ball directly strikes the tube. Louder, more reliable contact.
- **Tuning:** Tube length determines pitch. Longer = lower. The 12 tubes span roughly one octave. No precision tuning needed — the semi-random pitches create a pleasant wind-chime effect, not a melody.
- **Sound volume:** Aluminum tube struck by a 2.75" whiffle ball produces a gentle but clearly audible chime. With 4-5 balls cascading simultaneously, the overlapping chimes create a distinctive "cascading bells" sound audible from 15-20 feet away.
- **Weight:** All 12 tubes total ~0.3 lbs

### 7. Warp Zone Tunnel

- **Location:** Center of the board, 30" from bottom, centered left-to-right
- **Construction:** 3D-printed tunnel ring, 3.5" inner diameter, 4" long (spans the full depth from pegboard face to polycarbonate). Press-fits into the 3.5" hole drilled in the pegboard. Flares slightly on both openings to guide balls in.
- **How it works:** Balls cascading through the center of the board can enter the tunnel from either side. The tunnel passes through the center divider, depositing the ball on the other player's peg field approximately at the mid-height mark. The ball then cascades through the other player's pegs.
- **Probability:** ~1 in 5 balls that reach the center zone will enter the warp (based on approach angle and momentum). Not every ball warps — it's a special event.
- **Visual:** Printed in glow-in-the-dark or fluorescent purple PETG. Unmistakable on the board.

### 8. Ball Magazine & Auto-Feed System

- **Location:** Top of the board, spanning full 48" width
- **Construction:** 3D-printed open trough (V-shaped channel, 3" wide, 3" deep) that hooks onto the magazine crossbar. Holds up to 12 balls (6 per player side).
- **Feed mechanism:** Gravity gate — a 3D-printed paddle on a simple escapement mechanism (weight-driven, no electronics). A small counterweight lifts the gate every ~5 seconds, releasing one ball into the feed slot. The ball drops through a hole in the top crossbar area and enters the peg field from above.
- **Feed slots:** 2 feed points — one on each player's side, offset 12" from center (at the 12" and 36" marks across the width).
- **Loading:** Operator (volunteer) periodically adds balls to the magazine trough from a bucket. Between players, dump all balls back into the magazine. 10-second reset.
- **Simplification option:** Skip the escapement. Just have the operator hand-drop balls into the feed slots every few seconds. Zero mechanism. Pure simplicity. The auto-feed is nice-to-have, not essential.

### 9. Flipper System (x4 — TWO PER PLAYER)

**Per flipper (x4 total):**
- **Paddle:** 3D-printed, 6" long (shorter than Flipper Plinko's 8" to create the "death gap"), 1.5" wide, flat profile. Mounted on a 1/4" steel pivot bolt through the bottom crossbar rail.
- **Spring return:** Rubber band pulls flipper to resting position (~10 degrees above horizontal)
- **Actuation:** Bicycle brake lever mounted on the side upright at hip height. Brake cable runs inside PVC pipe to a pull arm on the flipper pivot.
- **Sweep:** 60-degree swing (from 10-degree rest to 70-degree up)

**Layout per player:**
- **Left flipper:** Positioned at the 25% mark of the player's half-width. Controlled by left-hand squeeze lever on the left upright.
- **Right flipper:** Positioned at the 75% mark of the player's half-width. Controlled by right-hand squeeze lever on the right upright (or a second lever on a center post).
- **Death gap:** ~3" gap between the left and right flippers where neither can reach. Balls that drop through the death gap drain instantly. Creates risk and forces ball-reading skill.
- **Flipper trough:** Angled channel (3D-printed) that funnels balls from above toward the flipper sweet spot. One trough feeds each flipper, angled inward from center.

**The feel:** Both hands gripping brake levers, eyes darting between multiple cascading balls, squeezing left-right-left-right in rapid succession. It's like drumming. Kids develop rhythm. Spectators can SEE the two-handed coordination.

### 10. Scoring Buckets (3D Printed + Pegboard Hooks)

- **Design:** Open-top trays with pegboard hook backs.
- **Layout:**

```
   [BALL MAGAZINE — auto-feeds every 5 sec]
   ========================================
   |  feed    ||     WARP      ||   feed   |
   |  slot    ||     ZONE      ||   slot   |
   |          || (3.5" tunnel) ||          |
   |  STATIC + SPINNER + CHIME PEG FIELD  |
   |  ~40 static, 20 spinners, 12 chimes  |
   |          ||               ||          |
   |  [50]    || [JACKPOT 100] ||   [50]   |
   |  [25]    ||               ||   [25]   |
   |  [10 ————||———————————————||———— 10]  |
   |  [L.FLIP]||  [DEATH GAP]  ||[R.FLIP]  |
   |  [DRAIN  ||    DRAIN      || DRAIN]   |
   ========================================
         Player 1    |    Player 2
```

- **Bucket sizes:** Jackpot (3" wide), 50 pts (4" wide), 25 pts (5" wide), 10 pts (8" wide)
- **Hook style:** Standard pegboard hook back — push on, lift off
- **Ball drainage:** Rear holes in each bucket. Ball rolls through, drops behind pegboard, slides down rear chute to collection bin.

### 11. Center Divider + Warp Zone Integration

- **Lower section (bottom 28"):** 3D-printed vertical rail hooks onto pegboard at center line. Separates player flipper zones and drain lanes.
- **At 30" height:** Warp Zone tunnel passes through the divider. Balls can cross sides here.
- **Upper section (above 32"):** No divider. Both players' balls share the upper peg field. Balls from either side can reach any upper bucket. Creates contested space.

### 12. Ball Return System

- **Gutter:** Balls that miss flippers drop through a slot in the bottom crossbar into a 3D-printed trough behind the pegboard
- **Rear chute:** Angled channel attached to back of pegboard, funnels all balls to a collection bin at base
- **Collection bin:** Open box at bottom rear. Operator scoops balls back into the top magazine between rounds.

---

## Materials List

### Pegboard & Panel
| Item | Qty | Est. Cost |
|------|-----|-----------|
| 1/4" pegboard sheet (4x8, cut to 4x5) | 1 | $12 |
| 1/8" clear polycarbonate (4x5 cut) | 1 | $55 |

### PVC Frame
| Item | Qty | Est. Cost |
|------|-----|-----------|
| 3/4" PVC conduit (10 ft sticks) | 4 | $12 |
| PVC pipe cutter (if not owned) | 1 | $8 |

### 3D Printed Parts (~2.2 kg filament total)
| Item | Qty | Est. Cost |
|------|-----|-----------|
| PETG filament, neon colors (1kg spools) | 2 | $40 |
| PETG filament, yellow (spinner pegs) | 1 | $20 |
| PETG filament, fluorescent purple (warp zone) | 0.2kg | (from neon spool) |
| Connector joints (corners, tees, feet, magazine brackets) | 14 | (printed) |
| Static pegs (mushroom cap) | ~40 | (printed) |
| Spinner peg windmills + backing washers | 20 | (printed) |
| Chime tube clips (rear-mount) | 12 | (printed) |
| Scoring buckets | 7 | (printed) |
| Flipper paddles | 4 | (printed) |
| Flipper trough channels | 4 | (printed) |
| Warp Zone tunnel ring | 1 | (printed) |
| Ball magazine trough (2 sections) | 2 | (printed) |
| Ball return chute pieces | 3 | (printed) |
| Center divider rail | 1 | (printed) |

### Hardware
| Item | Qty | Est. Cost |
|------|-----|-----------|
| Bicycle brake levers + cables | 4 | $20 |
| 1/4" steel bolts + wing nuts (flipper pivots) | 8 | $6 |
| Rubber bands (flipper return springs) | 1 bag | $3 |
| Miniature skateboard bearings (608ZZ) | 20 | $12 |
| 1/4" steel pins / nails (spinner axles), 1.5" long | 20 | $4 |
| Rubber chair leg caps (frame feet) | 4 | $4 |
| Matte black spray paint | 2 cans | $10 |
| Neon spray paint (accent) | 2 cans | $10 |

### Chime Tubes
| Item | Qty | Est. Cost |
|------|-----|-----------|
| 3/8" aluminum tube stock (3 ft) | 2 | $8 |
| (Alternative: wind chime replacement tubes) | 1 set | $10 |

### Game Pieces
| Item | Qty | Est. Cost |
|------|-----|-----------|
| Whiffle balls (colored, neon) | 18 pack | $12 |
| Adhesive vinyl numbers (scoring) | 1 sheet | $5 |

### **Estimated Total: $220–245**

Only $25-35 more than original Flipper Plinko. The bearings ($12) and extra brake cables ($10) are the main additions.

---

## Build Sequence

### Phase 1: Print Week (Evenings, ~55 hrs print time)
1. Print all connector joints including magazine brackets (10 hrs)
2. Print static pegs in batches of 20 per plate (2 plates x 3 hrs = 6 hrs)
3. Print spinner windmills — 4 per plate (5 plates x 2.5 hrs = 12 hrs)
4. Print spinner backing washers — 20 per plate (1 plate x 1 hr)
5. Print scoring buckets (7 x 1.5 hrs = 10 hrs)
6. Print flipper components — 4 paddles, 4 troughs, 4 pull arms (6 hrs)
7. Print Warp Zone tunnel ring (2 hrs)
8. Print ball magazine trough (2 sections x 2 hrs = 4 hrs)
9. Print ball return chute + chime tube clips (4 hrs)

*Run prints overnight and during work hours. Actual hands-on time: ~3 hrs total (slicing, bed prep, part removal, bearing press-fit into spinner hubs)*

### Phase 2: Frame & Panels (Saturday Morning, 2.5 hrs)
1. Cut PVC pipes to length (12 cuts with pipe cutter)
2. Test-fit all connector joints — sand any tight fits
3. Assemble frame, verify it stands square
4. Cut pegboard to 48" x 60" (circular saw or jigsaw)
5. Drill 3.5" hole at center point for Warp Zone (hole saw)
6. Spray paint pegboard matte black, let dry
7. Test panel slide into channel rails

### Phase 3: Spinners & Chimes (Saturday Afternoon, 2 hrs)
1. Press 608ZZ bearings into 20 spinner windmill hubs (arbor press or vise + socket)
2. Insert 1/4" steel pins through bearings. Test spin — should rotate freely for 3+ seconds
3. Insert spinner pin posts through pegboard holes from front. Attach backing washer on rear. Test spin in-situ
4. Cut 12 aluminum tubes to length (hacksaw): 2x 6", 3x 5", 3x 4", 4x 3"
5. Deburr tube ends with file
6. Attach chime tube clips to rear of pegboard at designated peg positions
7. Hang tubes in clips. Test — flick each one, verify it rings clearly

### Phase 4: Flippers & Warp Zone (Sunday Morning, 2.5 hrs)
1. Drill 4 flipper pivot holes in bottom crossbar
2. Assemble 4 flipper mechanisms — bolt through pivot, attach rubber band return
3. Route 4 brake cables from levers through PVC uprights to flipper pull arms
4. Mount brake levers on side uprights (2 per side — one at hip height, one slightly lower for left-hand access)
5. Press-fit Warp Zone tunnel into pegboard center hole
6. Test flipper action — adjust cable tension until satisfying snap on all 4
7. Test Warp Zone — roll ball through from each side, verify smooth passage

### Phase 5: Assembly & Playtest (Sunday Afternoon, 1.5 hrs)
1. Full assembly from packed state — time it (goal: under 12 minutes)
2. Pop in all static pegs, spinner pegs, and chime clips
3. Hook on scoring buckets
4. Attach ball magazine trough to top crossbar
5. Hook on ball return chute behind pegboard
6. Slide in polycarbonate front panel
7. Load 12 balls into magazine (6 per side)
8. Test: drop balls from magazine, watch cascade, test all 4 flippers, test warp zone
9. Listen to chimes — adjust tube positions if any are muffled by pegboard contact
10. Check spinner rotation after 20 ball passes — should still spin freely
11. Adjust peg layout if balls get stuck or paths are too predictable
12. Apply scoring vinyl numbers to buckets

### Phase 6: Transport Test
1. Full disassembly — time it (goal: under 7 minutes)
2. Pack panel bundle (pegboard + polycarbonate, rubber-banded)
3. Pack everything else into duffel bag (spinners stay mounted in pegboard)
4. Load into car. Confirm it fits. Drive around the block.
5. Unload. Reassemble. Verify no spinners loosened in transit. Test chime tubes didn't shift.

---

## Transport Comparison

| | OG Air Plinko | Flipper Plinko | **Flipper Frenzy** |
|---|---|---|---|
| Weight | ~85 lbs | ~30 lbs | **~33 lbs** |
| Vehicle needed | Truck/SUV | Sedan | **Sedan** |
| Assembly time | 45-60 min | 10 min | **10-12 min** |
| Tools for assembly | Drill, wrench | None (1 wing nut) | **None (4 wing nuts)** |
| People to carry | 2 | 1 | **1** |
| Cost | $350-400 | $195-210 | **$220-245** |
| Chaos level | ??? | 6/10 | **9/10** |
| Memorability | ??? | 7/10 | **10/10** |

---

## Open Questions
- [ ] Spinner bearing longevity — 608ZZ rated for millions of rotations, but press-fit housing in PETG may loosen. Test after 500 ball impacts. May need a dab of CA glue on the housing.
- [ ] Chime volume — aluminum tube struck by whiffle ball may be too quiet in a noisy carnival. Fallback: use thinner-wall tube or mount a small resonance chamber behind each tube (printed).
- [ ] Warp Zone angle — the 3.5" tunnel needs the right entry angle to catch ~20% of center-bound balls. May need a small funnel lip or guide rail above the opening to increase warp probability.
- [ ] 4 brake cables in PVC — routing 2 cables per upright (one per flipper) may cause friction. May need to route outer cables externally along the PVC with printed cable guides.
- [ ] Auto-feed escapement — gravity-driven escapement timing is finicky. Prototype first. Fallback: operator hand-drops (works great, just needs a dedicated person).
- [ ] Polycarbonate flex — same concern as Flipper Plinko. 1/8" over 48" unsupported may bow. Add a mid-height horizontal PVC stiffener if needed.
