# OrthusTrackpad

A capacitive trackpad PCB designed as a component of the [Orthus](https://github.com/Hob-dev/Orthus) split keyboard, but also usable as a standalone mutual-capacitance touch sensor.

The PCB carries a diamond-pattern mutual-capacitance sensor grid intended to be paired with a touch controller IC and read over I²C. The grill cutout in `Fabrication/` matches the sensor pitch and is meant to be laser/CNC-cut from a thin overlay.

## Status

**Functionally complete.** Gerbers, BOM, and pick-and-place (CPL) files are all generated and present under `JLCPCB/`.

## Renders

| | | |
|---|---|---|
| ![](Renders/man4_00000.png) | ![](Renders/man5_00000.png) | ![](Renders/man6_00000.png) |

*Note: the renders are PCB-only views with the silkscreen and sensor traces on a white background; the geometry is faint at fit-to-screen zoom. Open the PNGs locally or load `KiCad/OrthusTrackpad.kicad_pcb` in KiCad's 3D viewer for a clearer view.*

## Folder layout

```
OrthusTrackpad/
├── KiCad/              KiCad 7+ project — open OrthusTrackpad.kicad_pro
│   ├── OrthusTrackpad.kicad_pcb     Board layout (sensor grid + routing)
│   ├── OrthusTrackpad.kicad_sch     Schematic
│   ├── fp-info-cache                KiCad footprint cache
│   └── backups/                     Dated KiCad auto-backups
├── Renders/            Sensor-grid PNG exports (man4/5/6_00000.png)
├── 3D/                 OrthusTrackpad.step — mechanical model of the PCB
├── Fabrication/        MutualCapSensorGride.dxf — sensor-grid overlay cutout
└── JLCPCB/             Production-ready output
    ├── gerber/                      Per-layer .gbr + .drl files (Cu/Mask/Silk top+bottom, NPTH/PTH drills)
    ├── production_files/            Ready-to-upload bundle:
    │                                  GERBER-OrthusTrackpad.zip
    │                                  BOM-OrthusTrackpad.csv
    │                                  CPL-OrthusTrackpad.csv
    └── project.db                   JLCPCB project metadata
```

## Relationship to Orthus

This PCB also lives inside the main Orthus repo at [`Orthus/Components/OrthusTrackpad/`](https://github.com/Hob-dev/Orthus/tree/main/Components/OrthusTrackpad). The two folders are independent copies — edits in one do **not** propagate to the other. Treat this standalone repo as the canonical version when iterating on the trackpad in isolation.

## Original source

All files were originally copied from `Custom/Ergomania/OrthusTrackpad/` in the local working tree; the original folder is preserved at that location.
