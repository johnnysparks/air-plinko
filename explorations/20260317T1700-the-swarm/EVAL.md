# THE SWARM — Carnival Game Evaluation

## Scoring (1–10 scale)

### Overall Entertainment: 8/10
The stomp pads are a genuine upgrade over plungers — full-body jumping is inherently more engaging than pulling a spring. Simultaneous two-player action means both kids are active the entire round, solving Buzz Ball's idle-half-the-time problem. The hex pegs and multi-ball interactions are visually interesting.

But the entertainment case rests on three ambitious subsystems all working: (1) the stomp-to-pneumatic-launch pipeline, (2) the Queen Bee Spinner catching and ejecting balls reliably, and (3) the candy dispensing. If ANY of these is unreliable on carnival day, the experience degrades fast. A stomp pad that launches balls inconsistently is worse than a plunger that always works. A Queen Spinner that balls bounce off of instead of entering is a decorative obstacle, not a mechanic. The candy dispensing gates are the most fragile mechanism — if they jam (and weight-activated gates will jam), the beekeeper is manually dropping candy behind the board all day, which breaks their ability to crank.

The beekeeper volunteer is still the most interesting role, not the player's. The player stomps and watches. It's a MORE interesting watch than Buzz Ball (more balls, more happening), but the fundamental loop is still "provide input, then spectate." Two docks: the player agency ceiling, and the mechanical reliability risk.

### Memorability: 8/10
The concept IS visually and mechanically distinct from anything at a typical school carnival. Nobody has a stomp-launched hex plinko board with a rotating drum in the center. The bee theming is cohesive and tied to Grattan specifically. A kid would describe this as "the game where you JUMP on flowers and balls go into a spinning thing" — that's a distinctive description.

However: memorability requires the signature moments to actually happen. The Queen Bee Spinner is memorable IF balls reliably enter and exit it. If the drum openings don't line up well with ball trajectories, most balls just bounce off the drum's exterior like an oversized peg. The "ball gets swallowed by the Queen" moment needs to happen at least 3-4 times per round to register as a mechanic rather than a fluke. This has not been playtested. The fog zone is memorable IF the fog machine works outdoors — fog dissipates in seconds in any breeze, and Michigan spring weather is unpredictable. The multi-sensory elements (beeswax scent, bass hum) are subtle enough that most kids won't consciously notice them in the excitement of play.

Compared to Wreck-O-Rama's tower-smashing crash (visceral, zero mechanical risk, impossible to not notice), the memorable moments here require more things to go right.

### Ease of Construction: 4/10
This is the most complex build in the exploration set by a significant margin. The subsystem count:

1. Standard plinko board with hex pegs (straightforward)
2. Pneumatic stomp pad launchers with bladders, hoses, check valves, calibrated launch tubes (moderate — pneumatics are finicky, leaks are common, stomp force varies dramatically by child weight from 35lb to 120lb)
3. Queen Bee Spinner with bearing mount, belt drive, 6-slot drum (hard — tolerances matter, a 10" drum with 3" slots that balls reliably enter is precision work, belt tension affects spin speed which affects gameplay)
4. Cam-driven bee bumper mechanism (hard — same precision concerns as Buzz Ball but now sharing a drive system with the Queen)
5. Candy dispensing with weight-activated gates on 7 buckets (fragile — this mechanism works in theory, rarely works reliably in practice with variable ball weights and velocities)
6. Sensory systems: fog machine + UV strip + bass transducer + beeswax warmer + mist jets (individually trivial, collectively a wiring and maintenance burden)

A two-dad team with Milwaukee tools can build a plinko board in a weekend. Adding stomp pads is another weekend. Adding the Queen Spinner and bumper mechanism is another weekend. Calibrating everything to work together is AT LEAST another weekend. That's 4 weekends minimum, probably 5-6 once you hit issues — and you will hit issues, because the pneumatic calibration changes with temperature, the belt drive needs tuning, and the candy gates need redesigning after the first test.

The 3D printing load (~85 hours) is manageable with a Bambu printer across 3 weeks. But it's not just printing — it's designing, test-fitting, reprinting, and iterating. The Queen Bee Spinner drum is the riskiest print: 6 sections that need to assemble into a balanced, smooth-spinning drum with precise slot openings.

**Honest build risk:** If you're not comfortable debugging pneumatic leaks, adjusting belt tensions, and redesigning 3D-printed mechanisms after failed tests, this build will be frustrating. The number of "calibrate until it works" steps is high.

