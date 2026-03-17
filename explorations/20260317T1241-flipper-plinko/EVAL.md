# Flipper Plinko — Carnival Game Evaluation

## Scoring Rubric
Each heuristic scored 1–10 (10 = best possible).

---

### Overall Entertainment: 6/10
For most of a ball's journey, you're watching — plinko is a spectator experience with gravity doing the work. The flipper adds one decision point per ball at the very end of each pass. Kids who time it right get a satisfying save; kids who miss (most of them, especially early on) just watch the ball drain. The combo scoring system is a nice idea on paper, but achieving multi-pass combos requires flipper timing that most elementary schoolers won't develop in a 3-ball turn. The honest comparison: this is plinko with a single pinball flipper bolted on. It's pleasant and watchable, not riveting.

### Memorability: 5/10
"Remember that plinko game?" — yes, because every carnival has one. The flipper is a differentiator, but a subtle one. Kids who successfully flip a ball back up will remember it; kids who miss every flip will remember a plinko board. The neon-on-black color scheme is visually clean but not unique to this concept. The portability story matters to parent volunteers, not to the kids who are your actual audience. A year later, this blends into the "ball drop games" category in a kid's memory.

### Ease of Construction: 8/10
The pegboard-and-PVC approach is genuinely simpler than plywood-and-lumber alternatives. Most of the parts list is straightforward:
- **Pegboard:** $12, pre-drilled, cuts with a jigsaw
- **Frame:** PVC pipes press into 3D-printed connectors
- **Pegs:** Batch-printed overnight, push into holes
- **Buckets:** Print and hook on

But the flipper mechanism — brake cable routing through PVC, pivot bolts, rubber band springs, lever handle — is the one part that can't be hand-waved. If the cable has too much friction, the flipper feels mushy. If the rubber band tension is wrong, balls dribble instead of launching. This is a mechanism that needs prototyping and tuning, not just assembly. Two evenings is realistic for the pegboard and frame; the flipper alone could eat a third evening of fiddling. Assembly on carnival day is still fast (10-15 minutes, no power tools), which is a real advantage.

### Appeal by Elementary School Grade
| Grade | Appeal (1-10) | Notes |
|-------|--------------|-------|
| K–1st | 6/10 | They enjoy watching balls bounce through colorful pegs, but most kindergartners will miss every flipper attempt. At that point you've handed them a standard plinko board with a confusing lever at the bottom. The plunger launch is satisfying, but the core mechanic (flipper timing) is above their motor skill level |
| 2nd–3rd | 7/10 | Closest to the sweet spot — quick enough reflexes to occasionally hit the flipper, competitive enough to care about scores. But "occasionally" is the key word; most flips will still miss, and the peg cascade between flips is passive watching. They'll enjoy it, not obsess over it |
| 4th–5th | 7/10 | The pinball skill layer keeps it from feeling babyish, which matters at this age. But 4th-5th graders have played actual pinball (or phone pinball) with two flippers, bumpers, and continuous action. One flipper on a gravity board is a downgrade from the reference experience they already have |

### Skill to Luck Spectrum: 7/10 (Decent balance)
**Skill factors:** Flipper timing is genuine skill — too early or late and the ball drains. Launch strength has some effect on trajectory.
**Luck factors:** Once the ball enters the peg field, it's pure plinko chaos. No amount of skill controls which bucket it lands in.
The flipper is a second-chance mechanic, not a core skill loop. A skilled player might successfully flip 1-2 out of 3 balls back up. That's meaningful but limited — most of the scoring outcome is still determined by peg chaos. The strategic layer (combos, launch strength choices) sounds good in a design doc but is unlikely to develop in a 3-ball carnival turn. Score reflects that the flipper does add real skill input to what would otherwise be a pure-luck plinko board, which is worth something.

### Chaos Level: 6/10
Honestly, the lowest chaos score of the three explorations. The peg cascade is visually exciting but contained — balls move in predictable downward paths with random lateral bounces. The flipper adds drama but not pandemonium. There's no air blasting balls sideways, no full-body stomping, no vortex cannons. It's controlled, rhythmic chaos rather than all-out bedlam. That said, when both players have 3 balls cascading simultaneously and are frantically squeezing flippers, the board becomes a neon pinball fever dream.

