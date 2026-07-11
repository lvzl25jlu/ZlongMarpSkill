---
name: zlong-marp
description: Create complete Marp presentations from user-provided outlines and research materials using Zlong's bundled templates and presentation conventions. Use when creating, revising, compiling, or exporting group-meeting slides, research updates, experiment reports, and academic presentations with Marp.
---

# Zlong Marp

Create a presentation-ready technical or academic Marp deck in Zlong's recognizable white-background, cyan-blue, semantic-card style.

## Workflow

1. Inspect the outline wherever the user supplied it: in the request, an attachment, a separate outline file, or an existing Marp source such as `slide.md`. Inspect every supplied asset. Determine the target presentation folder and Markdown filename from the request and surrounding context; create missing targets only when presentation generation is requested.
2. Read `references/style-guide.md` and `references/slide-patterns.md` before planning the deck. Read `references/latex-style.md` whenever the deck contains mathematics. Read `references/visual-diagrams.md` whenever a concept could benefit from a diagram.
3. When the outline is already stored in the target Marp file, replace that outline in place with the completed deck. Otherwise, write to the user-specified target file; when no filename is specified, use `slide.md` in the target presentation folder as the default. Preserve the outline's facts, order, hierarchy, emphasis, and intended scope. Do not overwrite unrelated files or create a second deck file unless the user requests one.
4. Before inspecting `assets/template.md`, map each planned slide as a content structure: identify the number of peer items, hierarchy levels, shared inputs or outputs, comparisons, sequences, continua, and parallel requirements. Design the provisional layout from that map.
5. Only after the content structure is clear, inspect `assets/template.md` for reusable styling, CSS techniques, and occasional structural inspiration. Templates are examples, not a catalog of permitted layouts. Create a new CSS layout whenever none of the examples faithfully represents the content.
6. Determine the presentation language from the user's request, outline, source materials, topic, and intended audience.
7. Write concise content and implement the layout derived from the content; favor comparisons, processes, equations, figures, and conclusion cards only when those forms match the underlying relationship.
8. Audit the semantic mapping before delivery: confirm that visual grouping, rank, direction, and cardinality match the content structure, and that no template artifact has introduced a relationship absent from the outline.
9. Preserve the bundled Marp frontmatter, theme, and CSS conventions.
10. Leave the target Marp Markdown file ready for the user's manual revisions and normal manual export workflow. Do not export automatically unless the user requests it.
11. When export or rendered validation is requested and Marp CLI is available, run the appropriate Marp CLI command, inspect the rendered output, and fix overflow, crowding, missing assets, and poor contrast.

## Language selection

- Follow an explicit language request when provided.
- Otherwise, use the dominant language of the outline and source materials.
- If the inputs mix languages, infer the best audience-facing language from the surrounding context, intended audience, and topic.
- Keep established technical terms, symbols, acronyms, paper titles, and proper nouns in their clearest conventional form even when they differ from the main language.
- Keep the deck internally consistent; do not switch languages casually between headings or slides.

## Content rules

- Express one main idea per slide.
- Infer the layout from semantic structure and item count, not from resemblance to an existing template.
- Give peer items equal visual rank and choose a balanced geometry that fits their count and content length. Four equal peers normally suggest a `2 × 2` grid; other counts require an equally deliberate arrangement rather than forcing one item into a different rank.
- Represent hierarchy, convergence, divergence, comparison, sequence, and continuity only when those relationships exist in the content.
- Build a new arrangement from CSS primitives whenever the available examples do not match. Reuse colors, card treatments, typography, spacing, and diagram techniques independently of the example's original composition.
- Derive slide titles and section labels from the outline. Preserve meaningful user-provided headings; do not replace them with generic labels such as `Background`, `Model`, or `Process` merely because those labels appeared in a template.
- Do not invent experimental results, citations, or missing facts.
- Mark missing information with explicit `TODO` placeholders.
- Prefer figures, diagrams, and tables over dense paragraphs.
- When a concept would otherwise require a long paragraph plus several equations, first attempt a purpose-built CSS diagram that exposes the spatial, sequential, hierarchical, or state relationship.
- Preserve image aspect ratios and use relative asset paths.
- Distinguish observations from interpretations and hypotheses.
- Keep terminology consistent across the deck.
- Add agenda, section-divider, summary, next-step, or closing slides only when the outline, user request, deck length, or audience need justifies them. Do not impose a standard academic-presentation sequence on every outline.
- Never insert a real person's name unless the user explicitly supplies it for the current deck. Use a natural neutral label such as `Author` in reusable templates, then replace or remove it for the final deck as appropriate.

## Marp syntax constraints

