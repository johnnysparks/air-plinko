# AIRFALL — Build Plan

## Concept

Two-player Waterfuls-inspired carnival game. Players aim cordless leaf blowers through ports at the base of a tall acrylic cabinet, blasting ultra-light ping pong balls upward onto scoring shelves at various heights. Balls hover, drift, cascade, and collide in the air streams — recreating the floating, drifting feel of the classic handheld water toy at 10x scale.

## Modes
- **Competitive:** Left shelves vs Right shelves — highest score wins
- **Cooperative:** Both players combine scores, beat a target number
- **Solo:** One blower, one player, beat your own high score

---

## Overall Dimensions

| Dimension | Size | Notes |
|-----------|------|-------|
| Width | 36" (3 ft) | Narrow enough for focused air columns, wide enough for two air streams to interact |
| Height | 72" (6 ft) | Tall cabinet — shelves span from 18" to 66" above the trough. Top shelf is a reach even for air |
| Depth (gap) | 8" | Ping pong balls (40mm / 1.6") need room to float and pass each other without constant jamming |
| Tilt angle | 0° — fully vertical | Vertical = balls fall straight down when air stops. No tilt needed — air does all the work |

Total footprint with frame: ~36"W × 30"D × 78"H (frame adds 6" above cabinet for signage bar)

---

## Architecture

### 1. Cabinet Frame & Walls

