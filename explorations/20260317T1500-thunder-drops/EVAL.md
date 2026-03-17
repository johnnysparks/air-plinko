# Thunder Drops — Carnival Game Evaluation

## Scoring Summary

| Heuristic | Score (1–10) | Notes |
|-----------|:---:|-------|
| Overall Entertainment | **7** | The core plinko-with-a-crank mechanic is solid, and the candy payoff gives it a real hook. But five layered sensory systems on paper is not five working sensory systems on carnival day. Fog dissipates in outdoor heat, mist is a liability near electronics, and each subsystem is a point of failure a parent volunteer has to troubleshoot. The game that works is a decorated plinko board with candy and wind chimes — which is good, not transcendent |
| Memorability | **7** | "The game that rains candy" is a strong hook — candy-as-scoring alone makes it stick. The claim that petrichor fog and eucalyptus mist "lock this into long-term memory" is pseudo-neuroscience dressing up a fog machine and a garden sprayer. A plinko board with a fog machine is not a transformative sensory experience. It's a plinko board with a fog machine. The candy angle is genuinely memorable; the rest is set dressing that may or may not be running |
| Ease of Construction | **4** | The original score of 5 was one of the more honest numbers here, but it still understates the problem. This is a 4-weekend build with 5 subsystems, Arduino programming, waterproofing for mist-near-electronics, conformal coating, and $750–850 in materials — more than double the base concept cost. For a school carnival where the norm is "parent builds a booth in a Saturday," this is a serious barrier. Most carnival committees will not approve this budget or this timeline |
| Appeal by Elementary School Grade | **8** | K–1: candy + loud noises + stomping = reliable fun. 2–3: competitive candy tiers add motivation. 4–5: crank mastery and jackpot chasing. The grade spread is real. Loses points because the crank mechanism requires grip strength that youngest K players will struggle with, and the sensory spectacle (fog, mist, blacklights) only lands if those systems are actually running — which is not guaranteed |
| Skill to Luck Spectrum | **8** | Crank tension controlling launch height is a genuine skill input. Plinko cascade is pure chance. ~40/60 skill-to-luck is a good ratio for a carnival game — enough skill for repeat play, enough luck that a kindergartner can beat a 5th grader. This score holds up |
| Chaos Level | **8** | Wind chimes creating random melodies, multiple balls cascading, candy dispensing — the observable chaos is real and entertaining. Docked from 9 because the fog/lightning/mist chaos only exists when those systems are functioning. The baseline chaos (balls + chimes + candy) is an 8. The aspirational chaos (add fog, LED lightning, mist spray) would be a 9 but cannot be scored for the ideal scenario |
| Durability | **5** | The base plinko structure (plywood, cedar pegs, acrylic) is sturdy and reusable. But this concept defines itself by its five sensory systems, and three of them have real durability problems. Mist jets near Arduino wiring and LED strips is water-near-electronics at an outdoor school event — conformal coating helps but is not foolproof, and one rain or aggressive mist cycle can kill components. Fog machines are consumer-grade and unreliable after a season. Solenoid valves corrode. The mechanical candy system (gravity + levers) is the one subsystem that will actually last. Scoring for what will realistically survive 2–3 carnival seasons, not the ideal case |
| Photogenicity | **7** | At night with blacklights, fog, and neon pegs all working: genuinely photogenic, maybe a 9. But score for the likely scenario: daytime, outdoor, fog machine struggling in heat, LEDs washing out in sunlight, mist system maybe running. In that reality it's a colorfully decorated plinko board — nice-looking but not the light show promised. The neon color scheme is visible from a distance and the candy moment photographs well regardless, which saves the score |
| Onboarding Time | **8** | "Crank the handle. Pull the lever. Watch your ball. Catch your candy." Four sentences. The crank mechanism has a small learning curve, but the first launch teaches everything. This score holds up — onboarding is straightforward |

## Overall Score: **6.9 / 10**

