# The Great Heist — Build Plan

## Concept
Giant tilting labyrinth table themed as a bank vault heist. Players use two hand cranks to tilt a 48"×36" maze surface, guiding a steel ball bearing from ENTRANCE to VAULT through corridors, past trap holes (alarms), and around dead ends. Timed at 60 seconds. The dual-crank mechanic requires coordinating both hands on independent tilt axes — intuitive to learn, deeply satisfying to master.

## Modes
- **Solo (default):** Beat the clock — reach the vault in under 60 seconds
- **Speed Run:** Time trial — fastest vault crack wins (leaderboard on whiteboard)
- **Head-to-Head:** Two identical tables side by side, first to the vault wins (requires 2 tables)
- **Nightmare Mode:** Blindfold on, friend calls out directions. Pure chaos.

---

## Overall Dimensions

| Component | Size | Notes |
|-----------|------|-------|
| Maze playing surface | 48"W × 36"D | Plywood with wall strips glued on |
| Table frame height | 30" to surface | Waist height for kids |
| Frame footprint | 56"W × 44"D | Frame slightly larger than maze for gimbal |
| Surface tilt range | ±5° in each direction | Gentle enough for control, steep enough to roll |
| Ball bearing | 1" diameter, steel | Heavy enough to feel the tilt, visible from distance |
| Total height | ~36" | Low enough for K–1st, comfortable for 5th grade |

---

## Architecture

### 1. Maze Surface (The Bank Floor Plan)

A 48"×36" sheet of ¼" plywood forms the maze base. Walls are ¼" plywood strips (1.5" tall) glued and pinned to the surface, creating corridors.

- **Surface material:** ¼" plywood (smooth birch preferred — ball rolls cleanly)
- **Wall strips:** ¼" plywood, ripped to 1.5" tall on a table saw. Glued and pin-nailed to the surface
- **Maze design:** Three paths from ENTRANCE (front-left corner) to VAULT (center):
  - **Easy Street** — wide corridors, gentle curves, 2 trap holes
  - **Side Hustle** — medium corridors, sharper turns, 4 trap holes
  - **Air Duct** — narrow passages, tight angles, 6 trap holes (some shared with other paths)
- **Trap holes:** 1.5" diameter holes drilled through the surface (ball falls through = alarm triggered)
- **Trap count:** 8 total, distributed across paths
- **ENTRANCE:** Open notch at front-left edge, ball placed here at start
- **VAULT:** A 3"×3" recessed pocket at center of the maze, painted gold. Ball rolls in = heist complete
- **Surface paint:** Base coat dark navy/charcoal (blueprint style). Corridor walls painted with white edge highlights. Trap holes circled in red ("ALARM" labels). Optional: blueprint grid lines, room labels ("LOBBY", "SECURITY", "SERVER ROOM", "AIR DUCT")

### 2. Trap Hole Mechanism (The Alarm)

Each trap hole has a simple mechanical alarm — when the ball falls through, it triggers a sound.

- **Mechanism:** Below each trap hole, a small hinged PVC flap (2"×2") mounted on a pin. The flap rests at a slight angle. Ball drops through hole, hits flap, flap swings down and strikes a bicycle bell mounted below it
- **Bicycle bell:** Standard handlebar bell ($2 each), mounted on a bracket directly below the flap's swing path. Ball hits flap → flap hits bell → DING! (the alarm)
- **Alternative (simpler):** Skip the flap mechanism. Just mount a metal bowl/tin below each hole. Ball drops in → CLANK. Less theatrical but zero-mechanism
- **Ball recovery:** All trap bells/bowls drain into a foam-lined collection tray that slopes toward the front of the table. Ball rolls to an access slot where the player can retrieve it and place it back at the ENTRANCE
- **The drama:** The bell/clank is the game's signature sound. It echoes across the carnival. Everyone within earshot knows someone just triggered the alarm. DING = failure. Silence = heist in progress. The tension of NO sound is almost as compelling as the alarm itself.

### 3. Gimbal Mount (Tilt Mechanism)

The maze surface sits on a two-axis gimbal, allowing independent tilt on X and Y axes.

- **Primary (left/right) axis:** A ½" steel rod (or hardwood dowel) runs through the center of the maze surface from left to right. The rod rests in pillow block bearings (or drilled hardwood brackets) mounted on the inner frame rails. This allows the surface to tilt forward/back
- **Secondary (forward/back) axis:** The inner frame itself sits on a second rod running front-to-back, mounted in bearings on the outer frame legs. This allows the surface + inner frame to tilt left/right
- **Tilt limiters:** Rubber bumpers (small rubber feet) glued to the underside of the maze surface and inner frame, limiting tilt to ±5° in each direction. Prevents the surface from over-tilting and launching the ball
- **Gimbal feel:** The bearings should be smooth but not frictionless — slight resistance helps players make small adjustments. A thin washer between bearing and frame adds just enough drag

### 4. Hand Cranks (Player Controls)

Two hand cranks on the front rail of the outer frame give the player proportional tilt control.

- **Construction:** Each crank is a ½" wooden dowel (10" long) mounted perpendicular to a ½" threaded rod that runs through the frame rail. The threaded rod connects to the corresponding gimbal axis via a cable or linkage
- **Linkage option A (cable):** Bicycle brake cable. One end attaches to the crank shaft, the other to the gimbal axis rod. Turn the crank → cable pulls → surface tilts. Spring return to center
  - Pros: Smooth, quiet, adjustable
  - Cons: Requires cable routing, spring tension tuning
