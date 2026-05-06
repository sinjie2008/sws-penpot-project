# Fixed Issue Log

Use this file to record issues that have been fixed.

Do not delete old entries. Add new entries at the top.

---

## Fixed Issue 0012
Date:
2026-05-06 15:55:04 +08:00

Related error ID:
Error 0016

Stage:
01 Wireframe

Target Penpot page:
01 Wireframe

Target frame:
Header / Wireframe / Desktop

Issue:
The first PNG export showed the editable text layers were not visibly rendering inside the header board because Penpot text glyph bounds were offset below their boxes.

Fix applied:
Adjusted the editable text-layer positions using their rendered `textBounds`, kept the exact source strings as editable text, and re-exported the board.

Verified:
Yes

Notes:
Final verification passed with 11 expected readable text occurrences, 11 editable text layers, 4 editable dropdown chevron shapes, no unexpected text, no image fills, no non-grayscale fills, no shadows, and protected frames unchanged.

---

## Fixed Issue 0011
Date:
2026-05-06 15:51:23 +08:00

Related error ID:
Error 0015

Stage:
01 Wireframe

Target Penpot page:
01 Wireframe

Target frame:
Footer / Wireframe / Desktop

Issue:
`git diff` could not run because the current workspace is not a Git repository.

Fix applied:
Verified the required tracking-file updates directly with PowerShell `Get-Content` instead of relying on Git diff output.

Verified:
Yes

Notes:
The command issue did not affect Penpot content or any existing approved frame.

---

## Fixed Issue 0010
Date:
2026-05-06 15:51:23 +08:00

Related error ID:
Error 0013

Stage:
01 Wireframe

Target Penpot page:
01 Wireframe

Target frame:
Footer / Wireframe / Desktop

Issue:
`rg --files` failed with access denied while checking project tracking files.

Fix applied:
Replaced the file enumeration command with PowerShell `Get-ChildItem`, confirmed the required tracking files, and continued with the footer-only Penpot task.

Verified:
Yes

Notes:
The command issue did not affect Penpot content or any existing approved frame.

---

## Fixed Issue 0009
Date:
2026-05-06 15:40:38 +08:00

Related error ID:
Error 0012

Stage:
01 Wireframe

Target Penpot page:
01 Wireframe

Target frame:
Home / Our Products / General Components / EMC Components / Chip Array Ferrite Bead / A4K / Wireframe / Desktop

Issue:
Penpot creation initially failed on font-weight validation, then the corrected large creation call timed out before returning verification.

Fix applied:
Applied valid Inter font variants before styling text, inspected the created target board after the timeout, corrected the source checklist count for the standalone `-40°C to +125°C` value, and reran verification against all target-board editable text layers.

Verified:
Yes

Notes:
Final verification passed with 114 checklist entries, 160 expected readable text occurrences, 160 editable Penpot text layers, no extra or missing text, no `UNCERTAIN:` text, no image fills, no non-grayscale fills, no shadows, and no protected-frame changes.

---

## Fixed Issue 0008
Date:
2026-05-06 15:36:32 +08:00

Related error ID:
Error 0011

Stage:
01 Wireframe

Target Penpot page:
01 Wireframe

Target frame:
Home / Our Products / General Components / EMC Components / Wireframe / Desktop

Issue:
Local repository search with `rg` failed due to access denial.

Fix applied:
Used PowerShell `Get-ChildItem` and `Select-String` fallback commands to complete repository inspection.

Verified:
Yes

Notes:
The command failure did not affect the Penpot frame creation or checklist verification.

---

## Fixed Issue 0007
Date:
2026-05-06 15:36:32 +08:00

Related error ID:
Error 0010

Stage:
01 Wireframe

Target Penpot page:
01 Wireframe

Target frame:
Home / Our Products / General Components / EMC Components / Wireframe / Desktop

Issue:
The first Penpot-side text verification query returned 0 text layers, and text boxes had oversized heights because line-height was interpreted as a multiplier.

Fix applied:
Verified direct children of the target board, corrected all 124 text layers to line-height `1.35`, resized text boxes to controlled heights, and reran the checklist verification.

Verified:
Yes

