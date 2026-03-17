# Thunder Drops — Festival Booth Build Plan

## Concept
Full-sensory storm-themed plinko. Glowing balls launch through fog into a blacklit chime-filled peg field, cascade into candy-dispensing scoring buckets, while mist jets and bass thunder hit the players. All five senses engaged.

## Modes
- **Competitive:** Player vs player — highest score wins
- **Cooperative:** Combined score vs. weather thresholds (Drizzle: 500, Storm: 1000, Hurricane: 2000)

---

## Overall Dimensions

| Dimension | Size | Notes |
|-----------|------|-------|
| Board width | 48" (4 ft) | Two-player side-by-side |
| Board height | 72" (6 ft) | Taller than original — more peg rows, more chaos |
| Depth (gap) | 5" | Ball travel zone between back panel and acrylic |
| Tilt angle | ~20° from vertical | Gravity return, good ball cascade speed |
| Peak height (mounted) | ~84" (7 ft) | Top of board on frame — fog zone visible from distance |
| Fog canopy overhang | 12" forward | Shelf above board holding fog machine + blacklights |

Total footprint with frame legs: ~54"W × 42"D × 84"H

---

## Architecture

### 1. Frame & Playing Field

- **Back panel:** 4×6 ft sheet of ¾" plywood, painted matte black (UV-reactive paint splatters optional for cosmic storm vibe)
- **Front panel:** 4×6 ft clear acrylic sheet (¼" thick), mounted with wing nut spacers for tool-free removal
- **Peg grid:** Cedar dowels (¾" diameter, 4" long) in offset plinko rows, ~5.5" spacing. 11 columns × 14 rows = ~154 pegs. Cedar chosen for natural scent release under blacklight warmth
- **Mushroom caps:** 3D-printed UV-reactive neon caps (pink, green, yellow, blue) press-fit onto cedar dowel tips. Alternating colors per row. Caps are 1.5" diameter hemispheres — catch the light, increase ball deflection randomness
- **Edge rails:** 1×6 lumber on all four sides, painted matte black, sandwiched between plywood and acrylic
- **Tilt frame:** Rear A-frame legs (2×4), hinged at top, chain angle limiter. Same modular bolt-together design as original Air Plinko

### 2. Fog Canopy & Blacklight Array

- **Canopy shelf:** 48"W × 12"D plywood shelf mounted on top of the board frame, extending forward
- **Fog machine:** 400W fog machine ($25-35), mounted on canopy shelf behind a 3" lip. Aimed to roll fog DOWN across the top third of the board front
- **Fog fluid:** Standard glycol/glycerin fog juice. Add 2-3 drops petrichor essential oil to the fluid reservoir for rain scent
- **Blacklight strips:** Two 24" UV LED strip lights ($12 each), mounted on the underside of the canopy shelf, angled down at the board. Everything UV-reactive glows
- **Canopy drape:** Black fabric draped from canopy edges to create a "storm cloud" visual frame. Cheap black tablecloths work great

### 3. Crank Catapult Launcher (×2)

- **Mechanism:** Spring-loaded lever arm with a ratcheting crank handle
  - Base: 12"×8" plywood platform, bolted to the main frame's bottom rail
  - Lever arm: 14" piece of 1×2 hardwood, pivot-bolted at one end
  - Spring: Screen door closer spring ($4) connecting lever arm to base — provides launch tension
  - Ratchet: Simple pawl-and-gear from a ratchet strap mechanism — holds the arm in cranked position until release lever is pulled
  - Ball cup: 3D-printed hemisphere cradle glued to the free end of the lever arm
  - Release lever: Small handle/trigger that lifts the pawl. Pull to fire
- **Crank handle:** Textured rubber grip (bicycle handlebar grip, $3) on a crank arm that tensions the spring through a simple cam or winding spool
- **Launch channel:** Ball cup snaps upward, ball enters a short 3" PVC guide tube that aims it into the bottom of the playing field at ~70° angle
- **Ball magazine:** Gravity-fed PVC tube (2" diameter, 24" tall) holding 10 balls, positioned above the launch cup. After each launch, next ball drops into the cup via gravity gate

### 4. Wind Chime Peg Array

- **Chime pegs:** Every 3rd row (rows 3, 6, 9, 12), the cedar pegs also have a small aluminum wind chime tube attached
- **Chime construction:** 3" aluminum tube segments (from a $15 wind chime set, disassembled) zip-tied or wire-attached to the side of select pegs
- **Tuning:** Different length tubes = different pitches. Arrange so upper rows are higher pitched, lower rows deeper. Ball cascade creates a descending scale
- **Count:** ~40 chime pegs across 4 chime rows (10 per row)

### 5. LED Lightning System

- **LED strips:** WS2812B addressable LED strip (one 5m roll, $15), adhered to the back of the back panel in a zigzag pattern. Light bleeds through drilled holes and around peg mounts
- **Trigger:** Arduino Nano ($8) connected to 6 piezo vibration sensors glued to the back of the back panel at strategic peg locations
- **Behavior:** When a ball hits a sensor peg, the Arduino fires a quick 200ms white flash pattern across a section of LEDs — mimics lightning
- **Jackpot flash:** When the center scoring bucket's sensor triggers, ALL LEDs strobe gold for 2 seconds
- **Ambient mode:** Slow blue/purple breathing pattern between ball hits — "distant lightning" ambiance
- **Power:** 5V USB power bank or 5V/3A wall adapter

### 6. Scoring Buckets & Candy Dispensers

- **Buckets:** 7 angled slots cut into a bottom rail, each sized per scoring table. Lined with foam to dampen ball impact sound (so the chimes remain the dominant audio)
- **Candy tubes:** Behind each bucket, a 2" PVC tube rises vertically to a gravity-fed candy hopper at the back of the board
- **Dispensing mechanism:** Ball lands in bucket → rolls onto a simple lever/seesaw → lever tips → releases one candy from the hopper tube into a front-facing chute at player height
  - The ball's weight IS the trigger mechanism — no electronics needed for candy dispensing
  - Lever resets via counterweight when ball rolls off into the return trough
- **Candy chute:** Angled PVC half-pipe from the dispenser to a collection cup at each player station. Candy slides down to the player
- **Hopper capacity:** Each tube holds ~20 pieces. Refill from the back between rounds
- **Jackpot chute:** Center bucket's tube is larger (3" PVC) to accommodate full-size bars. Has a longer lever arm for the heavier candy

### 7. Mist Jet System

- **Mister nozzles:** Two adjustable garden misting nozzles ($5 each), mounted on gooseneck arms at each player station, aimed at chest/face height
- **Water supply:** 1-gallon garden sprayer (pump-pressurized, $12) mounted behind the board. Pressurize before each session
- **Solenoid valves:** 12V normally-closed solenoid valves ($8 each) inline on each mist line
- **Trigger:** Wired to the Arduino — scoring bucket piezo sensor fires → Arduino opens solenoid for 0.5s (standard hit) or 2s (jackpot)
- **Scent:** 5-10 drops of eucalyptus or pine essential oil added to the water reservoir. Subtle forest-rain smell on every mist hit
- **Drainage:** Player stations have a slatted wood floor over a shallow drip tray. Keeps footing safe

### 8. Sound System

- **Subwoofer:** Used car subwoofer (6.5" or 8") mounted behind the back panel in a sealed box. Powered by a cheap $20 amp board
- **Thunder sound:** Pre-recorded thunder crack WAV file triggered by Arduino on jackpot hits. Played through the sub — you FEEL this
- **Ambient track:** Small bluetooth speaker ($15) mounted on the canopy. Plays a looping thunderstorm ambiance track (rain, distant rumbles, wind)
- **Bucket sounds:** Arduino triggers different pitched tones through a small piezo buzzer per bucket hit. Or route through the bluetooth speaker via audio module
- **Sad rain sound:** Gutter hits play a descending "drip drip drip" through the speaker

### 9. Ball Return System

- **Collection trough:** Angled channel at the bottom of the playing field (below scoring buckets), funnels all balls to center
- **Rear chute:** Balls drop through the bottom trough into a tube behind the board
- **Return track:** Angled PVC half-pipe behind the board routes balls back to each player's magazine hopper
- **Divider:** Center split sends balls to alternating sides, keeping magazines roughly balanced
- **Overflow bin:** If magazines are full, excess balls drop into a catch bucket at the base

---

## Materials List

### Lumber & Sheet
| Item | Qty | Est. Cost |
|------|-----|-----------|
| ¾" plywood sheet (4×6 cut) | 1 | $42 |
| ¼" clear acrylic sheet (4×6 cut) | 1 | $100–140 |
| 1×6 lumber (edge rails, 20 lin. ft) | 3 (8ft) | $24 |
| ¾" cedar dowels (36" length) | 14 | $42 |
| 2×4 lumber (frame/legs/canopy) | 4 (8ft) | $24 |
| 1×2 hardwood (launcher arms) | 1 (4ft) | $6 |
| Scrap plywood (launcher bases, canopy shelf, drip trays) | — | $15 |

