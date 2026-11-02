# Lesson 1: Your Study Area

<div class="question-box"><strong>Planning question:</strong> What is my study area?</div>

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg){ .colab-badge }](https://colab.research.google.com/github/soniadas123/rs-gis-spatial-planner/blob/main/notebooks/01_study_area.ipynb)
&nbsp; [View on GitHub](https://github.com/soniadas123/rs-gis-spatial-planner/blob/main/notebooks/01_study_area.ipynb)

Every planning project starts with a clear boundary. You will download the official Bengaluru boundary, measure its area, load the BBMP ward boundaries and make your first maps.

## What you will learn

- Load a city boundary from OpenStreetMap with one line of code
- Reproject data to metres to measure areas correctly
- Read open ward data straight from the web
- Make a choropleth map
- Save layers as a GeoPackage for QGIS

## Key concepts

- **GeoDataFrame**: a table where each row has a shape
- **CRS**: latitude and longitude for storing, UTM (metres) for measuring
- **Choropleth map**: areas coloured by a value

## What you will make

A map of the city boundary, and a map of the BBMP wards coloured by size.

| | |
|---|---|
| **Packages** | geopandas, osmnx, matplotlib |
| **Data** | OpenStreetMap, DataMeet BBMP wards |
| **Time** | 30 to 45 minutes |

## Try it yourself

The end of the notebook includes these exercises:

1. Compare the area of Bengaluru with Mysuru.
2. Find the smallest ward.
3. Try a different colour scale for the ward map.

*Enjoying the course? Support it with a [star on GitHub](https://github.com/soniadas123/rs-gis-spatial-planner).*

---

[All lessons](index.md) | [Next: Lesson 2](02_osm_city_map.md)
