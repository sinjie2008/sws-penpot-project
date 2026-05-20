# Fixed Issue Log

Use this file to record issues that have been fixed.

Do not delete old entries. Add new entries at the top.

---

## Fixed Issue 0017
Date:
2026-05-13 16:07:09 +08:00

Related error ID:
Error 0017

Stage:
01 Wireframe

Target Penpot page:
01 Wireframe

Target frame:
Lo - App / Com & Networking

Issue:
Previous rename attempt from `Home / Application / Communication & Networking / Wireframe / Desktop` to `Lo - App / Com & Networking` could not be verified because Penpot MCP timed out.

Fix applied:
Retried the target-only Penpot board rename after MCP responded again.

Verified:
Yes

Notes:
Verification confirmed exactly one board named `Lo - App / Com & Networking`, zero boards named `Home / Application / Communication & Networking / Wireframe / Desktop`, and only the target board name changed.

---

## Fixed Issue 2026-05-08-1511
Date:
2026-05-08 15:11:16 +08:00

Related error ID:
Error 2026-05-08-1511 / Error 2026-05-08-1511A

Stage:
01 Wireframe

Target Penpot page:
01 Wireframe

Target frame:
Home / Our Products / Wireframe / Desktop

Issue:
The previous target frame content matched by count but the visual layout did not match the source because text rendered displaced/clipped.

Fix applied:
Rebuilt the target frame at 1440 x 1170 px using source-scaled geometry, corrected text rendering with top-aligned auto-height text, adjusted the Latest Release section/card positions, restored a temporarily shifted related board order, and reran target verification.

Verified:
Yes

Notes:
Verification passed with 54/54 exact readable text occurrences, no missing/wrong-count/unexpected text, no `UNCERTAIN:` text, no image/non-grayscale/shadow/out-of-bounds target issues, max text height 49 px, successful SVG export with key text, and unchanged homepage position/size/child count. PNG export still returned `http error`.

---

## Fixed Issue 2026-05-08-1508
Date:
2026-05-08 15:07:56 +08:00

Related error ID:
Error 2026-05-08-1508

Stage:
01 Wireframe

Target Penpot page:
01 Wireframe

Target frame:
Home / Our Company / Wireframe / Desktop

Issue:
The previous target frame had exact text counts but did not follow the source image layout closely enough.

Fix applied:
Corrected only the target board by using the source PNG dimensions (`5020 x 17000`) to restore source-proportional 1440 px layout coordinates, resizing the target board to 1440 x 4878, repositioning all 188 editable target child objects, and normalizing all 103 editable text layers to valid Penpot line-height behavior.

Verified:
Yes for target text, object, style, bounds, and key layout anchors.

Notes:
Final Penpot-side verification passed with 103/103 exact readable text occurrences, 103 editable text layers, 0 missing text items, 0 wrong-count text items, 0 unexpected text items, no `UNCERTAIN:` text, 0 image fills, 0 non-grayscale fills, 0 shadows, 0 out-of-bounds target objects, and key section anchors matching the source-scaled layout. Full-height PNG export timed out after the 4878 px board repair, so visual evidence is limited to the successful repaired export before final height restoration plus Penpot-side coordinate verification.

---

## Fixed Issue 2026-05-13-1558
Date:
2026-05-13 15:58:13 +08:00

Related error ID:
Error 2026-05-13-1045

Stage:
01 Wireframe

Target Penpot page:
01 Wireframe

Target frame:
Lo - Our Products / General

Issue:
Previous rename attempt could not be verified because Penpot MCP timed out.

Fix applied:
Retried the rename and verified top-level board names on `01 Wireframe`.

Verified:
Yes

Notes:
Verification found the old board name count is 0 and `Lo - Our Products / General` count is 1.

---

## Fixed Issue 2026-05-13-0913
Date:
2026-05-13 09:13:35 +08:00

Related error ID:
Error 2026-05-13-0913

Stage:
01 Wireframe

Target Penpot page:
01 Wireframe

Target frame:
Home / Our Products / General Components / Wireframe / Desktop

Issue:
The target frame still rendered with incorrect layout after the prior correction.

Fix applied:
Rebuilt only the target board with parent-relative placement and fixed text boxes, preserving the exact readable source text checklist and replacing image/photo areas with editable placeholder rectangles.

Verified:
Yes

Notes:
Rendered PNG export succeeded. Verification passed with 32/32 editable text layers, 27 editable rectangles, 0 missing/unexpected text items, 0 image fills, 0 shadows, 0 bad text boxes, 0 source-anchor failures, and 0 changed/added non-target frames.

---

## Fixed Issue 2026-05-08-1504
Date:
2026-05-08 15:04:18 +08:00

Related error ID:
Error 2026-05-08-1504

Stage:
01 Wireframe

Target Penpot page:
01 Wireframe

Target frame:
Home / Our Products / General Components / Wireframe / Desktop

Issue:
The previous target frame had exact text counts but did not follow the source image layout closely enough.

Fix applied:
Recreated only the target board with source-proportional coordinates from `HOME _ OUR PRODUCTS _ GENERAL COMPONENTS.png`, restoring the section spacing, product-grid placement, selected product outline, and right-side placeholder positions.

Verified:
Yes

Notes:
Final Penpot-side verification passed with 32/32 exact editable text layers, 27 editable rectangle placeholders, 0 missing text items, 0 unexpected text items, 0 image fills, 0 shadows, 0 non-grayscale colors, 0 target overlaps, 0 changed/added non-target frames, and 0 failures across key source-layout anchors.

---

## Fixed Issue 2026-05-08-0927
Date:
2026-05-08 09:27:45 +08:00

Related error ID:
Error 2026-05-08-0927

Stage:
01 Wireframe

Target Penpot page:
01 Wireframe

Target frame:
News / Product News / New Product Releases / Wireframe / Desktop

Issue:
The first target creation attempt failed because font weight `600` was unsupported, and a duplicated target-owned breadcrumb temporarily existed as a loose root-level text artifact.

