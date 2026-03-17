# CAD Architect Skill — Effective Diagram Descriptions

## Lessons Learned

### What works well in HTML/Canvas diagrams:
1. **Multiple views** — Always include at least a top-down/front view AND a side cross-section. Different views communicate different aspects (layout vs depth vs construction)
2. **Dark background, bright elements** — Dark navy/black backgrounds with color-coded elements are highly readable in screenshots
3. **Labeled dimensions** — Always add dimension lines with measurements at the margins
4. **Color-coded legend** — Every element type gets a unique color. Include a legend section below the diagram
5. **Key specs table** — Separate section with structured specs makes it scannable

### Building descriptions that translate to accurate diagrams:
1. **Use coordinate-based positioning** — Describe positions as percentages or fractions of the field ("center", "mid-field offset left", "near corners")
2. **Specify relative sizes** — "small", "large", "wide" are vague. Use ratios ("half the width of the store", "3x the opening of the barn")
3. **Call out visual indicators** — Flags, poles, steeples, and other vertical elements help distinguish similar shapes from a top-down view
4. **Show gameplay in action** — Include at least one "action" element (a ball being blasted, an air stream) to communicate the dynamic
5. **Dashed lines for transparent/conceptual elements** — Acrylic, air flow, blast paths — use dashed/dotted lines with reduced opacity
6. **Label everything, even if small** — 6-7px labels are still readable in 900px-wide screenshots. Every element should have text

### Common pitfalls:
- **Never use emoji characters in Canvas diagrams** — headless Chromium renders them as purple squares or missing glyphs. Always DRAW icons (bees, crowns, droplets, bells) with Canvas paths instead. A 10-line drawBee() function beats a one-line emoji every time in screenshot reliability
- Side cross-sections need more vertical exaggeration to be readable — a 6" gap drawn to scale on a 900px canvas is nearly invisible. Scale it up
- Canvas text at < 6px becomes unreadable in screenshots
- Overlapping elements in the center get cluttered fast — space out the most important elements first, fill gaps with secondary items
- Don't forget to show how the player interacts — hands, positions, sight lines help communicate ergonomics
- When scoring buckets/zones are tightly packed horizontally, their labels can overlap. Use smaller font or vertically stagger labels for narrow adjacent elements
- For vertical games (tall boards), choose FRONT + SIDE views rather than TOP-DOWN + SIDE. The front view is the player's perspective and communicates the most gameplay information
- Show multiple trajectories (weak vs strong) to communicate variable mechanics — use different opacities to distinguish primary vs secondary examples
- For complex machines with moving parts (flippers, bumpers), show GHOST positions at reduced opacity to communicate range of motion. This immediately conveys "this thing moves" without animation
- Cable/linkage mechanisms (like bike cable to flipper) benefit from showing the external control AND the internal part connected by a dashed line — communicates the actuation path
- When a game has distinct vertical zones (bumper zone, peg field, flipper zone), use subtle colored bands on a sidebar to annotate the zone structure — helps readers understand spatial layout at a glance
- For head-to-head 2-player games, a TOP-DOWN view is essential to communicate the spatial relationship between players. FRONT view shows one side's mechanics, TOP-DOWN shows the competitive dynamic. Both views together tell the full story
- When a game has pass-through mechanics (balls going through a wall/barrier), show the path crossing the barrier in the top-down view with contrasting player colors to make the interaction clear
- Estimate total page height carefully — legend + specs below two canvas views can easily push past 1600px. Use `<!-- screenshot: 900xNNNN -->` hints and test at 1900px+ for content-heavy pages
- Warm color palettes (browns, oranges, golds) work well for craft/wood-themed projects — don't default to dark navy for everything. Match the background to the project's material palette
- When a game has a distinctive aesthetic (craft supplies, neon, rustic), lean into it in the diagram styling — background colors, border styles, font choices should reinforce the theme
- Callout boxes for non-structural features (e.g. take-home kits, prize info) can be added as styled HTML sections below the canvas — keeps the diagram clean while communicating the full experience
- Stick figures in side cross-sections effectively communicate player height and interaction posture — worth the 10 lines of code
- For games with projectile/swing mechanics, show the object in its "ready" position AND a ghost at the impact point — the two positions connected by a trajectory arc communicate the full action in a single frame
- Flying/scattering objects (debris, blocks) at partial opacity with slight rotation angles convey impact energy and chaos without animation
- For tech-augmented concepts (CV, monitors, cameras), show THREE views: physical setup (front), physical construction (side cross-section), AND the digital display layout (monitor mockup). The monitor mockup is essential — it communicates the software experience that makes the concept unique
- When showing camera FOV cones, use dashed low-opacity lines from the lens to the field edges. This immediately communicates "this camera sees this area" without cluttering the diagram
- Connection lines between compute (Pi, laptop) and peripherals (cameras, monitor, speakers) should use dashed lines with labeled protocol (USB, HDMI, AUX) — communicates the wiring without looking like structural elements
- For pose detection visualization, show a stick figure with colored joint dots and bone lines — the "skeleton overlay" look is universally recognized from sports/fitness apps and immediately communicates "computer vision tracking"
- A "gameplay sequence" strip at the bottom (numbered circles with short labels connected by arrows) is an effective way to communicate game flow in a static diagram — especially for non-obvious games
- Radial gradient fills on spheres/balls create convincing 3D depth on a 2D canvas — place the highlight offset from center toward the "light source"
- For freestanding structures (gantry, frame), showing sandbags/anchoring in the diagram communicates stability and safety — reviewers immediately understand "this won't tip over"

