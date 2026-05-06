# 01 Wireframe / codex-goal-command.md

## Goal command
Use this command when asking Codex or the agent to create the wireframe in Penpot through Penpot MCP.

---

## Command

Read and follow these files:

1. `00_Rules/AGENTS.md`
2. `00_Rules/design-rules.md`
3. `03_Penpot_Status/status.md`
4. `02_Prompt/01_wireframe/design.md`
5. `02_Prompt/01_wireframe/wireframe-prd.md`

Use input files from:

- `01_Input/raw-wireframe/`
- `01_Input/reference-image/`
- `01_Input/content-notes/`
- `01_Input/product-info/`

Use Penpot MCP only.

Target Penpot page:

`01 Wireframe`

Task:

Create or update the approved desktop wireframe frame based on the provided raw wireframe > Wireframe image and instruction files.

Rules:

- Confirm Penpot MCP is available before editing.
- Confirm the active Penpot project/file before editing.
- Work only on Penpot page `01 Wireframe`.
- Do not update `02 Components / Design System`.
- Do not update `03 Final Design`.
- Do not update `04 Mobile Design`.
- Do not update `05 Prototype / Flow`.
- Create low-fidelity wireframe only.
- Use black and white only.
- Use pure white background.
- Use editable text layers.
- Use separately editable objects.
- Convert all images into placeholder boxes.
- Preserve structure and hierarchy from the raw wireframe.
- Do not use final colors, gradients, shadows, photos, or polished design styling.
- Do not invent missing content.
- If text is unclear, mark it as uncertain.
- Keep spacing consistent using the 8-point spacing scale.
- Use desktop frame width `1440 px` unless another approved size is provided.
- Use content width `1200 px` to `1280 px`.

Logging requirement:

- Add a new entry to `05_Log_Tracking/mcp-log.md`.
- If any issue happens, add a new entry to `05_Log_Tracking/error-log.md`.
- If any issue is fixed, add a new entry to `05_Log_Tracking/fixed-issue-log.md`.
- Update `03_Penpot_Status/status.md` after completion.

After completion, report:

1. Penpot page updated
2. Frame updated or created
3. Input files used
4. Prompt files used
5. Exact sections created
6. Any issue found
7. Log files updated
8. Next step
