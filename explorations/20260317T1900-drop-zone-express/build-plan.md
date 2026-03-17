# Drop Zone Express — Build Plan

## Design Priority: OPERATIONS FIRST

Every design decision below optimizes for three things:
1. **Setup speed** — truck to game-ready in 8 minutes, two people
2. **Player turnover** — 15-second waves, 3 kids at a time
3. **Teardown speed** — game-ready to truck in 6 minutes, two people

---

## Overall Dimensions

| Dimension | Size | Notes |
|-----------|------|-------|
| Board width | 48" (4 ft) | Three drop slots across the top |
| Board height | 60" (5 ft) | Standing height for K–5th graders |
| Depth (gap) | 4" | Whiffle ball (2.75") + clearance, no air system = thinner |
| Tilt angle | 20° from vertical | Steep enough for fast ball cascades (~5 sec drop time) |
| Total footprint | 48"W × 30"D × 72"H (with scoreboard) | Compact — fits in one parking space |

---

## Architecture

### 1. Main Board Assembly (ONE PIECE — Does Not Disassemble)

The board is the game. It ships as one unit. No field assembly of the playing surface.

- **Back panel:** 4×5 ft sheet of ¾" plywood, painted matte black
- **Edge rails:** 1×4 lumber on all four sides, pre-attached with screws and glue
- **Peg grid:** 80 pegs in offset rows (8 columns × 10 rows, 5" horizontal spacing, 5" vertical spacing)
  - Standard pegs: ¾" wooden dowels, 3" long, glued into drilled holes
  - Spinner pegs (×3): 3D-printed helicopter rotors on a 6mm bearing, mounted at mid-field choke points (rows 4, 6, 8 center area)
- **Front panel:** 4×5 ft clear ¼" acrylic, attached with wing nut + carriage bolt at 8 points around the perimeter
- **Scoring buckets:** 9 angled dividers at the bottom creating 9 slots, permanently attached
- **Ball return chute:** Enclosed channel behind the back panel — balls exit buckets through rear holes, gravity-feed down to three output slots at the top of the board (one per drop station)
- **Ball return risers:** The chute runs along the back of the board, angled to route balls from the bottom collection trough UP to the top drop slots. Uses a gentle S-curve channel with 1" PVC half-pipe as the track. Balls are lifted by the tilt angle — the board's own 20° tilt means the "back" of the board has a natural rise from bottom to top

**KEY DECISION:** The board does NOT break down. It's 48×60" — fits flat in a truck bed, SUV with seats down, or lashed to a roof rack. Eliminating field assembly of the playing surface saves 20+ minutes and removes alignment headaches.

### 2. Drop Mechanism (×3)

- **Gate:** 3D-printed pivoting gate at each drop slot, spring-loaded closed
- **Handle:** Steel rod with rubber grip, connected to gate via linkage
- **Action:** Pull handle down → gate opens → ball drops → spring closes gate → next ball rolls into position from return chute
- **Ball seat:** Small cradle above the gate holds one ball visible to the player (the "loaded" indicator)
- **Reliability:** No electronics. No air. Pure mechanical. Spring + gravity + a pivot. Cannot fail unless physically broken

### 3. Support Frame (QUICK-DEPLOY)

This is where the setup speed lives.

- **Design:** Two A-frame leg assemblies that attach to the back of the board
- **Attachment:** Two T-bolts per leg assembly — slide into pre-mounted keyhole brackets on the back panel, quarter-turn to lock. **No tools. 15 seconds per leg.**
- **Angle lock:** Built-in chain (pre-cut to length, permanently attached to legs) sets the 20° tilt automatically when legs are fully spread
- **Base feet:** 12" wide rubber-padded feet for stability on grass or concrete
- **Anti-tip:** Two 25lb sandbags hang from hooks on the rear crossbar (sandbags travel in the truck, hooks are permanent)
- **Total leg setup time: 45 seconds**

### 4. Score Display (Overhead)

