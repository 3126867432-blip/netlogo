# Urban Heat Commuting Model for NetLogo

This repository contains a NetLogo model for route choice under urban heat exposure.

The model integrates:
- road networks
- buildings and office buildings
- metro stations
- shadow layers
- UTCI raster inputs
- per-agent heterogeneity at initialization

## Main file

- `netlogo.txt` — main model code for the current open-source submission

## Agent heterogeneity included

Each commuter can start with different individual attributes, including:
- walking speed
- departure delay
- heat tolerance threshold
- route preference weights

These heterogeneity variables are included directly in the model code.

## Current model scope

The model includes:
- road-network construction from GIS vector data
- time-slot-based morning and evening commuting simulation
- shadow-aware and UTCI-aware path computation
- active path selection under distance and time budgets
- counterfactual scenario switches for shadow and UTCI ablation
- CSV export functions for path comparison and thermal exposure analysis

## Important note before public release

The current code still contains local absolute file paths such as:

- `C:/Users/.../road3_clip.shp`
- `C:/Users/.../UTCI_...asc`
- `C:/Users/.../greensp_binary.asc`

Before making the repository fully public, you should either:
1. replace them with relative paths, or
2. move them into a user-editable configuration block.

## Data availability note

This repository contains code only.

If the GIS layers, shadow shapefiles, or UTCI rasters cannot be redistributed, do not upload them to the public repository. Instead, describe:
- what datasets are required
- expected file formats
- how users can prepare their own inputs

## Recommended repository contents

```text
.
├── netlogo.txt
├── README.md
├── LICENSE
└── .gitignore
```

## License

This project is released under the MIT License. See `LICENSE` for details.
