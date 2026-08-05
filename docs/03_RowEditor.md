# Property Editing and Row Workflows

Browse mode displays the loaded DataTable as a multi-column editor. Columns are generated from the DataTable row struct.

## Property Editing

### Direct Inline Editing

The following property groups are edited directly in the table:

| Property Group | Editing Workflow |
|---|---|
| String, Name, Text | Inline text editing |
| Integer types | Inline numeric editing |
| Float, Double | Inline numeric editing with decimal formatting |
| Boolean | Checkbox |
| Enum | Enum selection control |

Integer columns display integer values without unnecessary decimal places. Float and Double columns retain decimal formatting. `int64` and `uint64` columns use the `int64` type badge. Full signed `int64` boundary values were tested through editing, saving, and reloading.

### Built-in Property Editor

The following property groups use Unreal Engine's built-in property editor through **Edit**:

- Struct
- Array
- Set
- Map
- Object Reference
- Soft Object Reference
- Class Reference
- Soft Class Reference

Struct examples include Gameplay Tags, Gameplay Tag Containers, Vector, Vector2D, Rotator, Transform, Linear Color, and Color.

Complex values show compact previews in the table. Property support depends on the property's compatibility with the provided editor workflow; the plugin does not claim support for every Unreal Engine property type.

## Row Selection

- **Click** selects a row.
- **Ctrl+Click** adds or removes individual rows.
- **Shift+Click** selects a continuous range.

The interface shows displayed-row and selected-row counters.

## Active Cell and Active Column

Several clipboard actions depend on the active cell:

1. Click a cell in a data column.
2. The clicked cell becomes the active cell.
3. Its column becomes the active column.
4. **Ctrl+C** copies the active cell value.
5. **Ctrl+V** targets the active column across the selected rows.

The **Row Name** column is not a valid destination for multi-row value paste.

## Row Actions

### Add Row

Use **Add Row** or press **Ctrl+N**. A new row is created with a unique row name and default property values.

### Duplicate Rows

1. Select one or more rows.
2. Use **Duplicate** or press **Ctrl+D**.

Each selected row is duplicated. Multi-row duplication is handled through an Unreal Engine transaction and supports Undo/Redo.

### Delete Rows

1. Select one or more rows.
2. Use **Delete** or press the **Delete** key.
3. Confirm the action when deleting more than one row.

Multi-row deletion supports Undo/Redo. Undo restores all rows deleted by the transaction.

### Rename a Row

1. Select the target row.
2. Focus the **Row Name** cell.
3. Press **F2**.
4. Enter a unique row name and confirm.

Row names must remain unique.

## Clipboard Actions

The row context menu provides:

- **Copy Row Name**
- **Copy Cell Value**
- **Copy Row as CSV**

Keyboard actions include:

- **Ctrl+C** — copy the active cell value
- **Ctrl+V** — paste a compatible value to the active column across selected rows

See [Exports and Clipboard Data](06_Export.md) for format scope.

## Undo, Redo, and Saving

- **Ctrl+Z** — Undo
- **Ctrl+Y** — Redo
- **Ctrl+S** — Unreal Engine's normal save behavior

Editing, multi-row paste, multi-row duplication, and multi-row deletion use Unreal Engine transactions.

Modified DataTables are marked dirty. Changes are not automatically saved. Save through Unreal Engine's normal save workflow.

## Important Shortcuts

| Shortcut | Action |
|---|---|
| Ctrl+N | Add Row |
| Ctrl+D | Duplicate selected row or rows |
| Delete | Delete selected row or rows |
| F2 | Rename the selected Row Name |
| Ctrl+C | Copy active cell value |
| Ctrl+V | Paste to selected rows in the active column |
| Ctrl+Z | Undo |
| Ctrl+Y | Redo |
| Ctrl+S | Use Unreal Engine save behavior |

Previous: [Quick Start and Browse Workflow](02_Browse.md) · [Documentation Index](INDEX.md) · Next: [Search, Find and Replace, Columns, and Navigation](04_Search_Filter_Sort.md)
