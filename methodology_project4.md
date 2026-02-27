# Methodology: Project 4 — Version Control and Feature Digitization for Geospatial Data

This document contains the detailed step-by-step methodology followed in Project 4.

---

## Task 1: Configure Git, Install Kart, and Create a Repository
- Configured Git with a username and email address using Git Bash
- Installed the Kart plugin in QGIS via the Plugin Manager
- Created a new local Kart repository directory and initialized it as a Geopackage-type repository
- Connected to the UBC PostgreSQL server from the Kart repository pane and imported the `ubcv_campus_trees` table into the repository
- Added the most recent UBC orthophoto (Cloud Optimized GeoTiff) to the QGIS project via a remote HTTP URL
- Dragged the `ubcv_campus_trees` layer from the Kart pane into the map and visually compared tree point locations against the orthophoto

---

## Task 2: Edit a Layer in QGIS with Version Control
- Started an editing session on `ubcv_campus_trees` using the Toggle Editing tool
- Used the Vertex Tool to reposition 3–5 existing tree points to better align with tree trunk locations visible in the orthophoto
- Added at least one missing tree point using the Add Point Feature tool, including a note in the attributes field
- Saved edits to the layer and inspected the changes using Kart's diff viewer (working copy changes)
- Committed the changes to the repository with a descriptive commit message
- Reviewed the commit history using the Show Log tool

---

## Task 3: Working on and Merging Different Branches
- Created a new branch called `mybranch` from the most recent commit in the repository
- Switched to `mybranch` and digitized 5–10 additional missing tree points, then committed the changes
- Switched back to the `main` branch and digitized 5–10 different missing tree points, then committed those changes separately
- Merged `mybranch` into `main` using the Merge into Current Branch option
- A merge conflict occurred due to overlapping edits on the same features across the two branches
- Inspected the conflict using the Resolve Conflicts tool and resolved it by accepting the modified feature for each conflicting record
- Verified the merged commit history showed a single unified `main` branch

---

## Task 4: Digitize Buildings in ArcGIS Pro
- Created a VRT reference file from the UBC orthophoto COG in QGIS and loaded it into ArcGIS Pro
- Created a new polygon feature class called `my_ubc_buildings` in the project geodatabase with fields for Name (text) and Vertices (double), projected to NAD 1983 UTM Zone 10N
- Digitized five campus buildings by tracing their rooftop outlines from the orthophoto and entering building names in the attribute table
- Exported `ubcv_buildings` from the PostgreSQL server and reprojected to NAD 1983 UTM Zone 10N as `ubcv_buildings_utm`
- Added a Vertices field to both layers and calculated vertex count using Calculate Geometry
- Compared Shape_Area, Shape_Length, and Vertices between the digitized buildings and the official dataset to evaluate accuracy

---

*Back to [README](README_project4.md)*
