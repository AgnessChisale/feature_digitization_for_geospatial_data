# Project 4: Version Control and Feature Digitization for Geospatial Data

[Github Repo](https://github.com/AgnessChisale/feature_digitization_for_geospatial_data)

## Overview
This project explores version control for geospatial data using Git and Kart, and practices feature digitization in both QGIS and ArcGIS Pro. Campus tree locations at UBC Vancouver were edited and validated against a recent orthophoto using Kart's branching and merging capabilities. Five campus buildings were then manually digitized in ArcGIS Pro and compared against the official UBC building dataset to evaluate positional and geometric accuracy.

---

## Objectives
- Configure Git and Kart for geospatial version control
- Edit and commit point feature changes using branching workflows
- Manage and resolve merge conflicts between branches
- Digitize polygon features from an orthophoto in ArcGIS Pro
- Evaluate digitization accuracy against an official reference dataset

---

## Data Sources & Tools

**Data**
| Layer | Description | Source |
|-------|-------------|--------|
| `ubcv_campus_trees` | Point layer of trees on UBC Vancouver campus | UBC PostgreSQL Server (`ubcv` database) |
| `UBC_ORTHOPHOTO_YEAR_COG.tif` | Most recent UBC Vancouver orthophoto (Cloud Optimized GeoTiff) | MGEM Orthophoto Data Store |
| `ubcv_buildings` | Official UBC Campus building polygons | UBC PostgreSQL Server (`ubcv` database) |

**Tools**
| Tool | Purpose |
|------|---------|
| Git | Distributed version control for file tracking |
| Kart (QGIS plugin) | Version control extended to geospatial vector data |
| QGIS | Editing point features and inspecting diffs |
| ArcGIS Pro | Digitizing building polygons and geometry calculations |

---

## Methods
Campus tree points were imported into a local Kart repository and compared against a UBC orthophoto. Point locations were corrected and new trees were added through an editing session, with changes committed to version control. A separate branch was created to simulate collaborative editing, and a merge conflict was intentionally triggered and resolved. Five UBC buildings were then digitized as polygons in ArcGIS Pro using the orthophoto as a reference, and geometry metrics (area, perimeter, vertex count) were compared against the official UBC buildings dataset.

📄 *For a detailed breakdown of the methodology, [click here](https://github.com/AgnessChisale/feature_digitization_for_geospatial_data/blob/main/methodology_project4.md)*

---

## Outputs

- `digitization_accuracy_map.pdf` — Annotated map comparing digitized building vertices against the official UBC dataset, with discussion of accuracy implications

---

## Key Findings
- Campus tree locations showed positional offsets from the orthophoto due to GPS error, data age, and canopy offset
- Merge conflicts arose when the same features were edited independently across two branches
- Digitized buildings deviated from the official dataset in area, perimeter, and vertex count, illustrating how vertex density and operator judgement affect positional accuracy

---

## Skills Learned
- Configuring and using Git for version control
- Importing geospatial data into a Kart repository
- Editing point features in QGIS with version tracking
- Committing changes and writing informative commit messages
- Creating and switching between branches in Kart
- Resolving merge conflicts in geospatial data
- Digitizing polygon features from an orthophoto in ArcGIS Pro
- Calculating geometry metrics (area, perimeter, vertices) in ArcGIS Pro
- Evaluating digitization accuracy against a reference dataset
