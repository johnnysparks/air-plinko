# THE GREAT CRANK DERBY — Carnival Game Evaluation

## Scoring (1-10 scale)

### Overall Entertainment: 7/10
Head-to-head racing is a proven format. But strip away the terrain zone labels and what's the actual player experience? Turning a crank handle as fast as you can for 30 seconds. That's it. There's no aiming, no timing decision, no moment-to-moment choice. Compare to water-gun horse-racing games at real carnivals — those work because you're aiming at a target while racing. This is pure output: crank harder. The first 10 seconds are exciting. The last 20 are arm fatigue. The entertainment is real but shallow — it's a sprint, not a game.

### Memorability: 7/10
"I turned a crank and my car went up a board" is a thinner story than it sounds on paper. The bell is a nice touch — audible finish lines matter. But the physical experience is repetitive single-motion exertion, not the kind of varied sensory input that burns into memory. Compare honestly: a kid who launched a water balloon from a trebuchet, or steered a ball through fog with an air cannon, has a richer story to tell at dinner. The head-to-head format adds social memorability ("I beat Jake"), but the game itself doesn't give you much to describe beyond "I cranked really fast."

### Ease of Construction: 6/10
The build plan undersells the complexity. Routing two 7-foot S-curve tracks into plywood requires a plunge router, a steady hand, and a template. The curves need to be smooth enough that a wooden car slides without catching — any rough spot or misalignment and the car jams mid-race. The pulley system has 16 pulleys that all need precise alignment or the string jumps the sheave. The 3D-printed ratchet mechanism needs to be reliable under repeated kid-force cranking — a pawl that slips means cars slide backward. Two handy dads can build it in two weekends, but expect frustrating debugging of the string routing and car-to-track fit. This is more fiddly than it looks.

### Appeal by Elementary School Grade:
| Grade | Appeal | Notes |
|-------|--------|-------|
| K-1 | 5/10 | Most kindergartners lack the sustained arm strength for a 30-second crank session. They'll stall on Dead Man's Hill and watch their opponent's car pull away. Losing because you're physically weaker — not because of bad aim or bad luck — feels bad for a 6-year-old. A "short race" mode helps but splits the booth's attention. |
| 2-3 | 7/10 | Can physically complete the race. Enjoy competition. But the lack of variety means diminishing returns — the second race feels the same as the first. No "I want to try a different strategy" pull. |
| 4-5 | 8/10 | Best demographic. Strong enough, competitive enough, old enough for bragging rights to matter. But even here, after 2-3 races they've seen everything the game has to offer. |

### Skill to Luck Spectrum: 9/10 (Pure Skill)
Zero randomness. This is honestly scored — the game is 100% physical output. But "pure skill" in a carnival context is a double-edged sword. Carnivals thrive on the possibility that anyone might win. A smaller kid will never beat a bigger kid at this game. There's no lucky bounce, no clutch shot, no moment where the underdog pulls it off. Competitive dads will love it. The kid who loses every race will hate it.

### Chaos Level: 3/10
The original eval scored this 5/10 by counting "social chaos" (crowd energy, trash talk). That's not game chaos — that's atmosphere, and it applies to any competitive game. The mechanical chaos of this game is near zero: cars go up tracks on strings. There are no surprising moments, no unexpected interactions, no "did you SEE that?!" physics. What you see is what you get, every single time. For a concept repo that includes games with vortex cannons, trebuchets, and mechanical flippers, this is the least chaotic option.

### Durability: 8/10
Legitimately durable. Plywood, wood blocks, nylon cord — these are robust materials. Docking one point because the string-and-pulley system is the Achilles heel: nylon cord frays under repeated winding, and a frayed cord catching on a pulley sheave mid-race is a real failure mode. You'll want spare cord and the knowledge to re-route it. The 3D-printed ratchet pawl is also a wear point — PLA under repeated impact stress cracks. Print spares in PETG.

### Photogenicity: 6/10
Two kids turning cranks next to a plywood board. The cars are 4 inches long and invisible in photos from more than 6 feet away. The tracks are colored grooves — visible up close, unreadable in a wide shot. Compare to concepts with giant castle walls, glowing fog, or flying stuffed animals. A parent taking photos from the crowd line gets: two kids straining at waist-height handles, a mostly-brown plywood rectangle behind them. The flag pop is a split-second moment that's hard to capture. The bell ring is auditory, not visual. This game photographs like a science fair project, not a carnival attraction.

### Onboarding Time: 10/10 (Instant)
"Grab the crank. When I say GO, crank as fast as you can. First car to ring the bell wins." This is genuinely the simplest game in the entire repo. No scoring rules, no aiming, no multi-step process. A volunteer who's never seen the game can run it after a 10-second briefing. This score survives scrutiny.

---

## Summary Scores

| Heuristic | Score |
|-----------|-------|
| Overall Entertainment | 7/10 |
| Memorability | 7/10 |
| Ease of Construction | 6/10 |
| Appeal (K-1) | 5/10 |
| Appeal (2-3) | 7/10 |
| Appeal (4-5) | 8/10 |
| Skill to Luck | 9/10 (Pure Skill) |
| Chaos Level | 3/10 |
| Durability | 8/10 |
| Photogenicity | 6/10 |
| Onboarding Time | 10/10 |

**Average: 6.9/10**

---

## Strengths
- Genuinely different from every other concept — breaks the plinko paradigm completely
- Fastest onboarding in the repo — any volunteer can run it immediately
- High throughput (30-sec games + 5-sec resets) keeps lines moving
- Cheap build ($250-300) with no electrical systems
- The bell finish line is a smart design choice — audible, dramatic, unambiguous

## Weaknesses
- **The core loop is thin.** The player makes one decision (crank fast) and repeats it for 30 seconds. No aiming, no timing, no tactical choices. Games with richer moment-to-moment decisions sustain engagement better.
- **Pure skill excludes young kids.** A kindergartner physically cannot beat a 5th grader. In a school carnival where K-5 share the same booth, 20% of your audience will lose every race. Losing because you're smaller feels worse than losing to bad luck.
- **Invisible to passersby.** The game's appeal requires being AT the booth. From 20 feet away, it's a brown plywood board with two kids turning handles. No visual hook to pull in foot traffic. Contrast with concepts that have flying projectiles, glowing lights, or dramatic destruction.
- **Repetitive after 2 races.** Every race plays out identically — crank, car goes up, bell rings. There's no "I want to try a different strategy" replay motivation. The game doesn't deepen with experience.
- **String routing is fragile operationally.** 16 pulleys × 2 tracks = 32 points where string can jump a sheave, tangle, or fray. A mid-race string failure kills the game until a knowledgeable person re-routes it. This is the kind of problem that doesn't show up in testing but appears at hour 3 of a hot carnival day.

## Verdict
Build this if you want a fast, cheap, easy-to-run booth and your carnival skews toward 3rd-5th graders. Don't build this if you need a visual centerpiece that draws a crowd from across the field, or if your audience includes a lot of K-1 kids. The game works — but it's a good booth, not a great one. It fills a role (head-to-head competition, fast throughput, simple operation) that no other concept in the repo covers, which has value. But it won't be the game kids talk about for years unless the competitive moment happens to land perfectly — and you can't engineer that.

Consider this as a **second booth** alongside a higher-spectacle primary game, not as the sole attraction.
