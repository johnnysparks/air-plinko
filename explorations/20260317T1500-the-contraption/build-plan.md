# THE CONTRAPTION — Build Plan

## Concept
A 4×6 ft vertical game board where every interaction point is a unique 3D-printed mechanism. Two players crank Archimedes screw lifts to launch balls into a Rube Goldberg plinko wonderland of spinning wheels, pendulum gates, gear ratchets, trap doors, funnel spirals, and two centrepiece showstoppers (The Octopus and The Volcano). Balls from both players share the same mechanisms, creating cross-player chaos. Modular bolt-on design means mechanisms are hot-swappable.

---

## Overall Dimensions

| Dimension | Size | Notes |
|-----------|------|-------|
| Board Width | 48" (4 ft) | Two-player side-by-side |
| Board Height | 72" (6 ft) | Tall to fit all mechanism tiers |
| Depth (gap) | 6" | Extra depth for spinning wheels and gear mechanisms |
| Tilt angle | ~20° from vertical | Gravity drives balls through mechanisms |
| Peak height on frame | ~84" (7 ft) | Top of board when tilted |
| Footprint with legs | 48"W × 40"D × 84"H | Needs clearance for crank operators |

---

## Architecture

### 1. Frame & Playing Field

#### Back Panel
- **Material:** ¾" plywood, 48×72" (two 4×4 sheets joined or one 4×8 sheet cut down)
- **Finish:** Matte black paint — makes neon mechanisms POP
- **Mounting grid:** Pre-drill a 6" grid of M6 bolt holes across the entire board. This is the universal mounting pattern for all 3D-printed mechanisms. Each mechanism uses 4 bolts on a 4×4" square from this grid
- **Hole layout:** 7 columns × 11 rows = 77 mounting positions. Not all will be used — the grid provides layout flexibility

#### Front Panel
- **Material:** ¼" clear acrylic sheet, 48×72"
- **Mounting:** Bolts through at the edges and at select mechanism locations (mechanisms that protrude through both panels)
- **Access panels (×2):** Cut two 12×12" hinged access doors in the acrylic at mid-height, left and right sides. These allow quick mechanism swaps and ball jam clearing without removing the whole front panel. Use small cabinet hinges + magnetic catches

#### Edge Rails
- **Material:** 1×8 lumber (7.25" actual width matches the 6" gap + panel thicknesses)
- **All four sides:** Screwed to plywood edges, acrylic bolts to the front face of the rails
- **Bottom rail:** Has two 3" holes for ball returns — balls exit the playing field into collection troughs

#### Support Frame
- **Rear legs (×2):** 2×4 lumber, 72" long, hinged at top for fold-flat storage
- **Cross brace:** 2×4 at 30" height between legs
- **Angle limiters:** Chain + turnbuckle between legs and back panel — sets 20° tilt
- **Base feet:** Rubber caps, wide stance for stability on grass
- **Handles (×2):** Heavy-duty rope handles on each side of the board
- **All joints:** Carriage bolts + wing nuts — tool-free setup/teardown

### 2. Ball Launcher System — Archimedes Screw Cranks (×2)

The signature launcher. Each player operates a hand crank that drives a 3D-printed Archimedes screw inside a clear tube, visibly carrying balls upward from the collection trough to the launch point.