- **Linkage option B (direct rod):** A connecting rod (wooden dowel with drilled ends) directly links the crank to the gimbal axis via a simple lever arm
  - Pros: Simpler, no cables, direct feel
  - Cons: Slightly clunkier, limited tilt angle transfer
- **Recommendation:** Start with Option B (direct rod) — simpler to build and debug. Upgrade to cables later if needed
- **Crank handles:** 3D-printed or turned wooden knobs on the crank ends for comfortable grip
- **Labeling:** Left crank labeled "← LEFT / RIGHT →", Right crank labeled "↑ FORWARD / BACK ↓"

### 5. Outer Frame (Table Structure)

The outer frame holds everything at playing height and houses the gimbal.

- **Legs:** Four 2×4 legs, 28" tall (surface at ~30" with gimbal hardware)
- **Top rails:** 2×4 lumber forming a rectangular frame 56"×44" (slightly larger than maze surface for gimbal clearance)
- **Cross braces:** 2×4 braces at mid-height between legs for rigidity
- **Front rail:** Where the cranks mount. Slightly thicker (doubled 2×4) for crank bearing support
- **Ball recovery tray:** A shallow plywood tray mounted under the maze surface, sloping toward a front access slot. Catches balls from trap holes
- **Skirt panels (optional):** ¼" plywood panels around the frame sides, painted to match the bank vault theme. Hides the gimbal mechanism from curious fingers

### 6. Timer

- **Option A (analog):** Large 60-second sand timer mounted on a post at the corner of the frame. Player flips it to start. Beautifully tactile and thematic ("the vault's time lock is ticking!")
- **Option B (phone):** Operator uses a phone timer. Less theatrical but easier
- **Option C (DIY):** Kitchen timer ($5) mounted on the frame. Beeps when time's up

### 7. Vault (Goal)

- **Construction:** A 3"×3" square pocket routed ¼" deep into the maze surface at center. Ball rolls in and stops
- **Visual:** Painted gold with a small vinyl decal of a vault door. The gold pocket is visible from the player's position and glows under the corridor walls
- **Celebration:** When the ball enters the vault, the operator rings a desk bell or the player raises their fists. Keep it simple — the crowd does the rest

---

## Materials List

### Lumber & Sheet
| Item | Qty | Est. Cost |
|------|-----|-----------|
| ¼" birch plywood (4×3 cut, maze surface) | 1 | $18 |
| ¼" plywood (wall strips — rip to 1.5" tall) | 2 sheets | $16 |
| 2×4 lumber (frame legs + rails, 8ft) | 4 | $24 |
| ¼" plywood (recovery tray + optional skirt panels) | 1 sheet | $8 |