### Durability: 7/10
**Strong points:** PVC frame is nearly indestructible. 3D-printed PETG pegs can take many impacts. Modular design means individual parts are replaceable without tools.
**Weak points:** Pegboard is cheap *and* flimsy — standard 1/8" hardboard pegboard flexes under load and degrades with humidity. After a few carnivals in a garage, warping is likely. The "shatter-proof polycarbonate" front panel sounds great but adds real cost (~$40-60 for a 4x5 ft sheet) that isn't reflected in the $200 budget; acrylic is cheaper but cracks. Rubber bands on flippers fatigue quickly under repeated use — a busy carnival day could burn through several. The brake cable is the single most failure-prone component: cable stretch, housing friction, and pivot wear all accumulate.
**Modularity is real:** Pull a broken peg, push in a new one. Swap a rubber band. That ease of repair partially compensates for the higher breakage rate of lightweight materials. But "easy to fix" is not the same as "durable."

### Photogenicity: 7/10
Neon pegs on matte black pegboard is a clean look — visible and colorful in photos. The compact 4x5 ft size means the whole game fits in a phone frame, which is a practical advantage over larger builds. Action shots of a kid squeezing the brake lever while a ball cascades through pegs will photograph decently.
The flipper action happens at the bottom of the board, mostly invisible to spectators and cameras behind the player. The game lacks a single visual spectacle moment — no explosion of balls, no dramatic physical action, no "you had to see it" element. It photographs as "a colorful plinko board," which is fine but not share-worthy. The LED upgrade would help but isn't in the base build.

### Onboarding Time: 7/10
**15-second explanation:** "Pull the plunger to launch the ball. Watch it bounce through the pegs. If it drops to the bottom, squeeze this handle to flip it back up. Score as many points as you can. Go."
The plinko part is instantly understood. The flipper concept is familiar from pinball. But flipper *timing* is a real learning curve — the ball arrives at the flipper fast and at unpredictable lateral positions. "One ball to calibrate" is optimistic; most kids will whiff their first 2-3 attempts and some will never connect during a 3-ball turn. A K-1st grader who misses every flip doesn't understand what went wrong, just that the game didn't work for them. The volunteer running the booth will spend time explaining and re-explaining the flipper to frustrated kids, which slows the line.

---

## Summary Scorecard

| Heuristic | Score |
|-----------|-------|
| Overall Entertainment | 6/10 |
| Memorability | 5/10 |
| Ease of Construction | 8/10 |
| Appeal (K–1st) | 6/10 |
| Appeal (2nd–3rd) | 7/10 |
| Appeal (4th–5th) | 7/10 |
| Skill/Luck Balance | 7/10 |
| Chaos Level | 6/10 |
| Durability | 7/10 |
| Photogenicity | 7/10 |
| Onboarding Time | 7/10 |
| **Average** | **6.6/10** |

## Verdict
Flipper Plinko is the logistics winner. It is lighter, cheaper, faster to build, faster to set up, and easier to transport than every other concept in this repo. Those are real advantages that matter on carnival day. If your biggest constraint is volunteer time and vehicle size, this is the strongest option.

The honest trade-off: the gameplay is mild. For most of each turn, the player is watching a ball bounce down a peg board — the same experience available at any carnival plinko booth. The flipper adds a moment of agency, but it's a narrow one, and younger kids will miss it entirely. This concept will not generate lines, will not draw crowds from across the field, and will not be the game kids talk about on Monday.

**Build this if** your school carnival needs a reliable, low-effort booth and you don't have the volunteer hours or workshop space for a more ambitious build. **Don't build this if** you want a flagship game that defines the carnival — Flipper Plinko is a solid supporting act, not a headliner.

### Comparison

| | OG Air Plinko | Tornado Alley | Stomp Rockets | **Flipper Plinko** |
|---|---|---|---|---|
| Average Score | — | 8.1 | 8.8 | **6.6** |
| Construction | Hard | Hard | Medium | **Easy** |
| Transport | Truck | Truck | Truck/SUV | **Sedan** |
| Assembly Time | 45-60 min | 30-45 min | 30-45 min | **10 min** |
| Total Weight | ~85 lbs | ~70 lbs | ~90 lbs | **~30 lbs** |
| Total Cost | $350-400 | $300-350 | $280-330 | **~$200** |
| Tools Needed | Drill, wrench | Drill, wrench | Drill, saw | **None** |
| Year-Over-Year | Rebuild needed | Rebuild needed | Rebuild needed | **Snap together** |

**Biggest risk:** The flipper pneumatics — er, mechanics. The brake-lever-to-cable-to-flipper chain has multiple failure points. Prototype one flipper assembly first and abuse-test it with 500 squeezes before committing to the full build. If the cable routing through PVC pipes creates too much friction, switch to external cable routing with 3D-printed guides.

**Biggest upgrade opportunity:** Swap the standard pegboard for 1/4" white pegboard and add RGB LED strips behind it. The pegs cast shadows, the board glows, and the game becomes more visually distinctive at evening carnivals. This is a $15-20 addition that addresses the photogenicity weakness — though it doesn't fix the core gameplay limitation.
