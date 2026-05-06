# AGENTS.md

## Project purpose
This project is used to manage Superworld Electronics website design work in Penpot through Penpot MCP, Codex, and final front-end handoff.

The agent must understand the folder structure, follow the correct design stage, use Penpot MCP only for Penpot work, and track all errors.

---

## Required MCP
- Use Penpot MCP for all Penpot inspection, page creation, frame creation, wireframe recreation, design recreation, component creation, and prototype preparation.
- Do not use another design MCP server unless the user explicitly approves it.
- Before any Penpot action, confirm Penpot MCP is available.
- If Penpot MCP is not available, stop and record the issue in `05_Log_Tracking/error-log.md`.

---

## Penpot file rule
- Work only inside the current approved Penpot project file.
- Do not create, duplicate, rename, delete, or switch Penpot files unless the user explicitly approves it.
- Do not assume the correct Penpot file is open.
- Before editing, inspect the active Penpot file/project and confirm the target page.

---

## Approved Penpot pages
The project should use these Penpot pages only:

1. `01 Wireframe`
2. `02 Components / Design System`
3. `03 Final Design`
4. `04 Mobile Design`
5. `05 Prototype / Flow`

Do not create extra Penpot pages unless the user explicitly requests it.

---

## Folder map

### `00_Rules/`
Permanent project rules.

- `AGENTS.md`  
  Explains how the agent should work, what folders mean, which Penpot pages are allowed, and how errors must be tracked.

- `design-rules.md`  
  Defines visual design rules, wireframe rules, spacing, typography, components, and Superworld design style.

### `01_Input/`
Raw input files provided by the user.

- `raw-wireframe/`  
  Raw wireframe images, sketches, screenshots, or layout references.

- `reference-image/`  
  Website references, visual references, design references, screenshots.

- `content-notes/`  
  Text content, section notes, page purpose, product/application notes.

- `product-info/`  
  Product data, product family notes, series notes, specifications, catalog content.

### `02_Prompt/`
Instruction files for Codex, Penpot MCP, and design agents.

- `01_wireframe/`  
  Instructions for creating or updating Penpot page `01 Wireframe`.

- `03_final-design/`  
  Instructions for creating or updating Penpot page `03 Final Design`.

- `05_prototype/`  
  Instructions for creating or updating Penpot page `05 Prototype / Flow`.

### `03_Penpot_Status/`
Current stage tracking.

- `status.md`  
  Shows current stage, current Penpot page, latest action, next step, blocked items, and pages that must not be touched.

### `04_Final_Code/`
Final front-end output after design approval.

- `assets/`  
  All website assets, including images, icons, logos, videos, documents.

- `scss/`  
  Source SCSS files only.

- `js/`  
  Source JavaScript files.

- `dist/css/`  
  Compiled and minified CSS.

- `dist/js/`  
  Minified JavaScript.

- `index.html`  
  Final HTML page structure.

### `05_Log_Tracking/`
Mandatory tracking logs.

- `error-log.md`  
  Records MCP errors, broken layout issues, wrong page edits, missing content, failed actions, and unexpected results.

- `mcp-log.md`  
  Records Penpot MCP actions, inspections, page updates, frame updates, and MCP availability checks.

- `codex-log.md`  
  Records Codex commands, output summary, failed commands, and fixes.

- `design-change-log.md`  
  Records every user-requested design change.

- `fixed-issue-log.md`  
  Records resolved issues and the exact fix applied.

### `99_Archive/`
Old versions, rejected drafts, backup files, and previous outputs.

---

## Current stage rule
Before starting work, read:

1. `03_Penpot_Status/status.md`
2. `00_Rules/AGENTS.md`
3. `00_Rules/design-rules.md`
4. The relevant prompt folder for the current stage

Use the current stage to decide the correct Penpot page.

---

## Task mode rule
First decide whether the task is:

1. Inspection only
2. Wireframe
3. Components / Design System
4. Final Design
5. Mobile Design
6. Prototype / Flow
7. Final Code

If unclear, use the lower-fidelity stage and do not move forward automatically.

---

## Stage-to-page rule

### Wireframe task
Use:
- Folder: `02_Prompt/01_wireframe/`
- Penpot page: `01 Wireframe`
- Rules: low-fidelity only, black and white only

### Components task
Use:
- Folder: `00_Rules/design-rules.md`
- Penpot page: `02 Components / Design System`
- Rules: reusable components only

### Final design task
Use:
- Folder: `02_Prompt/03_final-design/`
- Penpot page: `03 Final Design`
- Rules: high-fidelity desktop design only

### Mobile design task
Use:
- Folder: `02_Prompt/03_final-design/` plus any mobile instruction
- Penpot page: `04 Mobile Design`
- Rules: mobile layout only

