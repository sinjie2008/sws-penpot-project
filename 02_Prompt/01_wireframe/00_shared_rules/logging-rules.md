# Shared Logging Rules

After each Codex + Penpot MCP run, update the log files.

---

## Required log files

Update:

```text
05_Log_Tracking/mcp-log.md
03_Penpot_Status/status.md
```

Update only if needed:

```text
05_Log_Tracking/error-log.md
05_Log_Tracking/fixed-issue-log.md
```

---

## mcp-log.md

Add a new entry for every completed MCP action.

Include:

```text
Date/time:
Prompt used:
Target page:
Target board/frame/section:
Action completed:
Files read:
Result:
Next step:
```

---

## error-log.md

Only add entry if an issue happens.

Examples:

```text
MCP timeout
Target board not found
Unclear source text
Layer grouping failed
Visual change detected
Permission or MCP connection issue
```

---

## fixed-issue-log.md

Only add entry if an issue was fixed.

Include:

```text
Issue:
Fix applied:
Target:
Result:
```

---

## status.md

Update current status after completion.

Examples:

```text
01 Wireframe / Homepage / Header section completed
01 Wireframe / Homepage / Section boards created
01 Wireframe / HOME NEWS image-to-wireframe scan completed
```
