# Lesson 3: Street Network Analysis

<div class="question-box"><strong>Planning question:</strong> How connected and walkable are the streets?</div>

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg){ .colab-badge }](https://colab.research.google.com/github/soniadas123/rs-gis-spatial-planner/blob/main/notebooks/03_street_network.ipynb)
&nbsp; [View on GitHub](https://github.com/soniadas123/rs-gis-spatial-planner/blob/main/notebooks/03_street_network.ipynb)

Street patterns shape how people move. You will compare the planned grid of Jayanagar with the organic old market area of Chickpet, using standard measures of network form.

## What you will learn

- Download a street network as a graph of nodes and edges
- Calculate intersection density, street density, dead ends and circuity
- Map junctions and dead ends
- Compare street orientation with polar histograms

## Key concepts

- **Graph**: nodes (intersections) and edges (street segments)
- **Intersection density**: more junctions usually mean better walkability
- **Orientation entropy**: how ordered or grid-like a street pattern is

## What you will make

Side-by-side street maps, a comparison table and street orientation roses for the two areas.

| | |
|---|---|
| **Packages** | osmnx, networkx, pandas |
| **Data** | OpenStreetMap |
| **Time** | 30 to 45 minutes |

## Try it yourself

The end of the notebook includes these exercises:

1. Add a newer suburb such as Whitefield.
2. Switch to the drive network.
3. Test a larger study area.

*Enjoying the course? Support it with a [star on GitHub](https://github.com/soniadas123/rs-gis-spatial-planner).*

---

[Previous: Lesson 2](02_osm_city_map.md) | [Next: Lesson 4](04_15min_city.md)
