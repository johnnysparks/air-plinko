# Stomp Rockets Plinko — Carnival Game Evaluation

## Scoring Rubric
Each heuristic scored 1–10 (10 = best possible).

---

### Overall Entertainment: 7/10
The stomp mechanic is genuinely physical and satisfying — kids use their whole body, which is more engaging than standing and tossing. But the actual gameplay loop is: stomp, watch ball bounce through pegs, repeat. The stomping is active; the plinko half is passive spectating. Stomp rockets already exist as a popular kids' toy, so the core thrill (stomp and watch something fly) is familiar, not novel. The 45-second timed round adds urgency, and dual-player competition helps. This is a solidly fun booth — better than most carnival games — but it's not the best carnival game imaginable. That would require the player to be engaged for the full duration, not just during the stomp.

### Memorability: 7/10
Kids will remember stomping on a pad and watching balls fly into a neon board. That's a good hook. But stomp rockets are a toy most kids have already played with, and plinko boards are at every carnival and game show. The combination is clever — genuinely more interesting than either component alone — but it's a mashup of two known things, not something unprecedented. The neon aesthetic helps it stand out visually on carnival day. The sound effects (if implemented) add identity. A parent volunteer watching this for the first time would say "oh, that's cool" — which is a 7, not a 10.

### Ease of Construction: 6/10
The plinko board is standard construction — plywood, pegs, acrylic, edge rails. Two dads can build that in a weekend. But the full system is more than a plinko board. It requires: (1) stomp pads with bladders and hoses that reliably translate foot force into ball launches — this has never been prototyped and is the core unknown, (2) a ball magazine auto-feed gate with a moving part that needs design iteration, (3) a ball return system routing 3" PVC from buckets back to magazines, (4) 60 3D-printed pegs across multiple overnight print jobs, (5) a 7ft-tall support frame. The optional sound system adds more. Any one of these is manageable; together, this is a 3-weekend project for experienced builders assuming the pneumatics work on the first prototype attempt. They probably won't.

### Appeal by Elementary School Grade
| Grade | Appeal (1-10) | Notes |
|-------|--------------|-------|
| K–1st | 6/10 | Stomping is fun at this age, but the evaluation already concedes they "may not stomp hard enough for top-zone launches." That's not a footnote — it means the core mechanic partially fails for the youngest players. They'll get some balls in play and enjoy watching the pegs, but if their stomps produce weak dribbles instead of satisfying launches, the experience is frustrating, not magical. The lower scoring zones help, but the payoff is muted. |
| 2nd–3rd | 8/10 | The right age for this game. Strong enough to get real launches, competitive enough to care about scores, energetic enough to stomp repeatedly for 45 seconds. This age group will have genuine fun and want to play again. |
| 4th–5th | 7/10 | The physicality keeps it from feeling too young. The strategy of force calibration is real but shallow — after 2-3 stomps you've learned all there is to learn. Competitive kids will enjoy it, but the "stomp and watch" loop doesn't have enough depth to truly impress a 10-year-old the way a game with continuous engagement would. |

### Skill to Luck Spectrum: 7/10 (Good balance)
**Skill factors:** Stomp force controls launch height. Harder stomp = higher entry point on the board. Pace management across 45 seconds matters. There's a real risk/reward choice between monster stomps (high zone, but also near gutters) and controlled stomps (safer mid-zone).
**Luck factors:** Once the ball enters the peg field, the player has zero control. It's pure plinko randomness from that point. This means roughly half the gameplay experience (the cascade) has no skill component at all.
The skill axis is real but narrow — it's essentially one variable (stomp force). Compare to a game where the player makes continuous decisions throughout. The balance is good, not excellent.

### Chaos Level: 7/10
With two players stomping simultaneously, multiple balls can cascade through the peg field at once. Balls collide and redirect, which creates some visual excitement. But plinko chaos is orderly chaos — balls bouncing through evenly spaced pegs in a downward path is more mesmerizing than chaotic. The gutters add tension. It's visually interesting, but "20 balls cascading at once" is only possible if both players are stomping at maximum speed and the pneumatics keep up, which is an optimistic scenario.

