---
name: qgis-process
description: >
  Run QGIS geospatial processing algorithms from the command line.
---

# QGIS Headless Process Tool

## Overview
QGIS includes the `qgis_process` CLI command, allowing users to run geospatial analyses (such as buffer calculations, polygon clipping, and raster statistics) directly from a shell script without launching the graphical application.

## Common CLI Commands
```bash
# List all available processing algorithms
qgis_process list

# Show details for a specific algorithm
qgis_process help native:buffer

# Execute buffer calculation
qgis_process run native:buffer --INPUT=input.shp --DISTANCE=10 --OUTPUT=output.shp
```