#### Construction (per launcher)
- **Screw:** 3D-printed helical screw, 18" long, printed in 4 interlocking 4.5" sections that snap together. 2" OD helix, ¾" center shaft. Printed in metallic gold PLA
- **Tube:** 2.5" ID clear acrylic tube, 18" long. Ball (2.75" whiffle) rides on top of the screw flights in the tube
- **Crank handle:** 3D-printed hand crank with ergonomic grip, keyed to the screw shaft. Printed in player color (red or blue)
- **Mounting bracket:** 3D-printed clamp that bolts to the bottom edge rail. Holds the tube at 60° angle from horizontal
- **Ball feed:** Bottom of tube is submerged in the collection trough. Turning the crank scoops a ball from the trough and lifts it
- **Launch point:** Top of tube exits through the bottom edge of the playing field. Ball rolls off the screw flight and enters the mechanism zone

#### Mechanics
- One full crank rotation advances the ball ~3". Six turns = one ball launched (about 3-4 seconds of cranking for fast kids)
- Satisfying mechanical clicking from 3D-printed ratchet teeth that prevent back-spin
- Ball visibly spiraling upward inside clear tube — the crowd sees the lift in action

### 3. Mechanism Modules — Standard Interface

ALL mechanisms mount to the backboard via a universal bolt pattern:
- **4× M6 bolts** on a **4" × 4" square** pattern
- **T-nuts** embedded in the plywood from the back side — mechanisms bolt on from the front
- **Maximum protrusion:** 5" from backboard (stays within the 6" gap, 1" clearance to acrylic)
- **Maximum footprint:** 8" × 8" for large mechanisms, centered on a 4" mounting pattern (occupies 2×2 grid positions)
- **Bearing standard:** All rotating parts use **608ZZ bearings** (standard skateboard bearing, $0.50 each, available everywhere). Printed housings press-fit around the bearings

### 3a. Tier 1 — Passive Chaos Mechanisms

#### Spinning Wheels (×4)
- Free-spinning paddle wheel, 5" diameter, 4 paddles, on a central 608ZZ bearing
- Ball impacts a paddle, wheel spins freely, deflects ball unpredictably
- **Filament:** Neon green PLA
- **Print time:** ~2 hrs each
- **Mounting:** Single bolt pattern, wheel centered

#### Funnel Spirals (×3)
- Cone-shaped funnel, 6" top diameter, 2" bottom opening
- Ball enters the rim, spirals around the inside 1-3 times, exits the bottom hole at an unpredictable angle
- Internal spiral ridge guides the ball path
- **Filament:** Translucent purple PETG
- **Print time:** ~3 hrs each
- **Mounting:** Single bolt pattern, funnel centered

#### Bumper Mushrooms (×6)
- Oversized mushroom cap, 3" diameter dome on a 1" stem
- Curved top creates wild deflections — balls hit the dome and ricochet
- Simple but effective — the classic plinko energy
- **Filament:** Hot pink PLA
- **Print time:** ~1.5 hrs each
- **Mounting:** Single bolt through center stem into backboard

#### Helix Drops (×2)
- Vertical helical chute, 8" tall, 3" OD
- Ball enters the top, corkscrews down inside, exits the bottom moving laterally
- Open-sided design so the corkscrew motion is visible
- **Filament:** Neon orange PLA
- **Print time:** ~3 hrs each
- **Mounting:** Single bolt pattern, top-mounted

### 3b. Tier 2 — Stateful Machines

#### Pendulum Gates (×3)
- Weighted pendulum arm, 6" long, pivoting on a 608ZZ bearing at the center
- Arm blocks one of two ball paths (left or right)
- When a ball pushes through the unblocked side, its weight shifts the pendulum to block THAT side and open the other
- **State:** Alternates between left-open and right-open with each ball
- **Filament:** Silver PLA (chrome look)
- **Print time:** ~6 hrs each
- **Mounting:** Single bolt pattern, pendulum centered

#### See-Saw Catapults (×2)
- Balanced beam, 8" long, pivot at center on 608ZZ bearing
- Ball lands on one end → beam tips → launches whatever is on the other end
- **Interaction:** Ball A loads one side. Ball B (from same or other player) lands on the opposite side, launching Ball A into an unexpected trajectory
- 3D-printed cup at each end holds the ball until tipped
- **Filament:** Bright yellow PLA
- **Print time:** ~8 hrs each (beam + cups + pivot housing)
- **Mounting:** Double-wide bolt pattern (2 grid positions wide)

#### Gear Ratchets (×2)
- Ratcheting gear wheel, 6" diameter, with 6 ball-sized buckets around the rim
- Each arriving ball lands in an open bucket, its weight advances the wheel one notch (ratchet pawl prevents back-spin)
- As the wheel advances, the bucket on the opposite side tips and dumps its ball out a chute
- **State:** Always holds 3 balls, always dumping the ball that arrived 3 turns ago. Creates a delay effect
- **Filament:** Metallic blue PLA
- **Print time:** ~8 hrs each (wheel + ratchet pawl + housing + axle)
- **Mounting:** Single bolt pattern, extra-deep (uses full 5" protrusion)

#### Trap Doors (×3)
- Platform with a spring-loaded hinge (3D-printed living hinge + rubber band for spring)
- Ball A rolls onto the platform and sits
- Ball B hits the trigger lever (a small arm extending to the side)
- Trigger releases the door, Ball A drops through
- Door springs back closed, ready for the next pair
- **Filament:** Red PLA
- **Print time:** ~5 hrs each
- **Mounting:** Single bolt pattern

### 3c. Tier 3 — Showstopper Centrepieces

#### THE OCTOPUS (×1) — Center of board
- Central hub, 8" diameter, with 8 articulated arms radiating outward
- Each arm is a 6" channel that can receive and route a ball
- Arms pivot on 608ZZ bearings at their base — they swing freely
- Ball enters any arm from above, gravity routes it down the arm's current angle to one of 8 exit points
- **State:** Each ball shifts the arm positions slightly. After 5-10 balls, the octopus has completely reconfigured its routing pattern
- Arms are loosely coupled — a ball in one arm can bump adjacent arms, creating cascading position changes
- **Filament:** Gradient purple-to-teal PLA (Bambu AMS color mixing)
- **Print time:** ~20 hrs total (hub + 8 arms + 8 bearing housings + mounting plate), printed in 6 sub-assemblies
- **Mounting:** 4× bolt pattern, centered at board center, occupies 3×3 grid area (12" × 12")
- **Assembly:** Arms snap onto hub bearings. Full assembly in 10 minutes

#### THE VOLCANO (×1) — Top center of board
- Cone shape, 10" base diameter, 12" tall, with external helical ramp
- Ball lands on the exterior ramp at the base, spirals upward around the outside of the cone to the top
- At the caldera (top), ball drops in and exits from one of 3 randomized chutes at the base (120° apart)
- Interior has a 3D-printed ball-guide with 3 curved channels — ball's entry angle determines which channel it follows to which exit
- **Filament:** Red-to-orange gradient PLA
- **Print time:** ~15 hrs total (cone exterior in 3 vertical sections + interior guide + base), 4 sub-assemblies
- **Mounting:** 4× bolt pattern, top-center of board
- **Assembly:** Sections stack and lock with dovetail keys

### 4. Scoring Buckets (bottom of board)

11 buckets span the bottom edge, each a uniquely 3D-printed container:

| Position | Zone | Points | Width | Bucket Design | Filament |
|----------|------|--------|-------|--------------|----------|
| Center | JACKPOT | 1000 | 2.5" | Gold crown trophy | Gold silk PLA |
| Center±1 | MEGA | 500 | 3" | Flame columns | Orange PLA |
| Center±2 | GREAT | 200 | 4" | Star shape | Yellow PLA |
| Center±3 | NICE | 100 | 5" | Thumbs-up | Green PLA |
| Center±4 | MEH | 25 | 6" | Plain + shrug face | Grey PLA |
| Edges | THE PIT | 0 | 2" | Toilet bowl | White PLA |

- All buckets have a drain hole at the back → balls fall through into the rear collection chute
- Buckets bolt to the bottom edge rail using the same M6 standard

### 5. Ball Return System

- **Collection chute:** Angled PVC half-pipe behind the board, running from top to bottom
- **Bucket drains:** Each scoring bucket and the board bottom both feed into this chute
- **Return trough:** At the base of the board, a divided trough (one per player) collects balls from the chute
- **Back to launcher:** Trough is angled so balls roll by gravity toward the Archimedes screw intake
- **Divider:** Center divider in the bottom trough — balls from the left half go to Player 1's crank, right half to Player 2
- **Cycle time:** Ball exits a bucket → 2-3 seconds to roll down rear chute and back into the crank trough. Self-resetting

### 6. Sound System (Optional but Recommended)

- **Arduino + DFPlayer Mini** module behind the board
- **Piezo contact sensors** on the jackpot bucket, pit/toilet buckets, and the volcano caldera
- **Sounds:**
  - Jackpot hit → triumphant fanfare
  - Toilet hit → sad trombone (WAH WAH WAHHH)
  - Volcano eruption → explosion sound when ball enters caldera
  - Background: gentle mechanical clicking/ticking ambiance
- **Speaker:** Single 3W speaker mounted behind the board, facing forward through a sound port in the plywood
- **Power:** USB battery pack

---

## Materials List

### Lumber & Sheet
| Item | Qty | Est. Cost |
|------|-----|-----------|
| ¾" plywood (4×8, cut to 48×72) | 1 | $40 |
| ¼" clear acrylic sheet (48×72) | 1 | $100-140 |
| 1×8 lumber (edge rails, 20 lin ft) | 3 (8ft) | $30 |
| 2×4 lumber (legs, braces) | 2 (8ft) | $12 |

### Hardware
| Item | Qty | Est. Cost |
|------|-----|-----------|
| M6 × 30mm bolts | 100 | $20 |
| M6 T-nuts (for plywood) | 80 | $15 |
| 608ZZ bearings (skateboard) | 30 | $15 |
| Wood screws (assorted) | 1 box | $8 |
| Hinges (legs + access panels) | 6 | $15 |
| Chain + turnbuckle | 1 | $8 |
| Wing nuts + carriage bolts | 1 set | $15 |
| Cabinet magnetic catches (access panels) | 4 | $8 |
| Rubber feet | 4 | $6 |
| Rope handles | 2 | $8 |

### 3D Printing Supplies
| Item | Qty | Est. Cost |
|------|-----|-----------|
| PLA filament — Neon Green (1kg) | 1 | $20 |
| PLA filament — Hot Pink (1kg) | 1 | $20 |
| PLA filament — Neon Orange (1kg) | 1 | $20 |
| PLA filament — Bright Yellow (1kg) | 1 | $20 |
| PLA filament — Silver/Chrome (1kg) | 1 | $20 |
| PLA filament — Metallic Blue (1kg) | 1 | $20 |
| PLA filament — Red (1kg) | 1 | $20 |
| PLA filament — Gold Silk (1kg) | 1 | $22 |
| PETG filament — Translucent Purple (1kg) | 1 | $22 |
| PLA filament — White (1kg) | 1 | $18 |
| PLA filament — Grey (1kg) | 1 | $18 |
| PLA filament — Matte Black (1kg) | 1 | $18 |
| **Filament subtotal** | | **~$238** |

### Acrylic Tubes (for Archimedes lifts)
| Item | Qty | Est. Cost |
|------|-----|-----------|
| 2.5" ID clear acrylic tube, 24" long | 2 | $30 |

### Game Pieces
| Item | Qty | Est. Cost |
|------|-----|-----------|
| Whiffle balls (red + blue, 2.75") | 24 | $12 |
| Spray paint — matte black (board) | 2 cans | $10 |

### Electronics (optional sound system)
| Item | Qty | Est. Cost |
|------|-----|-----------|
| Arduino Nano | 1 | $8 |
| DFPlayer Mini + SD card | 1 | $6 |
| Piezo contact sensors | 4 | $8 |
| 3W speaker | 1 | $5 |
| USB battery pack | 1 | $12 |

### **Estimated Total: $700–850**

*The itemized materials above sum to $630–670 before contingency. Add realistic 3D printing waste (~20–30% across 170+ print hours and 12 filament types — failed prints, supports, purge towers, retries on complex mechanisms like the gear ratchets and Octopus arms), plus upgrading from bargain-bin 608ZZ bearings ($0.50 each) to reliable ones ($1.50 each) for the high-impact mechanisms, and the realistic range is $700–850. Budget $800 to be safe.*

---

## Build Sequence

### Phase 0: Print Farm Begins (Weeks 1-4)
Start printing immediately while the frame isn't built yet. **Total print time is 170+ hours** — with a single printer running 10–12 hrs/day, this is 3–4 weeks of continuous printing. Failed prints (expect 10–15% failure rate on complex parts like gear ratchets and Octopus arms) add another week.
1. Print all Tier 1 passive mechanisms (bumper mushrooms, spinning wheels, funnel spirals, helix drops) — ~32 hrs
2. Begin Tier 2 mechanisms — pendulum gates first (most critical to test)
3. Test-fit mechanisms with scrap plywood + T-nuts to verify the universal bolt pattern
4. **Prototype before batch printing:** Print ONE of each Tier 2 mechanism and test with real balls before committing to the full batch. The gear ratchet pawl, see-saw balance, and trap door spring tension all need tuning in the CAD before final prints

### Phase 1: Frame & Board (Weekend 1)
1. Cut plywood to 48×72"
2. Paint matte black, let dry overnight
3. Drill the M6 mounting grid — 7 columns × 11 rows, 6" spacing, using a drill press jig for accuracy
4. Hammer in T-nuts from the back side at all grid positions
5. Cut edge rails from 1×8, attach to plywood edges
6. Cut two 3" holes in bottom edge rail for ball returns
7. Build A-frame legs with hinges, attach with carriage bolts + wing nuts
8. Mount rope handles

### Phase 2: Launchers & Ball Return (Weekend 2)
1. Assemble Archimedes screws (snap together printed sections)
2. Mount acrylic tubes in printed brackets on bottom edge rail at 60° angle
3. Build PVC collection chute on the back of the board
4. Build the divided return trough at the base
5. Test the crank → lift → launch cycle with balls
6. Tune the screw pitch — sand down any tight spots, ensure smooth cranking

### Phase 3: Mechanism Installation (Weekend 3)
1. Lay out all printed mechanisms on the board — arrange for maximum chaos and visual appeal
2. The Octopus goes dead center
3. The Volcano goes top center
4. Spinning wheels and pendulum gates at key junction points
5. Funnel spirals and helix drops as mid-board transitional elements
6. See-saw catapults and gear ratchets at strategic convergence points where balls from both players might interact
7. Trap doors scattered at choke points
8. Bumper mushrooms fill remaining gaps
9. Bolt everything on from the front — M6 bolts into T-nuts, hand-tight

### Phase 4: Scoring Buckets & Front Panel (Weekend 4)
1. Mount scoring buckets along the bottom rail
2. Connect bucket drains to the rear collection chute
3. Drill acrylic front panel — holes at edges and at mechanism pass-through points
4. Cut two 12×12" access panel doors, mount with hinges + magnetic catches
5. Mount acrylic front panel — bolts through rails
6. Seal all edges — no ball escape routes

### Phase 5: Playtest & Tune (Weeks 9-10)
1. Load balls, crank, watch
2. Identify dead zones where balls get stuck — add bumper mushrooms or adjust mechanism angles
3. Tune pendulum gate weights — should alternate cleanly
4. Verify gear ratchets advance reliably — adjust pawl tension
5. Check see-saw catapult balance — add/remove weight as needed
6. Verify ball return cycle — no jams from trough to crank to launch

### Phase 6: Sound & Polish (Weeks 11-12)
1. Wire up Arduino sound system (optional)
2. Mount piezo sensors on target buckets
3. Test sounds + adjust trigger sensitivity
4. Print and mount signage — game name, scoring legend, player positions
5. Print spare mechanisms for game day (at least 1 extra of each Tier 1)
6. Final full playtest with actual kids if possible

---

## Open Questions
- [ ] Whiffle ball diameter — 2.75" standard? Or use smaller practice golf balls for more chaotic peg interactions?
- [ ] Acrylic vs polycarbonate for front panel — polycarb is tougher but harder to cut access panels in
- [ ] AMS color mixing for octopus and volcano gradient — test print a small gradient piece first
- [ ] Archimedes screw pitch optimization — need to prototype and test with real balls
- [ ] Will 608ZZ bearings handle the repeated ball impacts on spinning wheels? May need to test and possibly upgrade to 6001ZZ for the high-impact mechanisms
