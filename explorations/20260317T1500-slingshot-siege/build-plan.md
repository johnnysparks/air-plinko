# Slingshot Siege — Build Plan

## Concept
Two-player head-to-head siege game. Players face each other across a vertical fortress wall (plinko board) and launch whiffle balls through castle gates using swivel-mounted slingshots. Balls that breach a gate cascade through pegs on the opponent's side into scoring moats. Higher gates = harder shots = bigger multipliers.

## Modes
- **Competitive (default):** Red balls vs Blue balls — highest total score wins
- **Cooperative:** Same color — combine scores, beat a target (Bronze 500, Silver 1000, Gold 1500)
- **Speed Siege:** 60-second timer — fire as many as you can, unfired balls don't count

---

## Overall Dimensions

| Component | Size | Notes |
|-----------|------|-------|
| Fortress Wall (playing field) | 60"W × 48"H × 8"D | Double-sided plinko board |
| Wall thickness (plywood core) | ¾" | Standard plywood |
| Peg field depth (each side) | 3.5" | Whiffle ball (2.75") + clearance |
| Gate pass-through depth | ¾" (board thickness) | Ball passes through the plywood itself |
| Slingshot station height | 36" (post top) | Kid-friendly, adjustable |
| Slingshot distance from wall | 48"–60" (adjustable) | Closer for younger kids |
| Total footprint | 60"W × 120"D × 60"H | Wall + two shooting lanes |

---

## Architecture

### 1. Fortress Wall (Core Structure)

The wall is a double-sided plinko board — pegs on both the front AND back faces, with castle gates cut through the board.

- **Core panel:** 60"W × 48"H sheet of ¾" plywood
- **Front acrylic:** 60"W × 48"H clear acrylic (¼" thick), mounted 3.5" from the front face of the plywood via spacer pegs
- **Rear acrylic:** Same dimensions, mounted 3.5" from the rear face
- **Edge rails:** 1×4 lumber framing all four sides of each face, sandwiched between plywood and acrylic
- **Spacer/pegs:** ¾" wooden dowels, 3" long, drilled into the plywood face. Serve as both structural spacers and plinko pegs. ~40 pegs per side, offset grid pattern, 5" spacing
- **Castle gates:** Rectangular holes cut through the plywood at 3 height tiers (see Gate Specifications below). Gates are framed with 3D-printed archway pieces for aesthetics and to create the "sweet spot" entry angle
- **Decorative elements:** 3D-printed castle turrets on top corners, battlements (crenellations) along the top edge rail, pennant flags (fabric triangles on dowels)

### 2. Castle Gates (Pass-Through Holes)

Six gates total, arranged symmetrically (mirrored left-right). Cut through the ¾" plywood with a jigsaw.

| Gate Name | Qty | Center Height | Opening Size | Notes |
|-----------|-----|---------------|-------------|-------|
| MAIN GATE | 2 | 12" from bottom | 6"W × 4"H | Widest, easiest to hit. Arched top (3D-printed frame) |
| ARROW SLIT | 2 | 28" from bottom | 4.5"W × 3.5"H | Mid-height, moderate difficulty |
| TOWER GATE | 2 | 42" from bottom | 3.5"W × 3"H | Highest, smallest, hardest to hit |

- **Horizontal spacing:** Gates are positioned at 18" and 42" from left edge (symmetric about center)
- **Gate frames:** 3D-printed PLA archway surrounds. Serve two purposes: (1) aesthetics — looks like a castle gate, (2) funnel geometry — angled inner edges guide slightly off-center shots through, but reject wild misses
- **Pass-through clearance:** The ¾" plywood thickness is thin enough that a whiffle ball (2.75" dia) passes through a 3.5"+ opening easily

### 3. Peg Field (Both Sides)

Each side of the wall has its own peg field between the plywood and the acrylic panel.

- **Peg count:** ~40 per side (80 total)
- **Peg material:** ¾" wooden dowels, 3" long, glued into holes drilled into the plywood face
- **Layout:** Offset grid, 5" horizontal spacing, 4" vertical spacing
- **Peg-free zones:** No pegs within 2" of any gate opening (balls need clear entry)
- **Peg colors:** Alternating neon colors — spray-painted or dipped (neon pink, green, yellow, orange). Against a matte black plywood face, these POP
- **Cascade physics:** Ball enters through gate, immediately hits pegs, bounces chaotically downward through 3–9 rows (depending on gate height) into scoring moats

### 4. Scoring Moats (Both Sides, Mirrored)

At the bottom of each side's peg field, 7 collection channels funnel balls into scoring zones.

- **Construction:** Angled dividers (¼" plywood strips, 4" tall) mounted to the back panel, creating V-shaped channels
- **Channel widths (left to right):**

| Zone | Width | Points | Color |
|------|-------|--------|-------|
| SWAMP (gutter) | 3" | 0 | Black |
| PEASANT'S MOAT | 6" | 50 | Green |
| KNIGHT'S MOAT | 5" | 100 | Blue |
| ROYAL MOAT (center) | 4" | 250 | Gold |
| KNIGHT'S MOAT | 5" | 100 | Blue |
| PEASANT'S MOAT | 6" | 50 | Green |
| SWAMP (gutter) | 3" | 0 | Black |

