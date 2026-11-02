# Glossary

Key terms used in the course, explained for planners.

**Band**
:   One layer of a satellite image, recording one colour of light (for example red, or near-infrared). A colour photo has three bands. Sentinel-2 has thirteen.

**Bounding box (bbox)**
:   The rectangle that encloses an area, written as four numbers: west, south, east, north.

**Centroid**
:   The centre point of a shape.

**Circuity**
:   How much longer a route along the streets is than the straight-line distance. A value of 1.0 means the streets are perfectly direct.

**CRS (Coordinate Reference System)**
:   The system used to give locations coordinates. Latitude and longitude (EPSG:4326) are good for storing data. A projected CRS such as UTM zone 43N (EPSG:32643) is used for measuring distances and areas in metres around Bengaluru.

**DEM (Digital Elevation Model)**
:   A raster where each pixel holds the ground height above sea level.

**Footprint**
:   The outline of a building on the ground, stored as a polygon.

**GeoDataFrame**
:   A table (like a spreadsheet) where each row also has a shape: a point, line or polygon. It comes from the GeoPandas package.

**Ground coverage**
:   The share of a plot or area covered by building footprints, in percent.

**Intersection density**
:   The number of street intersections per square kilometre. Higher values usually mean smaller blocks and a more walkable area.

**Isochrone**
:   The area you can reach from a point within a set time, for example a 15-minute walk.

**Land cover**
:   What physically covers the ground: trees, water, buildings, bare soil. It differs from land use, which is what people use the land for.

**LST (Land Surface Temperature)**
:   How hot the ground surface is, measured by a satellite's thermal sensor. On a sunny day it is often much hotter than the air temperature.

**NDBI (Normalised Difference Built-up Index)**
:   A satellite index that highlights built-up areas. It is calculated from short-wave infrared and near-infrared bands.

**NDVI (Normalised Difference Vegetation Index)**
:   A satellite index that measures how green and healthy vegetation is. It ranges from -1 to 1, and values above about 0.4 usually mean dense vegetation.

**Network graph**
:   A street network stored as **nodes** (intersections) and **edges** (street segments between them).

**OpenStreetMap (OSM)**
:   A free, editable map of the world built by volunteers, like a Wikipedia for maps.

**Pixel / resolution**
:   The smallest square in a raster. "10 m resolution" means each pixel covers 10 m by 10 m on the ground.

**Random Forest**
:   A machine learning method that learns from labelled examples and then predicts labels for new data. It works by combining many simple decision trees.

**Raster**
:   Data stored as a grid of pixels, like a photo. Satellite images and elevation models are rasters.

**Remote sensing**
:   Collecting information about the Earth from a distance, usually with satellites or drones.

**Slope**
:   How steep the ground is, in degrees.

**STAC (SpatioTemporal Asset Catalog)**
:   A standard way to search catalogues of satellite images by place, date and cloud cover.

**Suitability analysis**
:   Combining several map layers, each given a weight, to score how suitable every location is for a use.

**Vector**
:   Data stored as points, lines and polygons, for example bus stops, roads and building footprints.

**Zonal statistics**
:   Summarising raster values inside each zone, for example the average NDVI in each ward.
