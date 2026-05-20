# Component Workflow Rules

## Main Workflow

Use this workflow only:

1. Collect scan data
2. Review and suggest improvements
3. User approval
4. Create approved components

Codex must not skip any step.

## Scan First Rule

Codex must scan only the user-provided Penpot page and target board.

Codex must not scan the full Penpot file.
Codex must not scan all boards.
Codex must not process a full page in one run.
Codex must not create components during the scan step.
Codex must not review or suggest changes during the collect scan step.

## Raw Scan Data Rule

During collect scan, Codex must collect only raw values from the target board:

- font family
- font size
- font weight
- line height
- heading style
- body style
- button text style
- caption or label style if detected
- spacing between elements
- padding
- margin
- section height
- section width
- container width
- card padding
- card gap
- button padding
- image area size
- grid gap if detected
- detected reusable components
- repeated UI patterns
- possible base components
- possible layout components
- possible section components
- possible component variants
- desktop layout pattern
- tablet layout clue if visible
- mobile layout clue if visible
- possible responsive issue

## Record Keeping Rule

When updating:

02_components/02_result/scan-result.md

Do not overwrite previous scan records.

If scanning a new target board, append the result as a new section using this format:

## Board: [Target Board Name]

If the same board already exists in scan-result.md, update only that board section.

Do not remove other board scan records.
Do not delete previous scan history.

## Color Rule

Color must come from user confirmation only.

Codex must not hardcode color values.
Codex must not scan final color tokens from the wireframe.
Codex must not create color tokens until the user confirms the palette.

During review, Codex must ask the user to provide or confirm:

- Primary color
- Secondary color
- Accent color
- Background color
- Text color
- Usage rule

## Breakpoint Rule

Use these recommended Penpot frame widths unless the user provides different values:

- Desktop frame width: 1440px
- Tablet frame width: 834px
- Mobile frame width: 390px

Recommended breakpoint ranges:

- Desktop: 1200px and above
- Tablet: 768px to 1199px
- Mobile: 320px to 767px

Breakpoint widths use px only.
Typography can include px and rem for developer handoff.
Avoid em for main font sizing.

## Review Rule

After raw scan is complete, Codex must review the collected values and suggest improvements.

Review must include:

- scanned value
- status
- suggested value
- reason
- user approval status

Review must cover:

- font family
- font size
- font weight
- line height
- spacing
- padding
- margin
- section height
- container width
- card padding
- button padding
- responsive suitability
- detected reusable components

Codex must not create components during review.

## Approval Rule

Codex must wait for user approval before creating anything.

Approved items must be recorded in:

02_components/02_result/approved-component-list.md

Only approved items can be created.

## Component Creation Rule

Create approved items only inside Penpot:

Page: 02_components
Board: 02 Components

Creation order:

1. Design Tokens
2. Base Components
3. Layout Components
4. Section Components
5. Notes / Logs

## 02 Components Board Structure

The proposed Penpot board structure should be:

01 Design Tokens
- Color Tokens
- Typography Tokens
- Spacing Tokens
- Padding Tokens
- Margin Tokens
- Section Height Tokens
- Breakpoint Tokens

02 Base Components
- only detected and approved base components

03 Layout Components
- only detected and approved layout components

04 Section Components
- only detected and approved section components

05 Notes
- created log
- skipped items
- duplicate notes