- **Moat labels:** Adhesive vinyl numbers + names on the dividers
- **Ball drainage:** Each moat angles backward (2° slope) toward a collection slot in the back panel. Balls roll through into a rear collection chute.

### 5. Slingshot Stations (×2)

Each player gets a slingshot on a swivel-mounted post.

- **Post:** 4×4 lumber, 36" tall, mounted to a 24"×24" plywood base (weighted with sandbags for stability)
- **Swivel mount:** ½" bolt through the top of the post. The slingshot Y-frame sits on a bearing/washer stack and rotates freely
- **Angle limiter:** Two stop bolts on the post cap limit the slingshot's rotation to a 60° cone aimed at the wall. Cannot aim sideways or backward
- **Slingshot Y-frame:** 3D-printed (PETG for strength) or bent ½" steel rod. Fork width: 5" (wide enough for a 2.75" whiffle ball with clearance). Fork height: 8"
- **Elastic:** Theraband Gold surgical tubing, doubled. ~12" relaxed length per side. Provides enough force to propel a whiffle ball ~8ft with a 10" pull-back
- **Pouch:** 3"×4" leather or heavy canvas rectangle, holes punched for tubing attachment
- **Height adjustment:** The post has 3 bolt holes at different heights (28", 32", 36") — move the swivel bolt to adjust slingshot height for different-aged kids
- **Ball holder:** Small 3D-printed cup/tray mounted on the post at waist height — holds 3-4 balls for quick reloading

### 6. Ball Return System

- **Rear collection chute:** A V-shaped trough runs along the bottom of the back panel on each side, collecting balls from the moat drainage slots
- **Chute routing:** Each side's chute angles toward the CENTER of the wall, where balls drop into a shared collection bin at floor level
- **Operator retrieval:** Between rounds, the operator grabs balls from the bin and re-stocks each player's ball holder
- **Ricochet balls:** Balls that miss gates bounce back toward the shooter. A low fabric net (12" tall, stretched between two posts) runs across the front of each shooting lane to catch ground-level ricochets. Players grab bounce-backs and re-fire during the round
- **Miss collection:** Balls that miss the wall entirely hit a backstop net behind the opponent's slingshot station

### 7. Support Frame

- **Wall feet:** Two T-shaped base supports (2×4 lumber) extending 24" front and back from the bottom of the wall. Rubber-capped feet. Wide enough for stability against slingshot impacts
- **Cross brace:** Horizontal 2×4 connecting the two base supports at floor level
- **Anti-tip:** Sandbags (2×25 lb) on the rear base extensions prevent the wall from tipping toward the shooter
- **Teardown:** All joints use carriage bolts + wing nuts — tool-free assembly/disassembly
- **Transport:** Wall panel is one piece (60"×48" — fits in a truck bed or on a roof rack). Frame breaks down to 5 pieces of 2×4. Slingshot posts are freestanding

---

## Materials List

### Lumber & Sheet
| Item | Qty | Est. Cost |
|------|-----|-----------|
| ¾" plywood sheet (5×4 cut) | 1 | $30 |
| ¼" clear acrylic sheet (5×4 cut) | 2 | $160–200 |
| 1×4 lumber (edge rails, 20 lin. ft) | 3 (8ft) | $18 |
| ¾" wooden dowels (36" length) | 14 | $28 |
| 2×4 lumber (frame/legs/base) | 3 (8ft) | $18 |
| 4×4 lumber (slingshot posts) | 1 (8ft, cut in half) | $10 |
| ¼" plywood strips (moat dividers) | scraps | $5 |
| 24"×24" plywood (slingshot bases, ×2) | scraps | $8 |

### Hardware
| Item | Qty | Est. Cost |
|------|-----|-----------|
| Carriage bolts + wing nuts (¼"-20, various lengths) | 1 set (20pc) | $15 |
| ½" bolts + nylon lock nuts (slingshot swivels) | 4 | $6 |
| Washers / thrust bearings (swivel smooth rotation) | 4 | $8 |
| Wood screws (assorted) | 1 box | $8 |
| Rubber feet caps (1.5") | 8 | $8 |
| L-brackets (moat-to-backpanel) | 12 | $10 |
| Eye bolts (angle limiter stops) | 4 | $6 |

### Slingshot Components
| Item | Qty | Est. Cost |
|------|-----|-----------|
| Theraband Gold tubing (10ft roll) | 1 | $12 |
| Leather scraps (pouch material) | 2 pcs | $5 |
| ½" steel rod (Y-frame, 3ft) OR 3D-print PETG | 2 | $10 |

### Game Pieces & Finish
| Item | Qty | Est. Cost |
|------|-----|-----------|
| Whiffle balls (red + blue, 2.75") | 30 pack | $12 |
| Spray paint — matte black (back panel) | 2 cans | $10 |
| Spray paint — neon assorted (pegs) | 4 cans | $20 |
| Spray paint — gold metallic (royal moat) | 1 can | $5 |
| Adhesive vinyl (scoring labels, gate names) | 1 sheet | $5 |
| Fabric (ricochet nets, pennant flags) | 3 yards | $10 |

### 3D-Printed Parts
| Part | Qty | Material | Print Time |
|------|-----|----------|------------|
| Castle gate arch frames | 6 | PLA | 3hr each |
| Battlements / crenellations (top rail) | 10 segments | PLA | 1hr each |
| Corner turrets | 4 | PLA | 2hr each |
| Slingshot Y-frames (if not using steel) | 2 | PETG | 2hr each |
| Ball holder cups | 2 | PLA | 30min each |
| Pennant flag mounts | 6 | PLA | 15min each |

**Total 3D print time: ~40 hours** (spread across several overnight runs)

### **Estimated Total: $475–550**

*The original estimate of $400–450 didn't cover the itemized line items above (which sum to $452–492). The main driver is the double acrylic — two 5×4 ft panels at $80–100 each is the optimistic case; acrylic prices vary widely and $100–130 per panel is common at retail. Plus 40 hours of 3D printing, slingshot station materials, and ricochet/backstop netting all add up. Budget $500+ to be realistic.*

---

## Build Sequence

### Phase 1: Fortress Wall Core (Weekend 1, Day 1)
1. Cut plywood to 60"×48"
2. Mark and cut 6 castle gate openings with jigsaw (measure twice!)
3. Sand gate edges smooth — no splinters for little fingers reaching in
4. Drill peg holes on BOTH faces — offset grid, 5" horizontal × 4" vertical spacing, skipping 2" clearance zones around gates
5. Paint both plywood faces matte black. Let dry.
6. Glue and insert dowel pegs (3" long) into all holes on both faces
7. Spray-paint pegs in alternating neon colors while mounted

### Phase 2: Edge Rails & Moats (Weekend 1, Day 2)
1. Cut and attach 1×4 edge rails to all four sides of each face (sandwiching between plywood and where acrylic will go)
2. Build scoring moat dividers — cut ¼" plywood into 4" strips, attach at bottom of each face with L-brackets
3. Route moat drainage — drill 1.5" holes through plywood at the back of each moat, behind the dividers
4. Build rear collection chutes (V-trough from scrap lumber) and attach to back of wall
5. Apply scoring labels and gate name decals

### Phase 3: Acrylic & Aesthetics (Weekend 2, Day 1)
1. Drill acrylic panels to match peg hole pattern (pegs pass through both plywood and acrylic as spacers)
2. Mount acrylic panels to both faces — pegs act as spacers maintaining 3.5" gap
3. Seal edges — balls must not escape from any side
4. Glue/mount 3D-printed gate arch frames around each gate opening
5. Attach 3D-printed battlements along top edge rail
6. Mount corner turrets
7. Add pennant flags on dowel poles

### Phase 4: Slingshot Stations & Frame (Weekend 2, Day 2)
1. Cut 4×4 posts to 36" each
2. Drill 3 height-adjustment holes in each post (28", 32", 36")
3. Mount slingshot Y-frames on swivel bolts with bearing/washer stacks
4. Install angle-limiter stop bolts on post caps
5. String Theraband tubing through Y-frame forks, attach pouches
6. Build 24"×24" plywood base platforms, attach posts with lag bolts
7. Build wall base frame (T-supports + cross brace) with wing nut joints
8. Mount wall to base frame
9. Set up ricochet nets (fabric between small posts, 12" tall)
10. Load sandbags on rear base extensions

### Phase 5: Testing & Tuning
1. Test slingshot force — can a whiffle ball reach the tower gates (42" high) from 5ft away? Adjust tubing tension
2. Test gate clearance — balls should pass through cleanly, not jam
3. Test peg cascade — balls entering each gate tier should cascade through the correct number of peg rows
4. Test moat scoring — balls should land cleanly in moats, not bounce out
5. Test ball return — moat drainage into rear chute should flow smoothly
6. Adjust slingshot angle limiters — verify 60° cone covers all 6 gates
7. Play a full round. Adjust anything that feels off.

---

## Safety Notes
- Slingshot swivel limiters are CRITICAL — the 60° cone prevents aiming at people
- Ricochet nets catch stray bounce-backs at ground level
- Backstop nets behind each slingshot station catch wild misses
- Acrylic panels prevent hands from entering the peg field
- Gate openings are too small for a child's head (max 6"W × 4"H) but large enough for hands — add a "keep hands out of gates" sign
- Sandbags + wide base prevent wall from tipping under slingshot impacts
- Whiffle balls are lightweight and slow — even a direct hit is harmless

## Open Questions
- [ ] Power? None needed — fully mechanical, no electronics
- [ ] Signage / castle branding theming
- [ ] Prize structure — tiered by score?
- [ ] Do we want a digital scoreboard (Arduino + IR sensors in moats) or manual scoring?
- [ ] Fog machine behind the wall for dramatic "castle mist" effect?
