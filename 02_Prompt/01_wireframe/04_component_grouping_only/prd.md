# 04 Component-Grouping-Only / prd.md

## Product requirement

Group related existing elements inside already-created section boards.

The section boards already exist.
Do not create new section boards.
Do not separate the layout again.
Do not work on the full Penpot file.

---

## Objective

Organize existing layers by grouping related elements together inside the target section board only.

Do not only rename layers.
You must create groups for related components.

---

## Required user input

Before working, Codex must ask for or confirm:

```text
Target board name or target section board name:
Target Penpot page:
```

If target is missing, stop and ask:

```text
Please provide the target board name or section board name before I continue.
```

---

## Required grouping examples

Button:

```text
Button background
Button text
Button icon if available
```

Card:

```text
Card background
Card image
Card icon
Card title
Card description
Card button if available
```

Navigation:

```text
All related navigation menu items
```

Breadcrumb:

```text
Breadcrumb links
Breadcrumb separators
Current page text
```

Sub Navigation:

```text
Sub navigation items
Active tab indicator
Divider line if related
```

News Card:

```text
News card image
Date
Title
Description
Button if available
```

Footer Column:

```text
Footer column title
Related footer links
Related icons if available
```

---

## Do not group

Do not:

1. group unrelated elements together
2. group elements from different section boards together
3. group background elements with unrelated content
4. group all layers into one big group
5. use groups as new sections
6. create new boards

---

## Success criteria

The task is successful when:

1. only the target section board was modified
2. no new boards were created
3. related elements were grouped properly
4. groups use clear names ending with `_Group`
5. unclear child layers were renamed clearly
6. no element visually moved
7. no element resized
8. no content or style changed
9. non-target boards were untouched
10. final canvas appearance is preserved
11. logs were updated
