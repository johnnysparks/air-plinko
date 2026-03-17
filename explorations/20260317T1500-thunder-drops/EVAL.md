# Thunder Drops — Carnival Game Evaluation

## Scoring Summary

| Heuristic | Score (1–10) | Notes |
|-----------|:---:|-------|
| Overall Entertainment | **10** | Five-sense immersion creates an experience, not just a game. Fog, lightning, chimes, mist, candy — every second is happening |
| Memorability | **10** | "The game that sprays you and rains candy." Smell is the most memory-linked sense — petrichor fog and eucalyptus mist lock this into long-term memory. Kids will describe this to friends for years |
| Ease of Construction | **5** | Honest assessment: this is a 4-weekend build, not 2. The base plinko board is straightforward, but the five sensory systems (fog, LED/Arduino, chimes, mist/solenoids, candy dispensers) each add a mini-project. Two dads with Milwaukee tools can do it, but they'll earn it |
| Appeal by Elementary School Grade | **9** | K–1: stomping, spraying, candy, LOUD — pure joy. 2–3: strategy emerges (how many cranks?), competitive mode, candy tiers motivate. 4–5: mastering the crank, chasing the 500-pt jackpot, developing stomp-vs-finesse strategies. Loses one point because the crank mechanism requires some grip strength that the youngest K players might struggle with |
| Skill to Luck Spectrum | **8** | Skill: crank tension directly controls launch height (3 cranks vs 7). Over-cranking is punished. Experienced players learn the sweet spot. Luck: plinko cascade is pure chaos once the ball enters the peg field — nobody controls which bucket it lands in. The fog zone adds beautiful uncertainty. Ratio: ~40% skill / 60% luck — enough skill for repeat play, enough luck that a kindergartner can beat a 5th grader |
| Chaos Level | **9** | Balls vanishing into fog then erupting through neon pegs. Wind chimes creating random melodies. Lightning flashing. Mist spraying. Thunder rumbling. Multiple balls cascading simultaneously. This is controlled mayhem — the good kind where the chaos IS the entertainment. Not quite 10 because the crank-and-release is methodical (intentional pacing) |
| Durability | **7** | The base plinko structure (plywood, cedar pegs, acrylic) is tank-grade — years of reuse. Wind chimes are zip-tied and easily replaced. 3D-printed mushroom caps can be reprinted. Electronics (Arduino, LEDs, solenoids) are the weak point — moisture from mist jets near wiring requires careful sealing. Fog machine and pump sprayer are consumer-grade and may need replacement every 2-3 seasons. Candy system is pure mechanical (gravity + levers) — nearly indestructible |
| Photogenicity | **10** | This game was born for photos and video. Blacklight neon glow pegs. Fog rolling across the board. LED lightning flashes. Kids getting misted mid-celebration. Glowing UV balls cascading through a neon forest. After dark? This becomes a straight-up light show. Parents will be filming TikToks. The game photographs itself |
| Onboarding Time | **8** | "Crank the handle. Pull the lever. Watch your ball. Catch your candy." Four sentences. The crank mechanism has a tiny learning curve (how hard to crank?) but the first launch teaches everything. Loses 2 points vs perfect cornhole-simplicity because the crank-pull-release is one step more complex than "throw the thing" |

## Overall Score: **8.4 / 10**

## Strengths
1. **Only carnival game that hits all five senses.** This is the differentiator. No other booth smells like rain, sprays you with mist, feeds you candy, AND shakes your ribs with bass. It's not a game — it's a 60-second weather event
2. **Night mode is a killer feature.** After dark, blacklights + fog + LED lightning + neon glow pegs = the booth draws crowds from across the festival. Most carnival games look the same day and night. This one transforms
3. **Candy-as-scoring is genius-level incentive design.** Kids don't need a scoreboard. They don't need to count. The candy IS the score. Immediate, tangible, delicious feedback. The full-size jackpot bar is legendary-tier motivation
4. **The fog zone creates spectator drama.** Ball disappears into clouds → 2 seconds of anticipation → ball erupts into the visible peg field. Every. Single. Launch. Has a reveal moment. Spectators gasp
5. **The chime cascade is accidental music.** 40 aluminum tubes at varying pitches means every ball run creates a unique descending melody. 5 balls simultaneously = a waterfall of random music. Nothing else at the carnival sounds like this

## Weaknesses
1. **Build complexity is real.** Five sensory subsystems means five things that can break, five things to test, five things to troubleshoot at 7am on festival morning. Mitigation: each system is independent — if the fog machine dies, the game still works. Degrade gracefully
2. **Cost is 2× the original concept.** $750–850 vs $350–400. The sensory systems add real cost. Mitigation: most components are reusable year over year. Only candy is consumable (~$55/event)
3. **Moisture management.** Mist jets + fog machine + outdoor environment = moisture near electronics. Arduino, LED strips, and solenoid connections need waterproofing (conformal coating or sealed enclosures). This is solvable but adds build complexity
4. **Fog machine regulations.** Some school events restrict fog machines (fire alarm triggers, asthma concerns). Need to verify before committing. Mitigation: the game works without fog — it just loses the "reveal moment"
5. **Power requirements.** Needs 2 outlets minimum. Most festival booths have one. May need an extension cord run or a small generator. Plan ahead

## Comparison to Other Explorations

| | Thunder Drops | Stomp Rockets | Tornado Alley |
|---|:---:|:---:|:---:|
| Entertainment | 10 | 10 | 9 |
| Memorability | 10 | 10 | 9 |
| Ease of Construction | 5 | 7 | 6 |
| Grade Appeal | 9 | 9 | 8 |
| Skill/Luck | 8 | 7 | 7 |
| Chaos | 9 | 9 | 8 |
| Durability | 7 | 8 | 7 |
| Photogenicity | 10 | 8 | 8 |
| Onboarding | 8 | 9 | 8 |
| **Average** | **8.4** | **8.6** | **7.8** |

Thunder Drops trades ease-of-construction for maximum sensory impact and photogenicity. It's the hardest to build but the most memorable to experience. If the goal is "kids talking about that crazy rad game for years to come," the five-sense immersion gives it the strongest long-term memory formation of any variant.

## Build-or-Kill Verdict

**BUILD IT.** The sensory systems are individually simple (fog machine = plug in, chimes = zip-tie, mist = garden sprayer, candy = gravity + levers, LEDs = Arduino starter project). The complexity is in the integration, not the components. Two weekenders with a plan can do this. The result is a carnival game that doesn't exist anywhere else — because nobody has built a plinko board that smells like rain and feeds you chocolate.
