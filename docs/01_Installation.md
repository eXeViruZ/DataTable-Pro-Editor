# Installation

This page explains how to install and enable DataTable Pro Editor v1.1.0 for Unreal Engine 5.8.

## Requirements

- Unreal Engine 5.8
- A project that uses Unreal Engine DataTables
- Win64, Linux, or Mac editor
- No runtime setup
- No Blueprint modification
- No external third-party dependency

DataTable Pro Editor v1.1.0 is distributed as an Unreal Engine 5.8 package. Older UE 5.7-compatible releases do not include the v1.1.0 features described in this documentation.

## Install from Fab

1. Acquire **DataTable Pro Editor** from the [Fab listing](https://www.fab.com/listings/1021a6d3-16de-4a89-a2af-981c89f36b18).
2. Open the **Epic Games Launcher**.
3. Open your Fab Library and locate **DataTable Pro Editor**.
4. Install the Unreal Engine 5.8 package to the engine or add it to the target project, depending on the launcher option shown.
5. Open the project in Unreal Engine 5.8.
6. Open **Edit → Plugins**.
7. Search for **DataTable Pro Editor** and enable the plugin.
8. Restart the Unreal Editor when prompted.

## Install a Manually Supplied Package

Use these steps only when you received an authorized plugin package outside the launcher workflow.

1. Close the Unreal Editor.
2. Copy the plugin folder into the project's `Plugins/` directory.
3. Reopen the project in Unreal Engine 5.8.
4. Enable **DataTable Pro Editor** under **Edit → Plugins**.
5. Restart the editor when prompted.

No game module, Actor, Component, Blueprint, input mapping, or Project Settings setup is required.

## Open the Editor

Open the dockable panel from:

`Window → DataTable Pro`

The panel can be docked like other Unreal Editor tabs.

## Verify the Installation

The installation is successful when:

- **Window → DataTable Pro** is available.
- The DataTable Pro panel opens without a plugin load error.
- The project browser lists DataTable assets from the project.

## Update the Plugin

1. Close the Unreal Editor.
2. Install or replace the plugin with the package for the target Unreal Engine version.
3. Reopen the project.
4. Confirm that the plugin is enabled.
5. Review the [Changelog](08_Changelog.md) for version-specific behavior.

Do not use the UE 5.7 package when following the v1.1.0 documentation.

## Remove the Plugin

1. Disable **DataTable Pro Editor** under **Edit → Plugins**.
2. Restart the editor when prompted.
3. Remove the plugin package only after the project has closed.

Because the plugin is editor-only, removal does not remove a required runtime gameplay system.

## Support

- [Discord Support and Community](https://discord.gg/vgpmnN6nCR)
- [Email Support](mailto:Tom.Hanke.Official@web.de)

[Documentation Index](INDEX.md) · Next: [Quick Start and Browse Workflow](02_Browse.md)
