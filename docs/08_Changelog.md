# Changelog — DataTable Pro Editor

All notable changes to this project are documented here.

---

## [1.0.0] — 2026-04-15

### Features

- Browse View: project-wide DataTable browser with inline editing
- Diff View: side-by-side DataTable comparison
- Type-aware cell widgets: Enum dropdowns, Bool checkboxes, Numeric spinboxes
- Full Undo/Redo support via `FScopedTransaction`
- Add, Delete, Duplicate rows
- Search, filter, sort
- Export Diff to CSV and JSON
- Locale-invariant float/double formatting (`FString::SanitizeFloat`)

### Fixed

#### Diff View — Field names showed internal GUID-suffixed names
- **Problem:** Blueprint struct properties have internal names like `Rarity_13_859092AD4F3CE...` as their `FName`. `DTPDiffService::ExportRow` used `It->GetFName()` as the map key, causing the Diff View **Field** column to display GUID-suffixed names instead of readable names like `Rarity`.
- **Fix:** Changed `ExportRow` to use `FName(*It->GetAuthoredName())` as the map key.
- **File:** `DTPDiffService.cpp`

#### Diff View — Enum values showed `NewEnumerator0` instead of display names
- **Problem:** Blueprint-defined enums have auto-generated internal enumerator names (e.g. `NewEnumerator0`). The generic `ExportTextItem_Direct` fallback exported these internal names instead of the readable display names.
- **Fix:** Added explicit `FByteProperty` (TEnumAsByte) and `FEnumProperty` branches in `ExportRow` that call `UEnum::GetDisplayNameTextByValue()` to resolve the human-readable name.
- **File:** `DTPDiffService.cpp`
- **Required include:** `#include "UObject/EnumProperty.h"`

#### Browse View — Bool checkboxes and Enum dropdowns disappeared after column key change
- **Problem:** `BuildColumnMetaFromStruct` in `SDataTableRowList` used `It->GetFName()` to populate `BoolColumns`, `EnumOptionsMap`, `IntColumns` etc. After column keys were switched to `GetAuthoredName()`, the meta lookup no longer matched — causing Bool checkboxes, Enum dropdowns, and numeric spinboxes to disappear.
- **Fix:** Changed `const FName PropName = It->GetFName()` to `const FName PropName = FName(*It->GetAuthoredName())` in `BuildColumnMetaFromStruct` and the header label resolution loop.
- **File:** `SDataTableRowList.cpp`
