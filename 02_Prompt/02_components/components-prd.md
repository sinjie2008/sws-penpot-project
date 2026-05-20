# Components PRD — Superworld Electronics

## Purpose

Create a reusable component system for the Superworld Electronics website design.

The component system must be created only after scanning the existing `01 Wireframe` page and after user approval.

## Required Workflow

Codex must follow this process:

```text
Scan 01 Wireframe
↓
List font, spacing, repeated UI patterns
↓
Recommend components
↓
Ask user approval
↓
Ask color confirmation
↓
Create approved components in 02 Components
```

## Components to Check

Codex should scan the wireframe and check whether these components are needed:

```text
Header / Navigation
Footer
Button
Breadcrumb
Sub Navigation
Hero Section
Section Title Block
Product Card
Application Card
News Card
CTA Block
Image + Text Section
Icon + Text Block
Stats Block
Table Style
Form Field
Dropdown
Textarea
Checkbox
Certificate Card
Download Card
Timeline Item
Country / Region Item
Slider Card
Tabs
Accordion
Filter Bar
Pagination
```

## Must Create Components

If found in the wireframe, these components should be considered high priority:

```text
Header / Navigation
Footer
Button
Breadcrumb
Sub Navigation
Hero Section
Section Title Block
Product Card
Application Card
News Card
CTA Block
Image + Text Section
Table Style
Form Field
```

## Optional Components

Only create these if they are clearly used in the wireframe:

```text
Slider Card
Tabs
Accordion
Filter Bar
Pagination
Certificate Card
Download Card
Timeline Item
Country / Region Item
Stats Block
Icon + Text Block
```

## 02 Components Page Structure

Inside `02 Components`, organize components like this:

```text
02 Components

├── 01 Foundations
│   ├── Colors
│   ├── Typography
│   ├── Spacing
│   ├── Grid
│   ├── Border
│   └── Shadow
│
├── 02 Buttons
│   ├── Primary Button
│   ├── Secondary Button
│   ├── Outline Button
│   └── Disabled Button
│
├── 03 Navigation
│   ├── Header
│   ├── Breadcrumb
│   └── Sub Navigation
│
├── 04 Cards
│   ├── Product Card
│   ├── Application Card
│   ├── News Card
│   ├── Certificate Card
│   └── Download Card
│
├── 05 Content Sections
│   ├── Hero Section
│   ├── Section Title Block
│   ├── Image + Text Section
│   ├── Icon + Text Block
│   ├── CTA Block
│   └── Stats Block
│
├── 06 Tables & Forms
│   ├── Table Style
│   ├── Form Input
│   ├── Dropdown
│   ├── Textarea
│   └── Checkbox
│
└── 07 Footer
    └── Footer Component
```

## Approval Rule

Codex must not create components until user approves the component list.

Before creation, Codex must ask:

```text
Please confirm which components you approve to create inside 02 Components.
```

## Color Gate Rule

Codex must ask user to confirm color before creating styled components.

If color is not confirmed, Codex must stop.

## Final Check

After creation, Codex must check:

| Check Item | Status | Notes |
|---|---|---|
| Approved components created |  |  |
| No unapproved components created |  |  |
| `01 Wireframe` untouched |  |  |
| Colors follow approved palette |  |  |
| Heading uses Poppins |  |  |
| Body uses Inter |  |  |
| Component names are clear |  |  |
| Components organized properly |  |  |

Status should be:

```text
Pass
Need Fix
Not Applicable
```
