# Search, Find and Replace, Columns, and Navigation

This page covers row filtering, table-wide Find and Replace, sorting, column layouts, Jump to Row, refresh, and row counters.

## Browse Search and Filtering

The Browse search field filters the displayed rows as you type.

- Search across **All Columns** or choose a specific column.
- Clear the search field to restore the full displayed result set.
- Filtering changes what is displayed; it does not remove rows from the loaded DataTable.

## Find and Replace

Press **Ctrl+F** to open Find and Replace for the loaded DataTable.

Available controls include:

- **Match Case**
- **Previous**
- **Next**
- **Replace**
- **Replace All**
- Search across all columns or a selected column

Keyboard navigation:

- **F3** — next result
- **Shift+F3** — previous result

Find and Replace operates across the loaded DataTable, including rows currently hidden by Browse search or filtering. Review the selected column and replacement text before using **Replace All**.

## Column Sorting

Click a sortable column header to change the displayed order.

Numeric columns sort by numeric value. Text-based columns sort by their displayed text. Sorting changes the view and does not rewrite the underlying DataTable row order unless a separate documented operation explicitly does so.

## Column Management

Open the column controls to manage the current Browse layout.

- Toggle individual data columns.
- Use **Show All** to make every data column visible.
- Use **Reset Layout** to restore the default layout.
- Column layout is persisted separately for each DataTable.
- The **Row Name** column always remains visible.

## Jump to Row

Press **Ctrl+G** to open Jump to Row.

1. Enter the target Row Name.
2. Confirm the request.
3. Browse selects the matching row and scrolls it into view.

Diff result navigation also returns to Browse and selects the corresponding row.

## Manual Refresh

Use **Refresh** to reload the current DataTable view when external changes are not yet represented in the panel. Save pending edits before refreshing when necessary.

## Row Counters

Browse displays:

- the number of rows currently displayed after search or filtering
- the number of currently selected rows

Use these counters to verify the target scope before multi-row duplication, deletion, or paste.

## Related Shortcuts

| Shortcut | Action |
|---|---|
| Ctrl+F | Open Find and Replace |
| F3 | Find next |
| Shift+F3 | Find previous |
| Ctrl+G | Jump to Row |

Previous: [Property Editing and Row Workflows](03_RowEditor.md) · [Documentation Index](INDEX.md) · Next: [DataTable Diff](05_Diff.md)
