# 02 Board-to-Section-Boards / codex-goal-command.md

## Goal command

Use this command when asking Codex or the agent to split one existing Penpot board into Penpot section boards only.

This is an organization task.
It is not an image-to-wireframe task.
It is not a component grouping task.

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
02_Prompt/01_wireframe/02_board_to_section_boards/prd.md
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

Do not continue without a target board.
Do not guess the target board.
Do not apply changes to the whole file.

---

## Task

Organize only the target board provided by the user.

Separate the existing visible layout into Penpot section boards.

Section = Penpot Board.

Do not use groups as main sections.
Do not group components in this run unless the user explicitly asks and the section is small.

---

## MCP timeout-safe workflow

Step 1: Confirm the target board.
Step 2: Scan only the target board.
Step 3: Identify main visible sections.
Step 4: Report the detected sections and suggested section board names.
Step 5: Stop and ask the user which section or batch to process first.
Step 6: Create/move only the approved section board in that run.
Step 7: Verify only that section board.
Step 8: Stop and ask whether to continue.

Do not process the full board in one run if the board is large.

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
15. Do not touch boards outside the target board.
16. Do not run organization on the full file.

The canvas must look exactly the same after the work is completed.

---

## Final response required

After completing the approved section or batch, provide:

```text
Board-to-section-boards task completed.

Target board:
- [target board name or ID]

Section boards created or updated in this run:
- [list actual section boards]

Detected sections:
- [list all detected sections]

Actions completed:
- Only the target board was processed.
- Existing design was separated into section board(s).
- Existing elements were placed into the correct section board(s).
- Layer names were cleaned where needed.
- Groups were not used as main sections.

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
