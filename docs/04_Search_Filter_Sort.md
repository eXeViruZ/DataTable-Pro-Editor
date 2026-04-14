# Search, Filter & Sort

**Copyright (c) 2026 Tom Hanke Leon Vincent. All Rights Reserved.**

---

## Row Search

The **search bar** above the row list filters rows in real time as you type.

- Matches against **all columns** by default
- Case-insensitive
- Clears instantly when the search box is emptied

---

## Column Filter

Next to the search bar is a **column filter dropdown**.

| Selection | Behavior |
|-----------|----------|
| **All Columns** (default) | Search text is matched against every field in each row |
| **Row Name** | Search is restricted to the row name only |
| **[Column Name]** | Search is restricted to that specific column |

Example: Column = `ItemType`, Text = `Weapon` → shows only rows where `ItemType` contains "Weapon".

---

## Column Sorting

Click any **column header** to sort the row list by that column.

| Click | Result |
|-------|--------|
| 1st click | Ascending (A→Z, 0→9) |
| 2nd click | Descending (Z→A, 9→0) |
| 3rd click | Reset to original table order |

### Numeric Sorting

Columns with numeric types (`int32`, `int64`, `float`, `double`) sort **numerically**, not lexicographically.

> Example: `1, 2, 9, 10, 11` — correct numeric order instead of `1, 10, 11, 2, 9`.

---

## Scroll To Row

When navigating from the **Diff tab** to a specific row:

1. The Browse tab is automatically activated
2. The correct DataTable is loaded
3. If a search filter is active, it is **automatically cleared**
4. The list scrolls to the row and selects it

---

## Support

- **Discord:** https://discord.gg/vgpmnN6nCR
- **Email:** Tom.Hanke.Official@web.de