### Gimbal & Cranks
| Item | Qty | Est. Cost |
|------|-----|-----------|
| ½" steel rod (primary axis, 40" length) | 1 | $8 |
| ½" steel rod (secondary axis, 50" length) | 1 | $8 |
| Pillow block bearings (½" bore) | 4 | $16 |
| ½" wooden dowels (crank shafts, 36" length) | 1 | $3 |
| Connecting rods (¼" dowels, 12" each) | 2 | $2 |
| Rubber bumper feet (tilt limiters) | 8 | $6 |
| Springs (return to center, medium tension) | 4 | $8 |

### Trap Mechanism
| Item | Qty | Est. Cost |
|------|-----|-----------|
| Bicycle bells (handlebar style) | 8 | $16 |
| Small hinges (1" butt hinges for flaps) | 8 | $8 |
| PVC sheet scraps (flap material) | scraps | $3 |
| OR: Small metal bowls (simpler alternative) | 8 | $12 |

### Game Pieces & Finish
| Item | Qty | Est. Cost |
|------|-----|-----------|
| 1" steel ball bearings | 5 (spares) | $8 |
| Spray paint — dark navy (surface base coat) | 2 cans | $10 |
| Spray paint — gold metallic (vault + accents) | 1 can | $5 |
| White paint pen / fine brush (wall edge highlights) | 2 | $6 |
| Red paint (trap hole circles) | 1 small | $4 |
| Adhesive vinyl (labels, room names, signage) | 1 sheet | $5 |
| 60-second sand timer | 1 | $8 |

### Hardware
| Item | Qty | Est. Cost |
|------|-----|-----------|
| Wood screws (assorted) | 1 box | $8 |
| Carriage bolts + wing nuts (frame assembly) | 12 | $10 |
| Wood glue | 1 bottle | $5 |
| Pin nails (wall strip attachment, for nail gun or hand) | 1 box | $5 |

### **Estimated Total: $200–240**

---

## Build Sequence

### Phase 1: Maze Surface (Weekend 1, Day 1 — ~4 hours)
1. Cut ¼" birch plywood to 48"×36"
2. Sand smooth — the ball needs a clean roll surface
3. Design maze layout on paper first (full scale recommended — use butcher paper)
4. Transfer maze layout to plywood surface with pencil
5. Drill 8 trap holes (1.5" diameter) at planned locations
6. Route vault pocket (3"×3"×¼" deep) at center, or build up walls around a 3"×3" gap
7. Rip ¼" plywood into 1.5" tall strips on table saw (you'll need ~60 linear feet of wall strips)
8. Glue and pin-nail wall strips to surface following the maze layout. Use clamps. Work section by section
9. Test ball rolling through each path — verify no dead spots where ball gets stuck, verify all turns are rollable at ±5° tilt

### Phase 2: Paint & Theme (Weekend 1, Day 2 — ~3 hours)
1. Base coat entire surface dark navy/charcoal (2 coats). Paint inside corridors too — ball needs smooth paint
2. Once dry, paint white edge highlights on wall tops (makes corridors visible from player height)
3. Paint trap hole surrounds in red. Add "ALARM" labels
4. Paint vault pocket gold
5. Add room labels with adhesive vinyl or paint pen: "LOBBY", "SECURITY OFFICE", "SERVER ROOM", "AIR DUCT", "VAULT"
6. Optional: Add blueprint grid lines (very subtle, light gray) across the surface
7. Seal entire surface with clear matte polyurethane — critical for smooth ball rolling and paint protection

### Phase 3: Frame & Gimbal (Weekend 2, Day 1 — ~4 hours)
1. Cut and assemble outer frame: four 28" legs, two 56" side rails, two 44" front/back rails
2. Add mid-height cross braces for rigidity
3. Double up the front rail (crank mounting point)
4. Mount pillow block bearings on inner side rails (primary axis — left/right tilt)
5. Insert primary axis steel rod through bearings
6. Attach maze surface to primary axis (bolt/screw to center of surface's left and right edges)
7. Build inner frame: two short rails that hold the primary axis bearings and sit on the secondary axis
8. Mount secondary axis bearings on outer frame front/back rails
9. Insert secondary axis rod
10. Test gimbal: surface should tilt smoothly in both directions. Adjust bearing alignment if binding

### Phase 4: Cranks & Linkage (Weekend 2, Day 1 continued — ~2 hours)
1. Drill crank shaft holes through front rail
2. Insert crank dowels through front rail, add wooden knob handles on player side
3. Build connecting rods: ¼" dowels with drilled ends, connecting crank shafts to gimbal axis rods via lever arms
4. Attach connecting rods with bolts (loose enough to pivot)
5. Test crank operation: turning left crank should tilt surface left/right, turning right crank should tilt forward/back
6. Install rubber bumper tilt limiters — verify ±5° limit in each direction
7. Install return springs if the surface doesn't naturally center (gravity may be sufficient depending on balance)
8. Label cranks: "← LEFT / RIGHT →" and "↑ FORWARD / BACK ↓"

### Phase 5: Traps & Ball Recovery (Weekend 2, Day 2 — ~2 hours)
1. Mount bicycle bells on brackets below each trap hole
2. Build and mount hinged flaps above each bell (or just position metal bowls under holes for simpler approach)
3. Test each trap: drop ball through hole → should trigger bell/clank clearly
4. Build ball recovery tray: shallow plywood tray under the maze surface, sloped toward front
5. Cut access slot in front of tray where player can reach in and grab the returned ball
6. Line tray with foam or felt (quiets the ball, prevents bouncing)
7. Test full recovery cycle: ball falls in trap → bell rings → ball rolls to tray → player retrieves from slot

### Phase 6: Testing & Tuning
1. Place ball at ENTRANCE. Tilt with cranks. Verify ball rolls smoothly through all three paths
2. Time yourself on each path — Easy Street should be ~45 sec, Side Hustle ~30 sec, Air Duct ~20 sec for a practiced player
3. Verify trap holes are positioned where all three paths have genuine risk (not just dead-end decoration)
4. Check tilt sensitivity — ±5° should feel controllable but responsive. Adjust limiters if too sensitive or too sluggish
5. Verify cranks feel good — smooth rotation, proportional response, no binding
6. Check that vault pocket holds the ball securely (slight depression + walls prevent roll-out)
7. Full playtest: get a kid to play. Watch for confusion points. Simplify if any path feels unfair

---

## Safety Notes
- All edges sanded smooth
- Ball bearing is small (1") — appropriate for elementary schoolers but keep spares visible to avoid "lost ball" panic
- Trap holes (1.5") are too small for fingers to get stuck but large enough to visually read as hazards
- Frame at waist height — no bending, no climbing
- Gimbal tilt limited to ±5° — surface never gets steep enough to launch the ball off the table
- All mechanisms under the surface are enclosed by the skirt panels — no pinch points accessible to curious hands
- No electrical, no pneumatics, no projectiles

## Open Questions
- [ ] Should the maze be printed/laser-cut for precision, or hand-built with glued strips?
  → Recommendation: **Hand-built.** Glued strips are cheaper, more forgiving of errors, and can be adjusted during testing. Laser-cut walls would be more precise but requires access to equipment and adds cost
- [ ] Difficulty tuning: how narrow should "Air Duct" corridors be?
  → Start at 2" wide (ball is 1" dia = ½" clearance each side). Narrow to 1.5" if too easy. Anything under 1.25" becomes frustrating
- [ ] Should the maze surface be removable/swappable?
  → Cool idea for future: build a second maze surface ("THE SEQUEL: PRISON BREAK") and swap them between carnival days. Gimbal frame stays the same, just unbolt the surface
- [ ] Digital timer + leaderboard (Arduino + 7-segment display)?
  → Nice-to-have but not necessary. A whiteboard with the top 10 times is just as effective and costs $5
