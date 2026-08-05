# DataTable Diff

Diff mode compares two compatible DataTables and reports row-level and field-level differences.

## Run a Comparison

1. Switch to **Diff** mode.
2. Select **Table A**.
3. Select **Table B**.
4. Start the comparison.

The two DataTables must be compatible for a meaningful field comparison.

## Result Types

| Result | Meaning |
|---|---|
| Added | The row exists in Table B but not Table A |
| Modified | The row exists in both tables and one or more fields differ |
| Removed | The row exists in Table A but not Table B |
| Unchanged | The row and compared fields match |

Modified rows include field-level differences with the values from Table A and Table B.

## Search and Filtering

Use the Diff search and filtering controls to narrow the result list. Unchanged rows can be included or excluded through the Diff controls.

Filtering changes the visible Diff results; it does not modify either DataTable.

## Navigate Back to Browse

Click a Diff result to return to the corresponding row in **Browse** mode.

The editor loads the relevant DataTable, selects the row, and scrolls it into view. This allows the difference to be reviewed or edited in the normal Browse workflow.

## Export Diff Results

Diff results can be exported to:

- CSV
- JSON

The default format used by the Diff export dialog is controlled by **Default Export As JSON** in Project Settings.

Complete DataTable JSON export is not part of this workflow. See [Exports and Clipboard Data](06_Export.md) for the full export matrix.

## Saving

Diff is a comparison workflow. Editing a DataTable after navigating back to Browse marks that DataTable dirty, but does not automatically save it.

Previous: [Search, Find and Replace, Columns, and Navigation](04_Search_Filter_Sort.md) · [Documentation Index](INDEX.md) · Next: [Exports and Clipboard Data](06_Export.md)
