# Zlong Marp style guide

## Design identity

Use a white canvas with cyan-blue headings and small areas of saturated semantic color. Present dense technical material through cards, equations, figures, comparisons, and short takeaways. Keep the result academic, lively, and recognizably personal rather than corporate or minimalist.

## Palette

| Meaning | Border or accent | Dark text | Pale background |
|---|---:|---:|---:|
| Cyan | `#38bdf8` | `#0369a1` | `#e0f2fe` |
| Information or method | `#3b82f6` | `#1e40af` | `#dbeafe` |
| Success or conclusion | `#10b981` | `#065f46` | `#d1fae5` |
| Concept or intermediate stage | `#8b5cf6` | `#5b21b6` | `#ede9fe` |
| Attention or uncertainty | `#f59e0b` | `#92400e` | `#fef3c7` |
| Problem or key contradiction | `#d93a49` | `#7f0000` | `#fff1f2` |
| Additional category | `#ec4899` | `#9f1239` | `#fce7f3` |

Use only these seven border, legend, and pale-background triples for fieldset cards. Do not introduce near-duplicate fieldset palettes such as `#ef4444`, `#f97316`, or `#06b6d4`.

When the chosen palette needs yellow, use `#eab308` border, `#854d0e` legend text, and `#fef9c3` pale background as a compatible optional triple. Yellow is available to the color plan but is not a routine default.

Use orange and cyan fieldsets sparingly. They remain available for a deliberate accent or semantic distinction, but should not dominate routine card layouts.

Additional process-gradient pairs:

- Purple: `#667eea` to `#764ba2`
- Pink: `#f093fb` to `#f5576c`
- Bright blue: `#4facfe` to `#00f2fe`
- Green: `#43e97b` to `#38f9d7`
- Orange: `#f97316` to `#fbbf24`

For fieldset cards, favor `linear-gradient(to bottom, #ffffff, <pale-color> 61.8%)`.

## Color relationships

- Make color encode the relationship between items rather than decorate them arbitrarily.
- Match chromatic unity to semantic unity. A parent, center, or summary should synthesize or visibly reuse the colors of the elements it contains or explains. Related groups should use neighboring hues, shared undertones, or a continuous progression; reserve complementary or strongly separated theme families for a real opposition in the content rather than using contrast merely to distinguish columns.
- Match the geometry of a composite gradient to the geometry of its sources. For elements surrounded from several directions, place radial gradient sources at the corresponding edges or corners; use a linear gradient only when the content has a meaningful axis, and use a conic gradient only when cyclic order or rotation is part of the relationship and its seam can be made visually continuous.
- Treat input-to-output opposition, method-to-output transformation, parallel categories, and center-to-surrounding containment as different relationships. Select contrast, continuity, distinct peers, or a composite theme accordingly; do not infer opposition from a left-to-right layout alone.
- Select the palette autonomously according to semantic relationships, readable contrast, visual harmony, the slide's role, and the colors used on neighboring slides. Do not treat any example combination as a mandatory mapping or default priority.
- A contrast may use clearly separated hues such as red and green, but choose a different contrasting pair when it fits the content or composition better.
- Parallel or equally ranked categories may use a more harmonious pairing such as blue and green, but other balanced combinations are equally valid.
- Three related or ordered contributions from one paper may use a warm red-orange-yellow sequence, but this is an example of a coherent sequential palette rather than a required formula.
- Give every peer card, fieldset, or process node on the same slide a different dominant color. Do not reuse the same semantic color twice on one slide.
- Compare each slide with the slides immediately before and after it. Avoid repeating the same dominant block colors on adjacent slides whenever the content allows a different valid assignment.
- Treat the global cyan-blue heading system, neutral text, and small connective marks as structural colors. The no-repeat rule applies to dominant semantic blocks.

## Heading hierarchy

- Use `#` for section dividers: centered cyan text with thick cyan rules on both sides.
- Use `##` for content-page navigation: light blue, fixed at the top, with a blue underline.
- Use `###` for local emphasis: white text on a red block.
- Treat headings primarily as navigation labels. Do not force every title into a consulting-style conclusion statement.

## Composition

