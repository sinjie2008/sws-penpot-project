# 01 Image-to-Editable-Wireframe / prd.md

## Product requirement

Create or update one low-fidelity editable Penpot wireframe from the provided source image.

---

## Objective

The wireframe should help the user review:

1. page structure
2. content order
3. section hierarchy
4. layout balance
5. navigation flow
6. CTA position
7. image/content placement

This is not final design.

---

## Required user input

Before working, Codex must ask for or confirm:

```text
Source image path:
Target Penpot page:
Target frame name:
Desktop frame width:
```

Default target page:

```text
01 Wireframe
```

Default desktop frame width:

```text
1440 px
```

Recommended target frame name pattern:

```text
[Page Name] / Wireframe / Desktop
```

Example:

```text
Home / News / Wireframe / Desktop
```

If the user does not provide source image path or target frame name, stop and ask.

---

## Content accuracy requirement

Before creating the Penpot frame, Codex must create a complete text checklist from the source image.

Every readable text item must appear exactly the same number of times in the Penpot frame.

Preserve exact:

```text
wording
spelling
capitalization
punctuation
symbols
labels
navigation names
news titles
categories
dates
button text
```

Do not paraphrase, simplify, correct grammar, or rewrite any text.
Do not invent missing content.

If text is unclear or unreadable, mark it as:

```text
UNCERTAIN: [approximate section]
```

After creating the frame, verify every Penpot text layer against the checklist.
Completion is not valid unless all readable source content is matched exactly or marked uncertain.

---

## Wireframe sections

Use the sections required by the actual source image.

If no section list is provided, use a safe website structure only when visible in the source:

```text
Header
Hero
Intro / Overview
Main Content Section
Supporting Content Section
CTA Section
Footer
```

Do not add unnecessary sections.
Do not invent missing sections.

---

## Success criteria

The image-to-wireframe task is successful when:

1. the source image has been reviewed
2. a text checklist has been created
3. the target frame has been created or updated
4. all important visible text is included
5. all image/photo areas are placeholders
6. all text is editable
7. all objects are separately editable
8. no final color styling is used
9. no final design styling is used
10. spacing is consistent
11. correct Penpot page is updated
12. unrelated pages and boards are untouched
13. log files are updated
