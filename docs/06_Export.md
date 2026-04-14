# Export

**Copyright (c) 2026 Tom Hanke Leon Vincent. All Rights Reserved.**

---

## Overview

Diff results can be exported to **CSV** or **JSON** with a single click.

---

## How to Export

1. Run a diff (see [Diff Guide](./05_Diff.md))
2. Optionally apply a search filter to export only specific rows
3. Click the **Export...** button in the diff toolbar
4. A save dialog opens — choose a file name and location
5. Select the format: `.csv` or `.json`
6. Click **Save**

> The Export button is only enabled when there are results to export.

---

## Export Scope

Only **currently visible rows** are exported — the export respects the active search filter and the "Show Unchanged" toggle.

---

## CSV Format

```csv
Change,Row Name,Field,Value A,Value B
+ Added,NewRow_3,,,
~ Modified,Row_1,Health,100,150
- Removed,OldRow_7,,,
```

---

## JSON Format

```json
[
  {
    "change": "+ Added",
    "row": "NewRow_3",
    "field": "",
    "valueA": "",
    "valueB": ""
  },
  {
    "change": "~ Modified",
    "row": "Row_1",
    "field": "Health",
    "valueA": "100",
    "valueB": "150"
  }
]
```

All string values are **properly escaped** — special characters like quotes, backslashes, and newlines are handled correctly.

---

## Default Format

Configure the default export format in:

```
Project Settings → Plugins → DataTable Pro Editor → Export → Default Export As JSON
```

---

## Support

- **Discord:** https://discord.gg/vgpmnN6nCR
- **Email:** Tom.Hanke.Official@web.de