### Hardware
| Item | Qty | Est. Cost |
|------|-----|-----------|
| Bolts, wing nuts, carriage bolts (modular joints) | — | $20 |
| Wood screws (assorted) | 1 box | $8 |
| Hinges (for frame legs) | 2 | $8 |
| Chain (angle limiter) | 1 | $8 |
| Heavy-duty handles (side-mounted) | 2 | $12 |
| Rubber feet caps | 4 | $6 |
| Screen door closer springs (launcher) | 2 | $8 |
| Ratchet strap ratchet mechanisms (launcher pawl) | 2 | $10 |
| Bicycle handlebar grips (crank handles) | 2 | $6 |

### Sensory — Fog & Light
| Item | Qty | Est. Cost |
|------|-----|-----------|
| 400W fog machine | 1 | $30 |
| Fog fluid (1 qt) | 1 | $8 |
| 24" UV LED strip lights | 2 | $24 |
| WS2812B addressable LED strip (5m) | 1 | $15 |
| Arduino Nano clone | 1 | $8 |
| Piezo vibration sensors | 8 | $8 |
| 5V USB power bank or wall adapter | 1 | $12 |
| Black tablecloths (canopy drape) | 2 | $6 |

### Sensory — Sound
| Item | Qty | Est. Cost |
|------|-----|-----------|
| Used car subwoofer (6.5"–8") | 1 | $15 |
| Amp board (TPA3116 or similar) | 1 | $12 |
| Bluetooth speaker (ambient track) | 1 | $15 |
| Speaker wire | 10 ft | $4 |

