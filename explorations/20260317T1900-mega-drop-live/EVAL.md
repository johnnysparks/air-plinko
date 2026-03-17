# Mega Drop Live — Evaluation

## Overall Entertainment: 8/10

The original Mega Drop Live was a production layer on top of a passive game — you dropped a ball and watched a screen react. Combo Catcher fixes the fundamental problem: now the screen IS the game. Every bounce matters because the ball is threading a sequence of target zones, and the crowd can see the chain building in real-time. The pre-drop "read the board" moment adds genuine strategy (which slot gives the best path through zones 1→2→3?), and the combo counter creates escalating tension that plain plinko never had. A ball bouncing toward zone 4 after hitting 1→2→3 has the whole crowd leaning in. That said, the player still physically just drops a ball — the interaction happens before the drop (strategy) and on the screen (tension), not through continuous physical engagement during the drop. It's much better than the original concept, but still not as physically engaging as flipper or aim-based games.

## Memorability: 8/10

"I got a 4-chain on Mega Drop Live" is a specific, brag-worthy memory that kids will repeat. The original concept's memory was "I dropped a ball and there was a cool screen" — vague, passive. Now there's a story: "I read the board, dropped from slot 3, hit zone 1, then 2, BARELY caught zone 3 on a lucky bounce, and the crowd went crazy." The combo system gives every drop a narrative arc. The replay feature now has real content to replay — watching the chain build a second time is genuinely rewatchable. Near-misses are almost more memorable than perfect chains ("I was ONE zone away from a perfect!"). The difficulty modes also create aspiration: a 2nd grader who chains 3-for-3 on Easy will remember that and want to try Medium next year. Still docking 2 points because the physical action (dropping a ball) is forgettable even if the outcome isn't. You remember the chain, not the drop.

## Ease of Construction: 6/10

The physical build is unchanged — still the simplest board in the set, still a one-weekend job. The software is actually somewhat simpler than the original concept because we dropped the player cam entirely (no MediaPipe, no pose detection). One fewer camera to mount, calibrate, and debug. The combo zone engine is new code, but it's fundamentally straightforward: generate random circles, check if a point is inside a circle, track sequence state. That's 200 lines of Python, not a machine learning pipeline. The ghost path simulation is the most complex new feature (randomized peg-bounce model), but it's optional — the game works fine without it. Net: the software is still a real engineering project (30-50 hours), but it's more achievable than the original two-camera, pose-detection, skeleton-overlay stack. A dad who's done some Python scripting could pull this off. Bumping from 5 to 6.

## Appeal by Elementary School Grade

- **K–1st (ages 5-7): 7/10** — Easy mode (3 large zones) is designed for them. They don't need to understand the combo system deeply — they drop the ball, the screen makes things light up and go BOOM, and the announcer says exciting things. If a zone lights up green, they cheer. The "read the board" strategy step goes over their heads, but that's fine — random drop slot choice still produces occasional chains, and even a 1-chain gets a celebration. Much better than the original, where the pose-detection step was a stumbling block. Now there's nothing to explain beyond "drop the ball."

- **2nd–3rd (ages 7-9): 9/10** — This is the perfect age for Combo Catcher. They're old enough to understand "hit the numbers in order" (it's like connect-the-dots with gravity). They'll study the board, argue about which drop slot is best, and erupt when a chain builds. The leaderboard gives them a reason to play again. Medium difficulty (4 zones) is their sweet spot — achievable but not easy. They'll talk about their best chain for weeks.

