# Asset Browser

**Copyright (c) 2026 Tom Hanke Leon Vincent. All Rights Reserved.**

---

## Overview

The left panel of DataTable Pro is a **project-wide asset browser** that automatically lists every `UDataTable` asset in your project.

No configuration required — the list is built at startup using the Asset Registry and updates automatically when tables are added, removed, or renamed.

---

## Browser Columns

| Column | Description |
|--------|-------------|
| **Asset Name** | The name of the DataTable asset |
| **Row Struct** | The name of the row struct type (e.g. `FItemTableRow`) |
| **Row Count** | The number of rows in the table. Shows `-` if not yet loaded |

---

## Searching the Asset List

A **search bar** at the top of the browser filters the asset list in real time.

- Type any part of the asset name to filter
- Matching text is **highlighted** in the results
- Clear the search box to show all tables again

---

## Loading a Table

Click any row in the browser to load that DataTable into the **Row Editor** (right panel).

- The table loads instantly from the Asset Registry
- The row count in the browser column is updated on first load
- A large-table warning is shown if the row count exceeds the configured threshold (see [Settings](./07_Settings.md))

---

## Auto-Refresh

The browser listens to the Asset Registry for changes. It refreshes automatically when:

- A new DataTable is created in the project
- An existing DataTable is deleted or renamed
- A DataTable is imported from CSV

No manual refresh button is needed.

---

## Support

- **Discord:** https://discord.gg/vgpmnN6nCR
- **Email:** Tom.Hanke.Official@web.de