### Sensory — Touch & Smell
| Item | Qty | Est. Cost |
|------|-----|-----------|
| Garden misting nozzles | 2 | $10 |
| 1-gallon pump sprayer | 1 | $12 |
| 12V solenoid valves (normally closed) | 2 | $16 |
| Gooseneck mister arms | 2 | $8 |
| Petrichor/eucalyptus essential oil | 1 bottle | $8 |
| Drip tray materials (plastic sheeting) | — | $6 |

### Sensory — Taste (Candy System)
| Item | Qty | Est. Cost |
|------|-----|-----------|
| 2" PVC pipe (candy tubes, 3ft each) | 7 | $21 |
| 3" PVC pipe (jackpot tube) | 1 | $5 |
| PVC half-pipe (candy chutes) | 2 | $6 |
| Small lever hinges (seesaw dispensers) | 7 | $14 |
| Candy (bulk — Jolly Ranchers, fun-size bars, gummy packs) | — | $40 |
| Full-size candy bars (jackpot prizes) | 12 | $15 |

### Wind Chimes
| Item | Qty | Est. Cost |
|------|-----|-----------|
| Wind chime sets (to disassemble for tubes) | 3 | $15 |
| Zip ties / wire | 1 bag | $4 |

### Game Pieces & Finish
| Item | Qty | Est. Cost |
|------|-----|-----------|
| UV-reactive whiffle balls (or paint standard ones) | 24 | $15 |
| UV-reactive spray paint (pegs, accents) | 3 cans | $18 |
| Matte black spray paint (frame, back panel) | 2 cans | $10 |
| UV-reactive neon acrylic paint (peg caps) | 4 colors | $12 |