### Appeal by Elementary School Grade: 8/10
| Grade | Appeal | Notes |
|-------|--------|-------|
| K–1 | 6/10 | Love the idea of stomping. But a 40lb kindergartner's stomp produces dramatically less air pressure than a 90lb 4th grader's. If the launcher is calibrated for older kids, the K's balls dribble out of the launch tube. If calibrated for K's, older kids overshoot. This is a real design problem — pneumatic systems are sensitive to input force variation. You either exclude the littlest kids or accept wildly inconsistent launch heights |
| 2–3 | 9/10 | Sweet spot. Enough weight to generate good stomps. Old enough to figure out force control. Young enough to lose their minds at the Queen Spinner. This age group will have the most fun |
| 4–5 | 8/10 | Will enjoy the competitive element and will develop stomp strategies. May get frustrated that the Queen Spinner outcome is random regardless of skill — older kids want mastery, and this game caps mastery below the Queen's influence |
| Adults | 7/10 | Fine to play once. The stomp pads are more engaging than a plunger. But adults will quickly see through the randomness — the Queen Spinner is a roulette wheel, and no amount of stomping skill changes what it does. The sensory elements won't register much in the bustle of a carnival |

### Skill to Luck Spectrum: 7/10 (decent, with a structural problem)
- **Skill component:** Stomp force controls launch height. Stomp cadence controls ball volume. These are real skill expressions — a player who learns to stomp consistently at mid-force WILL score better than random stomping
- **Luck component:** Hex pegs add 6-directional chaos. Bee bumpers add crank-timing randomness. Multi-ball collisions are unpredictable. These are fine amounts of luck for a carnival game
- **The structural problem:** The Queen Bee Spinner. It's the centerpiece of the game, positioned in the highest-traffic zone of the board, and it's pure roulette. A ball enters, rattles around, and exits from whichever of 6 slots happens to face down. No amount of player skill influences the outcome. If 30-40% of balls hit the Queen (which the placement encourages), 30-40% of the game outcome is pure chance. That's not "skill with luck" — that's "skill until the Queen takes over." Compare to regular plinko where EVERY peg interaction is a small random event and skill accumulates across many of them. The Queen is a single, large random event that dominates the scoring of any ball that enters it

### Chaos Level: 8/10
Multi-ball simultaneous play is genuinely chaotic. Both players stomping at once means 4-6 balls in the field at a time — ball-on-ball collisions, emergent interactions, cross-player chaos. This is a real advantage over Buzz Ball's one-ball-at-a-time format.

The Queen Spinner adds unpredictability. The bee bumpers add surprise. The hex pegs scatter balls in 6 directions.

Docked because: the fog zone, described as adding suspense, actually obscures the chaos. If balls vanish into fog for 2 seconds, spectators can't SEE the chaotic bouncing in the top third of the board — the most visually interesting zone (where balls enter and scatter). Fog trades visibility for atmosphere. That's a legitimate design choice, but it costs chaos POINTS because chaos you can't see doesn't register as chaos. Also: outdoor fog machines in any breeze produce approximately nothing. The fog zone may simply not exist on carnival day.

### Durability: 6/10
This game has more moving parts and failure points than any other concept in the set:
- **Stomp pad bladders:** Rubber under repeated high-force impact. Will develop leaks. When a bladder leaks, that player's launcher fails — half the game is down until you swap it (10-minute job, but 10 minutes with 15 kids in line feels like an hour)
- **Pneumatic hoses:** Connections can pop under pressure spikes from aggressive stomps. You'll need hose clamps and spares
- **Queen Bee Spinner bearing:** Consumer lazy susan bearings have play. Under repeated ball impacts inside the drum, the bearing will develop wobble. The drum may start catching on the acrylic front or backboard
- **Belt drive:** Timing belts stretch. Belt tension changes how the Queen spins. A loose belt on carnival morning means the Queen barely turns. Over-tight means the crank is exhausting for the beekeeper
- **Cam mechanism:** Same durability concerns as Buzz Ball — springs fatigue, cam surfaces wear, pushrods develop slop
- **Candy dispensing gates:** The highest-failure-rate mechanism. Ball weight variation (whiffle balls are light), impact velocity variation, and gate alignment all contribute to either jam (no candy) or dump (all the candy at once). Expect this to need manual override
- **Board, pegs, acrylic, frame:** Fine. These are the same proven components as every other concept

