# Mega Pinball Plinko — Build Plan

## Overall Dimensions

| Dimension | Size | Notes |
|-----------|------|-------|
| Width | 48" (4 ft) | Two flippers side-by-side at bottom |
| Height | 72" (6 ft) | Tall enough to be impressive, playable for kids standing |
| Depth (gap) | 4" | Whiffle ball (2.75") + bounce clearance |
| Tilt angle | ~20° from vertical | Keeps balls moving but controllable with flippers |
| Footprint with legs | 48"W × 40"D × 72"H | A-frame rear support legs |

---

## Architecture

### 1. Cabinet / Playfield Box
- **Back panel:** 4×6 ft sheet of ¾" plywood — the main playfield surface
- **Front panel:** 4×6 ft clear acrylic sheet (¼" thick) — lets crowd see the action
- **Edge rails:** 1×4 lumber on all four sides, sandwiched between plywood and acrylic, forming the 4" deep playing box
- **Top rail gap:** 2" gap in the top-right corner for the launch lane exit
- **Bottom rail gap:** 5" gap in the bottom-center for the drain slot (between flippers)
- **Paint:** Back panel painted matte black with neon zone markings (UV-reactive paint optional for black-light mode)

### 2. Support Frame (Modular)
- **Rear legs (×2):** 2×4 lumber, 60" long, hinged at the top of the back panel for fold-flat transport
- **Cross brace:** 2×4 horizontal between legs at 24" height
- **Angle limiter:** Adjustable chain between legs and back panel — sets 20° tilt
- **Base feet:** Rubber-capped 2×4 pads on rear legs
- **Side handles (×2):** Heavy-duty gate handles on the cabinet sides for two-person carry
- **All joints:** Carriage bolts + wing nuts for tool-free setup/teardown

### 3. Peg Field
- **Pegs:** ¾" wooden dowels, 3" long, inserted into drilled holes in the back panel
- **Layout:** Offset grid pattern (plinko style), covering the center ~60% of the playfield
- **Rows:** 12 rows, ~5" vertical spacing, offset every other row by 2.5"
- **Columns:** 7-8 pegs per row
- **Zone:** Pegs span from ~18" above bottom rail to ~12" below top rail
- **Color:** Alternating neon green, neon pink, neon orange spray paint

### 4. Flippers (×2)

This is the heart of the game. Each flipper is a mechanical lever system.

- **Paddle:** 14" long × 3" wide piece of ¾" hardwood (maple or oak for durability), rounded at the tip, shaped like a real pinball flipper
- **Pivot:** Heavy-duty ½" bolt through the back panel, with bushings for smooth rotation. Left flipper pivot at bottom-left (12" from left edge, 8" up from bottom). Right flipper pivot at bottom-right (12" from right edge, 8" up from bottom)
- **Rest angle:** ~30° below horizontal (angled down toward drain)
- **Flip angle:** ~30° above horizontal (angled up to hit ball)
- **Total swing:** ~60° of rotation
- **Return spring:** Heavy bungee cord or extension spring — pulls flipper back to rest position when released
- **Actuation:** Each flipper connects via steel cable (bike brake cable) to an external lever/handle mounted on the bottom edge rail. Player PULLS the lever → cable pulls the flipper tail → paddle swings UP. Release → spring snaps it back DOWN
- **Lever handle:** 8" wooden handle (broom handle section) mounted on a pivot bracket on the outside of the cabinet. Ergonomic for kid-sized hands
- **Stop bolts:** Bolts on the back panel at the rest and flip positions to limit rotation range and prevent over-swing
- **Flipper gap (drain):** 5" gap between the two flipper tips at rest position — balls that slip through are drained

### 5. Spring Bumpers (×4)

- **Location:** Diamond pattern in the upper third of the playfield (above the peg field)
  - Top bumper: center, 8" below top rail
  - Left bumper: 14" from left, 16" below top rail
  - Right bumper: 14" from right, 16" below top rail
  - Bottom bumper: center, 24" below top rail
- **Construction:**
  - Base plate: 3" diameter wooden disc, screwed to back panel
  - Spring: 2" compression spring (medium-stiff), mounted vertically on the base plate center bolt
  - Cap: 3D-printed mushroom cap (3.5" diameter dome), sits on top of the spring with a guide bolt through the center
  - When a ball hits the cap, the spring compresses and rebounds, launching the ball away
- **Bumper ring:** Wrap each bumper base in a ring of bright rubber (cut from a bike inner tube) for ball grip and visual pop

### 6. Loop Ramp (×1)

- **Location:** Left side of the playfield, entrance at ~30" up from bottom, exit at ~54" up (re-enters ball at top of peg field)
- **Construction:** 4" wide PVC pipe cut in half lengthwise (half-pipe), bent into a sweeping J-curve
- **Path:** Ball enters from the center heading left → ramp curves up along the left edge → arcs over and deposits ball at the top-center of the playfield
- **Mounting:** PVC brackets screwed to back panel, half-pipe sits inside the playing gap
- **Ramp lip:** Small 3D-printed lip at entrance to funnel ball in cleanly

### 7. Spinner Target (×1)

- **Location:** Top-center of playfield, 6" below top rail
- **Construction:** 6" diameter 3D-printed disc with alternating colored wedges (red/yellow/blue/green), mounted on a bearing bolt so it spins freely
- **Action:** Ball hits an arm/vane extending from the disc → disc spins wildly. Visual spectacle for spectators
- **Bearing:** Skateboard bearing pressed into a 3D-printed housing, bolted to back panel

### 8. Jackpot Hole (×1)

- **Location:** Top-center, directly behind the spinner target (ball must get past the spinner)
- **Construction:** 3.5" hole drilled through the back panel with a funnel collar (3D-printed). Ball drops through the hole, rolls down a chute behind the board, and into a separate "JACKPOT" collection bin
- **Visual:** Ringed with reflective tape or LEDs (battery-powered LED strip)

### 9. Launch Lane

- **Location:** Right side of the playfield, running vertically from bottom-right to top-right
- **Construction:** 4" wide channel formed by a strip of ¼" plywood screwed to the back panel, creating a walled lane against the right edge rail
- **Plunger:** Standard pinball plunger assembly (~$8) mounted through the bottom edge rail, aligned with the launch lane
- **Lane exit:** Ball exits the lane at the top-right through a curved lip that directs it left into the top of the playfield
- **Ball feed:** Gravity-fed magazine (angled PVC pipe) above the plunger chamber. Holds 5 balls. After launch, next ball drops into the chamber automatically

### 10. Scoring Lanes (Bottom)

- **Location:** Bottom of the playfield, between and outside the flippers
- **Layout:** 5 lanes separated by 3D-printed dividers:

```
|  10  |  25  |  100  |  25  |  10  |
|      |      |       |      |      |
====LEFT FLIPPER====   ====RIGHT FLIPPER====
         [ DRAIN - 0 pts ]
```

- **Lane dividers:** Thin plywood strips (¼" × 3" tall) angled slightly to funnel balls, screwed to the back panel
- **Each lane:** Funnels into a hole through the back panel → ball rolls down a collection chute behind the board
- **Center lane (100 pts):** Narrowest (3" wide), directly above the drain gap
- **Inner lanes (25 pts):** 4" wide, flanking center
- **Outer lanes (10 pts):** 5" wide, near the edges

### 11. Ball Return / Collection

- **Drain + scoring lane balls:** All exit through holes in the back panel into chutes
- **Rear collection:** Angled plywood tray behind the back panel funnels all balls to a single collection bin at the bottom
- **Reload:** Between rounds, operator dumps the collection bin back into the ball magazine
- **Jackpot balls:** Separate bin (for visual confirmation of jackpot hits)

---

## Materials List

### Lumber & Sheet
| Item | Qty | Est. Cost |
|------|-----|-----------|
| ¾" plywood sheet (4×6 cut) | 1 | $45 |
| ¼" clear acrylic sheet (4×6 cut) | 1 | $100–140 |
| 1×4 lumber (edge rails, 20 lin. ft) | 3 (8ft) | $21 |
| ¾" wooden dowels (36" length) | 12 | $24 |
| 2×4 lumber (frame legs, cross brace) | 3 (8ft) | $18 |
| ¾" hardwood board (flippers, 1×4×3ft) | 1 | $12 |
| ¼" plywood scraps (lane dividers, launch lane wall, rear chutes) | 1 sheet | $15 |

### Hardware
| Item | Qty | Est. Cost |
|------|-----|-----------|
| ½" bolts + bushings (flipper pivots) | 2 sets | $12 |
| Bike brake cables + housings | 2 | $10 |
| Bungee cords or extension springs (flipper return) | 2 | $8 |
| Compression springs (bumpers, 2" medium) | 4 | $12 |
| Skateboard bearings (spinner) | 1 | $4 |
| Pinball plunger assembly | 1 | $8 |
| Hinges (frame legs) | 2 | $8 |
| Chain (angle limiter) | 4 ft | $8 |
| Heavy-duty handles | 2 | $12 |
| Carriage bolts + wing nuts | 1 set | $15 |
| Wood screws (assorted) | 1 box | $8 |
| Rubber feet caps | 4 | $6 |

### 3D-Printed Parts
| Item | Qty | Notes |
|------|-----|-------|
| Bumper mushroom caps | 4 | 3.5" dome, guide hole center |
| Spinner disc + vanes | 1 | 6" diameter, bearing housing |
| Jackpot funnel collar | 1 | 3.5" ID funnel |
| Ramp entrance lip | 1 | Funnel for loop ramp entry |
| Scoring lane dividers | 4 | Thin angled guides |

### Game Pieces & Finish
| Item | Qty | Est. Cost |
|------|-----|-----------|
| Whiffle balls (neon colors) | 12 pack | $8 |
| Spray paint (neon green, pink, orange, matte black) | 5 cans | $25 |
| Reflective tape (jackpot ring) | 1 roll | $5 |
| PVC pipe 4" (loop ramp, cut in half) | 4 ft | $8 |
| PVC pipe 3" (ball magazine) | 2 ft | $4 |
| Adhesive vinyl numbers/letters (scoring) | 1 sheet | $5 |
| Bike inner tubes (bumper rings) | 2 | $4 |

### **Estimated Total: $450–500**

---

## Build Sequence

### Phase 1: Cabinet & Frame (Weekend 1, Day 1)
1. Cut plywood back panel to 48×72"
2. Cut 1×4 edge rails — 2 at 72" (sides), 2 at 48" (top/bottom)
3. Leave gaps: 2" at top-right for launch lane exit, 5" at bottom-center for drain
4. Attach edge rails to plywood with wood screws (forms the box walls)
5. Build A-frame rear legs from 2×4, attach with hinges + carriage bolts
6. Add cross brace, chain angle limiter, rubber feet
7. Mount side carry handles
8. Paint back panel matte black, let dry

### Phase 2: Flippers & Plunger (Weekend 1, Day 2)
1. Cut and shape two flipper paddles from ¾" hardwood — 14" long, rounded tips
2. Drill ½" pivot holes in flippers and back panel at flipper positions
3. Install pivot bolts with bushings — test that flippers swing freely
4. Mount stop bolts for rest position (~30° below horizontal) and flip position (~30° above horizontal)
5. Attach bungee cord return springs (flipper tail to back panel)
6. Build external lever handles — broom handle sections on pivot brackets, mounted on bottom edge rail
7. Run bike brake cables from lever handles through cable housings to flipper tails
8. Test flipper action: pull lever → flipper swings up → release → snaps back
9. Install pinball plunger in bottom-right edge rail, aligned with launch lane position

### Phase 3: Playfield Features (Weekend 2, Day 1)
1. Drill peg holes — offset grid, 12 rows, ~84 holes total
2. Cut dowels to 3" lengths, paint alternating neon colors, let dry
3. Glue pegs into holes (wood glue + friction fit)
4. Build launch lane: ¼" plywood wall strip along right edge, creating 4" channel
5. Build ball magazine: angled 3" PVC pipe section above plunger, holds 5 balls
6. Cut 4" PVC pipe in half for loop ramp, heat-bend into J-curve
7. Mount loop ramp with PVC brackets on left side of playfield
8. Print and install 3D parts: bumper caps, spinner disc, jackpot funnel, ramp lip
9. Assemble spring bumpers: base disc → spring → guide bolt → mushroom cap. Mount at 4 positions
10. Mount spinner on skateboard bearing at top-center
11. Drill jackpot hole at top-center, install funnel collar

### Phase 4: Scoring & Finish (Weekend 2, Day 2)
1. Install scoring lane dividers at bottom of playfield (5 lanes)
2. Drill ball exit holes through back panel at each scoring lane + drain
3. Build rear collection chute from ¼" plywood — angled tray funneling to collection bin
4. Separate jackpot chute to its own bin
5. Mark scoring values with vinyl numbers on back panel
6. Paint scoring lane zones in different colors
7. Apply neon accents and reflective tape to jackpot ring
8. Drill acrylic front panel — match peg holes (pegs pass through acrylic for structural support)
9. Mount acrylic front panel onto edge rails
10. Final test: launch balls, test flipper action, check bumper bounce, verify all balls drain properly
11. Play 10 test rounds, adjust spring tensions and flipper geometry as needed

### Phase 5: Game Day Prep
1. Label all modular joints for easy reassembly
2. Pack: cabinet + acrylic (front panel removed), legs fold flat, hardware bag
3. Setup time target: 15 minutes with 2 people
4. Bring: spare balls, spare springs, Milwaukee impact driver for emergency adjustments

---

## Open Questions
- [ ] Flipper spring tension — needs playtesting to find the sweet spot between "too easy" and "impossible"
- [ ] Ball magazine capacity — 5 might not be enough for a satisfying round, consider 8
- [ ] Bumper spring stiffness — too soft = no bounce, too stiff = ball flies off playfield
- [ ] Lighting — battery-powered LED strip around the perimeter would make it POP at evening events
- [ ] Sound — optional: small Bluetooth speaker playing pinball machine sound effects
- [ ] Acrylic vs. polycarbonate — polycarb is more impact-resistant but scratches easier
