# Nodal.Design : Revit Add-in

ITS FREE! 

An aspiring professional Revit add-in for BIM and VDC. Version 1.0.0 only has two tools, but there are many more to come.

**Website:** [nodal.design](https://nodal.design) (not live as yet)
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

1. Download and unzip the release for your Revit version.
2. Copy **`Nodal.addin`** to:
   ```
   C:\ProgramData\Autodesk\Revit\Addins\<Year>\
   ```
3. Copy the **`Nodal`** folder to the same location:
   ```
   C:\ProgramData\Autodesk\Revit\Addins\<Year>\
   ```
4. Launch Revit. Look for the **Nodal** tab on the ribbon.

> **Note:** `ProgramData` is a hidden folder. Paste the path directly into File Explorer's address bar to navigate there.

To uninstall, delete the `Nodal.addin` file and the `Nodal` folder.

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

Edward Foster — [nodal.design](https://nodal.design)

## License

Copyright © Edward Foster 2026. All rights reserved.
