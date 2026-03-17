# Flipper Plinko — Build Plan

## Concept
Snap-together pinball/plinko hybrid built on hardware-store pegboard. Balls cascade through snap-in pegs, score in hook-on buckets, and get saved by pinball flippers at the bottom. Entire game packs into two flat bundles + a duffel bag. Zero tools to assemble. 30 lbs total.

## Overall Dimensions

| Dimension | Size | Notes |
|-----------|------|-------|
| Width | 48" (4 ft) | Two-player side-by-side |
| Height | 60" (5 ft) | Playable standing for kids & adults |
| Depth (gap) | 4" | Whiffle ball (2.75") + peg clearance |
| Tilt angle | ~20° from vertical | Balls roll down, flippers launch up |
| Frame footprint | 48"W × 24"D × 62"H | PVC frame with rear legs |

Transport size: Panel bundle 48"×60"×1", frame kit bag 36"×12"×8"

---

## Architecture

### 1. Frame — PVC Snap-Together Skeleton

**Pipes:** ¾" Schedule 40 PVC conduit, cut to length:
- 2× vertical uprights: 62" (front face, left & right)
- 2× horizontal crossbars: 48" (top & bottom of playing field)
- 2× rear legs: 48" (angled back for tilt)
- 2× rear cross-braces: 46" (lateral stability between rear legs)
- 2× diagonal braces: 24" (connect uprights to rear legs at top)

