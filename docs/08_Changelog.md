# Changelog

**Copyright (c) 2026 Tom Hanke Leon Vincent. All Rights Reserved.**

---

## [1.0.0] — 2026

Initial release.

### Browse
- Project-wide DataTable asset browser (Asset Name, Row Struct, Row Count)
- Live asset search with text highlight
- Auto-refresh via Asset Registry delegates

### Row Editor
- Dynamic column generation from row struct
- Inline editing: strings, integers, floats, booleans, enums
- Read-only display with tooltip for complex types (structs, arrays, maps)
- Add Row, Duplicate Row, Delete Row with unique name generation
- Row renaming via double-click
- Full Undo/Redo via `FScopedTransaction`

### Search, Filter & Sort
- Real-time row search across all columns or a specific column
- Column filter dropdown
- Column header sorting: ascending / descending / reset
- Numeric sort for int/float/double columns
- Scroll-to-row with automatic search filter clear

### Diff
- Side-by-side diff for any two DataTables
- Color-coded results: Added (green), Modified (yellow), Removed (red)
- Per-field diff detail for Modified rows
- Summary bar: Added / Modified / Removed counts
- Real-time diff search (row name and field name)
- Show Unchanged toggle
- Click-to-navigate: jump from diff result to Browse tab with row selected
- Struct mismatch warning with graceful fallback on common fields

### Export
- Export diff to CSV or JSON
- JSON via `TJsonWriter` (correct escaping of all special characters)
- Export respects active filter
- Configurable default format in Project Settings

### Technical
- Editor-only plugin (zero runtime overhead)
- Dockable Nomad Tab
- `UDeveloperSettings` integration
- Compatible with Unreal Engine 5.7

---

## Support

- **Discord:** https://discord.gg/vgpmnN6nCR
- **Email:** Tom.Hanke.Official@web.de
