# Lesson 7: Green Cover and Built-up Areas

<div class="question-box"><strong>Planning question:</strong> Where is green space lacking?</div>

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg){ .colab-badge }](https://colab.research.google.com/github/soniadas123/rs-gis-spatial-planner/blob/main/notebooks/07_green_builtup.ipynb)
&nbsp; [View on GitHub](https://github.com/soniadas123/rs-gis-spatial-planner/blob/main/notebooks/07_green_builtup.ipynb)

Bengaluru, the Garden City, has lost much of its tree cover. You will calculate NDVI and NDBI from Sentinel-2, mask out clouds and summarise green cover for every BBMP ward.

## What you will learn

- Mask clouds with the scene classification layer
- Calculate NDVI and NDBI
- Rasterize wards and calculate zonal statistics
- Rank the wards by green cover

## Key concepts

- **NDVI**: a vegetation index from -1 to 1
- **NDBI**: a built-up index
- **Zonal statistics**: summarising pixels within each area

## What you will make

A ward map of dense green cover, and a list of the least green wards.

| | |
|---|---|
| **Packages** | odc-stac, rioxarray, rasterio, pandas |
| **Data** | Sentinel-2 L2A, DataMeet BBMP wards |
| **Time** | 30 to 45 minutes |

## Try it yourself

The end of the notebook includes these exercises:

1. Compare 2019 with 2024.
2. Test a different NDVI threshold.
3. Look up your own ward.

---

[Previous: Lesson 6](06_satellite_basics.md) | [Next: Lesson 8](08_urban_heat.md)
