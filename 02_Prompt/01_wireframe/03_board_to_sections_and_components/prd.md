# 03 Board-to-Sections-and-Components / prd.md

## Product requirement

Organize one existing Penpot target board into:

1. section boards
2. component groups inside each section board

This prompt is heavier than prompt 02.
Use it only for small boards.
For large boards, use prompt 02 first, then prompt 04 section by section.

---

## Objective

The objective is to separate one existing board into section boards and group related elements inside each section board.

Section = Penpot Board.
Component = Group inside section board.

Use boards for main page sections.
Use groups only inside section boards to group related elements.
Do not use groups as main sections.

---

## Required user input

Before working, Codex must ask for or confirm:

```text
Target board name or target board ID:
Target Penpot page:
```

If target board is missing, stop and ask:

```text
Please provide the target board name or board ID before I continue.
```

---

## Required grouping

Codex must group related elements inside section boards.

Examples:

```text
Button background + button text = Button_Group
Card background + card image + card title + card description = Card_Group
Icon + label text = Icon_Label_Group
Navigation items = Navigation_Group
Breadcrumb links + separators = Breadcrumb_Group
Sub navigation tabs/items = Sub_Navigation_Group
News card image + date + title + description = News_Card_Group
Footer title + footer links = Footer_Column_Group
```

This task is not complete if Codex only renames layers.

---

## Success criteria

The task is successful when:

1. only the target board was processed
2. main sections were separated using boards
3. related components inside each section board were grouped
4. boards, groups, and layers were renamed clearly
5. no element visually moved
6. no element was resized
7. no content or design style changed
8. non-target boards were untouched
9. final canvas looks the same
10. logs were updated