Fix applied:
Recreated the target using supported font weights only, confirmed the target board retained its editable `HOME > NEWS` breadcrumb, and removed only the loose root-level duplicate breadcrumb artifact by id.

Verified:
Yes for the target frame.

Notes:
Final target verification showed 70 expected source text occurrences, 70 editable target text layers, no missing/wrong/unexpected text, no image fills, no image shapes, no non-grayscale colors, no shadows, and no out-of-bounds target objects. PNG/SVG export timeout and unrelated non-target added-board discrepancy remain open in `Error 2026-05-08-0927`.

---

## Fixed Issue 2026-05-08-0926
Date:
2026-05-08 09:25:57 +08:00

Related error ID:
Error 2026-05-08-0926

Stage:
01 Wireframe

Target Penpot page:
01 Wireframe

Target frame:
News / Events & Activities / Exhibitions & Trade Shows / Wireframe / Desktop

Issue:
Initial target verification found oversized text bounds on target text layers after the creation call committed.

Fix applied:
Resized only the target frame's affected editable text layers to fixed, contained text boxes and reran target object-level verification.

Verified:
Yes for the target text bounds.

Notes:
Final target object verification showed 0 out-of-bounds target objects, 0 image fills, 0 image shapes, 0 non-grayscale colors, and 0 shadows. Separate PNG/SVG export timeouts remain logged under `Error 2026-05-08-0926`.

---

## Fixed Issue 2026-05-08-0916
Date:
2026-05-08 09:16:45 +08:00

Related error ID:
Error 2026-05-08-0916

Stage:
01 Wireframe

Target Penpot page:
01 Wireframe

Target frame:
News / Company News / Corporate Social Responsibility / Wireframe / Desktop

Issue:
The initial target creation call timed out after 30 seconds, broad verification calls timed out, and the first target PNG export showed target-only spacing issues around the hero text and pagination.

Fix applied:
Inspected the committed target board after timeout, verified target text with smaller direct-child checks, adjusted only the target frame by moving pagination below the second row placeholders and improving hero/card text spacing, then reran smaller target text/style/bounds checks.

Verified:
Yes for target content and object-level wireframe constraints.

Notes:
Final target verification showed 50 expected readable text occurrences, 50 editable target text layers, no missing/wrong/unexpected text, no `UNCERTAIN:` text, no image fills, no image shapes, no non-grayscale colors, no shadows, and no out-of-bounds target objects. Post-adjustment PNG/SVG export and SVG markup generation still timed out and remain logged as unresolved. Six non-target boards appeared after the pre-edit snapshot and were left untouched.

---

## Fixed Issue 0022
Date:
2026-05-07 09:58:46 +08:00

Related error ID:
Error 0027

Stage:
01 Wireframe

Target Penpot page:
01 Wireframe

Target frame:
Home / Our Company / Quality Standards / Wireframe / Desktop

Issue:
The corrected Penpot MCP creation call timed out after 30 seconds while creating the editable Quality Standards desktop wireframe.

Fix applied:
Verified the completed target board after the timeout instead of rerunning against unrelated frames. Confirmed the target board contains 150 editable text layers matching the checklist exactly, 0 missing/wrong/unexpected text items, 0 image fills, 0 non-grayscale fills, 0 shadows, 0 out-of-bounds target objects, and exported PNG successfully.

Verified:
Yes

Notes:
The timeout did not require content repair. Non-target Penpot changes observed during snapshot comparison were left untouched and logged separately.

---

## Fixed Issue 0021
Date:
2026-05-07 09:58:46 +08:00

Related error ID:
Error 0026

Stage:
01 Wireframe

Target Penpot page:
01 Wireframe

Target frame:
Home / Our Company / Quality Standards / Wireframe / Desktop

Issue:
The first Penpot MCP creation attempt failed because Penpot rejected `lineHeight: 130%`.

Fix applied:
Changed the text helper to use Penpot-compatible `lineHeight = "1.3"` and reran creation for the exact target frame.

Verified:
Yes

Notes:
The corrected target frame passed final text-count verification with 150 expected readable text occurrences and 150 editable text layers.

---

## Fixed Issue 0020
Date:
2026-05-07 09:58:46 +08:00

Related error ID:
Error 0025

Stage:
01 Wireframe

Target Penpot page:
01 Wireframe

Target frame:
Home / Our Company / Quality Standards / Wireframe / Desktop

Issue:
Local helper checks failed or were unavailable during source inspection and completion audit.

Fix applied:
Read the correct Superpowers plugin skill path, created the readable content checklist by direct source-image inspection, used `Select-String` after `rg` failed, and used approved escalated reads after the sandbox resumed in read-only mode.

Verified:
Yes

Notes:
These local tooling issues did not affect Penpot content verification.

---

## Fixed Issue 2026-05-13-1614
Date:
2026-05-13 16:14:09 +08:00

Related error ID:
Error 2026-05-13-1553

Stage:
01 Wireframe

Target Penpot page:
01 Wireframe

Target frame:
Lo - News

Issue:
Earlier attempt to rename `Home / News / Wireframe / Desktop` to `Lo - News` timed out and could not be verified.

Fix applied:
Retried the rename after Penpot MCP responded. Verified that `Home / News / Wireframe / Desktop` no longer exists and exactly one `Lo - News` board exists with the same board id, position, size, and child count.

Verified:
Yes

Notes:
No layout/content changes were made.

---

## Fixed Issue 0019
Date:
2026-05-07 09:50:44 +08:00

Related error ID:
Error 0023

Stage:
01 Wireframe

Target Penpot page:
01 Wireframe

Target frame:
Home / News / Wireframe / Desktop

Issue:
The corrected Penpot MCP creation call timed out after 30 seconds while creating the editable Home / News desktop wireframe.

Fix applied:
Verified the completed target board after the timeout instead of rerunning against approved frames. Confirmed the target board contains 103 editable text layers matching the checklist exactly, 0 missing/wrong/unexpected text items, 0 image fills, 0 non-grayscale fills, 0 shadows, 0 out-of-bounds target objects, adjusted the related-news badge text sizing inside the target frame, and exported PNG successfully.

