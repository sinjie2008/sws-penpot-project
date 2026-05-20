# Safety and Naming Rules

## Safety Rules

Codex must not delete existing elements.
Codex must not modify unrelated boards.
Codex must not modify unrelated pages.
Codex must not create unapproved components.
Codex must not create duplicate components.
Codex must not rename unrelated layers or boards.

Before creating any component, Codex must check whether a similar component already exists inside the 02_components page or 02 Components board.

If a similar item exists, Codex must recommend one of these actions:

- reuse existing component
- create variant
- skip creation
- create new component only if clearly different

## Naming Rules

Use simple and clear names.

Folder names:
- lowercase + underscore

File names:
- lowercase + hyphen

Penpot component naming format:

[Category] / [Component Name] / [Variant]

Examples:

- Token / Color / Primary
- Token / Typography / H1 Desktop
- Token / Spacing / Section Padding Desktop
- Base / Button / Primary
- Base / Button / Secondary
- Layout / Header / Desktop
- Section / Hero / Desktop

## Result File Rule

All results must be written inside:

02_components/02_result/

Do not create extra result folders unless the user approves.
