# 02 Review Suggestion Prompt

Read:

02_components/00_shared_rules/
02_components/02_result/scan-result.md

Before starting the review, ask the user to provide or confirm the color palette.

Ask only this:

Please confirm the color palette for the 02 Components board.

Primary color:
Secondary color:
Accent color:
Background color:
Text color:
Usage rule:

Do not assume the color palette.
Do not hardcode any color.
Do not scan final color from the wireframe.
Do not create color tokens until the user confirms.

After the user confirms the color, update:

02_components/02_result/color-confirmation.md

Then review the collected scan result.

## Review required

Review:

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

For each item, provide:

- scanned value
- status
- suggested value
- reason
- user approval status

Use these recommended Penpot frame widths unless the user provides different values:

- Desktop frame width: 1440px
- Tablet frame width: 834px
- Mobile frame width: 390px

Recommended breakpoint ranges:

- Desktop: 1200px and above
- Tablet: 768px to 1199px
- Mobile: 320px to 767px

For typography handoff, provide px first and rem equivalent if useful.
Do not use em for main font sizing.

## Proposed 02 Components board plan

Prepare the proposed Penpot 02 Components board plan.

The board plan should include only what is detected from the scan result and what is needed for the approved design token system.

Required board structure:

01 Design Tokens
- Color Tokens
- Typography Tokens
- Spacing Tokens
- Padding Tokens
- Margin Tokens
- Section Height Tokens
- Breakpoint Tokens

02 Base Components
- only detected base components

03 Layout Components
- only detected layout components

04 Section Components
- only detected section components

05 Notes
- created log
- skipped items
- duplicate notes

Update:

02_components/02_result/design-token-review.md
02_components/02_result/components-board-plan.md

Do not create components yet.
Do not edit Penpot yet.
Stop and wait for user approval.
