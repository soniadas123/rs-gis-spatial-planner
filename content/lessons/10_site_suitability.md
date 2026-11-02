# Lesson 10: Site Suitability (Capstone)

<div class="question-box"><strong>Planning question:</strong> Where should a new park go?</div>

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg){ .colab-badge }](https://colab.research.google.com/github/soniadas123/rs-gis-spatial-planner/blob/main/notebooks/10_site_suitability.ipynb)
&nbsp; [View on GitHub](https://github.com/soniadas123/rs-gis-spatial-planner/blob/main/notebooks/10_site_suitability.ipynb)

The capstone has two parts. In Part 1 you combine everything from the course: four criteria layers (heat, green need, flatness and road access), limited to open land and combined with weights, to shortlist the 10 best park sites in south-east Bengaluru. In Part 2 you meet **interactive web maps** for the first time, and turn the results into a Leaflet map that anyone can open, zoom and click in a web browser.

## What you will learn

- Put satellite, elevation, land cover and OSM data onto one common grid
- Calculate slope and distance to roads with xarray-spatial
- Rescale criteria to 0 to 1 and apply weights
- Shortlist the top sites
- Build an interactive Leaflet web map with folium: basemaps, a raster overlay, layers, tooltips and popups
- Save the web map as a single HTML file and publish it

## Key concepts

- **Multi-criteria analysis**: combining weighted factors
- **Constraints** compared with **criteria**: excluded land compared with scored land
- **Sensitivity**: how results change with the weights
- **Web map**: tiles, layers, tooltips and popups in Leaflet

## What you will make

A suitability map, and an interactive web map of the 10 candidate park sites that you can share as a single HTML file.

| | |
|---|---|
| **Packages** | xarray-spatial, odc-stac, osmnx, folium |
| **Data** | Landsat, Copernicus DEM, ESA WorldCover, OpenStreetMap |
| **Time** | 30 to 45 minutes |

## Try it yourself

The end of the notebook includes these exercises:

1. Give heat more weight.
2. Add distance to existing parks.
3. Adapt the model for affordable housing.
4. Add the heat layer to the web map.
5. Add the ward boundaries to the web map.

!!! success "You finished the course!"
    Thank you for learning with us. If the course helped you, please **[give it a star on GitHub](https://github.com/soniadas123/rs-gis-spatial-planner)** and share it with a colleague or a student. Stars help other planners find it.

---

[Previous: Lesson 9](09_urban_growth.md) | [Glossary](../glossary.md)
