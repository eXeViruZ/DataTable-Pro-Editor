# Row Editor

**Copyright (c) 2026 Tom Hanke Leon Vincent. All Rights Reserved.**

---

## Overview

The Row Editor displays the rows of the selected DataTable as a **multi-column list**. Columns are built **dynamically** from the row struct — no manual setup is required.

---

## Supported Field Types

| Type | Editor Control |
|------|----------------|
| `FString`, `FName`, `FText` | Inline text input |
| `int32`, `int64`, `uint8`, etc. | Inline numeric text input |
| `float`, `double` | Inline numeric text input |
| `bool` | Checkbox |
| Enums (`UENUM`) | Dropdown with all enum values |
| Structs, Arrays, Maps, Sets | Read-only display (full value shown as tooltip) |

---

## Editing a Field

1. Click a row in the list to select it
2. Click the cell you want to edit
3. Type the new value and press **Enter** or click away to confirm
4. The change is saved to the DataTable immediately
5. Use **Ctrl+Z** to undo, **Ctrl+Y** to redo

> All edits use Unreal's `FScopedTransaction` — full Undo/Redo is guaranteed.

---

## Adding a Row

1. Click **+ Add Row** in the toolbar
2. A new row is added with a unique auto-generated name (e.g. `NewRow_1`, `NewRow_2`, ...)
3. All fields are initialized to their default values

---

## Duplicating a Row

1. Select a row by clicking it
2. Click **Duplicate** in the toolbar
3. A deep copy of the selected row is added with a new unique name

---

## Deleting a Row

1. Select a row by clicking it
2. Click **Delete** in the toolbar
3. The row is removed immediately (undoable via Ctrl+Z)

---

## Renaming a Row

1. Double-click the **Row Name** cell of any row
2. Type the new name and press **Enter** to confirm
3. The row is renamed in place — all data is preserved

> Row names must be unique. If the name already exists, the rename is rejected.

---

## Undo / Redo

All operations (edit, add, delete, duplicate, rename) are fully undoable:

- **Ctrl+Z** — Undo
- **Ctrl+Y** — Redo

The row list refreshes automatically after every Undo/Redo.

---

## Support

- **Discord:** https://discord.gg/vgpmnN6nCR
- **Email:** Tom.Hanke.Official@web.de
