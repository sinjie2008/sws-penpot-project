# 03 Board-to-Sections-and-Components / codex-goal-command.md

## Goal command

Use this command when asking Codex or the agent to split one small existing Penpot board into section boards and group related elements inside those section boards.

This prompt is heavier.
For large boards, do not use this prompt.
Use `02_board_to_section_boards` first, then `04_component_grouping_only`.

---

## Command

Read and follow these files:

```text
00_Rules/AGENTS.md
00_Rules/design-rules.md
03_Penpot_Status/status.md
02_Prompt/01_wireframe/00_shared_rules/mcp-safety-rules.md
02_Prompt/01_wireframe/00_shared_rules/mcp-timeout-rules.md
02_Prompt/01_wireframe/00_shared_rules/naming-rules.md
02_Prompt/01_wireframe/00_shared_rules/logging-rules.md
02_Prompt/01_wireframe/03_board_to_sections_and_components/prd.md
```

Use Penpot MCP only.

---

## Required user input

Before doing anything, confirm:

```text
Target board name or target board ID:
Target Penpot page:
```

If the user does not provide a target board name or board ID, stop immediately and ask:

```text
Please provide the target board name or board ID before I continue.
```

Do not scan, organize, rename, or modify the full Penpot file.
Do not touch any non-target board.

---

## Task

Organize only the target board provided by the user.

You must:

1. separate the target board into section boards
2. group related elements inside each section board
3. rename boards, groups, and unclear layers clearly
4. preserve the final canvas appearance exactly

---

## MCP timeout-safe workflow

Step 1: Confirm the target board.
Step 2: Scan only the target board.
Step 3: List detected sections and likely component groups.
Step 4: Estimate if the board is small enough for this combined operation.
Step 5: If the board is large, stop and recommend using prompt 02 then prompt 04.
Step 6: If the board is small, ask user approval to continue.
Step 7: Process only approved section or small batch.
Step 8: Verify only the processed batch.
Step 9: Stop and ask whether to continue.

---

## Strict rules

1. Do not delete any existing element.
2. Do not add any new UI element.
3. Do not duplicate any element.
4. Do not redesign anything.
5. Do not change text content.
6. Do not change images.
7. Do not change icons.
8. Do not change colors.
9. Do not change fonts.
10. Do not change font sizes.
11. Do not change spacing.
12. Do not change alignment.
13. Do not visually move any element.
14. Do not resize any element.
15. Do not change button style.
16. Do not change card style.
17. Do not add labels on the canvas.
18. Do not add placeholder boxes.
19. Do not add decoration elements.
20. Do not create extra content.
21. Do not touch boards outside the target board.
22. Do not run organization on the full file.

The canvas must look exactly the same after the work is completed.

---

## Required grouping examples

```text
Navigation items must be grouped.
Breadcrumb items must be grouped.
Sub navigation items must be grouped.
Button background and button text must be grouped.
Each card must be grouped.
Each icon and label must be grouped.
Each news card must be grouped.
Each footer column must be grouped.
Related image and text blocks must be grouped.
```

If the MCP does not support grouping safely, stop and report:

```text
I cannot safely group the related components without changing the visual layout.
```

Do not pretend grouping was completed.

---

## Final response required

After completing the approved section or batch, provide:

```text
Board-to-sections-and-components task completed.

Target board:
- [target board name or ID]

Section boards created or updated in this run:
- [list actual section boards]

Component groups created in this run:
- [list actual groups]

Actions completed:
- Only the target board was processed.
- Existing design was separated into section board(s).
- Related elements inside the section board(s) were grouped.
- Boards, groups, and layers were renamed clearly.

Validation:
- No non-target boards were touched.
- No elements deleted.
- No new UI elements added.
- No elements duplicated.
- No elements visually moved.
- No design style changed.
- No text content changed.
- Final canvas appearance preserved.

Next step:
- Please confirm the next section to continue.
```
