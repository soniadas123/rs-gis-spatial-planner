# Lesson 8: Urban Heat Island

<div class="question-box"><strong>Planning question:</strong> Which neighbourhoods are hottest?</div>

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg){ .colab-badge }](https://colab.research.google.com/github/soniadas123/rs-gis-spatial-planner/blob/main/notebooks/08_urban_heat.ipynb)
&nbsp; [View on GitHub](https://github.com/soniadas123/rs-gis-spatial-planner/blob/main/notebooks/08_urban_heat.ipynb)

Concrete and asphalt make cities hotter than their surroundings. You will map land surface temperature from Landsat's thermal band, find hot spots and the hottest wards, and measure how much cooler green areas are.

## What you will learn

- Load a Landsat thermal band and convert it to degrees Celsius
- Mask clouds with the quality band
- Measure heat island intensity and map hot spots
- Calculate the mean temperature per ward and its link to NDVI

## Key concepts

- **LST**: land surface temperature, not air temperature
- **Urban heat island**: built-up areas are hotter than green areas
- **Hot spot**: much hotter than the city average

## What you will make

A land surface temperature map of Bengaluru and a ward ranking by temperature.

| | |
|---|---|
| **Packages** | odc-stac, rioxarray, numpy |
| **Data** | Landsat 8/9 Collection 2 Level-2, DataMeet BBMP wards |
| **Time** | 30 to 45 minutes |

## Try it yourself

The end of the notebook includes these exercises:

1. Compare with 2015.
2. Change the hot spot threshold.
3. Check the hottest ward on a satellite basemap.

*Enjoying the course? Support it with a [star on GitHub](https://github.com/soniadas123/rs-gis-spatial-planner).*

---

[Previous: Lesson 7](07_green_builtup.md) | [Next: Lesson 9](09_urban_growth.md)
