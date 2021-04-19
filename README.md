# Clatsop County Oregon building footprints

This project uses Microsoft US Building Footprints as its source.
It imports and processes them to create a service for Clatsop County, Oregon
using standard Esri tools.

2021- switched from ArcMap to ArcGIS Pro.

Now in ESRI File Geodatabase format instead of shapefiles.

## Overview

1. Download Oregon data from
https://github.com/Microsoft/USBuildingFootprints and unzip to
Oregon.geojson.

2. Use model "Import" to convert geojson to FGDB
"oregon_buildings_wgs84". Project to oregon_buildings_wm" in web mercator.

3. Using Clip model, select shapes in Clatsop County and export to
clatsop_buildings_wgs84 then reproject to web mercator and local
projection.

4. Publish the footprints to our ArcGIS server as a Map Image Layer.

The publish model will copy the locally projected feature class to SDE
called "buildings_clatsop".  I also publish using "Sharing" as a
hosted feature layer "Building footprints for Clatsop County".