Verified:
Yes

Notes:
The timeout did not require content repair. Snapshot comparison confirmed all pre-existing approved frames were untouched.

---

## Fixed Issue 0018
Date:
2026-05-07 09:50:44 +08:00

Related error ID:
Error 0022

Stage:
01 Wireframe

Target Penpot page:
01 Wireframe

Target frame:
Home / News / Wireframe / Desktop

Issue:
The first Penpot MCP creation attempt failed because a table-cell helper passed a coordinate value into `penpot.createText`.

Fix applied:
Corrected the helper argument order, cleared only the partial `Home / News / Wireframe / Desktop` target-frame children, and reran creation with valid text strings.

Verified:
Yes

Notes:
The corrected target frame passed final text-count verification with 103 expected readable text occurrences and 103 editable text layers.

---

## Fixed Issue 0017
Date:
2026-05-07 09:45:57 +08:00

Related error ID:
Error 0021

Stage:
01 Wireframe

Target Penpot page:
01 Wireframe

Target frame:
Home / Application / Automotive / Wireframe / Desktop

Issue:
The Penpot MCP creation call timed out after 30 seconds while creating the editable automotive desktop wireframe.

Fix applied:
Verified the completed target board after the timeout instead of rerunning against approved frames. Confirmed the target board contains 138 editable text layers matching the checklist exactly, 0 missing/wrong/unexpected text items, 0 image fills, 0 non-grayscale fills, 0 shadows, 0 out-of-bounds target objects, and a successful PNG export.

Verified:
Yes

Notes:
The timeout did not require content repair. Snapshot comparison confirmed existing approved frames were untouched.

---

## Fixed Issue 0016
Date:
2026-05-07 09:45:57 +08:00

Related error ID:
Error 0020

Stage:
01 Wireframe

Target Penpot page:
01 Wireframe

Target frame:
Home / Application / Automotive / Wireframe / Desktop

Issue:
Local `tesseract` was unavailable for OCR-assisted checklist preparation.

Fix applied:
Created the complete readable text checklist by direct source-image inspection and verified the completed target board against that checklist.

Verified:
Yes

Notes:
The local OCR tool absence did not affect Penpot content accuracy; final verification matched 138 expected readable text occurrences exactly.

---

## Fixed Issue 2026-05-13-1558
Date:
2026-05-13 15:58:59 +08:00

Related error ID:
Error 2026-05-13-1552

Stage:
01 Wireframe

Target Penpot page:
01 Wireframe

Target frame:
Lo - App

Issue:
Previous rename attempt from `Home / Application / Wireframe / Desktop` to `Lo - App` timed out and could not be verified.

Fix applied:
Retried with a direct `01 Wireframe` root-children lookup and renamed the board by id.

Verified:
Yes

Notes:
Verification confirmed 0 boards with old name, 1 board with new name, board id `7af01ba4-9432-8055-8007-fb3fc5846500`, x `301`, y `8817`, width `1440`, height `4822`, and 169 children.

---

## Fixed Issue 0015
Date:
2026-05-07 09:01:41 +08:00

Related error ID:
Error 0019

Stage:
01 Wireframe

Target Penpot page:
01 Wireframe

Target frame:
Home / Application / Wireframe / Desktop

Issue:
`rg` failed with access denied while checking log numbering.

Fix applied:
Used PowerShell `Select-String` to retrieve log headings and continue file updates.

Verified:
Yes

Notes:
The fallback returned current log numbering for MCP, error, fixed issue, and Codex logs.

---

## Fixed Issue 0014
Date:
2026-05-07 09:01:41 +08:00

Related error ID:
Error 0018

Stage:
01 Wireframe

Target Penpot page:
01 Wireframe

Target frame:
Home / Application / Wireframe / Desktop

Issue:
Initial Penpot creation failed on invalid `lineHeight` value, and the retry timed out after 30 seconds even though the target board completed.

Fix applied:
Removed explicit percentage line-height styling, removed the partial failed text object, verified the completed board using the stored target frame id, resized the board to contain the final CTA, and adjusted wrapped labels in the target frame only.

Verified:
Yes

Notes:
Final verification confirmed 59 checklist entries, 74 expected readable text occurrences, 74 editable Penpot text layers, no missing/wrong/unexpected text, no image fills, no non-grayscale fills, no shadows, no out-of-bounds target objects, and no changed approved frame snapshots.

---

## Fixed Issue 0013
Date:
2026-05-07 08:59:44 +08:00

Related error ID:
Error 0017

Stage:
01 Wireframe

Target Penpot page:
01 Wireframe

Target frame:
Home / Application / Communication & Networking / Wireframe / Desktop

Issue:
The first Penpot MCP creation call timed out after 30 seconds while creating the editable desktop communication and networking wireframe.

Fix applied:
Verified the completed target board after the timeout instead of rerunning against approved frames. Confirmed the target board contains 127 editable text layers matching the checklist exactly, 0 missing/wrong/unexpected text items, 0 image fills, 0 non-grayscale fills, 0 shadows, and a successful PNG export.

Verified:
Yes

Notes:
The timeout did not require content repair. Snapshot comparison confirmed existing approved frames were untouched.

---

## Fixed Issue 0013
Date:
2026-05-13 15:59:24 +08:00

Related error ID:
Error 0017

Stage:
01 Wireframe

Target Penpot page:
01 Wireframe

Target frame:
Lo - Header

Issue:
Penpot MCP timed out during the first attempt to rename `Header / Wireframe / Desktop` to `Lo - Header`, and the immediate follow-up lookup also timed out.

Fix applied:
Retried against the current page root after confirming Penpot was responsive. Renamed board ID `b1e5258a-dded-808f-8007-fa552378bd47` to `Lo - Header`.

Verified:
Yes

