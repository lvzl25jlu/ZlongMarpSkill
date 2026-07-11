# Slide patterns

Derive each layout from the information structure before consulting the examples below. These patterns illustrate useful techniques but are not a menu that every slide must fit. Compose a new layout when the content has a different number of items, hierarchy, direction, or grouping. Do not repeat the same silhouette on every slide.

## Layout synthesis

1. Extract the atomic content units and count the peer items.
2. Classify their relationships: equal peers, comparison, hierarchy, shared input, shared output, sequence, branching, convergence, continuum, or parallel requirements.
3. Choose a geometry that preserves both rank and cardinality. Use equal cards for equal peers and distribute them in a balanced row or grid; four equal peers normally form a `2 × 2` grid rather than a one-over-three hierarchy.
4. Add arrows, spanning cards, nesting, or a progress bar only when the classified relationship calls for them.
5. After the geometry is decided, borrow styling and implementation techniques from `assets/template.md` or construct the slide directly with CSS.
6. Verify that the finished visual could be reconstructed back into the same content structure without inventing or losing relationships.

## Agenda

List major sections in cyan and subsections in light blue. Keep the hierarchy visible and concise.

When the agenda is too long for one vertical list, wrap the list in a `div` with `column-count:2` and an appropriate `column-gap`, for example `36px`. Keep each major section and its nested subsection list together when possible; do not use columns for a short agenda.

## Section divider

Use a standalone `#` heading with cyan text and thick horizontal rules on both sides. Keep the page otherwise sparse.

## Technical content

Use a fixed-top `##` heading as a concise navigation label derived from the outline. Preserve meaningful user-provided headings. Reuse a label across consecutive slides only when those slides genuinely belong to the same outline section; do not substitute generic labels merely because they appear in a template.

## Two-column comparison

Use equal-width gradient fieldset cards for theory comparisons, original-versus-reproduction results, method comparisons, or advantages versus limitations. Use semantic colors instead of arbitrary decoration.

Keep each fieldset legend short and plain text. Put formulas and all Markdown formatting in the fieldset body, separated from the surrounding HTML tags by blank lines.

## Asymmetric three-card composition

Use one large fieldset on the left and two stacked fieldsets on the right when one perspective is dominant and two compact supporting perspectives complete the argument. Keep the right cards equal in height. Use distinct but harmonious semantic colors, such as cyan for the main idea, purple for interpretation, and green for outcome.

## Stacked labeled information rows

Stack three to five compact horizontal rows vertically. Give each row a short bold label with a consistent minimum width and a concise explanation beside it. Use `div` elements for both label and description, especially when the description may contain mathematics or Markdown. The shared template rule `div p { margin:0; }` removes the default margin from Markdown-generated paragraphs so the text remains vertically centered. Use a pale background and a stronger left border in a distinct color for each row. Choose the row colors autonomously from their relationships and the surrounding slides rather than assigning fixed colors to fixed meanings. This structure works well for limitations, findings, assumptions, requirements, or parallel points that need more explanation than a card title but less hierarchy than separate fieldsets.

## Process

Use three to five horizontally connected gradient modules. Prefer a longer five-step row when the process genuinely contains five distinct stages and still fits the slide. Keep labels short and add one small explanatory line only when needed. Use for physical evolution, method stages, model components, and task progress.

Use arrows only when each item advances, produces, transforms into, constrains, or depends on the next. If several items are requirements that apply to every stage—such as inputs, outputs, uncertainty sources, and validation data—show them as a list or non-directional group instead of an arrow chain.

Assign one dominant hue to each node and use a subtle same-family gradient inside that node. Render each arrow with a text gradient that transitions from the dominant hue of the preceding node to the dominant hue of the following node. This makes the process read as a continuous color transition rather than a row of unrelated boxes.

When a node itself uses a gradient, treat its trailing color as the connector's source endpoint and the following node's leading color as the connector's target endpoint. Keep the connector direction and gradient direction consistent.

Use nested block elements for intentional line breaks inside process nodes. Do not rely on `white-space` properties, because they can inhibit wrapping and create overflow. Keep a blank line after every node or arrow `<div>` opening tag and before its closing tag when Markdown parsing is needed. Use `<br>` only when nested blocks cannot express the required layout reliably.

Keep the reusable template content-neutral. Use natural labels such as `Step 1` and `Stage 1 note` rather than brace-style variables or domain-specific steps, equations, and icons. Let real content determine the final node height; do not add fixed height merely to make an otherwise empty example look substantial.

## One-over-three card layout

Use one full-width card and three equal sibling cards only when the content actually contains one item of a different rank and three mutually parallel items. Determine direction from meaning rather than from the template example: place a shared input, premise, or preparation above three branches; place a shared output, synthesis, or conclusion below three peer inputs or goals. Keep all three peers aligned, equal in size, and at the same visual level. Invert the layout to three-over-one whenever the relationship requires it. Choose four distinct but harmonious card colors according to the actual content relationship.

