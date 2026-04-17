# OrthusTrackpad

A capacitive trackpad PCB designed for integration with the OrthusChoc keyboard (and usable standalone).

## Status

**Functionally complete.** Gerbers and JLCPCB production files are generated and present.

## Folder structure

```
OrthusTrackpad/
├── KiCad/              Main KiCad project
│   └── backups/        Dated auto-backups (5 snapshots kept)
├── Renders/            Capture/working PNGs (man4/5/6_00000.png)
├── 3D/                 OrthusTrackpad.step
├── Fabrication/        MutualCapSensorGride.dxf — capacitive sensor grid outline
└── JLCPCB/             gerber/, production_files/, project.db
```

## Relationship to OrthusChoc

This PCB is also included as a component inside `OrthusChoc/Components/OrthusTrackpad/`. The two folders are independent copies — edits made in one location will **not** propagate to the other. If you want this to be the canonical version, make a decision on which copy is the source of truth before further work.

## Original source

All files were copied from `Custom/Ergomania/OrthusTrackpad/`. The original folder is still intact at that location.