### Rendering intangible/atmospheric elements:
1. **Fog and mist zones** — Use gradient fills (opaque at source → transparent at edges) rather than solid fills. Add subtle curved stroke "swirl" hints to suggest movement
2. **Glow effects** — Canvas `shadowColor` + `shadowBlur` on small elements (pegs, balls) creates convincing blacklight/UV glow without cluttering the diagram. Keep blur radius small (3-8px)
3. **Lightning/electrical effects** — Zigzag line segments with reduced opacity + a glow shadow sell the effect. One bright bolt is more readable than many faint ones
4. **Sound indicators** — Small rectangles for chime tubes attached to pegs, speaker cone circles for subwoofers, and wave arcs for bass vibration. Sound is invisible but the hardware is drawable
5. **Smell and mist** — Show the physical delivery system (nozzles, spray lines) with dashed spray-pattern lines radiating outward. The viewer infers the sensation from the hardware
6. **Sensory system callouts** — When a game has multiple subsystems (fog, light, sound, mist, candy), label each one clearly in the side cross-section where spatial relationships between hidden components matter most
7. **Stagger dense labels vertically** — When multiple scoring buckets or elements are tightly packed, alternate label Y positions (even items above, odd items below) to prevent overlap

### Multi-phase gameplay diagrams:
- When a game has distinct phases (setup/build → action → scoring), use HTML-based gameplay sequence strips rather than canvas-drawn ones — HTML `flexbox` with styled divs renders more reliably than canvas text for complex layouts with arrows and labels
- For games where players modify the board (placing deflectors, ramps, etc.), show BOTH the player-placed elements AND the resulting ball trajectories in the front view. The "before/after" of player agency is the key story
- Inset detail views (zoomed cross-sections of specific mechanisms) work well in the side view canvas when the main view can't show small components clearly — e.g., magnetic attachment, hinge mechanisms, wedge geometry
- Zone sidebar annotations (colored bands on the edge of the board) effectively segment vertical games into functional regions (hopper zone, play zone, scoring zone) without cluttering the main diagram

### Non-plinko game types (ring toss, maze, reaction games):
1. **Tabletop/platform games need both TOP-DOWN and SIDE views** — For games played on a horizontal surface (ring toss platform, tilting maze table), the top-down view shows the gameplay layout while the side cross-section shows the structure, player height, and hidden mechanisms. Neither view alone tells the full story
2. **Variable-height elements on a platform** — When multiple objects rise from a surface at different heights (tentacles, pegs, posts), the front view communicates height differences and the top-down shows spatial distribution. Use color AND size differentiation — in a screenshot, two same-colored elements of different diameters are harder to distinguish than two different-colored elements
3. **Organic/irregular layouts** — For games where elements are intentionally non-grid (tentacles, scattered obstacles), the top-down view is critical for showing the actual spatial relationships. Label difficulty zones with subtle colored bands (HARD/MEDIUM/EASY) to communicate the strategic geography
4. **Mechanism cross-sections** — For hidden mechanisms (gimbal axes, bell alarms, plunger paths), the side cross-section needs exaggerated scale and clear labeling of each component in the chain. Show the full actuation path: crank → connecting rod → axis → surface tilt. A reviewer should understand how the mechanism works from the diagram alone
5. **Two-sided boards** — When a game has players on both sides of a board (whack-a-mole, slingshot siege), the side cross-section is essential for showing the spatial relationship between the two players and what each one sees/does. Color-code the two player zones with subtle background tints
6. **Character expressions** — For social/comedy games, adding simple expressions to stick figures (grins, raised eyebrows) and to game elements (googly eyes on mole faces) communicates the game's emotional tone in ways that structural diagrams alone cannot
7. **Motion blur and swing arcs** — For reaction/swinging games, show motion trails (parallel lines at reducing opacity trailing behind a moving object) and swing arcs (curved stroke with an arrowhead) to communicate speed and action in a still frame
8. **Hidden player visibility cues** — When one player is hidden behind a structure but partially visible (peeking eyes over a board, feet visible underneath), drawing these details communicates emergent gameplay mechanics that aren't obvious from the build plan alone
