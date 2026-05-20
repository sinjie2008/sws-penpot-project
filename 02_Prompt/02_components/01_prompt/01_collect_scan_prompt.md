# 01 Collect Scan Prompt

Read the rules inside:

02_components/00_shared_rules/

Before scanning, ask the user only this:

Which Penpot page and target board should I scan?

Required user answer format:

Page:
Target board:
Output page:
Output board:

After the user provides the target, scan only that target board.

Do not scan the full Penpot file.
Do not scan all boards.
Do not create components.
Do not review the design values yet.
Do not suggest changes yet.
Do not ask for color yet.
Do not edit, move, rename, delete, or add any Penpot element.

Collect scan data only.

## Data to collect

### Typography
- font family
- font size
- font weight
- line height
- heading style
- body style
- button text style
- caption or label style if detected

### Layout Measurement
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

### Component Detection
- detected reusable components
- repeated UI patterns
- possible base components
- possible layout components
- possible section components
- possible component variants

### Responsive Clues
- desktop layout pattern
- tablet layout clue if visible
- mobile layout clue if visible
- possible responsive issue

## Record keeping

Update only:

02_components/02_result/scan-result.md

Do not overwrite previous scan records.

If scanning a new target board, append the result as a new section:

## Board: [Target Board Name]

If the same board already exists in scan-result.md, update only that board section.

Do not remove other board scan records.
Do not delete previous scan history.

The scan result must be raw collection only.

Do not include design review.
Do not include suggested changes.
Do not include approved values.
Do not include color palette.
Do not create components.

After updating scan-result.md, stop and wait for the next prompt.