This pattern is especially useful for a prior-work recap: one common preparation stage followed by three related tasks.

## Directory-based task framework

Use an outer fieldset to represent the project or root directory. Place sibling workstream fieldsets inside it. Within each workstream, nest entities, conditions, repetitions, or outputs as small bordered groups and chips. Add a compact legend or engine strip below the main hierarchy for shared tools and execution settings.

Use this pattern primarily to visualize a real working-directory hierarchy for simulation or analysis tasks. Apply it to another hierarchy only when the nesting genuinely corresponds to root, branch, subdirectory, and leaf levels; do not treat the nested fieldsets as ordinary reusable cards. Keep legends plain text and move equations into body content.

## Grouped compound process

Use a large horizontal process when some stages contain internal serial or parallel work. Represent a compound stage with a transparent or white container whose border is a gradient. Place its internal nodes inside the container, using a row for serial steps and a column for parallel branches. Continue the outer process with gradient arrows.

Use this pattern when a simple chain hides meaningful internal structure. Keep the number of visual hierarchy levels to two whenever possible. Align serial members with the outer flow and arrange parallel members perpendicular to it, centered on the outer connector axis. Choose a coherent palette for a composite group, derive one representative group color from that palette, and use it as the endpoint color for external connectors.

## Stage with progress bar

Use a horizontal multicolor spectrum for a continuous variable, state fraction, maturity level, or physical regime. Label both endpoints and place the central definition or conserved quantity above the bar. Below it, explain the corresponding mechanism with a process diagram that reuses the spectrum colors in the same order.

Also label the physical endpoint states inside the left and right ends of the gradient bar. Give each process node a concise main label and, when useful, one smaller normal-weight explanatory line so the visual connects the variable definition to the physical mechanism rather than showing generic states.

Place the three labels in equal-width left, center, and right grid cells with explicit text alignment. Do not rely on `justify-content:space-between`, because unequal label lengths shift the center label away from the true midpoint.

The color correspondence must carry meaning: the audience should be able to map positions on the spectrum to stages in the process without rereading the prose.

## Visual contrast and self-critique

Use two strongly contrasted visual mockups to compare an elaborate plan with the actual state, an expected outcome with reality, or excessive complexity with a minimal result. Familiar interfaces such as a document window, editor, terminal, or folder tree may be recreated with CSS. Follow the comparison with one concise takeaway card that explains the root cause or lesson.

Use equal-width and equal-height comparison panels. Prefer a three-column grid with `minmax(0,1fr) auto minmax(0,1fr)` so the center comparison marker does not distort the panel widths. Constrain dense mock content with smaller responsive type, `min-width:0`, wrapping, and hidden overflow. Use the standard semantic gradient for the takeaway fieldset rather than a flat fill.

This pattern works because the contrast is visible before it is explained. Avoid replacing the mockups with two long text columns.

## Multiscale dependency ladder

Use centered bands that widen progressively from microscopic structure to macroscopic outcome. Apply a smooth palette progression such as green, cyan, blue, purple, and pink. The changing width should reinforce accumulation across scales rather than decorate the page arbitrarily.

## Method landscape

Use four equally sized method-family cards in a 2×2 grid with a compact central theme card over the intersection. Keep the four colors harmonious and reserve the dark center for the shared problem or research theme.

## Methods to outputs

Use a left column of methods, a narrow central arrow, and a right column of outputs. This structure can support different technical domains without changing its underlying logic. Allow the left and right card counts to differ when one method family produces several observables.

## Text and figure

Use `1fr 1fr`, `1.2fr 1fr`, `1fr 2fr`, or `1fr 3fr` according to the figure's importance. Preserve aspect ratio and center the figure.

## Equation and takeaway

Center the main equation, then place a red or blue gradient card below it to state the physical meaning, essential distinction, or key variable.

If an equation is inside a card, place it in the body with blank lines around the Markdown equation block. Never place the equation in the card legend.

## Experiment result

Show the primary figure or table, one highlighted observation, and a short interpretation. When comparing reproduction work, make the source-versus-current-work relationship explicit.

## Citation and note

Put short citations in the upper-right corner using `position:fixed; top:0; right:0; padding:15px; z-index:999`. Use black italic Times New Roman with `line-height:1.0`. One or two compact citation lines should occupy the right end of the space created by the fixed `##` heading and its underline without covering the main slide body.

Put supplementary annotations close to the content they qualify using a `span` with `font-size:small; color:gray; font-style:italic`. Keep annotation text concise and visually subordinate.

## Final slide

Use `Thank You!` or its natural equivalent in the selected presentation language as the primary heading. Use a brief invitation for comments as the secondary line. Do not include a personal name unless the user supplies one for the current deck.
