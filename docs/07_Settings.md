# Project Settings

DataTable Pro Editor exposes customer-facing settings under:

`Edit → Project Settings → Plugins → DataTable Pro Editor`

## Large Table Row Warning Threshold

The large-table warning threshold controls when DataTable Pro Editor warns that the loaded DataTable contains a large number of rows.

- Default: `1000`
- Minimum: `100`

Lower values show the warning for smaller DataTables. This setting does not block loading or editing.

## Default Export As JSON

**Default Export As JSON** controls the initial format selected by the Diff export dialog.

- `false` — Diff export defaults to CSV
- `true` — Diff export defaults to JSON

This setting applies only to Diff export. The complete loaded DataTable exports to CSV, and an individual row can be copied as CSV.

## Column Layout Persistence

Column visibility and layout choices are stored per DataTable through the editor configuration used by the plugin.

Use **Show All** or **Reset Layout** in Browse when a saved layout no longer matches the preferred view. The **Row Name** column remains visible.

## Saving Settings

Project Settings are persisted through Unreal Engine's configuration workflow. The exact config file used in a source-controlled project depends on how the setting is changed and saved by the editor.

## Related Documentation

- [Quick Start and Browse Workflow](02_Browse.md)
- [Search, Find and Replace, Columns, and Navigation](04_Search_Filter_Sort.md)
- [Exports and Clipboard Data](06_Export.md)

Previous: [Exports and Clipboard Data](06_Export.md) · [Documentation Index](INDEX.md) · Next: [Changelog](08_Changelog.md)
