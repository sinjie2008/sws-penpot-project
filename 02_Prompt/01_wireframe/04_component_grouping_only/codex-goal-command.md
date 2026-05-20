# 04 Component-Grouping-Only / codex-goal-command.md

## Goal command

Use this command when asking Codex or the agent to group related existing elements inside already-created section boards.

This is a grouping-only task.
It must not create new section boards.
It must not separate the layout again.
It must not work on the full Penpot file.

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
02_Prompt/01_wireframe/04_component_grouping_only/prd.md
```

Use Penpot MCP only.

---

## Required user input

Before doing anything, confirm:

```text
Target board name or target section board name:
Target Penpot page:
```

If the user does not provide a target board name or section board name, stop immediately and ask:

```text
Please provide the target board name or section board name before I continue.
```

Do not touch non-target boards.
Do not group elements across different section boards.

---

## Task

Group related existing elements inside the provided target board or target section board.

Do not only rename layers.
You must create groups for related components.

---

## MCP timeout-safe workflow

Step 1: Confirm the target board or section board.
Step 2: Scan only the target section board.
Step 3: List possible related component groups.
Step 4: Stop and ask user which group or section to process first if there are many layers.
Step 5: Group only the approved related elements.
Step 6: Verify only the processed group or section.
Step 7: Stop and ask whether to continue.

---

## Strict rules

1. Do not delete any element.
2. Do not add any new UI element.
3. Do not duplicate any element.
4. Do not move any element visually.
5. Do not resize any element.
6. Do not change color.
7. Do not change font.
8. Do not change font size.
9. Do not change spacing.
10. Do not change alignment.
11. Do not change text content.
12. Do not replace images.
13. Do not redesign anything.
14. Do not create new boards.
15. Do not touch non-target boards.
16. Do not group elements across different section boards.

The canvas must look exactly the same after grouping.

---

## Required grouping

```text
Button background and button text must be grouped.
Each card must be grouped.
Navigation items must be grouped.
Breadcrumb items must be grouped if breadcrumb exists.
Sub navigation items must be grouped if sub navigation exists.
Icon and label pairs must be grouped.
News cards must be grouped.
Footer columns must be grouped.
Related image and text blocks must be grouped.
```

---

## Final response

After completing the approved group or section, provide:

```text
Component grouping completed.

Target board / section board:
- [target board name]

Groups created in this run:
- [list groups created]

Validation:
- No elements deleted.
- No new elements added.
- No new boards created.
- No elements visually moved.
- No design style changed.
- No text content changed.
- Final canvas appearance preserved.

Next step:
- Please confirm the next group or section to continue.
```