**3D-Printed Connectors (PLA or PETG):**
- 4× corner joints (90° elbow with channel rail for panels)
- 2× top T-joints (upright-to-crossbar-to-diagonal)
- 2× bottom T-joints (upright-to-crossbar-to-rear-leg)
- 2× rear leg feet (with rubber bumper recess)
- 2× rear brace clips (snap onto rear legs at 24" height)

**Assembly:** All joints are friction-fit with a 3D-printed retaining clip that snaps over the joint to lock it. No glue, no screws. Pull the clip to disassemble.

**Channel Rails:** Each corner joint includes an integrated channel (slot) that accepts the pegboard and polycarbonate panels. Panels slide in from the top, gravity + a top crossbar clip holds them.

### 2. Playing Surface — Standard Pegboard

- **Material:** ¼" tempered hardboard pegboard, 48"×60" (cut from standard 4×8 sheet)
- **Hole pattern:** Standard 1" center-to-center, ¼" holes
- **Weight:** ~8 lbs
- **Finish:** Spray painted matte black (pegs pop against dark background)
- **Mounting:** Slides into channel rails on the PVC frame

### 3. Front Panel — Clear Polycarbonate

- **Material:** ⅛" clear polycarbonate (Lexan), 48"×60"
- **Weight:** ~10 lbs
- **Mounting:** Slides into front channel rails on same corner joints
- **Gap:** 4" between pegboard and polycarbonate (set by connector depth)
- **Access:** Slides out the top for peg reconfiguration between games

### 4. Snap-In Pegs (3D Printed)

- **Quantity:** ~80 pegs in offset rows
- **Design:** Mushroom-cap peg with a ¼" post that press-fits into pegboard holes. Cap diameter: 1.5". Post length: 1"
- **Material:** PETG (tough, slight flex, won't shatter)
- **Colors:** Neon green, neon orange, neon pink, neon blue — alternating rows
- **Layout:** Offset grid, 3" horizontal spacing, 4" vertical spacing, starting 12" from bottom (above flipper zone)
- **Reconfigurability:** Pull pegs out, push into different holes. Easy mode (wide spacing) for K-1st, chaos mode (tight zigzag) for 4th-5th

### 5. Scoring Buckets (3D Printed + Pegboard Hooks)

- **Design:** Open-top trays with pegboard hook backs. Ball rolls in, sits in bucket until round ends.
- **Sizes & scoring:**

```
        [JACKPOT 100] ← top center, 3" wide, hardest to reach
       /              \
   [50 pts]        [50 pts] ← upper wings, 4" wide
      |                |
   [25 pts]        [25 pts] ← mid sides, 5" wide
      |                |
   [10 pts ——————————— 10 pts] ← wide bottom shelf, 8" each side
      |                |
   [FLIPPER ZONE ————— DRAIN]
```

- **Hook style:** Standard pegboard hook back — same as hardware store bins. Push on, lift off.
- **Lip:** 1" front lip keeps balls from bouncing out
- **Drainage:** Each bucket has a rear hole. Ball rolls through, drops behind pegboard, slides down rear chute to ball return.

### 6. Flipper System

**Per player (×2):**
- **Paddle:** 3D-printed, 8" long, 1.5" wide, flat profile. Mounted on a ¼" steel pivot bolt through the bottom crossbar rail.
- **Spring return:** Rubber band (or small spring) pulls flipper to resting position (~10° above horizontal)
- **Actuation:** Bicycle brake lever mounted on the side upright at hip height. Brake cable runs inside the PVC pipe to a pull arm on the flipper pivot.
- **Sweep:** 60° swing (from 10° rest to 70° up)
- **Flipper trough:** Angled channel (3D-printed, hooks onto pegboard) that funnels balls from the center toward the flipper sweet spot. 6" long, 3" wide, 10° inward slope.

**The feel:** Squeeze the brake lever → cable pulls → flipper swings up with a satisfying *thwack* → ball arcs back into the peg field. Release → rubber band snaps flipper back down. Tactile, responsive, mechanical.

### 7. Ball Launcher (×2)

- **Type:** Spring-loaded pinball plunger
- **Position:** Bottom-left and bottom-right corners
- **Channel:** Short 3D-printed ramp that hooks onto pegboard, angled 60° upward. Ball sits in cradle, pull plunger, release, ball arcs up and into the peg field.
- **Plunger mounting:** Bolted through the bottom crossbar with a wing nut (the only threaded fastener in the whole build)

### 8. Ball Return System

- **Gutter:** Balls that miss the flippers drop through a slot in the bottom crossbar into a 3D-printed trough behind the pegboard
- **Rear chute:** Angled channel attached to the back of the pegboard (hooks on), funnels all balls (from gutters + bucket drainage) to a collection bin at the base
- **Collection bin:** Open box at the bottom rear. Players grab balls manually to reload the launcher.
- **Why manual reload:** Eliminates the most complex part of the OG design (auto ball return). One fewer thing to break. Kids don't mind grabbing a ball — it's a 2-second pause between launches.

### 9. Center Divider

- **3D-printed vertical rail** that hooks onto pegboard at the center line, from bottom crossbar up to ~24" height
- **Purpose:** Separates player flipper zones — your ball goes to your flipper
- **Above 24":** No divider — balls from either player can reach any bucket, creating competitive tension ("they're going for MY jackpot!")

---

## Materials List

### Pegboard & Panel
| Item | Qty | Est. Cost |
|------|-----|-----------|
| ¼" pegboard sheet (4×8, cut to 4×5) | 1 | $12 |
| ⅛" clear polycarbonate (4×5 cut) | 1 | $55 |

### PVC Frame
| Item | Qty | Est. Cost |
|------|-----|-----------|
| ¾" PVC conduit (10 ft sticks) | 3 | $9 |
| PVC pipe cutter (if not owned) | 1 | $8 |

### 3D Printed Parts (~1.5 kg filament total)
| Item | Qty | Est. Cost |
|------|-----|-----------|
| PETG filament (1kg spool, neon colors) | 2 | $40 |
| Connector joints (corners, tees, feet) | 12 | (printed) |
| Snap-in pegs | ~80 | (printed) |
| Scoring buckets | 7 | (printed) |
| Flipper paddles | 2 | (printed) |
| Flipper trough channels | 2 | (printed) |
| Launch ramps | 2 | (printed) |
| Ball return chute pieces | 3 | (printed) |
| Center divider rail | 1 | (printed) |

### Hardware
| Item | Qty | Est. Cost |
|------|-----|-----------|
| Pinball plunger assemblies | 2 | $16 |
| Bicycle brake levers + cables | 2 | $10 |
| ¼" steel bolts + wing nuts (flipper pivots) | 4 | $4 |
| Rubber bands (flipper return springs) | 1 bag | $3 |
| Rubber chair leg caps (frame feet) | 4 | $4 |
| Matte black spray paint | 2 cans | $10 |
| Neon spray paint (accent) | 2 cans | $10 |

### Game Pieces
| Item | Qty | Est. Cost |
|------|-----|-----------|
| Whiffle balls (colored, red + blue) | 12 pack | $8 |
| Adhesive vinyl numbers (scoring) | 1 sheet | $5 |

### **Estimated Total: $195–210**

Half the cost of the OG Air Plinko. No acrylic. No plywood. No lumber.

---

## Build Sequence

### Phase 1: Print Week (Evenings, ~40 hrs print time)
1. Print all connector joints (8 hrs)
2. Print pegs in batches of 20 per plate (4 plates × 3 hrs = 12 hrs)
3. Print scoring buckets (7 × 1.5 hrs = 10 hrs)
4. Print flipper components — paddles, troughs, pull arms (4 hrs)
5. Print launch ramps + ball return chute (4 hrs)
6. Print center divider rail (2 hrs)

*Run prints overnight. Actual hands-on time: ~2 hrs total (slicing, bed prep, part removal)*

### Phase 2: Frame & Panels (Saturday Morning, 2 hrs)
1. Cut PVC pipes to length (10 cuts with pipe cutter)
2. Test-fit all connector joints — sand any tight fits
3. Assemble frame, verify it stands square
4. Cut pegboard to 48"×60" (circular saw or jigsaw)
5. Spray paint pegboard matte black, let dry
6. Test panel slide into channel rails

### Phase 3: Flipper & Launcher (Saturday Afternoon, 2 hrs)
1. Drill flipper pivot holes in bottom crossbar (2 holes)
2. Assemble flipper mechanisms — bolt through pivot, attach rubber band return
3. Route brake cables from levers through PVC uprights to flipper pull arms
4. Mount pinball plungers at bottom corners with wing nuts
5. Attach launch ramp channels
6. Test flipper action — adjust cable tension until satisfying snap

### Phase 4: Assembly & Playtest (Sunday Morning, 1 hr)
1. Full assembly from packed state — time it (goal: under 10 minutes)
2. Pop in all pegs — test offset layout
3. Hook on scoring buckets
4. Hook on ball return chute behind pegboard
5. Slide in polycarbonate front panel
6. Test with whiffle balls — launch, cascade, flip, score, return
7. Adjust peg layout if balls get stuck or path is too predictable
8. Apply scoring vinyl numbers to buckets

### Phase 5: Transport Test (Sunday Afternoon)
1. Full disassembly — time it (goal: under 5 minutes)
2. Pack into panel bundle (pegboard + polycarbonate, rubber-banded)
3. Pack frame kit into duffel bag
4. Load into car. Confirm it fits. Drive around the block.
5. Unload. Reassemble. Verify nothing loosened in transit.

---

## Transport Comparison

| | OG Air Plinko | Flipper Plinko |
|---|---|---|
| Weight | ~85 lbs | ~30 lbs |
| Vehicle needed | Truck/SUV | Any sedan |
| Assembly time | 45-60 min | 10 min |
| Tools for assembly | Drill, wrench | None (1 wing nut by hand) |
| People to carry | 2 | 1 |
| Storage footprint | 48"×60"×8" rigid | 48"×60"×1" flat + duffel |
| Cost | $350-400 | $195-210 |

---

## Open Questions
- [ ] Flipper cable routing — brake cable inside PVC pipe confirmed feasible?
- [ ] Polycarbonate flex — will ⅛" flex too much at 48" wide unsupported span? May need a mid-height horizontal PVC stiffener
- [ ] Peg durability — PETG snap-in pegs after 500 ball impacts? Print 20 spares
- [ ] Pegboard paint adhesion — primer needed on tempered hardboard?
- [ ] Max ball speed off flipper — too fast = balls fly over buckets. Test with different rubber band tensions
