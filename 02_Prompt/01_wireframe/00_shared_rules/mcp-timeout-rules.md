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

## Existing browser session rule

If Penpot MCP times out, disconnects, or becomes unresponsive:

- Do not open Penpot in an isolated browser.
- Do not open Penpot in a new temporary browser session.
- Do not use a separate browser profile.
- Use the existing active browser session where the Penpot file is already opened.
- Use the existing logged-in Penpot browser tab whenever possible.
- If the Penpot page is already open, refresh that existing page only.
- After refresh, reconnect Penpot MCP to the same existing browser session.

---

## Timeout recovery rule

If timeout happens:

1. stop the current operation
2. do not retry the same large operation
3. record the timeout in `05_Log_Tracking/error-log.md`
4. suggest a smaller batch
5. ask the user which smaller section to continue with
6. try to reconnect only once
7. use the existing browser session only
8. refresh the existing Penpot page only if needed
9. continue only from the last unfinished section or batch

Do not restart the full task from the beginning.

---

## After reconnecting

After reconnecting, Codex must reconfirm:

1. Penpot MCP is available
2. the active Penpot project/file is correct
3. the active Penpot page is correct
4. the target board or section still exists
5. completed work is still present
6. the last unfinished section or batch is identified

Then continue only from the last unfinished section or batch.

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

## Resume rule

When resuming after timeout:

- resume only the same target board or target section board
- do not reprocess completed sections
- do not reprocess completed groups
- do not touch non-target boards
- do not duplicate groups or layers
- do not recreate section boards that already exist
- do not restart from the beginning unless the user confirms

---

## Stop instruction

After completing one section or one batch, Codex must stop and report:

```text
Completed this section only.
Please confirm the next section to continue.
```

---

## Final rule

Always prioritize safety over speed.

Use the existing browser session only.  
Do not use isolated browser.  
Scan first.  
Ask before editing.  
Process one section or one batch at a time.
