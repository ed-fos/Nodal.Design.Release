# Nodal.Design - Revit Add-in

A free Revit add-in for BIM and VDC professionals. Version 1.0.0 ships with two conduit routing tools, with many more on the way.

**Website:** [nodal.design](https://nodal.design) (coming soon)
**GitHub:** [github.com/ed-fos/Nodal.Design.Release](https://github.com/ed-fos/Nodal.Design.Release)

---

## Tools

### Conduit Offset
Creates a precise offset between two parallel conduits. Select two conduits, choose a bend angle, and the tool automatically calculates the optimal connection point, creates the transition conduit, and places elbow fittings at both ends. Supports pre-selection.

### Conduit Kick 90
Creates a kick 90 connection between two perpendicular conduits. Handles both coplanar (direct 90° elbow) and non-coplanar (angled kick) scenarios automatically. Supports pre-selection.

---

## Download

Go to the **[Releases](https://github.com/ed-fos/Nodal.Design.Release/releases)** page and download the ZIP for your Revit version:

- **Revit 2024** — `Nodal_v1.0.0_Revit2024.zip`
- **Revit 2025** — `Nodal_v1.0.0_Revit2025.zip`
- **Revit 2026** — `Nodal_v1.0.0_Revit2026.zip`

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
| 2024 | .NET Framework 4.8 | Supported |
| 2025 | .NET 8 | Supported |
| 2026 | .NET 8 | Supported |

---

## Tools in Pipeline

- Power Knife
- Power Connect
- Power Disconnect
- Parallelize

---

## Author

Edward Foster - [nodal.design](https://nodal.design)

## License

Copyright © Edward Foster 2026. All rights reserved.

This software is provided as a free download for personal and commercial use with Autodesk Revit. Redistribution of the compiled binaries or any modified versions is not permitted without written consent from the author.
