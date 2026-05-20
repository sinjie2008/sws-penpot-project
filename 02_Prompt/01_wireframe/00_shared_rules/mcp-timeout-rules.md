# Shared MCP Timeout Rules

These rules are used to reduce Penpot MCP timeout issues.

---

## Main timeout rule

Do not process the full Penpot file.
Do not process all boards.
Do not process the full page in one run.
Do not process a large board in one run.

Work in small batches only.

---

## Required scan-first workflow

Before editing any Penpot board or frame, Codex must:

1. scan only the provided target
2. list detected sections or components
3. estimate the task size
4. identify possible timeout risk
5. stop and ask the user which section or batch to process first

Codex must not edit during the scan step.

---

## One section per run

For large boards, Codex should process only one section per run.

Examples:

```text
Run 1: Header only
Run 2: Hero only
Run 3: Overview only
Run 4: Latest News only
Run 5: Footer only
```

Do not process Header + Hero + Footer together unless the user clearly approves and the layer count is small.

---

## Batch limit

Default batch limit:

```text
1 section board per run
or
1 visible page section per run
or
1 card group set per run
```

If the target section contains many cards, process by smaller groups:

```text
Cards 01 to 04 only
Footer column 01 only
Navigation only
Breadcrumb only
```

---

## Logging timeout behavior

If timeout happens:

1. stop the current operation
2. do not retry the same large operation
3. record the timeout in `05_Log_Tracking/error-log.md`
4. suggest a smaller batch
5. ask the user which smaller section to continue with

---

## Recommended large-board workflow

For large boards, use this order:

```text
1. 01_image_to_editable_wireframe
2. 02_board_to_section_boards
3. 04_component_grouping_only
```

Avoid using `03_board_to_sections_and_components` for large boards because it combines too many actions.

---

## Stop instruction

After completing one section or one batch, Codex must stop and report:

```text
Completed this section only.
Please confirm the next section to continue.
```
