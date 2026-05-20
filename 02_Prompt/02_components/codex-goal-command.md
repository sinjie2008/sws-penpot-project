# Codex Goal Command — Components

## Goal

Follow `00_Rules/AGENTS.md`.

Work on the component planning and component creation workflow for the Penpot file.

## Workflow

You must follow this order:

1. Scan `01 Wireframe` first.
2. Prepare a component planning report.
3. Stop and wait for user approval.
4. Ask user to confirm the color palette.
5. Only after approval and color confirmation, create approved components inside `02 Components`.

## Target Pages

Scan source page:

```text
01 Wireframe
```

Create components only inside:

```text
02 Components
```

## Strict Rules

1. Do not modify `01 Wireframe`.
2. Do not move, delete, resize, rename, or change any existing wireframe element.
3. Do not touch `03 Final Design`.
4. Do not create components before approval.
5. Do not continue if color palette is not confirmed.
6. Treat every Penpot Board as a section.
7. Do not use groups as sections.
8. Create only approved components.
9. Do not create extra components.
10. Use clear component and layer names.

## Step 1 — Scan Only

Scan `01 Wireframe` and list:

- Font family
- Font size
- Font weight
- Line height if available
- Spacing
- Repeated UI patterns
- Suggested components to create

Do not create anything.

## Step 2 — Component Planning Report

Prepare this table:

| No. | Component Name | Found In Board | Elements Included | Variants | Priority | Notes |
|---|---|---|---|---|---|---|

Priority must be:

```text
Must Create
Optional
Not Needed
```

## Step 3 — Stop for Approval

After the report, ask:

```text
Please confirm which components you approve to create inside 02 Components.
```

Then stop.

## Step 4 — Color Confirmation Gate

Before creating any component, ask the user to confirm the color palette.

Do not continue until the user confirms the color.

Ask user to confirm:

| Color Role | Color Code |
|---|---|
| Primary Color |  |
| Secondary Color |  |
| Accent Color |  |
| Background Color |  |
| Text Color |  |
| Border / Divider Color |  |
| Highlight Color |  |

## Step 5 — Create Approved Components

After approval and color confirmation, create approved components only inside `02 Components`.

Organize them properly by category.

## Final Report

After creation, provide this table:

| Component Created | Variants | Status | Notes |
|---|---|---|---|

Status must be:

```text
Created
Skipped
Need User Review
```