- **4th–5th (ages 9-11): 8/10** — The original concept scored 7 here because "I just drop a ball?" felt too simple. Combo Catcher answers that objection: the strategy of reading the target layout and choosing a drop position is a real skill input that rewards thinking. Hard mode (5 small zones) gives competitive kids a genuine challenge — a perfect chain on Hard is rare enough to be a bragging-rights achievement. The ghost path lines appeal to the analytical kids who want to optimize. Some will still find it luck-heavy once the ball is in play (and they're right — plinko physics are plinko physics), but the pre-drop strategy and the combo system give them enough agency to stay engaged.

## Skill-to-Luck Spectrum: 5.5/10 (balanced)

This is the single biggest improvement over the original concept (which scored 4/10, heavy luck). Combo Catcher adds two meaningful skill inputs:

1. **Board reading** — Studying the target layout and choosing the optimal drop slot is a real decision. A player who analyzes the zone positions and picks the slot with the best path will outperform a random dropper over many rounds.
2. **Pattern recognition** — After several rounds, skilled players develop intuition for how balls tend to move through the peg field. They learn that a ball dropped from slot 2 tends to drift right, or that the center slots produce more vertical paths.

Plinko is still fundamentally stochastic — even the perfect drop-slot choice gets randomized by peg bounces. But the combo system means that the range of outcomes is wider: a skilled reader might average 2-3 chains while a random dropper averages 0-1. That's enough for skill to matter without eliminating the upset potential that makes it fun for everyone. Scoring 5.5 — meaningfully more skill-influenced than raw plinko, but still luck-heavy enough that a kindergartner can beat a 5th grader on any given drop.

## Chaos Level: 6/10

Up from 5. The ball physics are identical (single ball, gravity speed), but the combo system manufactures tension that feels like chaos. When a ball is bouncing toward zone 3 after hitting 1→2, and it deflects right at the last second — that near-miss generates a visceral crowd reaction that raw plinko never produced. The Frenzy Round (moving target zones) kicks chaos up further every 30 minutes, creating event moments that draw a crowd. The announcer's escalating intensity — calm at 0 chains, SCREAMING at 4 chains — amplifies whatever physical chaos exists. It's still one ball at gravity speed, so the physical chaos ceiling is low. But the emotional chaos is high.

## Durability: 8.5/10

Slightly better than the original's 8. The physical board is still indestructible. The software stack is simpler: one camera instead of two (fewer USB bandwidth issues, fewer desync risks), no MediaPipe (significant CPU savings — OpenCV HSV tracking alone uses ~30% of a Pi 4's CPU vs ~70% with MediaPipe running simultaneously). The reduced thermal load means fewer crashes from throttling. The combo zone engine is pure Python math (no ML model inference), so it's deterministic and debuggable. Same caveats apply: SD card corruption, USB camera disconnects, and Python exceptions are still real failure modes that require a technical volunteer to resolve. But the simpler stack means fewer things CAN go wrong.

## Photogenicity: 7.5/10

Marginally better than the original's 7. The combo chain display — numbered zones lighting up green in sequence with a big "3× COMBO!" counter — is more visually dramatic and readable in a photo than the original's skeleton overlay and generic effects. A parent snapping the screen at the moment of a perfect chain capture gets a clear, exciting image: gold explosion, "5× PERFECT CHAIN!", score math. The board itself is still visually plain (dark rectangle, white pegs), but the screen content is more photogenic because the combo state tells a story in a single frame. Same outdoor/sun caveats apply.

## Onboarding Time: 9/10 (near-instant)

Even faster than the original's 8. The pose-detection step is gone entirely — there's nothing to explain beyond "drop the ball in a slot." The combo system explains itself on screen: numbered zones light up, the ball passes through them, a counter goes up. Kids in line watch other kids play and understand the rules by observation before they even step up. The attract mode demo drop teaches the system in 10 seconds. The ghost path lines are self-explanatory (fainter lines = less likely). A volunteer at this booth literally says "pick a slot, drop the ball, try to hit the numbers in order." Done.

## Verdict

Combo Catcher transforms Mega Drop Live from a "spectacle wrapper around a luck game" into a "combo-chasing skill game that uses plinko as its physics engine." The screen is no longer a replay layer — it's the game board. Every drop has a strategic decision (which slot?), escalating tension (will the chain continue?), and a clear outcome (combo multiplier × landing zone). The crowd engagement is dramatically higher because people can read the chain state on screen and anticipate what's about to happen.

The software is paradoxically simpler than the original concept (one camera, no pose detection, no skeleton overlay) while producing a more engaging game. The combo zone engine is straightforward collision math, not ML inference. The main engineering effort is the display layer (rendering zones, trails, and effects on the live camera feed) and the ghost path simulation (optional but cool).

**Build it if:** one of the two dads can write Python and is comfortable with OpenCV. The simplified single-camera stack is meaningfully more achievable than the original two-camera pose-detection design. Estimate 30-50 hours of software development.

**Don't build it if:** neither builder codes, the carnival is outdoors without shade (monitor washout kills the combo zone visibility, and visibility IS the game), or you want a game with continuous physical engagement during play. The player's physical action is still just "drop a ball" — the skill expression is cognitive (reading the board), not physical (aiming, steering, slamming).

**The honest trade-off:** Combo Catcher shifts the balance from pure spectacle toward genuine gameplay. You lose the "I was on TV" novelty of the player cam / skeleton overlay (some kids loved that). You gain a game that rewards thinking, creates narrative tension on every drop, and gives kids a specific achievement to brag about. It's a better game and a slightly less flashy production. For a carnival booth, that's the right trade.
