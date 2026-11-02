# Lesson 2: Mapping the City from OpenStreetMap

<div class="question-box"><strong>Planning question:</strong> What exists on the ground?</div>

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg){ .colab-badge }](https://colab.research.google.com/github/soniadas123/rs-gis-spatial-planner/blob/main/notebooks/02_osm_city_map.ipynb)
&nbsp; [View on GitHub](https://github.com/soniadas123/rs-gis-spatial-planner/blob/main/notebooks/02_osm_city_map.ipynb)

Before planning anything new, you need a base map of what is already there. You will download buildings, streets, parks and amenities for Indiranagar and combine them into a layered map.

## What you will learn

- Download any OSM layer by its tags
- Turn polygons into points with centroids
- Build a layered figure-ground map
- Do a quick open-space-per-person check
- Save all layers to one GeoPackage

## Key concepts

- **Tags**: OSM describes features with key=value pairs, such as `leisure=park`
- **Layers**: maps are built from the bottom up
- **Data quality**: OSM is free but uneven, so always check it

## What you will make

A figure-ground map of Indiranagar showing buildings, streets, parks and amenities.

| | |
|---|---|
| **Packages** | osmnx, geopandas, matplotlib |
| **Data** | OpenStreetMap |
| **Time** | 30 to 45 minutes |

## Try it yourself

The end of the notebook includes these exercises:

1. Compare Jayanagar with Indiranagar.
2. Add bus stations or libraries.
3. Add water bodies with `natural=water`.

*Enjoying the course? Support it with a [star on GitHub](https://github.com/soniadas123/rs-gis-spatial-planner).*

---

[Previous: Lesson 1](01_study_area.md) | [Next: Lesson 3](03_street_network.md)
