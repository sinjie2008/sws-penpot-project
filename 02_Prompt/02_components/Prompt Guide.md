Step 1
02_components/01_prompt/01_collect_scan_prompt.md

Page: 01_wireframe
Target board: Homepage - Hero Section
Output page: 02_components
Output board: 02 Components


----------------------------------------------------------------


Step 2
02_components/01_prompt/02_review_suggestion_prompt.md

Read:
02_components/00_shared_rules/
02_components/02_result/scan-result.md

Review the scan result and prepare the 02 Components plan.

Use these color inputs for review:

Primary color: #3ec272
Secondary color: #4077be
Accent color: #203362
Background color: #ffffff
Text color: #000000

Usage rule:
60% white
30% green
10% blue

Task:
1. Review detected typography.
2. Review detected spacing.
3. Review detected padding.
4. Review detected margin.
5. Review detected section height.
6. Review detected reusable components.
7. Suggest the final 02 Components board plan.
8. Suggest the approved component list.

Important:
Do not create components yet.
Do not edit the 02 Components board yet.
Do not delete or modify scan-result.md.
Do not treat this as creation approval.

Create or update these result files only:

02_components/02_result/design-token-review.md
02_components/02_result/color-confirmation.md
02_components/02_result/components-board-plan.md
02_components/02_result/approved-component-list.md

After completing the review, stop and wait for user approval.


----------------------------------------------------------------

Step 3
02_components/01_prompt/03_approval_create_components_prompt.md

The review and suggestions are approved.

Read:

02_components/00_shared_rules/
02_components/02_result/scan-result.md
02_components/02_result/design-token-review.md
02_components/02_result/color-confirmation.md
02_components/02_result/components-board-plan.md
02_components/02_result/approved-component-list.md

Before creating anything, confirm that:

- color is approved
- design token review is approved
- component board plan is approved
- component list is approved
- target output page is 02 Components
- target output board is 02 Components

Create only approved items.

Create inside Penpot:

Page: 02 Components
Board: 02 Components

Do not create unapproved components.
Do not create duplicate components.
Do not modify unrelated boards.
Do not scan the full Penpot file.
Do not use isolated browser.
Use existing browser session only.

Creation order:

1. Design Tokens
2. Base Components
3. Layout Components
4. Section Components
5. Notes / Logs

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
- only approved base components

03 Layout Components
- only approved layout components

04 Section Components
- only approved section components

05 Notes
- created log
- skipped items
- duplicate notes

Important:
Create components by batch.
Start with Design Tokens and Base Components only.
After finishing Base Components, stop and ask before continuing to Layout Components.

If timeout happens:
- stop immediately
- reload existing browser tab only
- do not open isolated browser
- do not open a new browser session
- confirm same Penpot file, page, and board before continuing

After creation, update:

02_components/02_result/creation-log.md

The log must include:
- created items
- skipped items
- duplicate items
- timeout issue if any
- final status

----------------------------------------------------------------