### Prototype task
Use:
- Folder: `02_Prompt/05_prototype/`
- Penpot page: `05 Prototype / Flow`
- Rules: click flow and interaction only

### Final code task
Use:
- Folder: `04_Final_Code/`
- Rules: HTML, SCSS source, JS source, compiled CSS, minified CSS, assets

---

## Permission rule
A user command counts as permission only for the exact page, frame, and task described in the command.

Do not edit other pages or frames.

If the target page or target frame is unclear, inspect first and ask for confirmation.

---

## Before any Penpot edit
Before editing, confirm:

1. Penpot MCP is available
2. Target Penpot project/file
3. Target Penpot page
4. Target frame name
5. Source input files to use
6. Prompt files to use
7. Whether the task is wireframe, final design, mobile, prototype, or code
8. Whether any page/frame will be created, renamed, deleted, duplicated, resized, or restructured

If the target is clear from the user's command, proceed only within that target.

---

## Penpot MCP action log rule
Every Penpot MCP action must be recorded in `05_Log_Tracking/mcp-log.md`.

Each log entry must include:

- Date
- Stage
- Target Penpot page
- Target frame
- MCP action
- Files read
- Result
- Error, if any
- Next step

---

## Error tracking rule
All errors must be tracked.

Record an error when:

- Penpot MCP is unavailable
- Wrong Penpot page is targeted
- Wrong frame is targeted
- Layout is broken
- Content is missing
- Text is not editable
- Elements are merged incorrectly
- Image placeholders are missing
- Wireframe becomes too polished
- Final design uses wrong style
- Spacing becomes inconsistent
- Component is detached or changed without approval
- Codex command fails
- SCSS compile fails
- JS has runtime errors
- Output is not generated correctly

Write all errors into:

`05_Log_Tracking/error-log.md`

When fixed, also update:

`05_Log_Tracking/fixed-issue-log.md`

---

## Design change log rule
Every requested design change must be recorded in:

`05_Log_Tracking/design-change-log.md`

Each entry must include:

- Date
- Requested by
- Stage
- Target Penpot page
- Target frame
- Change requested
- Change applied
- Status

---

## Codex log rule
Every Codex command or goal command must be recorded in:

`05_Log_Tracking/codex-log.md`

Each entry must include:

- Date
- Stage
- Command used
- Files read
- Files changed
- Result
- Error, if any
- Next step

---

## Wireframe rules
For wireframe tasks:

- Read `02_Prompt/01_wireframe/design.md`
- Read `02_Prompt/01_wireframe/wireframe-prd.md`
- Use Penpot page `01 Wireframe`
- Use black and white only
- Use pure white background
- Use editable text layers
- Use separate editable objects
- Convert all images into placeholder boxes
- Do not use final colors, gradients, shadows, photos, polished cards, or high-fidelity styling
- Do not create final design

---

## Final design rules
For final design tasks:

- Read `02_Prompt/03_final-design/design.md`
- Read `02_Prompt/03_final-design/final-design-prd.md`
- Use Penpot page `03 Final Design`
- Base the design on approved wireframe only
- Use reusable components from `02 Components / Design System` where available
- Use approved typography, spacing, layout, and style rules
- Do not change the wireframe page unless explicitly instructed
- Do not create mobile design unless explicitly instructed
- Do not create prototype flow unless explicitly instructed

---

## Image-to-Penpot recreation rule
When using an image as a reference:

- Extract visible structure, text, sections, and layout
- Keep text editable
- Keep elements separately editable
- Do not merge unrelated text into one layer
- Do not merge unrelated objects into one object
- If creating wireframe, convert images into placeholder boxes only
- If creating final design, use real images only if provided and approved
- If text is unclear, mark it as uncertain instead of guessing

---

## Separation rule
If an item looks separate, create it separately.

Separate:
- headings
- subheadings
- body text
- captions
- buttons
- cards
- dividers
- image placeholders
- icons
- badges
- tables
- list items
- section containers

Grouping is allowed only for organization. Grouping must not remove independent editability.

---

## No guessing rule
Do not guess:

- Target Penpot page
- Target frame
- Missing text
- Missing product specifications
- Missing content
- Missing image meaning
- Brand colors
- Component behavior
- Prototype flow

If unclear, inspect first. If still unclear, ask for confirmation.

---

## Completion check
Before marking a task as complete, check:

- Correct Penpot page was edited
- Correct frame was edited
- No other page was changed
- All visible text is represented
- All required sections are included
- Text remains editable
- Elements remain editable
- Spacing is consistent
- Content width is controlled
- Error logs are updated
- MCP log is updated
- Status file is updated

---

## Response after action
After each completed action, report:

1. Edited Penpot page
2. Edited frame
3. Files read
4. Files changed
5. Exact change made
6. Errors found
7. Logs updated
8. Next recommended step