- Use cards and color to segment technically dense information.
- Map semantic rank and item count before arranging cards. Equal-rank goals, methods, cases, or findings must use matching card size and placement in a balanced geometry; four equal peers normally use a `2 × 2` grid.
- Treat templates as references for visual language and implementation techniques, not as predefined slots. Design a new composition whenever the content structure does not match an example.
- Prefer one clear relationship per slide even when the page contains several details.
- Keep diagrams simple and horizontal when showing three to five stages.
- Use asymmetric text-image columns when the figure is the main evidence.
- Reserve large red areas for genuinely important problems or model distinctions.
- Use emoji sparingly as small semantic markers in process modules, not as decoration everywhere.
- In process diagrams, give each node a dominant color with a subtle local gradient. Every connector must interpolate from the source node's exit or dominant color to the target node's entry or dominant color; a connector must never use an unrelated decorative color.
- Give every composite group a representative theme color derived from its internal palette. Keep parallel members in a coherent color family so the group color can be inferred from their visual center rather than assigned arbitrarily.
- Align serial members with the main flow direction. Arrange parallel members perpendicular to it, balance them around the flow axis, and aim the incoming and outgoing connectors at the visual center of the group.
- Draw arrows only when they encode genuine sequence, causality, transformation, direction, or dependency. Use lists or non-directional groups for parallel requirements and attributes.
- Keep process-node and arrow contents separated from their `<div>` tags by blank lines, even when no Markdown is currently present.
- Use nested block elements for intentional line breaks inside process nodes. Avoid relying on `white-space` properties, which can make content resist wrapping and overflow. Use `<br>` only when nested blocks cannot express the required layout reliably.
- Use `line-height:1.5` as the default for card body text unless a specific compact visual requires a justified exception.
- Use `div p { margin:0; }` as the template default so Markdown-generated paragraphs inside HTML layout containers do not introduce unexpected vertical offsets. Restore paragraph spacing with a more specific local rule only when a multi-paragraph block genuinely needs it.
- Prefer explanatory visuals over long prose-plus-equation blocks when the content has a clear spatial, temporal, hierarchical, comparative, or state-transition structure.
- Use CSS diagrams as the default visual construction method because they remain editable, style-consistent, and easier to iterate in Marp.
- Reuse a meaningful color sequence across related diagrams on the same slide, especially when connecting a continuous spectrum to discrete process stages.
- When a summary strip or dependency band describes the same ordered layers or stages, reproduce their colors in the same order so the strip functions as a compact encoding of the diagram.
- Keep fieldset legends bold. Use the pattern `<legend style="font-weight:bold; color:<dark-card-color>; padding:0 6px;">Card title</legend>`, or provide the same weight, color, and padding through a class. Do not define legend classes that set only the color.

## Outline-first narrative

- Treat the supplied outline as authoritative for sequence, hierarchy, emphasis, and scope.
- Do not impose a default chain such as background, model, method, results, analysis, and outlook when the outline organizes the argument differently.
- Add navigation, section dividers, summaries, plans, or closing slides only when they serve the outline, audience, and deck length.
- Use general templates as routine layout tools and special templates as occasional inspiration; neither defines the presentation's storyline.

## Language

- Infer the most suitable presentation language from the explicit request, outline, source materials, intended audience, and surrounding context.
- Follow the outline's dominant language when no stronger signal exists.
- Preserve conventional English technical terms, acronyms, formulas, paper titles, and proper nouns when translating them would reduce clarity.
- Translate template placeholders and generic section labels into the chosen language.
- Keep audience-facing text consistent in language and register across the deck.

## Technical conventions

- Enable MathJax and keep important equations visually central.
- Follow `latex-style.md` for equation delimiters, upright symbols, semantic subscripts, parentheses, and spacing.
- Mix explanation in the selected presentation language with established English technical terms when that is clearer.
- Separate source-paper work from the user's reproduction or simulation results.
- Cite literature briefly in the upper-right corner of the relevant slide. Use a fixed black italic Times New Roman block with `top:0`, `right:0`, `padding:15px`, `z-index:999`, and `line-height:1.0`; allow up to two compact lines to fill the right end of the `##` heading-line area.
- Use small gray italic annotation spans for qualifications and secondary details.
- Do not invent data, citations, or missing technical facts.

## Marp and Markdown safety

- Treat `<legend>` as a plain-text-only label. Never place `$...$`, `$$...$$`, `\(...\)`, `\[...\]`, Markdown emphasis, links, or images inside it.
- Move mathematical notation out of `<legend>` and into the fieldset body. Use a short verbal legend such as `Governing equation`, `Key variable`, or `Model definition`.
- When Markdown appears inside an HTML container, keep the opening tag on its own line, insert one blank line, write the Markdown content, insert another blank line, and then write the closing tag.
- Apply the blank-line rule to paragraphs, emphasis, lists, tables, images, inline mathematics, and display mathematics whenever Markdown parsing is expected.
- Do not collapse the safe structure into a one-line HTML block during cleanup or optimization.

Safe card structure:

```html
<fieldset>
  <legend>Governing equation</legend>
  <div>

$$
E = mc^2
$$

  </div>
</fieldset>
```

Unsafe structures:

```html
<legend>$E = mc^2$</legend>
<div>**Important:** Markdown may not render reliably here.</div>
```

## Privacy

- Never hard-code a real person's name in this skill or generated deck.
- Use a natural neutral label such as `Author` in reusable templates rather than a brace-style variable.
- Replace the neutral label only when the user explicitly provides the desired display name for the current presentation; otherwise remove it when appropriate.