Notes:
Verification found 0 boards named `Header / Wireframe / Desktop` and 1 board named `Lo - Header` on active page `01 Wireframe` in active file `Main - Web Design`.

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

## Fixed Issue 2026-05-13-1557-footer-rename
Date:
2026-05-13 15:57:57 +08:00

Related error ID:
Error 2026-05-13-1554

Stage:
01 Wireframe

Target Penpot page:
01 Wireframe

Target frame:
Lo - Footer

Issue:
The previous attempt to rename `Footer / Wireframe / Desktop` to `Lo - Footer` timed out and could not be verified.

Fix applied:
Retried with a minimal Penpot MCP rename call and verified the result by direct shape id.

Verified:
Yes

Notes:
Board id `b1e5258a-dded-808f-8007-fa550cad5e6d` is now named `Lo - Footer`, with width 1440, height 640, and 35 children.

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

## Fixed Issue 0012
Date:
2026-05-13 09:50:57 +08:00

Related error ID:
Error 0015 / Error 0016

Stage:
01 Wireframe

Target Penpot page:
01 Wireframe

Target frame:
Home / Our Products / General Components / EMC Components / Chip Array Ferrite Bead / A4K / Wireframe / Desktop

Issue:
The A4K correction was blocked by Penpot MCP disconnect, and the retry text-coordinate update timed out.

Fix applied:
Reconnected to Penpot MCP, inspected the target frame, completed source-scaled text coordinate correction, and verified the corrected target by Penpot-side object/text inspection instead of PNG/SVG export.

Verified:
Yes

Notes:
Final verification reported 160/160 editable text occurrences, 315 source-traced geometry objects, 0 text-anchor errors, 0 key geometry-anchor errors, 0 missing/extra text, 0 image fills, 0 non-grayscale fills, 0 shadows, and 0 protected-frame changes.

---

## Fixed Issue 0011
Date:
2026-05-13 09:35:33 +08:00

Related error ID:
Error 0014

Stage:
01 Wireframe

Target Penpot page:
01 Wireframe

Target frame:
Home / Our Products / General Components / EMC Components / Chip Array Ferrite Bead / A4K / Wireframe / Desktop

Issue:
The A4K layout still did not match the source closely enough after the previous correction.

Fix applied:
Replaced the target frame's non-text hand-drawn geometry with source-traced line geometry scaled from the original PNG. Kept the 160 editable text layers and fixed text bounds.

Verified:
Partially

Notes:
Penpot-side inspection verified the target frame at 1440 x 4906 px with 160 editable text layers and 316 source-traced geometry objects. Key source-scaled anchors matched expected coordinates. PNG and SVG export timed out, so final visual export verification is still blocked.

---

## Fixed Issue 0010
Date:
2026-05-08 15:17:35 +08:00

Related error ID:
Error 0013

Stage:
01 Wireframe

Target Penpot page:
01 Wireframe

Target frame:
Home / Our Products / General Components / EMC Components / Chip Array Ferrite Bead / A4K / Wireframe / Desktop

Issue:
The A4K wireframe layout was visually incomplete and not source-proportional.

Fix applied:
Rebuilt only the target A4K frame to 1440 x 4906 px, using source-scaled major anchors for product summary, product details tabs, specifications, product table, environmental, performance curves, physical dimension, tape & reel, soldering/washing, and CTA sections. Fixed all 160 target text bounds after Penpot expanded them.

Verified:
Yes

Notes:
Verification passed with 160/160 editable text occurrences, 0 missing or unexpected text, no `UNCERTAIN:` text, no image fills, no non-grayscale fills, no shadows, max target text height 69 px, successful PNG export after bounds correction, and no protected-frame changes.

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

## Fixed Issue 0009
Date:
2026-05-13 16:10:32 +08:00

Related error ID:
Error 0012

Stage:
01 Wireframe

Target Penpot page:
01 Wireframe

Target frame:
Lo - Our Products / General / EMC

Issue:
Previous rename attempt timed out and could not be verified.

Fix applied:
Retried with a minimal Penpot MCP rename command and then ran a separate top-level board inspection.

Verified:
Yes

Notes:
Board `b1e5258a-dded-808f-8007-fa515eb14eb3` is now named `Lo - Our Products / General / EMC`; the old name `Home / Our Products / General Components / EMC Components / Wireframe / Desktop` no longer exists.

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

---

## Fixed Issue 2026-05-07-0955
Date:
2026-05-07 09:55:16 +08:00

Related error ID:
Error 2026-05-07-0955

Stage:
01 Wireframe

Target Penpot page:
01 Wireframe

Target frame:
Home / Our Company / Sustainability / Wireframe / Desktop

Issue:
Large Penpot MCP operations timed out, and one anchor navigation text layer overflowed the target board.

Fix applied:
Retried with smaller Penpot MCP calls, verified the committed target board directly, adjusted only the target board's anchor navigation positions and widths, and re-ran verification.

Verified:
Yes

Notes:
Final verification showed 65 checklist entries, 65 editable target text layers, no missing/wrong/unexpected text, no image fills, no non-grayscale colors, no shadows, no out-of-bounds objects, and unchanged original pre-edit boards. Full-frame PNG/SVG export still timed out and was not used for final validation.

---

## Fixed Issue 2026-05-13-1558
Date:
2026-05-13 15:58:42 +08:00

Related error ID:
Error 2026-05-13-1551

Stage:
01 Wireframe

Target Penpot page:
01 Wireframe

Target frame:
Lo - Home / Sustainability

Issue:
Previous sustainability board rename attempt timed out and could not be verified.

Fix applied:
Looked up the target by known board id `426d5645-8eaa-80d5-8007-fb4c877d7b1c`, confirmed it still had the old name, renamed it to `Lo - Home / Sustainability`, and verified the same id, position, size, and child count afterward.

Verified:
Yes

Notes:
No layout/content changes were made.

---

## Fixed Issue 2026-05-07-1357
Date:
2026-05-07 13:57:10 +08:00

Related error ID:
Error 2026-05-07-1357