## Strengths
1. **Candy-as-scoring is genuinely clever incentive design.** Kids don't need a scoreboard. The candy IS the score — immediate, tangible, and motivating. The full-size jackpot bar is a real draw. This mechanic alone justifies interest in the concept
2. **The chime cascade is a real differentiator.** 40 aluminum tubes at varying pitches means every ball run sounds different. This is low-cost, durable, zero-failure-risk, and unlike anything else at a carnival. The chimes are the best-designed subsystem in the concept
3. **Strong grade-range appeal.** The crank-to-plinko-to-candy loop works for K through 5th grade with different appeal at each level. Few carnival games genuinely engage the full elementary range
4. **The fog reveal moment is a good idea — when it works.** Ball disappears, reappears in the peg field. As a concept it adds real spectator drama. The problem is reliability, not the idea itself

## Weaknesses
1. **Five sensory systems means five points of failure.** Fog machine, Arduino/LED lightning, wind chimes, mist solenoids, candy dispensers. On carnival morning at 7am, a parent volunteer who arrived 10 minutes ago is responsible for all of these. Chimes and candy dispensers are robust. The other three are finicky electronics-plus-moisture systems that each need monitoring. When (not if) the fog machine dies or a solenoid sticks, the game degrades to a decorated plinko board — which is fine, but not what justified the $800 budget
2. **Cost is a dealbreaker for most school carnivals.** $750–850 is 2× the base concept and 3–4× what most carnival booths cost. School carnival budgets are typically $50–150 per booth. This needs explicit fundraising or sponsorship, and most carnival committees will pick three simpler games over one expensive one. This single factor should disqualify the concept from a default "build it" recommendation
3. **Water near electronics at an outdoor event.** Mist jets and fog machines produce moisture. Arduino boards, LED strips, and solenoid connections are nearby. Conformal coating and sealed enclosures mitigate this but add build complexity and are not foolproof. One aggressive mist cycle, one unexpected rain, one condensation buildup — and you're debugging dead electronics at a children's event
4. **Fog machine restrictions and practicality.** Some schools prohibit fog machines (fire alarms, asthma liability). Even where allowed: consumer fog machines overheat, need fluid refills, and produce visible output for ~30 seconds before needing recovery time. At 90°F outdoors the fog dissipates almost instantly. The signature "fog zone" may be more concept than reality
5. **The 4-weekend build timeline excludes most volunteers.** Two parents with tools and Arduino experience, four weekends, waterproofing, programming, integration testing. This is a hobby project, not a carnival booth build. The typical carnival setup is "buy plywood, cut holes, paint it, done in a weekend"

## Comparison to Other Explorations

| | Thunder Drops | Stomp Rockets | Tornado Alley |
|---|:---:|:---:|:---:|
| Entertainment | 7 | 10 | 9 |
| Memorability | 7 | 10 | 9 |
| Ease of Construction | 4 | 7 | 6 |
| Grade Appeal | 8 | 9 | 8 |
| Skill/Luck | 8 | 7 | 7 |
| Chaos | 8 | 9 | 8 |
| Durability | 5 | 8 | 7 |
| Photogenicity | 7 | 8 | 8 |
| Onboarding | 8 | 9 | 8 |
| **Average** | **6.9** | **8.6** | **7.8** |

Thunder Drops sacrifices buildability, durability, and budget-friendliness for a sensory concept that only delivers its full promise under ideal conditions. The core loop (crank + plinko + candy + chimes) is a 7–8 game. The additional three systems (fog, LEDs, mist) add cost, complexity, and fragility for marginal gain on carnival day.

## Build-or-Kill Verdict

**BUILD THE CORE. SKIP THE SPECTACLE.** The candy-dispensing plinko board with wind chimes is a genuinely good carnival game — fun, memorable, buildable in 2 weekends, and under $400. That version scores in the high 7s and is an easy recommendation.

The five-sense version as designed? Don't build it for a school carnival. The $800 budget, 4-weekend timeline, Arduino programming, waterproofing requirements, and five-subsystem fragility put it outside what school carnival volunteers can reliably execute and maintain. It's a cool maker project for someone who wants to build it for its own sake — but a carnival committee should spend that $800 on two simpler games that will definitely work on event day.

If you're committed to the theme, add the fog machine and LED lightning as optional stretch goals after the base game is proven. But don't design around them and don't budget for them up front.
