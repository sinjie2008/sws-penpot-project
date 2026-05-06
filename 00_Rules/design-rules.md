# design-rules.md

## Purpose
This file defines the design rules for Superworld Electronics Penpot website work.

It covers:
- wireframe rules
- final design rules
- spacing rules
- typography rules
- component rules
- Superworld content rules
- Penpot MCP design behavior

---

## Brand direction
The design must feel:

- modern
- clean
- professional
- B2B
- engineering-focused
- credible
- structured
- easy to scan

Avoid:

- childish visuals
- overly colorful design
- decorative clutter
- fake technical details
- long paragraphs
- duplicated content
- inconsistent spacing
- random styling

---

## Company name rule
Always keep the company name in English:

`Superworld Electronics`

Do not translate it.

---

## Website content direction
The design should support Superworld Electronics as a B2B electronics manufacturer and supplier.

Common content themes:

- magnetic components
- EMC components
- high-frequency transformers
- wireless power solutions
- automotive applications
- communication and networking applications
- consumer electronics
- healthcare devices
- industrial and energy
- smart home
- quality and reliability
- global manufacturing support
- engineering credibility

Do not invent product specifications.

---

# Wireframe rules

## Wireframe mode
Wireframe mode is low-fidelity only.

Use wireframe mode for:

- page structure
- section order
- content hierarchy
- layout planning
- spacing planning
- placement
- navigation structure

Do not make the wireframe look like final design.

## Wireframe visual style
Use:

- pure white background
- black text
- black, white, or grayscale lines
- simple boxes
- simple dividers
- simple placeholder blocks

Do not use:

- brand color
- accent color
- gradient
- shadow
- photo fill
- image fill
- illustration
- polished card styling
- glow
- blur
- texture
- decorative background

## Image-to-wireframe rule
When converting raw wireframe image or screenshot into Penpot wireframe:

- extract structure only
- extract visible text
- extract visible sections
- extract visible layout
- extract visible UI elements
- convert all images into placeholder boxes
- keep placeholders as simple rectangles
- label placeholders clearly, such as `Image`, `Banner`, `Product Image`, or `Thumbnail`
- do not preserve the original visual style
- do not preserve color from the image

## Wireframe text rule
All text must be editable.

Keep separate text layers for:

- heading
- subheading
- paragraph
- label
- caption
- button text
- card title
- list item
- table header
- table cell

Do not combine unrelated text into one text layer.

## Wireframe object rule
Keep visual elements separately editable.

Separate:

- boxes
- cards
- sections
- buttons
- dividers
- icons
- placeholders
- tables
- columns
- rows

Do not flatten the wireframe into one large object.

---

# Final design rules

## Final design mode
Only enter final design mode when the wireframe is approved or when the user explicitly requests final design.

Final design can include:

- color
- typography refinement
- component styling
- image placement
- polished layout
- visual hierarchy
- final desktop design presentation

Do not automatically convert wireframe into final design without approval.

## Final design objective
Final design must improve:

- clarity
- readability
- hierarchy
- consistency
- usability
- visual balance
- professional B2B presentation

## Layout foundation
Use:

- clean grid-based layout
- consistent content width
- controlled text width
- strong alignment
- balanced whitespace

Default desktop frame:

- frame width: `1440 px`
- content width: `1200 px` to `1280 px`
- content centered
- section spacing controlled

## Typography
Use:

- heading font: `Poppins`
- body font: `Inter`

Typography must show clear hierarchy:

- page title
- section heading
- subheading
- body text
- caption
- button text
- label

Avoid random font sizes.

## Spacing system
Use an 8-point spacing system.

Preferred spacing scale:

- 4
- 8
- 12
- 16
- 24
- 32
- 40
- 48
- 64
- 80
- 96

Use spacing intentionally.

## Spacing usage
Recommended use:

- `4 px`: very tight internal spacing only
- `8 px`: icon-to-text gap, small UI gap
- `12 px`: compact secondary spacing
- `16 px`: default related item spacing
- `24 px`: grouped content spacing
- `32 px`: card padding or medium block spacing
- `48 px`: tight section spacing
- `64 px`: normal section spacing
- `80 px`: spacious section spacing
- `96 px`: hero or major section spacing

## Container rule
Do not confuse:

- container padding
- gap between child items
- section margin
- card internal spacing

Similar containers should use the same padding logic.

## Alignment rule
Align related items to consistent edges.

Repeated items should use:

- same width
- same gap
- same padding
- same vertical rhythm
- same alignment

Avoid visual drift.

---

# Component rules

## Reusable component principle
Use reusable components when possible.

Recommended component groups:

- Header
- Footer
- Buttons
- Cards
- Tabs
- Accordions
- Product Cards
- Application Cards
- Forms
- Tables
- Section Titles
- CTA Blocks
- Badges
- Navigation
- Slider Controls

## Component behavior
Do not detach, rename, delete, or restructure components unless explicitly approved.

If a new reusable pattern appears more than once, create it as a component in:

`02 Components / Design System`

## Component naming
Use clear names.

Examples:

- `Buttons / Primary`
- `Buttons / Secondary`
- `Cards / Product Card`
- `Cards / Application Card`
- `Tabs / Default`
- `Accordion / Default`
- `Forms / Input`
- `Navigation / Section Nav`

---

# Penpot page rules

## `01 Wireframe`
Use for low-fidelity layout only.

Do not add:

- final colors
- final images
- final visual styling
- prototype interactions

## `02 Components / Design System`
Use for reusable UI elements.

Do not place full page design here unless it is a component example.

## `03 Final Design`
Use for approved desktop high-fidelity design.

Do not use this page for rough layout planning.

## `04 Mobile Design`
Use for mobile responsive layout only.

Do not assume mobile size unless confirmed.

## `05 Prototype / Flow`
Use for interaction flow only.

Examples:

- navigation flow
- tab switching
- slider behavior
- accordion behavior
- enquiry flow
- product selection flow
- mobile menu flow

---

# Superworld content rules

## Tone
Use a serious B2B tone.

The copy should sound:

- corporate
- clear
- practical
- engineering-aware
- credible
- concise

Avoid:

- hype
- vague marketing words
- overly long explanation
- unsupported claims
- copied competitor content

## Content structure
Make content scannable.

Prefer:

- short headings
- short paragraphs
- bullet points
- cards
- comparison blocks
- product/application mapping
- clear CTA

## Technical accuracy
Do not invent:

- product parameters
- part numbers
- certification claims
- test standards
- application fit
- component positions
- product availability

If unsure, use placeholder text or mark as pending input.

---

# Image rules

## Wireframe
Images become placeholders only.

## Final design
Use real images only when provided or approved.

If images are not available, use clean placeholders and label them clearly.

Do not use fake technical images.

---

# Error prevention rules

Before finishing any design or wireframe, check:

- correct Penpot page is used
- no wrong page was changed
- text is editable
- objects are separately editable
- spacing is consistent
- content width is controlled
- all required sections are included
- images are handled correctly
- no fake technical content is added
- no duplicate sections are created
- log files are updated

---

# Do not
- Do not update the wrong Penpot page
- Do not skip the status file
- Do not skip error logging
- Do not merge editable elements unnecessarily
- Do not use final design style in wireframe
- Do not copy competitor content
- Do not create fake product content
- Do not create mobile design inside desktop final design
- Do not create prototype flow inside final design unless requested