- **Hardware:** Arduino Mega + 3× large 7-segment LED modules (2.3" digits, red), mounted on a 48" horizontal bar
- **Mounting:** Bar slides into two U-brackets permanently bolted to the top of the board frame. One pin per side to lock
- **Sensors:** Tilt switches or IR break-beam sensors in each scoring bucket detect ball landing, send signal to Arduino
- **Power:** 12V battery pack (Milwaukee M18 with USB adapter, or a 20Ah portable battery). One charge = 8+ hours
- **High Score:** Fourth LED module on the far right shows "HI" + running high score of the day
- **Reset:** Auto-resets 3 seconds after last ball lands. Manual reset button on back for the operator
- **Sound:** Piezo buzzer for countdown beeps. Small powered speaker (M18 Bluetooth speaker or a JBL clip) for jackpot airhorn sound effect triggered by Arduino
- **Setup time: 30 seconds** (slide bar in, pin it, plug one power cable)

### 5. Queue Management Hardware

- **Stanchions:** 4× PVC pipe stanchions (1.5" PVC, 36" tall) with rope clips, mounted in weighted bases (5-gallon bucket bases filled with concrete, painted to match)
- **Rope:** 2× 8ft nylon ropes with snap hooks
- **On-Deck Mats:** 3× rubber mats (12"×12") spray-painted with footprint outlines and numbered 1-2-3. Placed on the ground in front of the three drop slots
- **Exit arrow:** 2× floor arrows (painted plywood cutouts) directing traffic right after play
- **Setup time: 90 seconds** (set stanchions, clip ropes, lay mats and arrows)

---

## Materials List

### Board & Playing Field
| Item | Qty | Est. Cost |
|------|-----|-----------|
| ¾" plywood sheet (4×5 cut) | 1 | $35 |
| ¼" clear acrylic sheet (4×5 cut) | 1 | $80–120 |
| 1×4 lumber (edge rails, 18 lin. ft) | 3 (8ft) | $18 |
| ¾" wooden dowels (36" length) | 8 | $16 |
| 1" PVC pipe (ball return track) | 10 ft | $8 |
| Carriage bolts + wing nuts (acrylic mount) | 8 sets | $10 |

### Drop Mechanism
| Item | Qty | Est. Cost |
|------|-----|-----------|
| 3D-printed gate assemblies | 3 | $5 (filament) |
| Steel rod + rubber grip (handles) | 3 | $15 |
| Return springs | 3 | $6 |
| 6mm bearings (for spinner pegs) | 3 | $5 |
| 3D-printed spinner rotors | 3 | $3 (filament) |

### Support Frame
| Item | Qty | Est. Cost |
|------|-----|-----------|
| 2×4 lumber (legs, crossbar) | 3 (8ft) | $18 |
| T-bolt hardware + keyhole brackets | 4 sets | $20 |
| Chain (pre-cut angle limiters) | 4 ft | $8 |
| Rubber foot pads | 4 | $10 |
| Heavy-duty hooks (sandbag) | 2 | $6 |
| Sandbags (25 lb) | 2 | $12 |

