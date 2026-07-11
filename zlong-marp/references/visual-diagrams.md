# Visual diagram strategy

Use diagrams to replace exposition only when the content has a relationship that can be shown more clearly than it can be described. Favor a single explanatory composition over many decorative components.

Before drawing, classify the relationship and count the peer items. Preserve equal visual rank and balanced geometry for peers, separate genuine shared inputs or outputs, and reserve arrows for actual directional relationships. Determine this topology independently before consulting any template; use templates only for reusable visual techniques.

## Selection order

1. Reuse an existing user-supplied figure when it already communicates the idea well.
2. Build an editable CSS and HTML diagram for boxes, bands, arrows, grids, trees, stages, spectra, mock interfaces, and architecture maps.
3. Use SVG only when precise custom geometry is necessary and CSS is insufficient.
4. Fall back to concise text and equations when a visual would add complexity without explanatory value.

## CSS diagram families

### Spatial or physical band

Use a bounded horizontal region divided into colored physical zones. Add absolute-positioned boundaries, dashed reference locations, direction arrows, and compact labels. Follow it with no more than two takeaway cards. This is suitable for waves, interfaces, reaction zones, material regions, and spatial regimes.

### Continuous spectrum

Use a horizontal gradient bar with labeled endpoints and an optional central definition. Reuse the same colors in a process or state diagram below it. Keep the order consistent so color becomes a semantic link between the two visuals.

Anchor labels with a three-column grid: left label aligned left, definition aligned center, and right label aligned right.

### Nested hierarchy

Use nested borders or fieldsets for layers, directories, workstreams, entities, and runs. Combine outer groups with small chips only when the hierarchy itself is the message. Avoid nesting deeper than three visible levels.

### Compound flow

Use a long outer flow with gradient arrows. A stage may be a grouped container holding serial inner nodes or parallel branches. Give grouped containers gradient borders and white interiors so the hierarchy remains visible without becoming visually heavy.

Connector colors are structural: interpolate from the source component's exit or dominant color to the target component's entry or dominant color. For a grouped component, derive a representative theme color from a coherent internal palette. Align serial members with the flow, arrange parallel members perpendicular to it, and center external connectors on the grouped component.

### Contrast mockup

Recreate familiar documents, editors, terminals, or folder trees with CSS when their visual contrast communicates the argument faster than prose. Pair the mockups with a short lesson card rather than a paragraph-heavy explanation.

Keep the two mockup frames exactly equal in width and height. Let their internal content adapt through constrained flex areas, responsive font sizing, line wrapping, and overflow control.

### Paired state sequence

Place two vertical or horizontal state sequences side by side, using semantic colors such as red for a false positive or failure case and green for a retained or correct state. Align corresponding frames so the comparison is immediate.

## Visual economy

- Do not decorate a slide with a diagram that merely repeats its text.
- Prefer one dominant visual and one or two short explanatory blocks.
- Reduce prose before reducing diagram labels below a readable size.
- Keep node labels short and use nested block elements for intentional line breaks. Avoid `white-space` properties so long labels can wrap instead of overflowing.
- Keep formula-bearing content outside legends and preserve blank lines around Markdown inside HTML containers.
- If a ladder, spectrum, or summary band restates the same ordered components as another visual, reuse the exact component colors in the same order rather than selecting a second palette.

## SVG policy

SVG is allowed but should not be the first choice. Use it for concepts such as atom neighborhoods, local geometry, bond deformation, electronic clouds, custom curves, or other scientific shapes that CSS boxes cannot express faithfully.

When using SVG:

- Start from the simplest geometry that communicates the concept.
- Use a clear `viewBox` and scale through CSS rather than hard-coding a fragile display size.
- Limit the palette and match the deck's semantic colors.
- Keep labels outside crowded geometry when possible.
- Build in small increments and render after each meaningful revision.
- Inspect the SVG at full slide size for clipping, overlap, illegible labels, distorted paths, and ambiguous visual meaning.
- Expect multiple iterations; do not trust a one-pass AI-generated SVG for a complex scientific illustration.

## SVG examples worth emulating cautiously

- A local atomic-neighborhood diagram can explain how a central atom and neighbors map to an energy contribution. Keep the mathematical statement in the surrounding card body, not in a legend.
- A paired three-frame state sequence can contrast geometrically close but unbonded atoms with a stretched but still bonded pair. Align the frames and use opposing semantic colors.
- A dense architecture map can combine nested layers, stages, principles, and object categories, but prefer a CSS reconstruction when the same structure can be expressed without custom paths.