Notes:
Final verification passed with 37 checklist entries, 124 expected text occurrences, 124 editable text layers, no missing text, no unexpected text, no image fills, no shadows, and grayscale-only styling.

---

## Fixed Issue 0006
Date:
2026-05-06 15:31:00 +08:00

Related error ID:
Error 0009

Stage:
01 Wireframe

Target Penpot page:
01 Wireframe

Target frame:
Home / Our Products / General Components / Wireframe / Desktop

Issue:
Initial placement of the new target frame overlapped or affected spacing near the protected `Home / Our Products / Wireframe / Desktop` frame.

Fix applied:
Restored `Home / Our Products / Wireframe / Desktop` to its pre-edit coordinate and placed `Home / Our Products / General Components / Wireframe / Desktop` separately. Final verification found no top-level frame overlaps.

Verified:
Yes

Notes:
Final target verification passed with 32 checklist items matched exactly, 32 editable text layers, 27 editable rectangle objects, no image fills, no shadows, grayscale-only styling, and 1248 px content width.

---

## Fixed Issue 0005
Date:
2026-05-06 15:25:23 +08:00

Related error ID:
Error 0008

Stage:
01 Wireframe

Target Penpot page:
01 Wireframe

Target frame:
Home / Our Products / Wireframe / Desktop

Issue:
Git verification commands failed because the workspace is not a Git repository.

Fix applied:
Verified the updated log and status files directly using `Get-Content`.

Verified:
Yes

Notes:
The Git command failure did not affect the Penpot frame creation or checklist verification.

---

## Fixed Issue 0004
Date:
2026-05-06 15:25:23 +08:00

Related error ID:
Error 0007

Stage:
01 Wireframe

Target Penpot page:
01 Wireframe

Target frame:
Home / Our Products / Wireframe / Desktop

Issue:
Local repository search with `rg` failed due to access denial.

Fix applied:
Used PowerShell `Get-ChildItem` and `Select-String` fallback commands to complete repository inspection.

Verified:
Yes

Notes:
The command failure did not affect the Penpot frame creation or checklist verification.

---

## Fixed Issue 0003
Date:
2026-05-06 15:13:12 +08:00

Related error ID:
Error 0005

Stage:
01 Wireframe

Target Penpot page:
01 Wireframe

Target frame:
Homepage / Wireframe / Desktop

Issue:
Penpot MCP editing access was initially unavailable, then the first creation attempt failed on unsupported font weight `600`.

Fix applied:
Discovered and used `mcp__penpot__.execute_code`, recreated the homepage board using default Penpot font weight, removed one partial text object from the failed attempt, and fixed arrow path contents.

Verified:
Yes

Notes:
Verification confirmed one top-level homepage board, 165 editable text layers, 0 missing text strings, 0 unexpected text strings, no image fills, no shadows, and no populated non-target pages.

---

## Fixed Issue 0002
Date:
2026-05-06 14:49:11 +08:00

Related error ID:
Error 0002 / Error 0003 / Error 0004

Stage:
01 Wireframe

Target Penpot page:
01 Wireframe

Target frame:
27 desktop wireframe frames from `01_Input/raw-wireframe/Wireframe/`

Issue:
Penpot MCP was initially missing editing access, then timed out after a bulk creation attempt, then became disconnected.

Fix applied:
Penpot MCP plugin connection recovered. Partial objects were removed, a smaller Penpot-side batch helper was used, and the 27 editable desktop wireframe boards were recreated in smaller batches.

Verified:
Yes

Notes:
Verification confirmed 27 boards on `01 Wireframe`, all 1440 px wide, all mapped to the 27 expected source files, with editable text/rectangle objects, no image fills, no shadows, and only black/white/grayscale colors.

---

## Fixed Issue 0001
Date:
YYYY-MM-DD

Related error ID:
Error 0001

Stage:
01 Wireframe / 03 Final Design / 04 Mobile Design / 05 Prototype / 04 Final Code

Target Penpot page:
Page name

Target frame:
Frame name

Issue:
Describe the original issue.

Fix applied:
Describe the fix.

Verified:
Yes / No

Notes:
Additional notes.
