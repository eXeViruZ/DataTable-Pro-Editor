# DataTable Diff

**Copyright (c) 2026 Tom Hanke Leon Vincent. All Rights Reserved.**

---

## Overview

The **Diff tab** lets you compare any two DataTables in your project side by side. Results are shown in a color-coded list with per-field detail for modified rows.

---

## Running a Diff

1. Switch to the **Diff** tab (top of the right panel)
2. Select **Table A** from the left dropdown
3. Select **Table B** from the right dropdown
4. Press **Compare**
5. Results appear instantly

---

## Color Coding

| Color | Label | Meaning |
|-------|-------|---------|
| Green | `+ Added` | Row exists in Table B only |
| Yellow | `~ Modified` | Row exists in both, but one or more fields differ |
| Red | `- Removed` | Row exists in Table A only |
| (none) | `Unchanged` | Row is identical in both tables (hidden by default) |

---

## Diff Result Columns

| Column | Description |
|--------|-------------|
| **Change** | The delta type: Added, Modified, Removed, Unchanged |
| **Row Name** | The name of the affected row |
| **Field** | The specific field that changed (Modified rows only) |
| **Value A** | The field value in Table A |
| **Value B** | The field value in Table B |

For **Modified** rows, one line is shown per changed field.  
For **Added** and **Removed** rows, a single summary line is shown.

---

## Blueprint Struct Support

DataTable Pro fully supports DataTables that use **Blueprint-defined row structs**.

- **Field names** are always shown as their readable authored names (e.g. `Rarity`, `SellPrice`) — never as internal GUID-suffixed names (e.g. `Rarity_13_859092AD...`)
- **Enum values** are resolved to their display names (e.g. `Rare`, `Uncommon`) — never as internal enumerator names (e.g. `NewEnumerator0`)

---

## Summary Bar

Above the results, a summary shows at a glance:

```
X Added   Y Modified   Z Removed
```

---

## Diff Search

The **search bar** below the summary filters diff results in real time.

- Matches against **Row Name** and **Field Name**
- Case-insensitive
- Example: type `Health` to show only rows/fields containing "Health"

---

## Show Unchanged

By default, unchanged rows are hidden. Enable the **Show Unchanged** checkbox to include them.

---

## Navigate to Row

Click any diff row to **jump to that row in the Browse tab**:

1. The Browse tab is activated
2. The correct DataTable is loaded (Table A or B depending on delta type)
3. The row is selected and scrolled into view
4. Any active search filter is cleared automatically

| Delta Type | Table Loaded |
|------------|--------------|
| Added | Table B |
| Removed | Table A |
| Modified | Table A |

---

## Struct Mismatch Warning

If Table A and Table B use **different row structs**, a warning is shown. The diff still runs on fields common to both structs.

---

## Support

- **Discord:** https://discord.gg/vgpmnN6nCR
- **Email:** Tom.Hanke.Official@web.de
