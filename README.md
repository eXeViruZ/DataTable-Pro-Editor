# DataTable Pro Editor

DataTable Pro Editor provides a project-wide Unreal Engine panel for browsing, editing, comparing, and exporting DataTables without opening each asset separately. Version 1.1.0 expands the editor with complex property editing, multi-row workflows, table-wide Find and Replace, persistent column layouts, navigation tools, and a clearer CSV/JSON export workflow.

| Product | Details |
|---|---|
| Version | 1.1.0 |
| Unreal Engine | 5.8 |
| Plugin Type | Editor-only C++ plugin |
| Supported Platforms | Win64, Linux, Mac |
| Runtime | No runtime gameplay dependency or runtime overhead |
| Blueprint Setup | No Blueprint modification required |
| Third-party Dependencies | None |

## Main Features

- Edit `String`, `Name`, `Text`, integer, `Float`, `Double`, `Boolean`, and `Enum` values directly in the table.
- Edit Structs, Arrays, Sets, Maps, Object References, Soft Object References, Class References, and Soft Class References through Unreal Engine's built-in property editor.
- Select multiple rows with **Ctrl+Click** or **Shift+Click**, then duplicate, delete, or paste compatible values across the selection.
- Use table-wide **Find and Replace** with Match Case, column targeting, previous/next navigation, Replace, and Replace All.
- Control individual column visibility, restore all columns, reset the layout, and keep a separate layout for each DataTable.
- Compare compatible DataTables with Added, Modified, Removed, and Unchanged results plus field-level differences.
- Export the complete loaded DataTable to CSV, copy an individual row as CSV, and export Diff results to CSV or JSON.
- Use keyboard navigation and clipboard workflows including **Ctrl+F**, **F3**, **Shift+F3**, **Ctrl+G**, **F2**, **Ctrl+C**, **Ctrl+V**, **Ctrl+Z**, and **Ctrl+Y**.

Complex values use compact table previews. The plugin does not claim support for every Unreal Engine property type.

## Quick Start

1. Install and enable the plugin for Unreal Engine 5.8.
2. Open **Window → DataTable Pro**.
3. Select a DataTable in the project browser.
4. Edit a simple value directly in the table, or use **Edit** for a complex property.
5. Select multiple rows and press **Ctrl+V** to paste a compatible clipboard value into the active data column.
6. Save the modified DataTable through Unreal Engine's normal save workflow, such as **Ctrl+S**.

Read the full [Quick Start and Browse Workflow](docs/02_Browse.md) for the complete first-use sequence.

## Documentation

- [Documentation Index](docs/INDEX.md)
- [Installation](docs/01_Installation.md)
- [Quick Start and Browse Workflow](docs/02_Browse.md)
- [Property Editing and Row Workflows](docs/03_RowEditor.md)
- [Search, Find and Replace, Columns, and Navigation](docs/04_Search_Filter_Sort.md)
- [DataTable Diff](docs/05_Diff.md)
- [Exports and Clipboard Data](docs/06_Export.md)
- [Project Settings](docs/07_Settings.md)
- [Changelog](docs/08_Changelog.md)
- [Troubleshooting, FAQ, and Limitations](docs/09_Troubleshooting_And_FAQ.md)

## Product Links

- [Fab Listing](https://www.fab.com/listings/1021a6d3-16de-4a89-a2af-981c89f36b18)
- [Selected Workflow Video](https://youtu.be/QIXhvCRBN_Y)
- [Older Product Overview Video](https://youtu.be/h22nwkMBxDY)

## Support

Discord is the primary channel for support, bug reports, and feature requests.

- [Hanke Unreal Tools Discord](https://discord.gg/vgpmnN6nCR)
- [Email Support](mailto:Tom.Hanke.Official@web.de)

## Copyright

Copyright © 2026 Tom Leon Vincent Hanke. All rights reserved.
