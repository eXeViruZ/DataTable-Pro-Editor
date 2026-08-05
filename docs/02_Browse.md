# Quick Start and Browse Workflow

This page leads a new user from opening DataTable Pro Editor to editing and saving a DataTable.

## Quick Start

### 1. Open DataTable Pro Editor

Open:

`Window → DataTable Pro`

The dockable DataTable Pro panel opens with the project DataTable browser.

### 2. Select a DataTable

Select a DataTable in the project browser. The selected asset loads in **Browse** mode and its rows appear in the table.

### 3. Edit a Simple Property

1. Select a row.
2. Click a directly editable cell such as a String, Name, Text, integer, Float, Double, Boolean, or Enum property.
3. Enter or select the new value.
4. Confirm the edit.

The DataTable package is marked dirty. The asset is not automatically saved.

### 4. Edit a Complex Property

1. Locate a Struct, Array, Set, Map, Object Reference, Soft Object Reference, Class Reference, or Soft Class Reference column.
2. Use **Edit** for the target value.
3. Change the value through Unreal Engine's built-in property editor.
4. Confirm the property edit.

Complex values remain visible as compact previews in the main table.

### 5. Select Multiple Rows

- Use **Ctrl+Click** to add or remove individual rows from the selection.
- Use **Shift+Click** to select a continuous row range.

The selected-row counter updates with the current selection.

### 6. Paste Across Selected Rows

1. Click a data cell to establish the active cell and active column.
2. Select the target rows.
3. Copy a compatible value to the system clipboard.
4. Press **Ctrl+V**.

The value is applied to the active data column for the selected rows. The operation participates in Unreal Engine Undo/Redo transactions.

### 7. Save the DataTable

Save through Unreal Engine's normal workflow, for example with **Ctrl+S** or the editor's standard save commands.

## Project Browser

The project browser provides a project-wide list of DataTable assets. Select an entry to load it into Browse.

Use the browser search field to narrow the asset list by name. The large-table warning appears when the loaded row count exceeds the configured threshold.

## Browse and Diff Modes

- **Browse** is used to inspect, edit, add, duplicate, delete, rename, search, sort, and export DataTable rows.
- **Diff** is used to compare two compatible DataTables and inspect Added, Modified, Removed, and Unchanged rows.

Switch between the two modes through the visible **Browse** and **Diff** controls in the DataTable Pro panel.

## Manual Refresh

Use **Refresh** when the loaded DataTable or its source data changed outside the current DataTable Pro workflow. Refresh reloads the table view; save pending changes before refreshing when necessary.

## Expected Result

After completing the Quick Start, the chosen value is changed in the DataTable, the package is marked dirty, and the saved asset retains the change after reloading.

## Next Steps

- Review detailed editing and row operations in [Property Editing and Row Workflows](03_RowEditor.md).
- Learn search, replacement, columns, and navigation in [Search, Find and Replace, Columns, and Navigation](04_Search_Filter_Sort.md).
- See clipboard troubleshooting in [Troubleshooting, FAQ, and Limitations](09_Troubleshooting_And_FAQ.md).

Previous: [Installation](01_Installation.md) · [Documentation Index](INDEX.md) · Next: [Property Editing and Row Workflows](03_RowEditor.md)