- **Back panel:** 36"W × 72"H sheet of ¾" plywood, painted matte black (high contrast for white/colored ping pong balls)
- **Front panel:** 36"W × 72"H clear acrylic sheet (¼" thick, shatter-resistant polycarbonate preferred). This is the viewing window — the crowd watches from here
- **Side panels:** Two 8"D × 72"H strips of ½" plywood, connecting front and back panels. Painted matte black interior
- **Top cap:** 36"W × 8"D plywood lid with ventilation holes (air must exit the top or pressure builds and balls won't rise). Covered with hardware cloth (¼" mesh) to prevent ball escape while allowing airflow
- **Bottom trough:** V-shaped channel at the base, 36" wide × 8" deep × 6" tall, angled toward center. Balls that fall or cascade collect here for re-launching by the blowers
- **Viewing height:** Bottom of the cabinet sits on a 12" riser platform so the trough is at waist height for kids (~30" from ground) and the blower ports are ergonomically accessible

### 2. Scoring Shelves (9 total)

Shelves are mounted to the back panel inside the cabinet. Each shelf is a small ledge with a front lip to hold balls.

- **Construction:** 3D-printed PLA trays OR cut from ¼" plywood with a ½" front lip strip glued on
- **Shelf depth:** 3" (from back panel) — enough to hold 2-3 ping pong balls per shelf
- **Shelf width varies by point value:**

| Shelf | Height from trough | Width | Points | Capacity |
|-------|-------------------|-------|--------|----------|
| Left/Right Low | 18" | 8" | 10 pts | 4-5 balls |
| Left/Right Mid | 30" | 6" | 25 pts | 3-4 balls |
| Left/Right Upper | 42" | 4" | 50 pts | 2-3 balls |
| Left/Right High | 54" | 3" | 75 pts | 1-2 balls |
| Top Center | 62" | 3" | 100 pts | 1-2 balls |

- **Shelf lip:** ½" tall front lip on each shelf. High enough that a resting ball stays put, low enough that a ball pushed by air can roll over the lip onto the shelf
- **Shelf angle:** Very slight backward tilt (2-3°) so balls that land tend to roll toward the back panel and settle, rather than rolling back off the front lip
- **Mounting:** Each shelf screws into the back panel from behind. Shelf positions are left-right symmetric except the top center 100-pointer
- **Trapdoor reset:** Each shelf has a hinged bottom panel operated by a pull-cable running down the back of the cabinet. Volunteer pulls a single handle → all trapdoors open → balls cascade to trough → release handle → trapdoors close via small return springs. One-pull reset

### 3. Blower Ports

Dead simple. A hole in the front panel. You stick the blower nozzle through it and aim.

- **Port holes:** Two 4" diameter holes through the front polycarbonate panel, positioned 8" from each side edge, at trough level (~6" above cabinet bottom). Cut with a hole saw at low RPM with masking tape
- **Brush seal ring:** Adhesive-backed brush strip weatherseal (the kind used for door bottoms, ~$4/roll at Home Depot) wrapped around the inside edge of each hole. The bristles compress around the blower nozzle, allowing it to pivot freely while blocking ping pong balls from escaping. Air passes through the bristles without resistance. A 40mm ping pong ball cannot push through a ring of compressed brush bristles
- **Ball screen backup:** A semicircle of ½" hardware cloth screwed to the inside face of the panel below each port hole. If a ball somehow gets past the brush seal, the mesh catches it. Belt and suspenders
- **Aim range:** The 4" hole with a ~2.5" blower nozzle gives about 45° of pivot in all directions. Player aims by physically moving the blower — up, down, left, right, angled. The blower nozzle pokes 2-3" into the cabinet. This IS the control mechanism. No gimbal, no socket, no 3D-printed anything. You grab the blower and steer
- **Why this works:** The M18 nozzle is tapered and smooth. It naturally self-centers in the hole. The brush seal provides just enough friction to keep air from leaking around the edges but zero resistance to movement. A kid can sweep the nozzle across the full range with one hand while squeezing the trigger with the other

### 4. Blower Tethers & Power

- **Blowers:** Two Milwaukee M18 blowers (model 0824-20 compact or 2724-20 full-size). If already owned, cost = $0. If purchasing, ~$80 each bare tool
- **Tether:** Each blower is attached to the frame via 3' retractable bungee tether (like a tool lanyard) clipped to the blower's belt hook. Prevents drops, keeps blowers at the station
- **Battery management:** M18 5.0Ah batteries last ~20 minutes of continuous use. At 60-second rounds with breaks, one battery lasts ~15-20 rounds. Keep two spare charged batteries at the booth. A M18 charger plugged in behind the booth keeps rotation going
- **Speed control:** The M18 blower has a variable-speed trigger. This IS the skill mechanic — trigger control is everything. Full blast sends balls everywhere. Controlled bursts place balls precisely. Players discover this naturally
- **No electricity required for blowers.** Battery-powered. The only outlet need is for the battery charger (optional, can pre-charge)

### 5. Ball Set

- **Standard balls:** 30 white ping pong balls (40mm, regulation 2.7g)
- **Bonus red balls:** 6 red ping pong balls (2x multiplier)
- **Bonus gold balls:** 4 gold ping pong balls (3x multiplier) — spray-painted or purchased
- **Total:** 40 balls in play
- **Why ping pong balls:** At 2.7 grams, they're light enough to hover in a 450 CFM air stream. They float, drift, and cascade exactly like the rings in a Waterfuls toy. Heavier balls (whiffle, golf practice) would need more air and fly less gracefully. Ping pong balls ARE the concept
- **Spare balls:** Keep a bag of 20 spares. Ping pong balls crack. Replace cracked ones between rounds — 3-second swap
- **Ball containment:** The sealed cabinet with mesh top cap prevents escapes. The blower ports are sealed by brush strip weatherseal that compresses around the nozzle — balls can't push through compressed bristles. Backup hardware cloth screens below each port catch anything that tries

### 6. Air Ventilation (Top)

- **Problem:** Two 450 CFM blowers push a LOT of air. If the cabinet is sealed, pressure builds instantly and balls won't rise — they'll just vibrate at the bottom
- **Solution:** The top cap has large ventilation openings covered by ¼" hardware cloth. Total open area: at least 200 sq inches (about half the top cap surface). Air exits freely, balls can't
- **Optional enhancement:** Side vent slots near the top of the side panels (covered with mesh) for additional airflow exit. Positioned above the highest shelf so rising balls can't escape through them
- **Turbulence benefit:** Air rising through the cabinet and exiting the top creates a natural upward current. Even without direct blower aim, there's a gentle background lift. This makes the "floating" effect more pronounced — balls drift and hover longer rather than dropping like stones when not in the direct air stream

### 7. Support Frame (Modular)

- **Base platform:** 36"W × 30"D sheet of ¾" plywood, raised on four 12" legs (4×4 posts). This elevates the cabinet to the right play height
- **Cabinet mounts:** The cabinet sits on the base platform and is bolted down with wing nuts (tool-free setup)
- **Rear bracing:** Two diagonal 2×4 braces from the base platform to the upper back of the cabinet. Prevents forward tipping when players lean into blower ports
- **Signage bar:** Horizontal 2×4 across the top, 6" above the cabinet, for hanging a banner/sign
- **Transport:** Cabinet lifts off base. Base folds (hinged legs). Two trips to the car, or one trip with a dolly
- **Fasteners:** Wing nuts + carriage bolts at all joints. No tools for setup

### 8. Timer & Feedback

- **Option A (cheap):** Volunteer phone timer, calls out countdown
- **Option B (better):** Battery-powered magnetic countdown timer ($15) stuck to the frame
- **Option C (best):** LED strip mounted along the top edge inside the cabinet. Runs on a $5 microcontroller + battery. Green for 60 sec → yellow at 15 sec → red at 5 sec → flashing at 0. Visible to players AND crowd. The light color change is the "time's almost up" cue that creates urgency

---

## Materials List

### Lumber & Sheet
| Item | Qty | Est. Cost |
|------|-----|-----------|
| ¾" plywood (4×8 sheet, cut for back panel + base + top) | 1 | $40 |
| ½" plywood (side panels, trough) | 1 (half sheet) | $20 |
| ¼" clear polycarbonate sheet (36×72 cut) | 1 | $90 |
| 4×4 posts (base legs, 12" each) | 1 (8ft, cut to 4) | $12 |
| 2×4 lumber (bracing, signage bar) | 2 (8ft) | $12 |
| ¼" plywood scraps (shelves if not 3D-printed) | — | $10 |

### Hardware
| Item | Qty | Est. Cost |
|------|-----|-----------|
| Wing nuts + carriage bolts (all joints) | 1 set | $15 |
| Wood screws (assorted) | 1 box | $8 |
| ¼" hardware cloth (top vent + port screens) | 3 ft roll | $10 |
| Small hinges (shelf trapdoors, 9×2) | 18 | $20 |
| Small extension springs (trapdoor return) | 9 | $10 |
| Braided steel cable + pull handle (reset system) | 15 ft | $12 |
| Cable ferrules and thimbles | 18 | $8 |
| Bungee tool tethers (3 ft, clip-on) | 2 | $12 |
| Rubber feet (base platform) | 4 | $6 |
| Gate handles (side-mounted for carry) | 2 | $12 |

### Blower Ports
| Item | Qty | Est. Cost |
|------|-----|-----------|
| Adhesive brush strip weatherseal (door bottom style) | 1 roll | $4 |
| ½" hardware cloth scraps (ball screen backup) | — | $0 (from vent roll) |

### Scoring Shelves (3D-Printed or Wood)
| Item | Qty | Est. Cost |
|------|-----|-----------|
| PLA filament (9 shelf trays) | ~300g | $8 |
| OR ¼" plywood + wood glue | — | $5 |

### Game Pieces
| Item | Qty | Est. Cost |
|------|-----|-----------|
| Ping pong balls, white (60-pack) | 1 | $8 |
| Ping pong balls, red (6-pack or spray paint) | 1 | $5 |
| Gold spray paint (for 4 bonus balls) | 1 can | $5 |

### Blowers (if not already owned)
| Item | Qty | Est. Cost |
|------|-----|-----------|
| Milwaukee M18 Compact Blower (0824-20, bare tool) | 2 | $160 |
| M18 5.0Ah batteries | 4 | $160 (or $0 if owned) |
| M18 charger | 1 | $40 (or $0 if owned) |

### Finish
| Item | Qty | Est. Cost |
|------|-----|-----------|
| Matte black spray paint (interior) | 2 cans | $10 |
| Scoring number vinyl stickers | 1 sheet | $5 |
| LED strip + microcontroller (timer, optional) | 1 | $15 |

### Estimated Total
- **If you own M18 blowers + batteries:** $330–380
- **If purchasing blowers + batteries:** $690–730

---

## Build Sequence

### Phase 1: Cabinet Box (Weekend 1, Day 1)
1. Cut back panel to 36×72" from ¾" plywood
2. Cut two side panels: 8"D × 72"H from ½" plywood
3. Cut top cap: 36"W × 8"D from ½" plywood. Cut ventilation opening (leave 2" frame border, cut center out). Staple ¼" hardware cloth over opening
4. Build V-shaped bottom trough from ½" plywood: 36" wide, 6" tall, angled sides meeting at center
5. Screw side panels to back panel edges
6. Mount trough at bottom
7. Mount top cap
8. Paint entire interior matte black (2 coats, dry overnight)

### Phase 2: Scoring Shelves & Reset System (Weekend 1, Day 2)
1. 3D-print 9 shelf trays (or cut from plywood + glue lips)
2. 3D-print 9 hinged trapdoor panels to fit each shelf bottom
3. Mount shelves to back panel at specified heights — mark positions from build diagram, pre-drill, screw from behind
4. Install small hinges on each shelf trapdoor
5. Attach extension springs for trapdoor return (closed = default)
6. Run braided cable from each trapdoor through eye hooks down the back of the cabinet to a single pull handle at the base
7. Test: pull handle → all trapdoors open → balls fall to trough → release → trapdoors close

### Phase 3: Blower Ports (Weekend 2, Day 1)
1. Cut two 4" holes in the front polycarbonate panel, 6" from bottom, 8" from each side edge (hole saw at low RPM with masking tape to prevent cracking)
2. Wrap adhesive brush strip weatherseal around the inside edge of each hole — bristles face inward
3. Cut two semicircles of ½" hardware cloth, screw to inside face of panel below each port as ball screen backup
4. Test: insert blower nozzle, sweep full range of motion, verify smooth pivot. Trim any brush bristles that snag
5. Test with blower on: verify air stream enters cabinet cleanly, no balls can escape through port

### Phase 4: Acrylic Front & Sealing (Weekend 2, Day 1)
1. Position acrylic front panel against side panel edges and bottom trough
2. Pre-drill through acrylic into side panels (go slow, use acrylic drill bit)
3. Screw acrylic to side panels and trough with pan-head screws + rubber washers (prevents cracking)
4. Seal all edges with clear silicone caulk — no gaps for ball or air escape
5. Verify top cap mesh is secure and no balls can escape
6. Drop 40 ping pong balls through the top (remove cap temporarily), replace cap, test containment

### Phase 5: Base Platform & Frame (Weekend 2, Day 2)
1. Cut base platform: 36"W × 30"D from ¾" plywood
2. Cut four 12" legs from 4×4 posts
3. Bolt legs to underside of platform with carriage bolts + wing nuts
4. Place cabinet on platform, bolt down with wing nuts through base into cabinet trough bottom
5. Cut and mount two diagonal 2×4 rear braces (base to upper cabinet back)
6. Mount side handles
7. Attach rubber feet to base legs
8. Cut and mount signage bar across the top

### Phase 6: Final Assembly & Test (Weekend 2, Day 2)
1. Attach bungee tethers to frame, clip to blowers
2. Spray-paint 4 gold balls, let dry
3. Load 40 balls into cabinet through top cap (temporarily remove mesh)
4. Secure top cap mesh
5. Full playtest: two players, blowers on, 60-second round
6. Verify: balls float and hover in air streams, balls land and stay on shelves, trapdoor reset works cleanly, balls don't escape through ports or vents
7. Tune shelf lip height if balls don't stay (add taller lips) or always stay (lower lips)
8. Verify battery life: run two full batteries through continuous play, note runtime
9. Apply vinyl scoring numbers to shelves

---

## Open Questions
- [ ] Exact M18 blower model — compact (0824-20) may not have enough CFM for the full 72" height. The 2724-20 full-size pushes 450 CFM but is heavier for small kids. Test both if possible
- [ ] Brush seal longevity — after 200+ rounds of nozzle pivoting, the bristles may flatten or the adhesive may peel. Bring a spare roll of brush strip ($4) for mid-carnival replacement if needed
- [ ] Noise level — two M18 blowers running simultaneously in a gym will be LOUD. This is a feature for the kids and a concern for the volunteers running adjacent booths. Position the game near the gym wall or in a corner to direct noise
- [ ] Ping pong ball cracking rate — balls hitting shelves and acrylic at speed may crack. With 20 spares and 3-second swaps this is manageable, but track the rate on carnival day
- [ ] Optimal ball count — 40 is a starting guess. Too few = not enough visual chaos. Too many = balls jam and pile rather than floating. Test with 30, 40, and 50 during play-testing
- [ ] Trapdoor cable routing — 9 trapdoors on one pull cable is mechanically complex. Simpler alternative: group into 3 cables (left shelves, right shelves, center shelf) with 3 pull handles. More volunteer effort but simpler mechanism
