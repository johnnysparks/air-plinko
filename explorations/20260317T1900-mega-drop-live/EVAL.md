# Mega Drop Live — Evaluation

## Overall Entertainment: 7/10

The core gameplay is plinko — drop a ball, watch it bounce, see where it lands. That's inherently satisfying but not novel. What elevates it is the production layer: the announcer, the effects, the crowd screen. But the player's actual physical interaction is minimal — you drop a ball and then watch. Compared to concepts where players actively steer, slam, or aim during play, the moment-to-moment engagement is passive. The spectacle carries the entertainment, not the mechanics. If the tech glitches (Pi crashes, camera loses tracking), you're left with a plain plinko board and no backup gameplay loop.

## Memorability: 7/10

A plinko board with a live game show overlay is unusual at a school carnival. The "I was on TV" factor is real — kids seeing themselves with a skeleton overlay on a big screen is a genuine novelty. But strip away the tech and ask: what did the player physically DO? They dropped a ball. That's the memory — "I dropped a ball and there was a cool screen." Compare to games where the physical action itself is memorable (stomping a rocket launcher, slamming a flipper, aiming a slingshot). The screen makes the experience impressive in the moment, but physical actions encode stronger memories than watching a display. A glitchy display or laggy tracking turns this from "cool future game" to "janky school project" instantly, and that's the memory that sticks.

## Ease of Construction: 5/10

The physical board is the simplest in the entire exploration set — it's a plinko board with no air system, no flippers, no servos. Two dads could build the board in a single Saturday. But a score of 5 because "ease of construction" means the WHOLE thing, not just the wood parts. The software stack — OpenCV ball tracking, MediaPipe pose detection, a WebSocket bridge, browser display app, sound system, instant replay, leaderboard — is a legitimate engineering project. The build plan says "flash an SD card" but creating that SD card image requires 40-60 hours of software development by someone fluent in Python, computer vision, and web development. That's not two dads over a few weekends — that's a software engineer burning evenings for a month. If neither builder codes, this concept is dead on arrival. The physical build is a 9/10. The software build is a 2/10 for typical carnival volunteers. The average is generous at 5.

## Appeal by Elementary School Grade

- **K–1st (ages 5-7): 6/10** — They'll enjoy dropping balls and watching the screen, but pose power-ups require body awareness and deliberate postures that many kindergartners will struggle with. The "choose your power-up" step adds cognitive overhead to what should be "drop ball, yay." They'll get impatient waiting for the pose detection to register. The screen is fun to watch but they'd rather be touching things.

- **2nd–3rd (ages 7-9): 8/10** — Sweet spot. Old enough to understand the power-up system, young enough to think being on TV is the coolest thing ever. They'll compete for high scores, try to figure out which power-up is best, and watch replays of their drops. The leaderboard gives them a reason to play again.

- **4th–5th (ages 9-11): 7/10** — They'll appreciate the tech and compete hard on the leaderboard, but may find the actual gameplay too simple. "I just... drop a ball?" The lack of active control during the drop phase means the game can feel like a slot machine — you make one choice (power-up + drop position) and then watch randomness unfold. Some 5th graders will call this boring after two rounds. Others will grind the leaderboard all day.

## Skill-to-Luck Spectrum: 4/10 (heavy luck)

This is the concept's biggest weakness. Drop position choice and power-up selection are the only skill inputs, and neither has a huge impact on outcome — plinko is fundamentally a random walk. A first-time player can beat a tenth-time player purely by chance. The power-ups add strategic flavor but don't change the underlying physics. Compare this to flipper-based or aim-based games where practiced players demonstrably outperform newcomers. Mega Drop Live is ~80% luck, 20% minor positional strategy. Some players love this (slot machine dopamine). Many competitive kids will find it frustrating.

## Chaos Level: 5/10

A single ball falling through pegs at gravity speed is not chaotic. Scatter Shot (3 balls at once) raises the energy briefly, but most drops are a single ball taking 3-5 seconds to reach the bottom. The chaos is all on-screen (effects, announcer, replays) rather than physical. Compare to concepts with air cannons, flying debris, or rapid-fire mechanics — the physical energy in the room is lower here. The speakers and monitor compensate, but manufactured excitement is not the same as genuine mechanical chaos that makes the crowd gasp.

## Durability: 8/10

The physical board is near-indestructible — plywood, dowels, acrylic, no moving parts. Physically, this is the most durable concept in the set. But "durability" includes "does it keep working," and software failures are real failures. A Raspberry Pi running OpenCV + MediaPipe + Chromium simultaneously will thermal-throttle or crash if ventilation is poor — and "behind a plywood board at a carnival in the sun" is poor ventilation. USB webcams can desync, SD cards corrupt, and a Python exception crashes the whole display. The spare SD card is smart but swapping it means 2-3 minutes of downtime and recalibration. A parent volunteer cannot debug a Python traceback. Physically: 10/10. As a system including software: 8/10, because the failure modes require technical knowledge to resolve and there's no graceful degradation — when the Pi dies, the game show dies with it.

## Photogenicity: 7/10

The monitor is the photo opportunity — parents will snap the big screen showing their kid's skeleton overlay and the score explosion. When conditions are right (shade, good display brightness), the screen is genuinely photo-worthy. But the board itself — a dark rectangle with white dots — is visually plain compared to a colorful pinball machine or a castle-themed slingshot game. You're photographing a TV, not a physical spectacle. At an outdoor carnival on a bright day, the monitor washes out and the board photographs as a dark box. The photogenicity is conditional on controlled lighting. Indoors or under a canopy: 8. In direct sun: 4. Splitting the difference at 7.

## Onboarding Time: 8/10 (very fast)

"Drop the ball in the top. Watch the screen. Strike a pose for bonus points." That's the entire explanation. The core mechanic (plinko) is universally understood. The power-up layer is optional — if a kid just drops a ball without posing, they still get a full game experience. The monitor provides its own tutorial through attract mode and on-screen prompts. A volunteer running this booth needs to know one thing: "refill the ball bin." Compare to games with complex aiming, multi-step mechanics, or unfamiliar controls — this is nearly zero-friction. Deducting 2 points because some kids will be confused by the pose step and need a demo.

## Verdict

Mega Drop Live is a production-heavy experience layered on top of a mechanically thin game. It solves the "boring plain plinko board" problem by making the OUTPUT spectacular rather than making the INPUT engaging. When the tech works perfectly, it's a noticeably polished booth that draws a crowd. When it doesn't — dead Pi, bad lighting for the cameras, sun-washed monitor — it's just a plinko board with a blank TV next to it, and that contrast makes the failure more conspicuous than if you'd never added the tech at all.

**Build it if:** one of the two dads is comfortable with Python/OpenCV and willing to put 40+ hours into the software stack before carnival day. The physical build takes one weekend. The software takes three.

**Don't build it if:** neither builder has programming experience, the carnival is outdoors without guaranteed shade, or the goal is a game where skill visibly matters. The luck-heavy gameplay means competitive kids may bounce after a few rounds.

**The honest trade-off:** This concept trades mechanical engagement for spectacle. You get the "wow" factor of being on a big screen, but you lose the "I got better at this" satisfaction of skill-based games. It's a crowd-pleaser, not a skill-builder. For a carnival where the goal is maximum smiles per minute across the widest age range, that trade-off works. For a carnival where kids want to master something, it doesn't.