Stage:
01 Wireframe

Target Penpot page:
01 Wireframe

Target frame:
Home / Our Company / Key Achievements / Wireframe / Desktop

Issue:
Penpot MCP timeout/rendering issues occurred during creation and verification, and snapshot comparison detected temporary approved-frame position drift.

Fix applied:
Retried with smaller Penpot MCP calls, removed partial target boards, recreated only the target frame, switched text to supported Source Sans Pro variants, corrected text z-order, changed text line heights to Penpot ratios, restored three approved frames to their original coordinates, and reran final verification.

Verified:
Yes

Notes:
Final verification showed 59 checklist entries, 59 editable target text layers, no missing/wrong/unexpected text, no `UNCERTAIN:` text, no image fills, no image shapes, no non-grayscale colors, no shadows, no out-of-bounds objects, readable PNG export, and no approved-frame drift.

---

## Fixed Issue 2026-05-07-1419
Date:
2026-05-07 14:19:16 +08:00

Related error ID:
Error 2026-05-07-1419

Stage:
01 Wireframe

Target Penpot page:
01 Wireframe

Target frame:
Global Presence / Wireframe / Desktop

Issue:
Initial target creation attempts failed on invalid Penpot text property assignments, and a protected non-target frame temporarily drifted in position.

Fix applied:
Removed partial `Global Presence / Wireframe / Desktop` boards, recreated only the target frame using supported Penpot font application without invalid text-decoration/font-family assignments, and restored `Home / Our Company / Wireframe / Desktop` to its pre-edit coordinates.

Verified:
Partially

Notes:
Target content/style verification passed with 178 checklist entries, 178 editable text layers, no missing/wrong/unexpected text, no `UNCERTAIN:` text, no image shapes/fills, no non-grayscale colors, no shadows, and no out-of-bounds target objects. Remaining unresolved issues are recorded in `Error 2026-05-07-1419`: target PNG export timeout and non-target snapshot discrepancies.

---

## Fixed Issue 2026-05-07-1410
Date:
2026-05-07 14:10:13 +08:00

Related error ID:
Error 2026-05-07-1410

Stage:
01 Wireframe

Target Penpot page:
01 Wireframe

Target frame:
Thank You Message / Wireframe / Desktop

Issue:
Initial Penpot font assignment failed, one broad verification call timed out, local `rg` search failed with access denied, and one approved non-target frame temporarily drifted.

Fix applied:
Removed only the partial target board, recreated the target using a supported Penpot font application method, verified with a smaller direct-child target pass, restored the approved frame from the pre-edit snapshot, and used direct file reads after the `rg` failure.

Verified:
Yes

Notes:
Final verification showed 10 checklist entries, 10 editable target text layers, no missing/wrong/unexpected text, no `UNCERTAIN:` text, no image fills, no image shapes, no non-grayscale colors, no shadows, no out-of-bounds objects, readable PNG export, and no approved-frame drift.

---

## Fixed Issue 2026-05-13-1010
Date:
2026-05-13 10:10:49 +08:00

Related error ID:
Error 2026-05-13-1010

Stage:
01 Wireframe

Target Penpot page:
01 Wireframe

Target frame:
Thank You Message / Wireframe / Desktop

Issue:
The target frame was content-correct but not layout-matched to the source image.

Fix applied:
Corrected only the target frame by using the source image dimensions as the coordinate basis, resizing the board to 1440 x 952, matching the panel outline position, and aligning text layers to measured source-scaled anchors.

Verified:
Yes

Notes:
Final verification showed 10 checklist entries, 10 editable target text layers, no missing/wrong/unexpected text, 0 source text-anchor issues, no image fills, no shadows, no out-of-bounds objects, PNG export completed, and no protected-frame drift.

---

## Fixed Issue 2026-05-07-1411
Date:
2026-05-07 14:11:35 +08:00

Related error ID:
Error 2026-05-07-1411

Stage:
01 Wireframe

Target Penpot page:
01 Wireframe

Target frame:
Inquiry Cart / Wireframe / Desktop

Issue:
Penpot MCP font validation failed during the first creation attempt, the larger creation call timed out after committing the target board, and snapshot comparison detected temporary approved-frame position drift.

Fix applied:
Removed only the partial target board, recreated only the target frame with supported Penpot-applied font variants, verified the committed target board with smaller calls, restored the approved non-target frame to its original coordinates, and reran final verification.

Verified:
Yes

Notes:
Final verification showed 99 checklist entries, 99 editable target text layers, no missing/wrong/unexpected text, no `UNCERTAIN:` text, no image fills, no image shapes, no non-grayscale colors, no shadows, no out-of-bounds objects, successful PNG export, and no approved-frame drift.

---

## Fixed Issue 2026-05-07-1421
Date:
2026-05-07 14:21:46 +08:00

Related error ID:
Error 2026-05-07-1415

Stage:
01 Wireframe

Target Penpot page:
01 Wireframe

Target frame:
Specification Search / Wireframe / Desktop

Issue:
Initial Penpot creation attempts failed on unsupported font-weight handling, one creation call timed out, subsequent MCP calls temporarily timed out, and target object verification initially found out-of-bounds objects caused by target board height and text line-height metadata.

Fix applied:
Allowed MCP to recover, inspected the committed target board, resized only the target board to contain all content, normalized only target text line-height metadata, brought target text layers forward, reran source-text and object-level verification, and exported the target as PNG.

Verified:
Yes for the target frame.

Notes:
Final target verification showed 171 checklist text occurrences across 93 unique values, 171 editable target text layers, no missing/wrong/unexpected text, no `UNCERTAIN:` text, no image fills, no image shapes, no non-grayscale colors, no shadows, no out-of-bounds target objects, and readable PNG export. A separate non-target `Thank You Message / Wireframe / Desktop` id/child-count snapshot anomaly remains logged for audit.

---

## Fixed Issue 2026-05-08-0923
Date:
2026-05-08 09:23:17 +08:00

