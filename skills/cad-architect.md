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
