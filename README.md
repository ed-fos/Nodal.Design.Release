# Nodal.Design - Revit Add-in

A free Revit add-in suite for BIM and VDC professionals. Version 1.1.1 ships with six tools, with many more on the way.

---

## What's New in v1.1.1

- Added support for Revit 2022 and 2023.

---

## Panels & Tools

### Conduits

Tools for conduit layout and bending.

#### Conduit Offset
Generates a parallel offset run from a selected conduit, automatically inserting the appropriate kick bends to connect the two elevations.

#### Conduit Kick 90
Draws a 90° kicked conduit segment from a selected conduit end, calculating the correct bend geometry based on conduit size and offset distance.

---

### Power Tools

General-purpose tools that work across disciplines — conduit, cable tray, pipe, duct, and more.

#### Power Knife
Slice or remove sections of Conduits, Cable Trays, Pipes, Ducts, and Lines by dragging a selection rectangle.

- **Fully enclosed** segments are deleted.
- **Crossing** segments are trimmed to the box boundary.
- No fittings or couplings are inserted.
- Works in Plan, RCP, Elevation, Section, and 3D Orthographic views.
- Detects overlapping elements at different elevations and prompts for resolution.

Open Settings to configure which categories are affected (e.g., exclude Pipes from cuts).

#### Power Connect
Connects two elements by powering a connection between their open connectors. Works across MEP disciplines wherever Revit connector logic applies.

#### Power Disconnect
Disconnects two connected elements. The inverse operation of Power Connect — cleanly severs the connector relationship without deleting either element.

#### Parallelize
Rotates one or more target elements to match the orientation of a reference element, constrained to the active view plane.

- Pre-select two elements to run instantly, or pick interactively.
- Works across disciplines on any rotatable element.

---

## Download

Go to the **[Releases](https://github.com/ed-fos/Nodal.Design.Release/releases)** page and download the ZIP for your Revit version:

- **Revit 2022** — `Nodal_v1.1.0_Revit2022.zip`
- **Revit 2023** — `Nodal_v1.1.0_Revit2023.zip`
- **Revit 2024** — `Nodal_v1.1.0_Revit2024.zip`
- **Revit 2025** — `Nodal_v1.1.0_Revit2025.zip`
- **Revit 2026** — `Nodal_v1.1.0_Revit2026.zip`

---

## Installation

**IMPORTANT: Do Step 1 before extracting. This prevents Windows from blocking the add-in files.**

1. **Unblock the ZIP file.** Right-click the downloaded ZIP → **Properties** → check the **"Unblock"** checkbox at the bottom of the General tab → click **OK**. This must be done before extracting.

2. **Extract the ZIP** to a temporary location.

3. **Copy `Nodal.addin`** to:
   ```
   C:\ProgramData\Autodesk\Revit\Addins\<Year>\
   ```

4. **Copy the `Nodal` folder** to the same location:
   ```
   C:\ProgramData\Autodesk\Revit\Addins\<Year>\
   ```

5. **Launch Revit.** Look for the **Nodal** tab on the ribbon.

> **Note:** `ProgramData` is a hidden folder. Paste the path directly into File Explorer's address bar.

To uninstall, delete the `Nodal.addin` file and the `Nodal` folder.

---

## Troubleshooting

### "Revit cannot run the external application" / System.IO.FileLoadException (0x80131515)

This means Windows blocked the DLL files because they were downloaded from the internet. To fix it:

1. **Delete** the `Nodal.addin` file and `Nodal` folder from your Addins directory.
2. Go back to the downloaded ZIP file in your Downloads folder.
3. Right-click the ZIP → **Properties** → check **"Unblock"** → **OK**.
4. Re-extract the ZIP and copy the files again following the installation steps above.

### "Could not load type" / System.TypeLoadException

This means you installed the wrong version. Make sure you download the ZIP that matches your Revit version exactly — the Revit 2025 ZIP will not work in Revit 2024 or 2026.

### Tools don't appear on the ribbon

Make sure the folder structure is correct. The Addins directory should look like this:
```
C:\ProgramData\Autodesk\Revit\Addins\2025\
├── Nodal.addin
└── Nodal\
    ├── Nodal.App.dll
    ├── Nodal.Core.dll
    ├── Nodal.UI.dll
    ├── Nodal.Conduit.dll
    └── assets\
        └── icons\
            └── (icon files)
```

---

## Supported Versions

| Revit Version | .NET Runtime | Status |
|--------------|-------------|--------|
| 2022 | .NET Framework 4.8 | Supported |
| 2023 | .NET Framework 4.8 | Supported |
| 2024 | .NET Framework 4.8 | Supported |
| 2025 | .NET 8 | Supported |
| 2026 | .NET 8 | Supported |

---

## Feedback & Issues

Found a bug or have a feature request? Open an issue on [GitHub](https://github.com/ed-fos/Nodal.Design.Release/issues) or reach out on LinkedIn.

---

## Tools in Pipeline

- Run Selector
- Run Lookup
- Renumber Elements
- Smart Section Box

---

## Author

Edward Foster - [nodal.design](https://nodal.design)

**Website:** [nodal.design](https://nodal.design) (coming soon)

**GitHub:** [github.com/ed-fos/Nodal.Design.Release](https://github.com/ed-fos/Nodal.Design.Release)

## License

Copyright © Edward Foster 2026. All rights reserved.

This software is provided as a free download for personal and commercial use with Autodesk Revit. Redistribution of the compiled binaries or any modified versions is not permitted without written consent from the author.
