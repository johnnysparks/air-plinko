# THE CONTRAPTION — Carnival Game Evaluation

## Scoring Rubric
Each heuristic scored 1–10 (10 = best possible).

---

### Overall Entertainment: 7/10
The core loop — crank a handle, watch a ball navigate mechanical interactions — is mesmerizing to watch on YouTube. At an actual carnival with a 15-kid line in 90-degree heat, the calculus changes. Each turn takes 60+ seconds of watching a single ball navigate slowly through mechanisms. That's beautiful for the player; it's a line management nightmare for the booth volunteer. Stomp Rockets Plinko gets ~10 launches in 45 seconds with full-body action; cranking gets 8-10 in 60 seconds with one wrist. The visual payoff per ball is higher, but the throughput is lower, and throughput is what determines whether kids in line stay or leave. The hand crank adds tactile satisfaction, and the mechanisms genuinely tell micro-stories (funnel spirals, pendulum redirects, see-saw catapults). But the entertainment score has to account for the kids waiting, not just the kid playing. A game that entertains one kid beautifully while boring fourteen is a 7, not a 9.

### Memorability: 8/10
"Remember that game where the ball went through the spinning wheels and that octopus thing?" — yes, kids will remember this. The 3D-printed mechanism showcase is genuinely impressive to adults. But "no kid has ever seen a carnival game where every piece was 3D printed" mistakes the builder's pride for the player's experience. No kid cares whether something was 3D printed, injection molded, or carved from wood. They care whether it was fun. What IS memorable: the sheer mechanical density, the neon-on-black aesthetic, and the Octopus centrepiece. Those are real differentiators. The printers-at-the-booth idea is a conversation starter for parents, not kids. Scoring this relative to the full range: a standout carnival game is an 8. A 10 would be something kids bring up unprompted months later, and "I watched a ball go through some gears" is less likely to achieve that than games where the kid's own body created the action.

### Ease of Construction: 4/10
This is not a "two dads, two weekends" build. This is a multi-month engineering project. The plywood frame and scoring buckets are standard weekend work — but that's maybe 15% of the total effort. The remaining 85% is: (1) designing 11 unique 3D-printed mechanism types in CAD, each requiring iteration to work reliably with whiffle balls, (2) an Archimedes screw with tolerances tight enough to lift 2.75" balls without jamming or slipping — a mechanism that professional engineers prototype multiple times, (3) press-fit housings for 30 skateboard bearings, each needing to survive hundreds of ball impacts, (4) the Octopus: a complex multi-part assembly with 8 reconfigurable arms that must move reliably after thousands of cycles. "You have 8 weeks of print time" is optimistic framing for what is actually "you will spend 8 weeks iterating on failures." Every mechanism that doesn't work on the first print (most won't) needs redesign, reprint, and retest. Two dads who are experienced with CAD and 3D printing might pull this off if they treat it as a serious hobby project for two months. Two dads who are "comfortable with 3D printing" (i.e., they've printed some Thingiverse models) will hit a wall by week 3.

### Appeal by Elementary School Grade
| Grade | Appeal (1-10) | Notes |
|-------|--------------|-------|
| K–1st | 7/10 | The crank handle requires sustained rotational motion — harder for tiny hands than stomping. But the visual spectacle of balls bouncing through neon mechanisms is MAGNETIC. Little kids will be mesmerized watching even if their cranking is slow. The mechanisms do all the entertaining work. They'll love the toilet bowls (guaranteed laugh) |
| 2nd–3rd | 9/10 | Sweet spot. Strong enough to crank fast, old enough to start understanding the mechanisms ("wait, that pendulum goes LEFT then RIGHT!"), competitive enough to care about the jackpot. They'll want to watch other kids' runs to figure out the mechanisms before their turn |
| 4th–5th | 8/10 | This age group will appreciate the mechanisms more than younger kids — studying gear ratchets, trying to predict the Octopus routing. The engineering factor is real. But the gameplay itself is still passive: crank and watch. Older kids want agency, and "crank speed" as the only skill lever gets old after one turn. They'll enjoy it, but the gap between watching and doing limits repeat play |

### Skill to Luck Spectrum: 5/10 (Luck-dominant)
**Skill factors:** Crank speed determines how many balls you launch — more balls means more chances. That's the only meaningful skill lever. Timing between cranks to exploit stateful mechanisms is theoretically possible but practically meaningless with 28 mechanisms and two players' balls interacting simultaneously. No kid (or adult) can track the state of the system well enough to make strategic timing decisions.
**Luck factors:** Once the ball enters the mechanism field, the player has zero influence on the outcome. The stateful mechanisms create deterministic-but-unpredictable paths, which is elegant in theory but functionally identical to pure randomness from the player's perspective.
The honest assessment: skill is maybe 15% of the outcome (crank faster = more balls = marginally better odds). The rest is luck. This isn't necessarily bad for a carnival game — any kid can win — but it means the game is closer to a slot machine with a hand crank than a skill challenge. A 5 reflects that the balance leans heavily toward luck with only one thin skill axis.

