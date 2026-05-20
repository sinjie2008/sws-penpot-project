# 02 Board-to-Section-Boards / prd.md

## Product requirement

Organize one existing Penpot target board into section boards only.

This prompt does not create a wireframe from image.
This prompt does not group detailed components.
This prompt does not redesign.

---

## Objective

The objective is to convert one large existing board into smaller Penpot boards that represent the visible sections.

Section = Penpot Board.

Use boards as the main section containers.
Do not use groups as main sections.

---

## Required user input

Before working, Codex must ask for or confirm:

```text
Target board name or target board ID:
Target Penpot page:
```

If the target board is missing, stop and ask:

```text
Please provide the target board name or board ID before I continue.
```

---

## Allowed actions

Codex is only allowed to:

1. read and understand the target board layout
2. identify the main visible sections inside the target board only
3. create one Penpot board for each existing visible section
4. place existing elements into the correct section board
5. keep all elements visually in the same position
6. rename each section board clearly
7. rename unclear layers clearly
8. arrange section boards from top to bottom
9. leave all non-target boards untouched

---

## Not allowed

Codex must not:

1. delete elements
2. add new UI elements
3. duplicate elements
4. redesign anything
5. change text content
6. change images
7. change icons
8. change colors
9. change fonts
10. change font sizes
11. change spacing
12. change alignment
13. visually move elements
14. resize elements
15. group detailed components as a main task
16. touch non-target boards
17. run on the full file

---

## Section detection examples

Create section boards only for visible sections that actually exist:

```text
Header
Breadcrumb
Sub_Navigation
Hero_Banner
Introduction
Overview
Content_Section
Product_Categories
Industries_We_Serve
Quality
Latest_News
Regional_Support
CTA
Footer
```

Do not invent missing sections.
Do not create empty boards.

---

## Success criteria

The task is successful when:

1. only the target board was processed
2. visible sections were separated into Penpot boards
3. board order follows top-to-bottom layout
4. no group was used as main section
5. all original elements still exist
6. no element visually moved
7. no element was resized
8. no content or style changed
9. non-target boards were untouched
10. log files were updated
