# Exports and Clipboard Data

DataTable Pro Editor provides different output formats depending on whether the source is the complete loaded DataTable, an individual row, or Diff results.

## Export Matrix

| Source | CSV | JSON | Destination |
|---|---:|---:|---|
| Complete loaded DataTable | Yes | No | File |
| Individual row | Yes | No | Clipboard through **Copy Row as CSV** |
| Diff results | Yes | Yes | File |

## Export the Complete Loaded DataTable

1. Load the target DataTable in **Browse** mode.
2. Use **Export CSV**.
3. Choose a file name and location.
4. Save the CSV file.

The export includes the complete loaded DataTable. A complete DataTable JSON export is not available.

## Copy an Individual Row as CSV

1. Select the target row.
2. Open the row context menu.
3. Choose **Copy Row as CSV**.
4. Paste the clipboard content into the target application.

Individual-row JSON output is not available.

## Copy Row Name or Cell Value

The row context menu also provides:

- **Copy Row Name**
- **Copy Cell Value**

Press **Ctrl+C** to copy the active cell value.

## Export Diff Results

1. Run a comparison in **Diff** mode.
2. Apply Diff search or filtering when needed.
3. Use **Export...**.
4. Choose CSV or JSON.
5. Save the file.

Diff export follows the current Diff result scope shown by the Diff workflow.

## Default Diff Export Format

Open:

`Edit → Project Settings → Plugins → DataTable Pro Editor`

Use **Default Export As JSON** to choose whether the Diff export dialog defaults to JSON instead of CSV.

This setting applies to Diff export. It does not add JSON export for the complete DataTable or an individual row.

## Clipboard Paste Is Not an Export

**Ctrl+V** imports a compatible clipboard value into the active data column across selected rows. It requires:

- at least one selected row
- an active data cell and active data column
- clipboard content compatible with the destination property type

See [Troubleshooting, FAQ, and Limitations](09_Troubleshooting_And_FAQ.md) when paste is rejected.

Previous: [DataTable Diff](05_Diff.md) · [Documentation Index](INDEX.md) · Next: [Project Settings](07_Settings.md)