Related error ID:
Error 2026-05-08-0923

Stage:
01 Wireframe

Target Penpot page:
01 Wireframe

Target frame:
News / Product News / Latest Product News / Wireframe / Desktop

Issue:
One target product-card title text layer was initially created with an inserted line break in `Radial-Leaded Inductor : Fully Automated Production Overview`.

Fix applied:
Updated only that target text layer so its editable text exactly matches the source checklist string.

Verified:
Yes for the target frame.

Notes:
Final exact target text verification showed 47 editable text layers, 0 missing text items, 0 wrong-count text items, and 0 unexpected text items. Broader protected-frame discrepancies remain logged separately.

---

## Fixed Issue 2026-05-08-0922
Date:
2026-05-08 09:22:35 +08:00

Related error ID:
Error 2026-05-08-0922

Stage:
01 Wireframe

Target Penpot page:
01 Wireframe

Target frame:
News / Events & Activities / Event Calendar / Wireframe / Desktop

Issue:
Initial target verification found oversized text bounds on target text layers after the creation call committed.

Fix applied:
Resized only the target frame's editable text layers to fixed, contained text boxes and reran target object-level verification.

Verified:
Yes for the target text bounds.

Notes:
Final target object verification showed 0 out-of-bounds target objects, 0 image fills, 0 image shapes, 0 non-grayscale colors, and 0 shadows. Separate PNG/SVG export timeouts and unexpected non-target frame additions remain logged as open under `Error 2026-05-08-0922`.

---

## Fixed Issue 2026-05-08-1504
Date:
2026-05-08 15:04:23 +08:00

Related error ID:
Error 2026-05-08-1504

Stage:
01 Wireframe

Target Penpot page:
01 Wireframe

Target frame:
News / Events & Activities / Event Calendar / Wireframe / Desktop

Issue:
Event Calendar target layout was vertically over-expanded compared with the source image.

Fix applied:
Rebuilt only the Event Calendar target at 1440 x 2336 using source-scaled coordinates for the top cards, event calendar panel, category navigation, filters, table, and pagination. Removed the stray top-level breadcrumb left by the failed first correction attempt and restored visible heights on affected non-target frames.

Verified:
Yes for the target frame and visible protected-frame geometry.

Notes:
Target verification passed with 110 editable text layers, all checklist counts matched exactly, no `UNCERTAIN:` text, no image/non-grayscale/shadow/out-of-bounds target issues, and successful PNG export. Final protected-frame visible comparison showed no non-target name/type/position/size/child-count differences. Remaining exact discrepancy: `Home / Our Products / General Components / Wireframe / Desktop` has the same visible geometry and child count but a changed Penpot id.

---

## Fixed Issue 2026-05-08-0923
Date:
2026-05-08 09:23:16 +08:00

Related error ID:
Error 2026-05-08-0923

Stage:
01 Wireframe

Target Penpot page:
01 Wireframe

Target frame:
News / Product News / End-of-Life / Wireframe / Desktop

Issue:
The target creation call timed out after committing the board, so completion could not rely on the timed-out response.

Fix applied:
Inspected the committed target board with smaller Penpot MCP calls and verified the target against the pre-created source text checklist and wireframe object constraints.

Verified:
Yes for the target frame.

Notes:
Final target verification showed 70 expected checklist text occurrences, 70 editable target text layers, no missing/wrong/unexpected text, no `UNCERTAIN:` text, no image fills, no image shapes, no non-grayscale colors, no shadows, and no coordinate out-of-bounds target objects. Full-frame export timeout and non-target added-board snapshot discrepancy remain open in the error log.

---

## Fixed Issue 2026-05-08-1505
Date:
2026-05-08 15:05:55 +08:00

Related error ID:
Error 2026-05-08-1505

Stage:
01 Wireframe

Target Penpot page:
01 Wireframe

Target frame:
News / Product News / End-of-Life / Wireframe / Desktop

Issue:
The target layout was too compressed compared with the source, and PNG export showed text was not visibly rendering even though editable text layers existed.

Fix applied:
Updated only the target frame to source-scaled 1440 px geometry, resized the board to 1440 x 2428 px, repositioned the major sections and product list, reapplied a supported sans font to all 70 editable target text layers, and brought the text layers forward.

Verified:
Yes.

Notes:
Verification passed with 70/70 exact editable text layers, 0 missing/wrong/unexpected text, no image fills/shapes, no non-grayscale colors, no shadows, no out-of-bounds target objects, and successful PNG export showing visible text and corrected source-like layout.

---

## Fixed Issue 2026-05-08-0923-brochures
Date:
2026-05-08 09:23:49 +08:00

Related error ID:
Error 2026-05-08-0923-brochures

Stage:
01 Wireframe

Target Penpot page:
01 Wireframe

Target frame:
News / Resources / Brochures / Wireframe / Desktop

Issue:
The target creation call timed out after committing the board, one broad verification call timed out, the target initially overlapped non-target boards that appeared after the pre-edit snapshot, and protected-frame comparison found one temporary non-target height drift.

Fix applied:
Inspected the committed target board with smaller Penpot MCP calls, verified the target against the pre-created source text checklist and wireframe object constraints, moved only the target frame to avoid overlap, restored `News / Company News / Corporate Social Responsibility / Wireframe / Desktop` to its pre-edit height, and reran final checks.

Verified:
Yes for the target frame and restored height drift.

Notes:
Final target verification showed 42 expected checklist text occurrences, 42 editable target text layers, no missing/wrong/unexpected text, no `UNCERTAIN:` text, no image fills, no image shapes, no non-grayscale colors, no shadows, and no out-of-bounds target objects. Full-frame export timeout and non-target added-board snapshot discrepancy remain open in the error log.

---

## Fixed Issue 2026-05-11-1007-header-translate-layout
Date:
2026-05-11 10:07:32 +08:00

Related error ID:
Error 2026-05-11-0948-header-translate

Stage:
01 Wireframe

Target Penpot page:
01 Wireframe

