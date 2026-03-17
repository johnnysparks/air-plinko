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
