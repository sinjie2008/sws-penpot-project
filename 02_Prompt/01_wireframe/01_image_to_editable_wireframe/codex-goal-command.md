# 01 Image-to-Editable-Wireframe / codex-goal-command.md

## Goal command

Use this command when asking Codex or the agent to convert a source wireframe image into one editable Penpot wireframe through Penpot MCP.

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
02_Prompt/01_wireframe/01_image_to_editable_wireframe/design.md
02_Prompt/01_wireframe/01_image_to_editable_wireframe/prd.md
```

Use input files from:

```text
01_Input/raw-wireframe/
01_Input/reference-image/
01_Input/content-notes/
01_Input/product-info/
```

Use Penpot MCP only.

---

## Required user input

Before doing anything, confirm:

```text
Source image path:
Target Penpot page:
Target frame name:
Desktop frame width:
```

Default target Penpot page:

```text
01 Wireframe
```

Default desktop frame width:

```text
1440 px
```

If the source image path or target frame name is missing, stop and ask:

```text
Please provide the source image path and target frame name before I continue.
```

Do not guess.
Do not scan the full file.
Do not update all wireframes.

---

## Task

Create or update only one approved desktop wireframe frame based on the provided source image and instruction files.

This is an image-to-editable-wireframe task.

---

## MCP timeout-safe workflow

Step 1: Confirm Penpot MCP is available.
Step 2: Confirm the active Penpot project/file.
Step 3: Confirm the active Penpot page is `01 Wireframe` unless the user approved another page.
Step 4: Read only the provided source image.
Step 5: Create a complete readable text checklist from the source image.
Step 6: Detect the visible sections from the source image.
Step 7: Stop and report the detected sections before building if the page is large.
Step 8: Ask which section to create first.
Step 9: Create or update one section per run.
Step 10: Verify only the completed section.
Step 11: Stop and ask whether to continue to the next section.

Do not build a large full page in one MCP run if timeout risk is detected.

---

## Penpot restrictions

Work only on:

```text
01 Wireframe
```

Do not update:

```text
02 Components / Design System
03 Final Design
04 Mobile Design
05 Prototype / Flow
Any unrelated approved frame
Any unrelated board
```

---

## Wireframe rules

Use low-fidelity wireframe only.
Use black, white, and simple grayscale only.
Use pure white background.
Use editable text layers.
Use separately editable objects.
Convert all images/photo/news thumbnail areas into placeholder boxes.
Use desktop frame width `1440 px` unless the user provides another approved size.
Use content width `1200 px` to `1280 px`.
Use consistent 8-point spacing.

Do not use final colors, gradients, shadows, photos, or polished design styling.
Do not invent missing content.

---

## Completion report

After completion, report:

```text
Image-to-editable-wireframe completed.

Penpot page updated:
- [page name]

Frame updated or created:
- [frame name]

Input file used:
- [source image path]

Prompt files used:
- [list files]

Sections detected:
- [list sections]

Section completed in this run:
- [section name]

Content checklist verification result:
- [pass / uncertain / issue]

Unclear or UNCERTAIN text:
- [list if any]

Issues found:
- [list if any]

Log files updated:
- [list]

Existing approved frames untouched:
- Yes / No

Next step:
- [ask user which section to continue]
```
