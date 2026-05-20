# Shared MCP Safety Rules

These rules apply to every prompt inside `02_Prompt/01_wireframe/`.

---

## Penpot MCP confirmation

Before editing, Codex must confirm:

1. Penpot MCP is available.
2. The active Penpot project/file is correct.
3. The active Penpot page is correct.
4. The target board, target frame, or target section board is clearly provided by the user.

If any item is unclear, stop and ask the user before editing.

---

## Target-only rule

Codex must work only on the target provided by the user.

Allowed target types:

```text
Target source image
Target Penpot page
Target frame
Target board
Target section board
```

Codex must not guess the target.

If the target is missing, Codex must stop and ask:

```text
Please provide the target board name, target frame name, or source image path before I continue.
```

---

## Do not touch unrelated areas

Do not edit:

```text
02 Components / Design System
03 Final Design
04 Mobile Design
05 Prototype / Flow
Any unrelated board
Any approved frame not named by the user
Any unrelated page
The full Penpot file
All boards
All frames
```

---

## Strict no-change rules

Unless the selected prompt specifically asks to create a low-fidelity wireframe from an image, Codex must not:

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
15. change button style
16. change card style
17. add labels on canvas
18. add decorations
19. create placeholder boxes
20. touch non-target boards

The canvas must look exactly the same after organization tasks.

---

## Emergency stop

Stop immediately if:

1. target is missing
2. Codex is unsure which board/frame/section is target
3. MCP cannot safely complete the action
4. grouping causes visual layout changes
5. board creation causes visual layout changes
6. operation starts affecting non-target boards
7. too many layers cause timeout risk

Do not continue.
Do not guess.
Do not force the change.