Target frame:
Header / Translate / Wireframe / Desktop

Issue:
The first target version passed exact text-count verification but did not match the source layout closely enough because the navigation and language-menu x positions were approximate and too spread out.

Fix applied:
Rebuilt only `Header / Translate / Wireframe / Desktop` using source-scaled geometry from the 5020 x 940 source image, including source-derived x positions for the top navigation, primary navigation, and language row, then resized the target board to 1440 x 270 px.

Verified:
Yes for source-scaled target geometry and exact text content.

Notes:
Verification passed with 17 expected readable text occurrences, 17 editable target text layers, 0 missing/wrong/unexpected text items, no `UNCERTAIN:` text, 0 source-position diffs, 0 text bounds violations, 0 image fills, 10 editable chevron strokes, and successful SVG markup generation. PNG export timeout remains open. A non-target `Header / News / Wireframe / Desktop` id/child-count change was observed during correction-pass protected-frame comparison and remains logged for separate audit.

Update:
2026-05-11 15:21:15 +08:00 - Fixed the remaining rendered layout issue where `Our Products` wrapped into two lines. Increased only the target `Primary nav / Our Products` text box width to 178 px. Verified by successful PNG export showing one-line `Our Products`, plus direct Penpot verification with 17/17 editable text layers, 0 missing/wrong/unexpected text, 0 source-position diffs, 0 bounds violations, 0 wrapping risks, 0 image fills, and 10 editable chevron strokes.

---

## Fixed Issue 2026-05-11-0948-header-about
Date:
2026-05-11 09:48:00 +08:00

Related error ID:
Error 2026-05-11-0948-header-about

Stage:
01 Wireframe

Target Penpot page:
01 Wireframe

Target frame:
Header / About / Wireframe / Desktop

Issue:
Broad Penpot MCP verification calls timed out, and initial target object verification found oversized text bounds on all 15 target text layers.

Fix applied:
Switched verification to direct current-page child traversal, resized only the target frame's 15 editable text layers to fixed single-line bounds, and reran target text and object verification.

Verified:
Yes for target content, target object bounds, and protected-frame stability.

Notes:
Final target verification showed 15 expected checklist text occurrences, 15 editable target text layers, no missing/wrong/unexpected text, no `UNCERTAIN:` text, no image fills, no image shapes, no non-grayscale fills, no shadows, no out-of-bounds target objects, and no diffs on the 26 pre-edit protected frames. PNG/SVG export timeout and unrelated post-snapshot board provenance remain open in the error log.

---

## Fixed Issue 2026-05-11-1005-header-about-correction
Date:
2026-05-11 10:05:59 +08:00

Related error ID:
Error 2026-05-11-1005-header-about-correction

Stage:
01 Wireframe

Target Penpot page:
01 Wireframe

Target frame:
Header / About / Wireframe / Desktop

Issue:
The first target layout matched text counts but did not match the source screenshot geometry closely enough. A temporary protected-frame height drift was detected on `Header / Translate / Wireframe / Desktop` during correction.

Fix applied:
Rebuilt only `Header / About / Wireframe / Desktop` in place to 1440 x 270 px using source-proportional coordinates from the 5020 x 940 image, then restored `Header / Translate / Wireframe / Desktop` to 1440 x 280 px.

Verified:
Yes.

Notes:
Final target verification passed with 15 expected readable text occurrences, 15 editable target text layers, 0 missing/unexpected text items, no `UNCERTAIN:` text, no image shapes/fills, no non-grayscale fills, no shadows, and no out-of-bounds target objects. `Header / Translate / Wireframe / Desktop` height drift was restored. Target PNG export and an unrelated `Header / News / Wireframe / Desktop` child-count discrepancy remain open in the error log.

---

## Fixed Issue 2026-05-11-1521-header-about-final-correction
Date:
2026-05-11 15:21:27 +08:00

Related error ID:
Error 2026-05-11-1521-header-about-final-correction

Stage:
01 Wireframe

Target Penpot page:
01 Wireframe

Target frame:
Header / About / Wireframe / Desktop

Issue:
The previous About correction still did not match the source visually because rendered text settings and text bounds were unsafe/clipped, despite passing text-count verification.

Fix applied:
Rebuilt only the target frame using the corrected shared header pattern, `Inter Tight`, fixed text boxes, `lineHeight` 1.2, text layers brought to front, and About dropdown items aligned across the source menu span.

Verified:
Yes.

Notes:
Verification passed with 15 expected readable text occurrences, 15 editable target text layers, 0 missing/unexpected text items, no `UNCERTAIN:` text, no clipped/bad text settings, no image shapes/fills, no non-grayscale fills, no shadows, 0 out-of-bounds target objects, 0 protected-frame diffs, and successful PNG export.
---

## Fixed Issue 2026-05-11-1005-header-support-correction
Date:
2026-05-11 10:05:00 +08:00

Related error ID:
Error 2026-05-11-1005-header-support-correction

Stage:
01 Wireframe

Target Penpot page:
01 Wireframe

Target frame:
Header / Support / Wireframe / Desktop

Issue:
The first Support header target was not visually close enough and used text line-height metadata that could make the layout render incorrectly.

Fix applied:
Rebuilt only the target frame child layers with source-scaled geometry, Penpot-safe `lineHeight` value `1.2`, corrected editable text boxes, and source-matched support dropdown menu sizing.

Verified:
Yes for the target frame.

Notes:
Final direct verification showed 15/15 exact editable text layers, 5/5 dropdown chevrons, 0 missing/wrong/unexpected text, no `UNCERTAIN:` text, no image fills/shapes, no non-grayscale colors, no shadows, and 0 out-of-bounds target objects. PNG/SVG export timeout remains logged.

---

## Fixed Issue 2026-05-11-0949-header-support
Date:
2026-05-11 09:49:00 +08:00

Related error ID:
Error 2026-05-11-0949-header-support

Stage:
01 Wireframe

Target Penpot page:
01 Wireframe

