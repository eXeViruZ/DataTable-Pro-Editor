# DataTable Pro Editor

**Version:** 1.0.0  
**Engine:** Unreal Engine 5.7  
**Author:** Tom Leon Vincent Hanke 
**Support:** https://discord.gg/vgpmnN6nCR  
**Docs:** https://github.com/eXeViruZ/DataTable-Pro-Editor/tree/main/docs

---

## Overview

DataTable Pro Editor is a project-wide DataTable editor built directly into Unreal Engine. It provides a single unified panel to browse, edit, and compare all DataTables in your project.

**Zero runtime overhead — Editor only.**

---

## Features

### Browse View
- View all DataTables in the project from one panel
- Inline row editing with full **Undo/Redo** support
- Type-aware cell widgets:
  - **Enums** → Dropdown (ComboBox)
  - **Booleans** → Checkbox
  - **Integers/Floats** → SpinBox (locale-invariant decimal formatting)
  - **Strings/Names/Text** → Editable text field
  - **Structs/Arrays/Maps** → Read-only display
- Add, Delete, Duplicate rows
- Search/filter rows by value
- Sort columns

### Diff View
- Compare any two DataTables side by side
- Color-coded change types: **Added**, **Modified**, **Removed**, **Unchanged**
- Shows exact field-level changes with **Value A** and **Value B**
- Filter diff results by row name or field name
- Export diff results to **CSV** or **JSON**
- Toggle visibility of unchanged rows

---

## Installation

1. Copy the `DataTableProEditor` plugin folder into your project's `Plugins/` directory
2. Restart the Unreal Editor
3. Enable the plugin via **Edit → Plugins → DataTable Pro Editor**
4. Open the panel via the toolbar button or **Window → DataTable Pro**

---

## Modules

| Module | Type | Description |
|---|---|---|
| `DataTableWorkflow` | EditorNoCommandlet | Core services: row loading, saving, diffing |
| `DataTableWorkflowEditor` | Editor | Slate UI: Browse panel, Diff view, window |

---

## Architecture

### Services (`DataTableWorkflow`)

| Class | Responsibility |
|---|---|
| `FDTPRowService` | Load/Save/Add/Delete/Duplicate/Filter/Sort rows |
| `FDTPDiffService` | Compare two DataTables, produce `FDTPDiffResult` |
| `FDTPAssetService` | Discover all DataTable assets in the project |

### UI (`DataTableWorkflowEditor`)

| Widget | Responsibility |
|---|---|
| `SDataTableProWindow` | Main window container |
| `SDataTableRowList` | Browse tab — table view with inline editing |
| `SDataTableDiffView` | Diff tab — side-by-side comparison |

---

## Known Blueprint Struct Behaviour

Blueprint-defined structs in Unreal Engine store properties with **internal GUID-suffixed names** (e.g. `Rarity_13_859092AD4F3CE...`) as their `FName`, while the human-readable name (e.g. `Rarity`) is stored as metadata via `GetAuthoredName()`.

DataTable Pro handles this transparently:
- **Browse View** uses `GetFName()` internally for stable property lookup and saving
- **Diff View** uses `GetAuthoredName()` for display so field names are always readable
- **Enum values** are resolved via `GetDisplayNameTextByValue()` in the Diff View

---

## Platforms

- Windows (Win64)
- Mac
- Linux
