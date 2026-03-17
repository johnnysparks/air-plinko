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

### Chaos Level: 9/10
Twenty balls from two players, simultaneously navigating 28 unique mechanisms, with stateful machines changing the board between every ball. See-saws catapulting balls from one player's side to the other. The Octopus reconfiguring its 8 arms mid-game. Gear ratchets holding balls for three turns then releasing them in bursts. Trap doors dropping balls through unexpected shortcuts. The chaos isn't just visual (though 12 neon colors bouncing through the board IS a visual feast) — it's MECHANICAL chaos. The machine itself is alive and changing. The only thing preventing a 10/10 is that the balls move slower through mechanisms than they do through simple pegs, so the chaos is more "mesmerizing complex system" than "absolute pandemonium."

### Durability: 9/10
This is where the 3D printer advantage is nuclear. **Every single mechanism is replaceable.** Print files live on a laptop. Break the Octopus arm? Print a new one overnight. Bearing seizes? Pop it out, press in a new $0.50 skateboard bearing. The plywood frame is bombproof. The acrylic front is shatter-resistant. The Archimedes screw sections snap together — replace one section, not the whole screw.
**High-wear parts:** Bearing housings on spinning wheels (hundreds of impacts per carnival day). Mitigation: PETG for bearing housings instead of PLA — better impact resistance. Budget extra bearings.
**The modularity IS the durability story.** Nothing is irreplaceable. Nothing takes more than 20 minutes to swap. Print spares of every Tier 1 mechanism and bring them to the carnival in a box.

### Photogenicity: 10/10
Twelve neon filament colors against a matte black backboard under clear acrylic. The Octopus in gradient purple-to-teal. The Volcano in red-to-orange gradient. Gold Archimedes screws. Spinning wheels in motion. Balls cascading through mechanisms. This board IS the photo. It's a kinetic sculpture that plays like a game. Close-up shots of individual mechanisms are Instagram gold. Wide shots of the whole board with 20 balls in play are mesmerizing. Action shots of kids cranking with the glowing board behind them are banger family photos. Add optional LED backlighting and this becomes the #1 visual landmark at any nighttime carnival. The density of visual detail means every photo from every angle reveals something new.

### Onboarding Time: 8/10 (Fast — slightly more than cornhole)
**20-second explanation:** "Turn the crank to launch balls. Watch them bounce through the machines. The ball ends up in a bucket at the bottom — bigger number is better! Crown bucket is 1000 points. Toilet is zero. You've got 60 seconds. GO."
Kids see a giant machine and intuitively want to interact. The crank is an obvious affordance — handle = turn. The only learning curve vs. Stomp Rockets Plinko is that cranking requires understanding rotational motion (stomping is more primal/instinctive). But one practice crank and they get it. The mechanisms themselves need zero explanation — kids don't need to know HOW the pendulum works, they just watch the ball and react.

---

## Summary Scorecard

| Heuristic | Score |
|-----------|-------|
| Overall Entertainment | 9/10 |
| Memorability | 10/10 |
| Ease of Construction | 6/10 |
| Appeal (K–1st) | 7/10 |
| Appeal (2nd–3rd) | 9/10 |
| Appeal (4th–5th) | 10/10 |
| Skill/Luck Balance | 7/10 |
| Chaos Level | 9/10 |
| Durability | 9/10 |
| Photogenicity | 10/10 |
| Onboarding Time | 8/10 |
| **Average** | **8.5/10** |

## Verdict
The Contraption scores 8.5/10 — slightly below Stomp Rockets Plinko (8.8) but for very different reasons. Where Stomp Rockets wins on ease of construction and universal accessibility (anyone can stomp), The Contraption wins on memorability, photogenicity, durability, and especially the 4th-5th grade demo. It's the most ambitious build by far, and the most visually stunning.

**The key trade-off:** The Contraption trades "ease of build" for "holy shit factor." It requires real 3D printing chops and 8 weeks of print time. But that's exactly what the user has — two Bambu Labs printers and two months. This concept exists specifically because those printers exist. Every print hour shows up on the board. The game IS the print farm's magnum opus.

**Who should build this:** Two dads who already own Bambu Labs printers, know their way around CAD (or are willing to learn Fusion 360/TinkerCAD over 8 weeks), and want their carnival booth to be the one people talk about for YEARS. Not just "that was a fun game" but "DUDE, did you SEE that machine thing? They MADE that."

**Biggest risk:** The Archimedes screw launcher. It needs to reliably lift 2.75" whiffle balls with smooth hand-crank action. Too loose = balls fall back. Too tight = hard to crank. Prototype this FIRST — week 1, before building anything else. Print a single screw section + tube + crank, test with real balls and real kids.

**Biggest upgrade opportunity:** Combine with Stomp Rockets Plinko's stomp launcher instead of cranks. Stomp pads at the bottom, but the board is The Contraption's mechanism wonderland instead of plain pegs. Best of both worlds — full-body stomp launch + mechanical peg chaos. The printers make the pegs, the stomp pads make the launch. That's the 9.5/10 build.

**Print farm flex:** Display both Bambu Labs printers at the booth during the carnival, running in real-time, printing spare mechanism parts. A sign reads: "Every piece on this board was printed on these two machines." Kids see the future. Parents see ambition. Everyone sees craft.