### Score Display
| Item | Qty | Est. Cost |
|------|-----|-----------|
| Arduino Mega | 1 | $15 |
| 2.3" 7-segment LED modules | 4 | $24 |
| IR break-beam sensors | 9 | $27 |
| 12V battery pack or M18 adapter | 1 | $15 |
| Small powered speaker | 1 | $20 |
| Aluminum bar (48" mounting rail) | 1 | $10 |
| U-brackets + pins | 2 sets | $8 |
| Wiring, connectors, proto board | — | $15 |

### Queue Management
| Item | Qty | Est. Cost |
|------|-----|-----------|
| 1.5" PVC pipe + fittings (stanchions) | 4 | $12 |
| 5-gal buckets + concrete mix (bases) | 4 | $20 |
| Nylon rope + snap hooks | 2 | $10 |
| Rubber mats (12×12) | 3 | $9 |
| Plywood arrow cutouts | 2 | $3 |
| Spray paint (footprints, arrows, bucket bases) | 2 cans | $10 |

### Game Pieces & Finish
| Item | Qty | Est. Cost |
|------|-----|-----------|
| Whiffle balls (neon assorted) | 12 | $8 |
| Spray paint (board, buckets, scoring zones) | 4 cans | $20 |
| Adhesive vinyl (numbers, labels, signage) | 1 roll | $10 |

### **Estimated Total: $490–540**

---

## Build Sequence

### Phase 1: Board Assembly (Weekend 1, Day 1)
1. Cut plywood to 48×60"
2. Cut edge rails from 1×4, attach to plywood edges (screw + glue — permanent)
3. Drill peg holes — offset grid, 5" spacing, 80 holes
4. Glue in all wooden dowel pegs
5. Build 9 scoring bucket dividers, attach permanently to bottom interior
6. Drill ball exit holes in back panel behind each bucket
7. Paint back panel matte black, bucket dividers in scoring colors (gold/red/blue/green)

### Phase 2: Ball Return & Drop Mechanism (Weekend 1, Day 2)
1. Build rear ball return chute from 1" PVC half-pipe, mounted to back of plywood
2. Route chute from bottom collection trough up to three top drop slots (S-curve path)
3. 3D print gate assemblies and spinner rotors
4. Install drop gates at top — test spring tension, adjust for reliable auto-close
5. Install spinner pegs on bearings at three mid-field positions
6. Install handles with linkage to gates
7. Test full ball cycle: drop → cascade → bucket → rear chute → back to top slot

### Phase 3: Frame & Mounting (Weekend 2, Day 1)
1. Build two A-frame leg assemblies from 2×4
2. Install keyhole brackets on back panel, T-bolts on legs
3. Test fit — verify quarter-turn lock is solid
4. Attach chains at correct length for 20° tilt
5. Install sandbag hooks on rear crossbar
6. Attach rubber foot pads
7. Build stanchion bases (concrete in buckets — needs 24hr cure)

### Phase 4: Electronics & Finish (Weekend 2, Day 2)
1. Mount IR sensors in each scoring bucket
2. Wire Arduino + LED modules on the scoreboard bar
3. Program scoring logic: detect ball → display score → auto-sum → reset after wave
4. Program countdown sequence (beep-beep-beep-HORN)
5. Program jackpot fanfare sound
6. Mount acrylic front panel with wing nut bolts
7. Apply vinyl scoring labels, booth signage
8. Paint queue stanchion bases, arrow cutouts, on-deck mats
9. Full dress rehearsal — simulate 10 waves of play

---

## EVENT DAY OPERATIONS

### Truck Pack List (Checklist)
```
□ Main board (48×60", ~45 lbs)
□ Leg assemblies ×2 (bundled, ~15 lbs each)
□ Sandbags ×2 (25 lbs each)
□ Scoreboard bar (48" tube with electronics, ~5 lbs)
□ Battery pack (charged night before)
□ Speaker (charged night before)
□ Stanchions ×4 (PVC poles, fit in a bucket)
□ Stanchion bases ×4 (concrete buckets, ~20 lbs each — load first)
□ Ropes ×2
□ On-deck mats ×3
□ Exit arrows ×2
□ Whiffle balls (12, in a gallon ziplock)
□ Backup whiffle balls (6 more, separate bag)
□ Dowel poker (for clearing jams — 36" dowel)
□ Toolkit: Phillips screwdriver, pliers, zip ties, duct tape, spare wing nuts
□ Signage (booth name banner, scoring rules poster)
□ Folding table (for prizes, if applicable)
□ Prizes (if applicable)
```

### SETUP PROCEDURE (Target: 8 minutes, 2 people)

**Minute 0:00–1:00 — UNLOAD**
- Person A: Carry main board from truck, set face-down on grass
- Person B: Grab both leg assemblies, set near board

**Minute 1:00–2:00 — LEGS ON**
- Person A: Slide T-bolts into keyhole brackets, left side. Quarter-turn. 15 sec
- Person B: Same, right side. 15 sec
- Together: Spread legs, chains catch at 20° tilt. Tip board upright
- Hang sandbags on rear hooks

**Minute 2:00–3:00 — SCOREBOARD**
- Person A: Slide scoreboard bar into U-brackets, insert pins. Plug power cable
- Person B: Power on. Verify LED test sequence (all segments light)

**Minute 3:00–5:00 — QUEUE HARDWARE**
- Person A: Place 4 stanchion bases, insert poles, clip ropes
- Person B: Lay on-deck mats (1-2-3), place exit arrows

**Minute 5:00–6:00 — GAME LOAD**
- Person A: Drop 9 whiffle balls into the top of the board (3 per slot + 6 in the return system)
- Person B: Test all 3 drop handles — verify balls drop and gates reset

**Minute 6:00–7:00 — SYSTEMS CHECK**
- Drop 3 test balls through a full cycle: drop → pegs → buckets → score displays → return → reload
- Verify all 9 bucket sensors fire
- Verify countdown sequence plays
- Verify jackpot sound triggers

**Minute 7:00–8:00 — SIGNAGE & FINAL**
- Hang booth banner
- Place rules poster (one sentence: "PULL THE HANDLE WHEN THE COUNTDOWN HITS DROP!")
- Operator takes position

**GAME ON.**

### DURING OPERATION

**Operator Cadence (Repeat Every 15 Seconds):**
1. "Next three, step to your marks!" (point to on-deck mats)
2. Wait for kids to grab handles
3. "Ready?! THREE... TWO... ONE... DROP!" (press countdown button or let auto-timer run)
4. Watch balls cascade (5 sec)
5. "SCORES! [read them out loud] — Great job! Step to the right!"
6. GOTO 1

**Jam Clearing:**
- If a ball gets stuck between pegs: tap the back of the board (usually clears it)
- If truly stuck: use the dowel poker through the access hole at the top of the board (small hinged door)
- Expected jam rate: ~1 per 50 waves (every ~12 minutes). 10-second fix

**Ball Escape:**
- If a ball pops out the top during a weird bounce: pick it up, drop it back in through the access door
- Spare balls in the backup ziplock handle any losses

**Battery:**
- Scoreboard: 8+ hours on one charge. No swap needed for a standard carnival (4–6 hours)
- If running 8+ hours: swap at lunch break (30-second swap)

**Shift Change:**
- Verbal handoff: "Here's the dowel for jams, battery's at [X], high score is [Y]"
- 30 seconds. No training needed — the operator's job is just hype and crowd control

### TEARDOWN PROCEDURE (Target: 6 minutes, 2 people)

**Minute 0:00–1:00 — QUEUE STRIKE**
- Person A: Unclip ropes, pull stanchion poles, stack on bases
- Person B: Pick up mats and arrows, stuff in a bucket

**Minute 1:00–2:00 — SCOREBOARD**
- Person A: Unplug power, pull pins, slide scoreboard bar out
- Person B: Collect remaining whiffle balls from board (shake board gently, balls fall to bottom buckets, scoop out)

**Minute 2:00–3:30 — BOARD DOWN**
- Together: Tip board onto its face (acrylic side down on grass)
- Unhook sandbags
- Person A: Quarter-turn T-bolts, slide out left legs
- Person B: Same, right side
- Stack legs together, velcro strap bundle

**Minute 3:30–5:00 — LOAD**
- Board goes in truck first (flat, face down, pad underneath)
- Legs alongside
- Stanchion buckets (heaviest, load last against the cab)
- Scoreboard bar, speaker, loose gear on top

**Minute 5:00–6:00 — SWEEP**
- Walk the area: any stray balls, mats, arrows, ropes?
- One final check: battery pack, toolkit, signage
- Done. Drive away.

### RAIN/WIND CONTINGENCY

- **Light rain:** Game plays fine. Acrylic front keeps the playing field dry. Wipe handles between waves if slippery
- **Heavy rain:** Move under a canopy/tent. The game's footprint (48"W × 30"D) fits under a standard 10×10 pop-up tent
- **Wind > 20mph:** Lower the tilt angle by shortening the chain (one link shorter ≈ 5° less tilt). Adds sandbag weight. If sustained gusts, lay board face-down and wait it out
- **Extreme wind/storm:** Teardown immediately. The 6-minute teardown means you can be loaded and gone before it gets bad

---

## Maintenance & Storage

### Post-Event (Same Night)
- Wipe down acrylic with microfiber cloth
- Check spinner peg bearings (spin freely?)
- Check drop gate springs (snappy return?)
- Charge battery packs
- Store board FLAT (not on edge — prevents warp)

### Annual Pre-Season
- Sand and repaint any chipped areas on the board
- Replace drop gate springs (they fatigue — $2 per spring, 5-minute swap)
- Test all 9 sensors with multimeter
- Update high score record (or reset it — your call)
- Verify all T-bolt/keyhole connections are snug

### Storage
- Board stores flat against a garage wall or overhead in ceiling-mount hooks
- Legs bundle together — hang on wall hooks
- All small parts in one labeled bin
- Stanchion buckets stack in a corner

**Total storage footprint: 48"×60" wall space + one bin + one corner**
