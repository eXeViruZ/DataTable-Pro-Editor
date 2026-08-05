# DataTable Pro Editor Changelog

This page records the public version history. Version 1.1.0 is compared with the immediately previous public version, 1.0.1.

## 1.1.0

**Engine:** Unreal Engine 5.8  
**Release Type:** Minor Release  
**Previous Public Version:** 1.0.1

### Release Summary

Version 1.1.0 expands DataTable Pro Editor with complex property editing, multi-row workflows, table-wide Find and Replace, persistent column management, navigation and clipboard tools, and a clearer export workflow.

### Added

- Added editing for Structs, Arrays, Sets, Maps, Object References, Soft Object References, Class References, and Soft Class References through Unreal Engine's built-in property editor.
- Added compact table previews for complex values.
- Added multi-row selection with **Ctrl+Click** and **Shift+Click**.
- Added multi-row duplication and deletion, including confirmation before deleting more than one row.
- Added **Ctrl+V** paste into the active data column across selected rows.
- Added table-wide Find and Replace with Match Case, previous/next navigation, Replace, Replace All, all-column search, and selected-column search.
- Added individual column visibility controls, **Show All**, **Reset Layout**, and per-DataTable layout persistence.
- Added **Jump to Row** with **Ctrl+G**.
- Added **Copy Row Name**, **Copy Cell Value**, **Copy Row as CSV**, manual **Refresh**, and displayed-row and selected-row counters.
- Added complete loaded DataTable export to CSV.

### Improved

- Improved row workflows with keyboard shortcuts for add, duplicate, delete, rename, copy, paste, Undo, Redo, Find, navigation, and standard Unreal Engine saving.
- Improved Diff-to-Browse navigation by returning to the corresponding row from a Diff result.
- Improved complex-property readability through compact previews while keeping editing in the built-in property editor.

### Fixed

- Fixed integer columns displaying unnecessary decimal places while preserving decimal formatting for Float and Double.
- Fixed `int64` and `uint64` columns using the generic integer type badge instead of the `int64` badge.

### Compatibility

- Supports Unreal Engine 5.8 for version 1.1.0.
- Editor-only C++ plugin with no runtime gameplay dependency or runtime overhead.
- Supported platforms: Win64, Linux, Mac.
- No Blueprint modification required.
- No external third-party dependencies.

### Documentation

- Updated README, installation, Quick Start, Browse, row editing, Find and Replace, Diff, export, settings, troubleshooting, FAQ, navigation, and public version history for v1.1.0.

### Known Limitations

- Complete DataTable JSON export is not available.
- Individual-row JSON export is not available.
- Property support is documented by workflow and does not claim every Unreal Engine property type.

## 1.0.1

**Release Type:** Maintenance Release

Version 1.0.1 is retained as the previous public comparison version. Detailed public release notes were not present in the repository documentation before this v1.1.0 documentation update, so no unverified changes are listed here.

## 1.0.0 — 2026-04-15

**Release Type:** Initial Release

### Release Summary

Initial public documentation for the project-wide DataTable Browse and Diff workflows.

### Added

- Added a project-wide DataTable browser.
- Added inline editing for the initially supported simple property workflows.
- Added row add, duplicate, delete, and rename workflows.
- Added search, filtering, and sorting.
- Added compatible DataTable comparison with Added, Modified, Removed, and Unchanged results.
- Added field-level Diff details.
- Added Diff export to CSV and JSON.
- Added Unreal Engine transaction support for documented editing operations.

### Compatibility

- Initial documentation targeted Unreal Engine 5.7.
- Editor-only plugin.

Previous: [Project Settings](07_Settings.md) · [Documentation Index](INDEX.md) · Next: [Troubleshooting, FAQ, and Limitations](09_Troubleshooting_And_FAQ.md)
