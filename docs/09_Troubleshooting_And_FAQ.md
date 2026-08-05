# Troubleshooting, FAQ, and Limitations

This page covers common v1.1.0 usage problems, frequently asked questions, and confirmed product boundaries.

## Ctrl+V Does Not Change Any Rows

### Symptom

Pressing **Ctrl+V** does not update the expected cells.

### Likely Causes

- No rows are selected.
- No data cell is active.
- The active column is **Row Name** instead of a data column.
- Clipboard content is not compatible with the destination property type.

### Resolution

1. Select one or more target rows.
2. Click a cell in the destination data column.
3. Copy a value that is valid for that property type.
4. Press **Ctrl+V**.
5. Check the selected-row counter and the active column before retrying.

### Expected Result

The compatible value is applied to the active column across the selected rows as one transaction.

## Clipboard Content Is Rejected

Clipboard text must be compatible with the destination property type. For example, a numeric destination requires a valid numeric value, and an Enum destination requires a value the property importer can resolve.

Use the normal inline or built-in property editor when a clipboard representation is unclear.

## A Complex Property Is Not Editable Inline

Structs, Arrays, Sets, Maps, Object References, Soft Object References, Class References, and Soft Class References use Unreal Engine's built-in property editor.

Use **Edit** for the target value. The main table shows a compact preview rather than the full editing interface.

## Changes Disappear After Reopening the Project

DataTable Pro Editor marks modified DataTables dirty but does not automatically save them.

Use Unreal Engine's normal save workflow, such as **Ctrl+S**, before closing the editor or project.

## Undo After Deleting Multiple Rows

Multi-row deletion uses an Unreal Engine transaction. **Ctrl+Z** restores all rows deleted by that transaction.

When checking the result, clear filters or search text that could hide restored rows.

## Complete DataTable JSON Export

Complete DataTable JSON export is not available in v1.1.0.

Available outputs are:

- complete loaded DataTable to CSV
- individual row copied as CSV
- Diff results exported to CSV or JSON

## Version Compatibility

DataTable Pro Editor v1.1.0 supports Unreal Engine 5.8.

Older UE 5.7-compatible releases do not contain the new v1.1.0 workflows documented here.

## The Row I Need Is Hidden

- Clear Browse search or filtering.
- Use **Ctrl+G** to open Jump to Row.
- Check individual column visibility only when the row is visible but the required field is hidden.
- Use **Show All** or **Reset Layout** to restore columns.

Find and Replace still searches the loaded DataTable, including rows hidden by Browse search or filtering.

## Diff Does Not Produce a Useful Comparison

Confirm that Table A and Table B are compatible DataTables with the expected row structure. Diff is intended for compatible tables.

## Known Limitations

- Complete DataTable JSON export is not available.
- Individual-row JSON export is not available.
- Complex values are edited through the built-in property editor rather than directly inline.
- Changes require manual saving through Unreal Engine.
- Property support is documented by supported workflows and examples; it is not described as universal support for every Unreal Engine property type.
- Version 1.1.0 is packaged for Unreal Engine 5.8.

## Still Not Working?

Provide the following information through Discord or email:

- DataTable Pro Editor version
- Unreal Engine version
- operating system
- the affected DataTable row struct
- exact reproduction steps
- screenshots of the panel and any notification
- whether the issue remains after reopening the editor

Support:

- [Discord Support and Community](https://discord.gg/vgpmnN6nCR)
- [Email Support](mailto:Tom.Hanke.Official@web.de)

Previous: [Changelog](08_Changelog.md) · [Documentation Index](INDEX.md) · [Repository README](../README.md)