- Keep every `<legend>` label plain text. Do not place LaTeX, MathJax delimiters, Markdown emphasis, images, links, or other Markdown syntax inside `<legend>`.
- When a card needs an equation, put the equation in the card body rather than in `<legend>`.
- Whenever Markdown must be rendered inside a `<div>`, `<span>`, `<fieldset>`, or other HTML container, place a blank line immediately after the opening tag and immediately before the closing tag.
- Put block Markdown such as lists, equations, tables, and images on their own lines inside the container. Do not write block Markdown on the same line as an HTML tag.
- Preserve these blank lines during revisions and formatting; they are required for reliable Marp rendering.
- Do not use CSS `white-space` properties in generated slides. Let text wrap naturally and use nested block elements for intentional line breaks.
- Use `line-height:1.5` as the normal card-body line height unless a specific compact visual requires a justified exception.

## Diagram constraints

- Prefer CSS and HTML diagrams for processes, spectra, state ranges, architecture maps, task trees, comparison mockups, and other box-and-arrow structures.
- Use arrows only for a real temporal, causal, transformational, directional, or dependency relationship. Do not connect parallel attributes, checklist items, required metadata, or equally ranked variables with arrows merely to decorate the line.
- Present parallel requirements as a Markdown list, aligned rows, chips without arrows, or another non-directional grouping.
- Color every connector as a gradient from the source's exit or dominant color to the target's entry or dominant color. For a composite group, derive a representative group color from its coherent internal palette and use that color at the external connector endpoint.
- Align serial members with the main flow direction. Arrange parallel members perpendicular to the main flow and center external connectors on the group so direction and grouping remain visually unambiguous.
- When a summary band, spectrum, legend, or dependency strip describes the same ordered components as a diagram, reuse the component colors in the same order.
- Coordinate colors across related visuals on the same slide; a spectrum bar and its explanatory process should reuse the same color progression.
- Make the unity or separation of colors match the unity or separation of the content. Let a central or parent element visibly synthesize the colors of its children; use neighboring hues or a continuous progression for related groups, stages, or transformations; reserve strongly opposed palettes for genuinely opposed states, inputs and outputs framed as a contrast, or other explicit conceptual opposition. Derive group theme colors from their members instead of assigning unrelated accents.
- Use SVG only when the concept depends on precise custom geometry that CSS cannot express clearly. Treat SVG as an iterative, render-and-inspect task rather than a one-pass default.

## Fieldset palette constraints

- Choose every fieldset card from the seven approved border, legend, and pale-background triples in `references/style-guide.md`.
- Do not invent near-duplicate fieldset colors. Preserve each approved triple as a unit.
- Treat orange and cyan fieldsets as occasional accents rather than default choices; prefer blue, green, purple, pink, or red when their semantics fit.
- Keep every `<legend>` bold by default, matching `font-weight:bold; color:<dark-card-color>; padding:0 6px;`. A color-only legend class is insufficient unless bold weight and padding are supplied by a shared rule.
- Choose each slide's palette autonomously from its semantic relationships, desired contrast, visual harmony, and neighboring slides. Treat the combinations in `references/style-guide.md` as examples, not mandatory mappings or default priorities.
- Never repeat a dominant semantic color across peer cards, fieldsets, or process nodes on the same slide.
- Avoid reusing the dominant semantic colors of one slide on the immediately adjacent slides when another semantically valid assignment is available.

## LaTeX constraints

- Use `$...$` for inline mathematics and `$$...$$` for display mathematics. Do not use `\(...\)` or `\[...\]` as equation delimiters.
- Typeset differential `d`, the natural-exponential constant `e`, and the imaginary unit `i` upright with `\mathrm`, for example `\mathrm{d}x`, `\mathrm{e}^{x}`, and `\mathrm{i}`.
- Wrap semantic-word subscripts in `\text`, for example `u_{\text{unreacted}}`. Leave variable subscripts italic, for example `p_x`.
- Use scalable round parentheses written as `\left(...\right)` for grouping and function calls. Do not substitute square brackets or braces merely to show precedence.
- Avoid decorative spacing commands such as `\,`. Use spacing commands only when they express a real structure; `a=b,\quad c=d` is acceptable for multiple relations on one line.

## Resource conventions

- Store reusable Marp templates, CSS, logos, fonts, and static media in `assets/`.
- Keep general-purpose layouts and curated visual excerpts in one coherent `assets/template.md`, separated by `# General Templates` and `# Special Templates`. Special templates represent occasional especially successful pages, not a default vocabulary, narrative sequence, or set of copy-ready requirements.
- Store detailed writing, layout, and slide-pattern guidance in `references/`.
- Keep generated presentations outside the skill directory unless the user explicitly requests otherwise.
- Remove unused example and reference slides when producing the final audience-facing deck; retain only structures that serve the supplied outline.
