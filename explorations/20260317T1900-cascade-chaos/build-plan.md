# CASCADE CHAOS — Build Plan

## Concept

Two-player plinko variant with a strategic twist: players place magnetic deflector shields on a steel-backed peg board, then a hopper dumps 50+ balls simultaneously. Deflector placement determines where the avalanche flows. Strategy phase + spectacle phase.

## Modes
- **Competitive:** Red vs Blue — most points in your bins wins
- **Cooperative:** Both players place deflectors, combine scores, beat a target number

---

## Overall Dimensions

| Dimension | Size | Notes |
|-----------|------|-------|
| Width | 48" (4 ft) | Two halves, one per player |
| Height | 60" (5 ft) | Playable standing for kids & adults |
| Depth (gap) | 4" | Enough for whiffle balls (2.75") + deflectors (1") |
| Tilt angle | ~20° from vertical | Steeper than OG — balls need momentum for the avalanche |
| Hopper | 48"W × 6"H × 4"D | Spans full width at top, holds 55+ balls |

Total footprint with legs: ~48"W × 36"D × 66"H (hopper adds 6" above playing field)

---

## Architecture

### 1. Frame & Playing Field

- **Back panel:** 4×5 ft sheet of ¾" plywood
- **Steel sheet overlay:** 4×5 ft sheet of 26-gauge galvanized steel, screwed to plywood face. This is what the magnetic deflectors stick to. Painted matte black for visibility
- **Front panel:** 4×5 ft clear acrylic sheet (¼" thick)
- **Peg grid:** ⅜" steel rods, 3" long, welded or press-fit through holes in the steel sheet into the plywood backing. 6" spacing, offset rows (standard plinko grid). Steel rods serve as pegs AND as additional magnetic anchor points for deflectors
- **Edge rails:** 1×4 lumber on all four sides, sandwiched between steel-backed plywood and acrylic
- **Center divider line:** Painted stripe (no physical wall) — each player places deflectors on their half only
- **Tilt frame:** A-frame legs, hinged, with chain angle limiter (same as OG design)

### 2. Hopper Assembly (Top)

- **Box:** 48"W × 6"H × 4"D box mounted on top of the playing field
- **Construction:** ¾" plywood bottom and sides, open top for loading
- **Gate mechanism:** A single hinged flap along the bottom edge of the hopper, running the full 48" width
- **Release mechanism:** Pull-rope attached to the flap via eye hooks and paracord. Volunteer pulls rope → flap drops → balls cascade out
- **Gate stop:** Small chain limits flap to 90° open so it doesn't slam
- **Ball guard:** 1" lip at the front (acrylic side) prevents balls from spilling forward during loading
- **Loading:** Balls are poured in from the top between rounds. Takes 10 seconds

### 3. Magnetic Deflector Shields (16 total — 8 per player)

- **Shape:** Right-triangle wedge, 3" hypotenuse × 2" base × 1" tall
- **Construction:** 3D-printed PLA wedges with a flat back face
- **Magnets:** Two ½" diameter × ⅛" thick neodymium disc magnets (N42 grade) epoxied into recesses on the flat back. Strong enough to hold against gravity + ball impacts, weak enough for a kid to pull off
- **Color coding:** Red set (8) and Blue set (8), matching ball colors
- **Grip:** Small 3D-printed fin on top for easy grab-and-place
- **Placement:** Players stick deflectors onto the steel sheet anywhere on their half. The angled face redirects ball flow. Placement on pegs or between pegs both work
- **Why magnets:** Instant on/off. No clips, no hooks, no tools. A kindergartner can do it. Reset takes 5 seconds — just sweep them off

### 4. Scoring Bins (Bottom)

- **Count:** 6 bins spanning the full width (3 per player's half)
- **Construction:** Angled wood dividers creating V-shaped troughs, each 8" wide
- **Scoring values (per half, inside to outside):**

```
  Player A side              │           Player B side
  [10 pts] [25 pts] [50 pts] │ [50 pts] [25 pts] [10 pts]
  (wide)   (medium) (narrow) │ (narrow) (medium) (wide)
```

- **Center bins (50 pts):** Narrowest, hardest to hit — right at the divider line where deflector territory ends
- **Outer bins (10 pts):** Widest, easiest — the "gutter" default
- **Bin depth:** 4" — matches playing field gap
- **Lip height:** 2" front lip to prevent bounce-outs during avalanche impacts
- **Overflow trough:** Below all bins, catches any balls that bounce out. These don't score

### 5. Ball Set

- **Red whiffle balls:** 25 (standard 2.75" practice golf ball size)
- **Blue whiffle balls:** 25
- **Gold whiffle balls:** 5 (spray-painted, worth 5× multiplier in any bin)
- **Total:** 55 balls
- **Why whiffle:** Light enough that magnetic deflectors hold against impacts. Holes create air drag for slower, more visible cascades. Loud clatter on steel pegs

### 6. Ball Return / Reset

- **No automated return.** After each round, a volunteer scoops balls from scoring bins into a bucket and pours them back into the hopper from the top. This is intentionally simple — no plumbing, no jams, no moving parts
- **Scoop tool:** A wide plastic dustpan or half-pipe scoop lives at the base of the game
- **Reset time:** Sweep deflectors off (5 sec) + scoop balls into bucket (10 sec) + pour into hopper (5 sec) = **~20 seconds between rounds**

### 7. Support Frame (Modular / Reusable)

- Same design as OG Air Plinko:
  - Rear 2×4 legs, hinged, fold flat
  - Cross brace at 24" height
  - Chain angle limiter
  - Rubber feet
  - Wing nut + carriage bolt joints (tool-free setup)
  - Side handles for two-person carry
  - Labeled connection points

### 8. Timer & Countdown

- **Option A (cheap):** Volunteer uses phone timer, calls out "10 seconds... 5... 4... 3... 2... 1... STOP"
- **Option B (better):** Battery-powered digital countdown timer ($15, magnetic mount) stuck to the steel board above the playing field. Visible to players and crowd
- **Option C (best):** 3D-printed countdown display housing with large LED segments, powered by a $5 Arduino Nano. Volunteer presses a button, 30 seconds count down with beeps at 10, 5, 4, 3, 2, 1. Buzzer at zero

---

## Materials List

### Lumber & Sheet
| Item | Qty | Est. Cost |
|------|-----|-----------|
| ¾" plywood sheet (4×5 cut for back panel) | 1 | $35 |
| ¼" clear acrylic sheet (4×5 cut for front) | 1 | $90 |
| 26-gauge galvanized steel sheet (4×5 cut) | 1 | $45 |
| 1×4 lumber (edge rails, 18 lin. ft) | 3 (8ft) | $18 |
| 2×4 lumber (frame/legs) | 2 (8ft) | $12 |
| ¾" plywood scraps (hopper box, bin dividers) | — | $15 |

### Hardware
| Item | Qty | Est. Cost |
|------|-----|-----------|
| ⅜" steel rods, 36" length (cut to 3" pegs) | 6 | $24 |
| Bolts, nuts, washers | — | $10 |
| Wood screws (assorted) | 1 box | $8 |
| Hinges (frame legs + hopper gate) | 4 | $14 |
| Chain (angle limiter + gate stop) | 10 ft | $10 |
| Eye hooks (rope routing) | 4 | $4 |
| Paracord (pull rope, 10 ft) | 1 | $5 |
| Wing nuts + carriage bolts | 1 set | $15 |
| Rubber feet caps | 4 | $6 |
| Heavy-duty handles | 2 | $12 |

### Deflector System
| Item | Qty | Est. Cost |
|------|-----|-----------|
| PLA filament (for 16 deflector wedges) | ~200g | $5 |
| N42 neodymium disc magnets (½" × ⅛") | 32 | $15 |
| 2-part epoxy | 1 tube | $5 |

### Game Pieces & Finish
| Item | Qty | Est. Cost |
|------|-----|-----------|
| Whiffle balls, red (26-pack) | 1 | $10 |
| Whiffle balls, blue (26-pack) | 1 | $10 |
| Gold spray paint (for 5 bonus balls) | 1 can | $5 |
| Matte black spray paint (steel sheet) | 2 cans | $10 |
| Scoring number stickers/vinyl | 1 sheet | $5 |

### Timer (Option B)
| Item | Qty | Est. Cost |
|------|-----|-----------|
| Digital countdown timer (magnetic, battery) | 1 | $15 |

### **Estimated Total: $400–450**

---

## Build Sequence

### Phase 1: Frame & Board (Weekend 1, Day 1)
1. Cut plywood back panel to 48×60"
2. Cut galvanized steel sheet to match (tin snips or angle grinder)
3. Drill peg holes through both steel and plywood — ⅜" holes, 6" spacing, offset rows (~80 holes)
4. Screw steel sheet to plywood face (sheet metal screws around perimeter + a few in center)
5. Cut ⅜" steel rods into 3" peg segments (~80 pegs)
6. Press-fit or epoxy pegs through steel into plywood
7. Paint steel surface matte black (spray paint, 2 coats, let dry overnight)

### Phase 2: Edge Rails & Frame (Weekend 1, Day 2)
1. Cut 1×4 edge rails, attach to plywood/steel edges with screws
2. Build A-frame legs from 2×4, attach with hinges
3. Install cross brace, chain angle limiter, rubber feet
4. Mount side handles
5. Label all modular connection points
6. Test: stand the board up, verify stability at 20° tilt

### Phase 3: Hopper & Gate (Weekend 2, Day 1)
1. Build hopper box from ¾" plywood: 48"W × 6"H × 4"D
2. Hinge the bottom flap (full 48" width)
3. Install gate stop chain (limits to 90°)
4. Route pull-rope through eye hooks — rope hangs down the side within volunteer's reach
5. Mount hopper on top of playing field (screws into edge rail)
6. Add 1" front lip (acrylic strip or wood strip)
7. Test: load 55 balls, pull rope, verify clean release

### Phase 4: Scoring Bins (Weekend 2, Day 1)
1. Cut plywood dividers for 6 bins
2. Angle-cut for V-shaped troughs
3. Mount to bottom edge rail
4. Add 2" front lips to each bin
5. Build overflow trough below bins
6. Label scoring values with vinyl numbers
7. Test: pour balls from top, verify bins catch properly

### Phase 5: Deflectors & Game Pieces (Weekend 2, Day 2)
1. 3D-print 16 deflector wedges (8 red PLA, 8 blue PLA) — ~4 hour print
2. Epoxy magnets into recesses on each deflector (let cure 24hr)
3. Spray-paint 5 whiffle balls gold
4. Test deflector hold: stick to board, bounce a ball off it, verify it stays put
5. Test deflector removal: a kid-strength pull should pop it off cleanly

### Phase 6: Seal & Final Assembly (Weekend 2, Day 2)
1. Paint center divider line on steel surface
2. Drill acrylic for peg pass-throughs (match all peg holes)
3. Mount acrylic front panel onto pegs/edge rails
4. Seal all edges — balls must not escape during avalanche
5. Full playtest: load hopper, place deflectors, release, count scores
6. Verify reset cycle: sweep deflectors → scoop balls → reload → under 30 seconds

---

## Open Questions
- [ ] Steel rod peg press-fit vs epoxy vs welding — which holds best against repeated ball impacts?
- [ ] Optimal deflector magnet strength — strong enough to hold during avalanche, weak enough for kids to remove
- [ ] Do whiffle balls jam at hopper gate during mass release? May need a vibration motor or agitator bar
- [ ] Noise level — 55 whiffle balls on steel pegs may be LOUD. Feature or bug? (Feature.)
- [ ] Center divider: paint line only, or add a subtle physical ridge to prevent cross-contamination of deflector placement?