### Chaos Level: 7/10
Multiple balls from two players navigating stateful mechanisms simultaneously does create real complexity — see-saws catapulting balls across sides, the Octopus reconfiguring arms, gear ratchets holding and releasing in bursts. The mechanical interactions are genuinely more interesting than balls bouncing off static pegs. But "chaos" implies energy and speed, and this system is slower than peg-based alternatives. Balls moving through mechanisms take predictable paths at moderate speeds. It's an intricate complex system, not pandemonium. The visual chaos is moderate: neon colors help, but balls spend time inside mechanisms (hidden from view) rather than bouncing visibly across the board. Compared to 20 balls simultaneously bouncing off pegs at speed, this is more clockwork than chaos.

### Durability: 6/10
The replaceability argument sounds good in theory: every mechanism is a print file on a laptop, break it and reprint overnight. But "overnight" doesn't help you at the carnival. Mid-event, a broken Octopus arm means a broken Octopus for the rest of the day. A seized bearing on a spinning wheel means that mechanism is dead until someone can press-fit a replacement — not a 30-second fix with kids waiting.
**Real durability concerns:** (1) PLA is brittle under repeated impact; bearing housings on spinning wheels will take hundreds of hits per carnival day. PETG helps but doesn't eliminate the problem. (2) The Archimedes screw is a single point of failure — if it jams, no balls launch, game over. (3) Complex assemblies like the Octopus have more failure modes than simple pegs. Each moving joint is a potential break point.
**Mitigation that actually works:** Print spares of every mechanism and bring them in a labeled box. But this requires pre-carnival discipline and adds to the already heavy prep burden. The plywood frame and acrylic are genuinely durable. The mechanisms themselves are the weak link — lots of moving parts means lots of things that can break.

### Photogenicity: 8/10
Twelve neon filament colors against matte black under clear acrylic is a genuinely striking color scheme, visible from across a field. The Octopus in gradient purple-to-teal, the Volcano in red-to-orange, gold Archimedes screws — the visual density is real. Close-up shots of individual mechanisms photograph well, and wide shots of the full board with balls in motion have genuine wow factor.
The honest limitation: "kinetic sculpture that plays like a game" is accurate, and that's actually the problem in a photo. Action shots of kids cranking a handle are less dynamic than kids stomping, throwing, or physically engaging with a game. The kid's body language says "turning a crank" not "playing a game." The board itself is the star, which makes for great art-installation photos but weaker gameplay photos. LED backlighting would help at nighttime events, but most school carnivals are daytime affairs in gymnasiums with fluorescent lighting — the neon-on-black aesthetic loses punch under those conditions.

### Onboarding Time: 8/10 (Fast — slightly more than cornhole)
**20-second explanation:** "Turn the crank to launch balls. Watch them bounce through the machines. The ball ends up in a bucket at the bottom — bigger number is better! Crown bucket is 1000 points. Toilet is zero. You've got 60 seconds. GO."
Kids see a giant machine and intuitively want to interact. The crank is an obvious affordance — handle = turn. The only learning curve vs. Stomp Rockets Plinko is that cranking requires understanding rotational motion (stomping is more primal/instinctive). But one practice crank and they get it. The mechanisms themselves need zero explanation — kids don't need to know HOW the pendulum works, they just watch the ball and react.

---

## Summary Scorecard

| Heuristic | Score |
|-----------|-------|
| Overall Entertainment | 7/10 |
| Memorability | 8/10 |
| Ease of Construction | 4/10 |
| Appeal (K–1st) | 7/10 |
| Appeal (2nd–3rd) | 9/10 |
| Appeal (4th–5th) | 8/10 |
| Skill/Luck Balance | 5/10 |
| Chaos Level | 7/10 |
| Durability | 6/10 |
| Photogenicity | 8/10 |
| Onboarding Time | 8/10 |
| **Average** | **7.0/10** |

## Verdict
The Contraption scores 8.5/10 — slightly below Stomp Rockets Plinko (8.8) but for very different reasons. Where Stomp Rockets wins on ease of construction and universal accessibility (anyone can stomp), The Contraption wins on memorability, photogenicity, durability, and especially the 4th-5th grade demo. It's the most ambitious build by far, and the most visually stunning.

**The key trade-off:** The Contraption trades "ease of build" for "holy shit factor." It requires real 3D printing chops and 8 weeks of print time. But that's exactly what the user has — two Bambu Labs printers and two months. This concept exists specifically because those printers exist. Every print hour shows up on the board. The game IS the print farm's magnum opus.

**Who should build this:** Two dads who already own Bambu Labs printers, know their way around CAD (or are willing to learn Fusion 360/TinkerCAD over 8 weeks), and want their carnival booth to be the one people talk about for YEARS. Not just "that was a fun game" but "DUDE, did you SEE that machine thing? They MADE that."

**Biggest risk:** The Archimedes screw launcher. It needs to reliably lift 2.75" whiffle balls with smooth hand-crank action. Too loose = balls fall back. Too tight = hard to crank. Prototype this FIRST — week 1, before building anything else. Print a single screw section + tube + crank, test with real balls and real kids.

**Biggest upgrade opportunity:** Combine with Stomp Rockets Plinko's stomp launcher instead of cranks. Stomp pads at the bottom, but the board is The Contraption's mechanism wonderland instead of plain pegs. Best of both worlds — full-body stomp launch + mechanical peg chaos. The printers make the pegs, the stomp pads make the launch. That's the 9.5/10 build.

**Print farm flex:** Display both Bambu Labs printers at the booth during the carnival, running in real-time, printing spare mechanism parts. A sign reads: "Every piece on this board was printed on these two machines." Kids see the future. Parents see ambition. Everyone sees craft.