### Durability: 7/10
**Strong points:** The plywood board and PVC components are robust. 3D-printed pegs are replaceable if broken. Acrylic front panel is shatter-resistant.
**Weak points:** The stomp bladders are the critical failure point. They absorb hundreds of full-force stomps from kids jumping with their full body weight. Bladder fatigue, hose disconnection, or air leaks would disable the game entirely — there's no degraded mode where the game still works without pneumatics. The ball magazine feed gate is a moving part under repeated stress that could jam. Budget for spare bladders and plan for mid-day repairs.
**Repairability:** High-wear parts are cheap, but swapping a bladder mid-carnival means taking a station offline and potentially losing air-tight seals under time pressure.

### Photogenicity: 7/10
The neon-on-black color scheme is visually striking and would stand out in a carnival setting. The acrylic front lets spectators see the ball action. But the game is vertically oriented — capturing both the kid stomping at ground level and the board towering above in one photo requires a wide-angle lens or significant distance. The most photogenic moment (kid mid-stomp with balls cascading) is difficult to time. Without the optional LED backlighting, this is a colorful booth; with it, it's more impressive but that adds construction scope. A parent with a phone will get a decent photo, not a great one.

### Onboarding Time: 7/10 (Fast, but not instant)
The explanation is short: "Stomp the pad, balls fly up, watch them score, 45 seconds." That's good. But "instant" and "easier than cornhole" are both wrong. Cornhole requires zero explanation — you see bags and a hole. This game requires explaining: (1) stomp the pad, (2) balls launch into the board, (3) they fall into scoring zones, (4) avoid gutters, (5) you have 45 seconds, (6) higher zones score more but risk gutters. Kids will figure it out after one stomp, but a parent volunteer running the booth needs to understand the scoring, the timer, and the dual-player setup. It's a 30-second onboarding, not a 5-second one.

---

## Summary Scorecard

| Heuristic | Score |
|-----------|-------|
| Overall Entertainment | 7/10 |
| Memorability | 7/10 |
| Ease of Construction | 6/10 |
| Appeal (K–1st) | 6/10 |
| Appeal (2nd–3rd) | 8/10 |
| Appeal (4th–5th) | 7/10 |
| Skill/Luck Balance | 7/10 |
| Chaos Level | 7/10 |
| Durability | 7/10 |
| Photogenicity | 7/10 |
| Onboarding Time | 7/10 |
| **Average** | **6.9/10** |

## Verdict

Stomp Rockets Plinko is a solid concept built on a genuinely appealing physical mechanic. The stomp-and-launch loop is more physically engaging than most carnival booth interactions, and the neon plinko board is a good visual anchor. It's a good game. It is not a great game pretending to be a perfect one.

**The existential risk is the pneumatics.** The entire concept depends on a stomp bladder reliably propelling a whiffle ball 4+ feet up a 1.5" tube. This has not been prototyped. If the bladder is too soft, stomps feel wimpy and balls dribble. If it's too stiff, kindergartners and small first-graders can't play at all — cutting out a meaningful chunk of the audience. The sweet spot between these failure modes may be narrow, and it may shift with temperature (bladder stiffness changes in heat), bladder fatigue (softens over hundreds of stomps), and child weight variation. This is not a "biggest risk" footnote — it is a go/no-go dependency. Build one pad, one tube, and one ball. Test it with a 40-pound kindergartner and a 90-pound fifth-grader. If both get satisfying launches, proceed. If not, the concept doesn't work.

**What this concept sacrifices:** Player engagement during the plinko cascade phase (passive watching), depth of skill expression (one variable: stomp force), and construction simplicity (pneumatics add meaningful build risk). It also underserves the youngest players if the force threshold can't be tuned low enough.

**Build recommendation:** Prototype the stomp-to-launch mechanism first. If it works reliably across the age/weight range, this is a top-half concept worth building. If it doesn't, no amount of neon pegs saves it.