### 3D Printed Parts
| Item | Qty | Est. Cost (filament) |
|------|-----|-----------|
| Mushroom cap peg toppers (1.5" dia) | 154 | $15 |
| Ball cup cradles (launcher) | 2 | $2 |
| Textured "storm ball" shells (optional) | 6 | $4 |

### **Estimated Total: $750–850**

*About 2× the original Air Plinko budget. The sensory systems (fog, lights, sound, mist, candy) add ~$350 over a basic plinko build. Most items are one-time purchases reusable year over year. Candy is the only consumable (~$55/event, refillable).*

---

## Build Sequence

### Phase 1: Frame, Board & Pegs (Weekend 1, Day 1)
1. Cut plywood to 48×72"
2. Paint back panel matte black. While drying, add UV-reactive paint splatters (optional cosmic storm effect)
3. Cut edge rails from 1×6, attach to plywood edges
4. Mark peg grid: 11 columns × 14 rows, 5.5" offset spacing. Drill ¾" holes
5. Cut 154 cedar dowels to 4" length. Sand ends
6. Insert and glue cedar pegs into back panel. Room should smell amazing
7. Press-fit 3D-printed neon mushroom caps onto peg tips
8. Build A-frame legs (2×4), attach with hinges and carriage bolts + wing nuts
9. Mount side handles. Label all joints for reassembly

### Phase 2: Scoring Buckets & Candy System (Weekend 1, Day 2)
1. Cut 7 scoring bucket slots into bottom edge rail — widths per scoring table (3" to 6")
2. Build lever/seesaw dispensers behind each bucket slot. Test: drop a ball → lever tips → releases candy
3. Mount vertical PVC candy tubes behind the board, one per bucket. Load test candy
4. Build candy chutes (PVC half-pipe) from dispensers to front-facing collection cups
5. Build ball return trough below buckets — angled channel to center
6. Build rear return chute (PVC) routing balls back to magazine hoppers
7. Build ball magazines (2" PVC, 24" tall) at each launcher position
8. Full ball-flow test: launch position → field → bucket → candy drops + ball returns to magazine

### Phase 3: Launchers (Weekend 2, Day 1)
1. Build launcher base platforms (12"×8" plywood each)
2. Mount lever arms on pivot bolts
3. Attach screen door springs (tension mechanism)
4. Install ratchet pawl mechanisms — test crank-and-hold
5. Glue 3D-printed ball cups to lever arm ends
6. Build short PVC guide tubes from launcher to field entry point
7. Attach bicycle grip handles to crank arms
8. Tune: 3 cranks = low launch, 5 cranks = mid, 7+ cranks = overshoot. Adjust spring tension as needed

### Phase 4: Sensory Systems (Weekend 2, Day 2)
1. **Chimes:** Disassemble wind chime sets. Cut tubes to graduated lengths. Zip-tie to every 3rd row pegs (rows 3, 6, 9, 12). Test cascade sound with test balls
2. **LEDs:** Adhere WS2812B strip to back panel in zigzag. Drill light-bleed holes near sensor pegs. Wire to Arduino Nano. Program flash patterns (200ms lightning, 2s jackpot strobe, slow ambient breathing)
3. **Piezo sensors:** Glue 6 sensors to back panel behind key pegs + scoring buckets. Wire to Arduino. Calibrate sensitivity
4. **Fog machine:** Mount on canopy shelf. Aim downward. Test fog flow — should roll across top third of board. Add petrichor oil to fluid
5. **Blacklights:** Mount UV strips under canopy shelf, angled at board. Test UV ball glow, peg cap glow, paint glow
6. **Canopy drape:** Attach black tablecloths from canopy edges. Frame the "storm cloud" visual
7. **Subwoofer:** Mount behind back panel in sealed box. Wire to amp board. Load thunder crack WAV on Arduino SD module or use a dedicated audio trigger board (Adafruit Audio FX, $20). Test — should rattle your chest
8. **Bluetooth speaker:** Mount on canopy. Pair with phone. Queue thunderstorm ambiance loop
9. **Mist jets:** Mount gooseneck nozzles at player stations. Plumb to pump sprayer with solenoid valves inline. Wire solenoids to Arduino (via relay module). Add essential oil to water. Test spray on scoring hit

### Phase 5: Seal, Test & Tune (Additional afternoon)
1. Drill acrylic front panel to match peg holes
2. Mount acrylic with wing-nut spacers (tool-free removal for maintenance)
3. Seal all edges — no ball escapes
4. Build drip trays under player stations, cover with slatted wood
5. Full integration test: launch balls → fog → chimes → lightning → scoring → candy → mist → thunder → ball return
6. Tune the experience: fog density, mist duration, lightning sensitivity, candy weight calibration
7. Night test: kill the lights, blacklights on, fog on. Verify the glow. Adjust

---

## Power Requirements
- Fog machine: 400W (standard outlet)
- LED strip + Arduino: 5V/3A (USB power bank or wall adapter)
- Subwoofer amp: 12V/3A (wall adapter or car battery)
- Solenoid valves: 12V (share amp power supply with relay board)
- Bluetooth speaker: Battery (charge before event)
- **Total: 1–2 standard outlets + 1 power bank**

## Transport & Setup
- Same modular wing-nut design as original Air Plinko
- Canopy shelf detaches (4 bolts)
- Fog machine, speaker, and pump sprayer are loose items — pack in a milk crate
- Candy tubes are PVC press-fit — disassemble for transport
- All electronics (Arduino, amp, LED strip) stay mounted to the back panel
- Setup time: ~45 minutes for two people (frame assembly + plug in sensory systems)
- Teardown: ~30 minutes

## Open Questions
- [ ] Festival date — drives build timeline
- [ ] Power availability — need 2 outlets minimum
- [ ] Candy budget per event (estimate ~200 pieces per session = $40-55)
- [ ] Water source for mist jets (1 gallon lasts ~2 hours of play)
- [ ] Fog machine outdoor wind tolerance — may need wind screen on canopy
- [ ] Local regulations on fog machines at school events
- [x] Transport plan — modular design, same as original