Target frame:
Header / Support / Wireframe / Desktop

Issue:
Initial target creation hit a font-weight validation error, and the first completed target had oversized auto-width text layer bounds.

Fix applied:
Rebuilt only the target board using supported Inter font variants and fixed editable text boxes for every readable source text item. Kept logo/icon/dropdown areas as editable grayscale placeholder shapes.

Verified:
Yes.

Notes:
Final verification showed 15/15 exact editable text layers, 5/5 dropdown chevrons, 0 missing/wrong/unexpected text items, no `UNCERTAIN:` text, no image fills/shapes, no non-grayscale colors, no shadows, no oversized text bounds, and 0 protected-frame changes. Full-frame PNG export timeout remains logged separately.

---

## Fixed Issue 2026-05-11-0948-header-news
Date:
2026-05-11 09:48:15 +08:00

Related error ID:
Error 2026-05-11-0948-header-news

Stage:
01 Wireframe

Target Penpot page:
01 Wireframe

Target frame:
Header / News / Wireframe / Desktop

Issue:
The first large target creation call timed out after committing a partial target board.

Fix applied:
Waited for Penpot MCP recovery, inspected only the target board with a smaller call, completed the missing dropdown/menu content with a smaller bounded creation call, and reran direct target and protected-frame verification.

Verified:
Yes for target creation and content verification.

Notes:
Final target verification showed 29 expected checklist text occurrences, 29 editable target text layers, no missing/wrong/unexpected text, no `UNCERTAIN:` text, no image fills, no image shapes, no non-grayscale colors, no shadows, and no protected-frame changes. Full-frame PNG export timeout remains logged in the error log.

---

## Fixed Issue 2026-05-11-1012-header-news-correction
Date:
2026-05-11 10:12:04 +08:00

Related error ID:
Error 2026-05-11-1012-header-news-correction

Stage:
01 Wireframe

Target Penpot page:
01 Wireframe

Target frame:
Header / News / Wireframe / Desktop

Issue:
The previous News header wireframe had layout fidelity problems: approximate positioning, oversized text bounds, too-short event placeholders, right-side overflow, incorrect main navigation spacing, and incorrect chevron direction.

Fix applied:
Rebuilt only the target frame with source-proportional 5020-to-1440 geometry, fixed main navigation positions, dropdown column spacing, event-card placeholder size/position, chevron direction, and editable text bounds.

Verified:
Yes for the target frame.

Notes:
Final target verification passed with 29/29 expected readable text occurrences, 29 editable target text layers, no missing/wrong/unexpected text items, no `UNCERTAIN:` text, no image fills/shapes, no non-grayscale colors, no shadows, 0 out-of-bounds target objects, and a successful PNG visual export. The unrelated `Header / About / Wireframe / Desktop` protected-frame discrepancy remains logged separately.

---

## Fixed Issue 2026-05-11-1521-header-news-second-correction
Date:
2026-05-11 15:21:37 +08:00

Related error ID:
Error 2026-05-11-1521-header-news-second-correction

Stage:
01 Wireframe

Target Penpot page:
01 Wireframe

Target frame:
Header / News / Wireframe / Desktop

Issue:
The corrected News frame still contained invented menu structure and event-card geometry drift compared with the resized source.

Fix applied:
Removed the invented first dropdown separator and company-column arrow, added/verified the far-right carousel arrow and left carousel arrow, realigned both event-card placeholders to source geometry, and shortened the Resources separator.

Verified:
Yes.

Notes:
Final target verification passed with 29/29 exact readable text occurrences, 0 missing/unexpected text, no `UNCERTAIN:` text, no invented first separator, no company arrow, expected carousel arrows, source-aligned event-card placeholders, and successful PNG visual export.

---

## Fixed Issue 2026-05-11-0952-home-application-open-all
Date:
2026-05-11 09:52:00 +08:00

Related error ID:
Error 2026-05-11-0952-home-application-open-all

Stage:
01 Wireframe

Target Penpot page:
01 Wireframe

Target frame:
Home / Application / Open All / Wireframe / Desktop

Issue:
The first committed target build had the correct text count, but the dense open-all application lists needed more vertical room for the Consumer and Industrial & Energy sections.

Fix applied:
Rebuilt only the target frame with a taller 1440 x 4448 px desktop board and preserved the six-card open dropdown/list hierarchy, exact source checklist text, grayscale wireframe style, editable text layers, and separately editable placeholder objects.

Verified:
Yes for target content and object verification.

Notes:
Final target verification showed 125 expected checklist text occurrences, 125 editable target text layers, 87 unique expected text values, no missing/wrong/unexpected text, no `UNCERTAIN:` text, no image fills, no image shapes, no non-grayscale colors, no shadows, 0 out-of-bounds target objects, and 0 protected-frame diffs. Penpot PNG export timeout and unrelated post-snapshot additions remain logged in the error log.

---

## Fixed Issue 2026-05-13-1026-a4k-chip-array-ferrite-bead-wireframe
Date:
2026-05-13 10:26:08 +08:00

Related error ID:
Error 2026-05-13-1026-a4k-chip-array-ferrite-bead-wireframe

Stage:
01 Wireframe

Target Penpot page:
01 Wireframe

Target frame:
Home / Our Products / General Components / EMC Components / Chip Array Ferrite Bead / A4K / Wireframe / Desktop

Issue:
The first committed A4K target board was taller than the source-scaled desktop frame because the initial large creation call timed out after committing a 1440 x 5488 px board.

Fix applied:
Corrected only the target board to 1440 x 4906 px and proportionally adjusted its internal vertical coordinates to keep all A4K source content inside the target frame.

Verified:
Yes.

Notes:
Final direct Penpot verification passed with 159/159 exact readable text occurrences, 0 missing/wrong/unexpected text items, no `UNCERTAIN:` text, no image fills, no non-grayscale fills/strokes, no shadows, 0 out-of-bounds target objects, and 0 protected-frame changes. Full-frame PNG export timeout remains logged separately.
