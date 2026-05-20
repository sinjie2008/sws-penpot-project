# 01 Wireframe / When To Use Each Prompt

Use this file as a menu before running Codex.

Do not paste this file as the main command.
This file only helps you choose which `codex-goal-command.md` to run.

---

## Recommended workflow

### Step 1 — Create editable wireframe from image

Use:

```text
02_Prompt/01_wireframe/01_image_to_editable_wireframe/codex-goal-command.md
```

Use this when you have a source image such as PNG/JPG and want Codex + Penpot MCP to rebuild it as an editable low-fidelity wireframe.

Example input:

```text
Source image: 01_Input/raw-wireframe/Wireframe/HOME _ NEWS.png
Target Penpot page: 01 Wireframe
Target frame: Home / News / Wireframe / Desktop
```

This prompt is image-related.
It creates or updates one editable wireframe frame from a source image.

---

### Step 2 — Split one Penpot board into section boards only

Use:

```text
02_Prompt/01_wireframe/02_board_to_section_boards/codex-goal-command.md
```

Use this after the wireframe already exists in Penpot and you want to separate one target board into Penpot section boards.

This prompt only creates section boards from existing content.
It does not group detailed components.
It is safer for large boards and timeout issues.

Example:

```text
Target board: Homepage / Wireframe / Desktop
```

---

### Step 3 — Split one board into section boards and component groups

Use:

```text
02_Prompt/01_wireframe/03_board_to_sections_and_components/codex-goal-command.md
```

Use this only for small boards.

This prompt does two tasks:

1. split the target board into section boards
2. group related elements inside each section board

For large boards, do not use this prompt because it may cause MCP timeout.
Use Step 2 first, then Step 4 section by section.

---

### Step 4 — Group components inside existing section boards only

Use:

```text
02_Prompt/01_wireframe/04_component_grouping_only/codex-goal-command.md
```

Use this when section boards already exist and you only want Codex to group related elements inside them.

Example:

```text
Target section board: 01_Header_Board
```

This prompt should be run one section board at a time for best stability.

---

## Simple rule

```text
Image file to Penpot wireframe = use 01
Existing board to section boards only = use 02
Small board to sections + groups = use 03
Existing section boards to groups only = use 04
```

---

## MCP timeout advice

For large boards, use this safest order:

```text
01 Image-to-Editable-Wireframe
02 Board-to-Section-Boards
04 Component-Grouping-Only
```

Avoid using prompt 03 for large boards.
