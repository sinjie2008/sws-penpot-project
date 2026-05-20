# Browser Timeout Rules

## Existing Browser Session Rule

Codex must use the existing browser session only.

Codex must not use an isolated browser.
Codex must not open an incognito browser.
Codex must not create a new browser session unless the user clearly requests it.

Use the current logged-in browser session so that:

- Penpot login state is preserved
- current file remains accessible
- current page remains accessible
- selected board or frame context is not lost

## Timeout Prevention Rule

Do not process the full Penpot file.
Do not process all boards.
Do not process the full page in one run.
Do not process a large board in one run.

Work in small batches only.

## Timeout Recovery Rule

If timeout happens, Codex must:

1. Stop the current action immediately.
2. Do not open an isolated browser.
3. Do not open a new browser session.
4. Reload the existing browser tab only.
5. Wait until Penpot is fully loaded again.
6. Confirm the same Penpot file is open.
7. Confirm the same page is open.
8. Confirm the same target board is visible.
9. Re-scan only the last target board or safe section.
10. Continue only from the last safe completed step.

Codex must not reprocess the full file after timeout.
Codex must not scan all boards after timeout.
Codex must not duplicate completed work after timeout.

## Timeout Log Rule

When timeout happens, update the relevant log with:

- timeout time
- target board name
- last completed action
- action that caused timeout
- browser reload status
- next safe action
