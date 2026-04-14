# Installation

**Copyright (c) 2026 Tom Hanke Leon Vincent. All Rights Reserved.**

---

## Requirements

- Unreal Engine **5.7**
- Windows (Editor)
- A C++ or Blueprint project (both supported)

---

## Installing from FAB

1. Purchase **DataTable Pro Editor** on FAB
2. Open the **Epic Games Launcher**
3. Go to **Library → FAB Library**
4. Find *DataTable Pro Editor* and click **Install to Engine** or **Add to Project**
5. Open your project in Unreal Engine 5.7
6. Go to **Edit → Plugins**
7. Search for `DataTable Pro` and ensure it is **enabled** (checkbox checked)
8. Restart the editor when prompted

---

## Manual Installation

1. Copy the `DataTablePro` folder into your project's `Plugins/` directory:
   ```
   YourProject/
   └── Plugins/
       └── DataTablePro/
           ├── DataTablePro.uplugin
           └── Source/
   ```
2. Right-click your `.uproject` file and select **Generate Visual Studio project files**
3. Open the solution and **Build** the project
4. Launch the editor — the plugin loads automatically

---

## Opening the Panel

After installation, open the plugin via:

```
Unreal Editor → Window → DataTable Pro
```

The panel is a **Nomad Tab** — it can be docked anywhere in the editor layout like any native Unreal panel.

---

## Verifying the Installation

If the plugin is correctly installed:
- **Window → DataTable Pro** appears in the menu
- The panel opens and shows your project's DataTables in the left browser
- The status bar shows no plugin errors

---

## Support

- **Discord:** https://discord.gg/vgpmnN6nCR
- **Email:** Tom.Hanke.Official@web.de