The modular design helps — everything is swappable. But swappable means you need SPARES. The spare parts kit for this game is larger than most concepts' entire parts list. Pre-carnival maintenance is 45-60 minutes, not 30.

### Photogenicity: 7/10
The hex board in gold-and-black is visually strong and reads as intentional from a distance. The flower stomp pads are colorful and fun to photograph — kids mid-jump is good content. The beekeeper in a hat and veil is a character. Multi-ball cascading through hex pegs is visually interesting.

But the two highest-hype visual elements don't survive outdoor daylight:
- **UV-reactive balls under blacklight:** UV strips are invisible in sunlight. The balls will look like regular yellow whiffle balls during a daytime carnival. This effect only works at dusk or indoors. Scoring the UV as a 10/10 photo feature assumes evening play, which most school carnivals aren't
- **Golden fog zone:** Fog machines outdoors in any breeze produce a wisp that dissipates in 2 seconds. In still air, maybe you get a haze. In the typical Michigan spring breeze, the fog machine is a $25 paperweight. The "balls vanishing into golden fog" moment probably doesn't happen

What IS photogenic: the hex board itself, the stomp action, the beekeeper, the Queen Spinner visible through acrylic, the candy chute moment. These work in any lighting. That's a solid 7, not a 10.

### Onboarding Time: 8/10 (fast, with one complication)
- "Stomp the flowers, launch balls, highest score wins" — near-instant understanding
- Stomping is intuitive. Every kid knows how to jump
- Point values are on the buckets. "STOMP HERE" on the pads
- Kids in line watch and learn before their turn

The complication: candy. The promise of candy on every score means kids expect immediate candy. If the dispensing mechanism jams or is delayed, you get confused/disappointed kids and a beekeeper who's troubleshooting candy tubes instead of cranking. The beekeeper's role is already split (crank the Queen/bumpers AND ring the bell AND control the mist jets AND manage candy), which is a lot for one volunteer. A second volunteer dedicated to candy/scoring would help, but that's twice the staffing.

Also: the 60-second timer adds operational overhead. Someone needs to time rounds, signal start/stop, and manage the transition between players. This is manageable but not zero-onboarding.

---

## Summary

| Criterion | Score |
|-----------|-------|
| Overall entertainment | 8/10 |
| Memorability | 8/10 |
| Ease of construction | 4/10 |
| Appeal by grade | 8/10 |
| Skill/luck balance | 7/10 |
| Chaos level | 8/10 |
| Durability | 6/10 |
| Photogenicity | 7/10 |
| Onboarding time | 8/10 |
| **Average** | **7.1/10** |

## Verdict

THE SWARM is the most ambitious concept in the exploration set. It combines the best mechanics from 7 different explorations into a single, cohesive, Grattan-branded bee game. The stomp pads solve Buzz Ball's passivity problem. Simultaneous play solves the idle-time problem. The Queen Bee Spinner is a genuinely novel mechanic. The bee theming is cohesive and school-specific.

The honest trade-off is reliability for ambition. Every subsystem that makes this game better than Buzz Ball also makes it harder to build, harder to maintain, and more likely to malfunction. The pneumatic stomp system is sensitive to child weight variation. The Queen Spinner needs precision tolerances. The candy dispensing is fragile. The fog and UV effects don't work outdoors in daylight. The beekeeper is managing 4+ responsibilities simultaneously.

**Build it if:** You have 5-6 weekends, a 3D printer, at least one builder comfortable debugging mechanical systems, AND you're willing to accept that some subsystems may need to be simplified or cut on carnival day. The fog machine might stay in the box. The candy tubes might be replaced by a volunteer handing out treats. The UV strip might be decorative. The core game — stomp pads + hex pegs + Queen Spinner + bee bumpers — is strong enough to carry the experience even if the sensory systems don't perform.

**Don't build it if:** Your build team tops out at basic woodworking, you have fewer than 3 weekends, or you can't guarantee two volunteers at the booth (one cranking, one managing operations). This game's failure mode is "half the mechanisms don't work and it's a confusing plinko board with broken stomp pads." A simpler concept executed perfectly will beat an ambitious concept executed halfway.

**The honest comparison to Buzz Ball:** THE SWARM fixes Buzz Ball's biggest weaknesses (passive play, one-ball-at-a-time) at the cost of Buzz Ball's biggest strength (relative simplicity). They score the same average (7.1), which is revealing: THE SWARM is the higher-ceiling, lower-floor version. When everything works, it's better. When things go wrong, it's worse. Choose based on your build team's confidence and appetite for mechanical complexity.
