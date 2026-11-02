# Lesson 4: The 15-Minute City

<div class="question-box"><strong>Planning question:</strong> Who can walk to a park or school within 15 minutes?</div>

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg){ .colab-badge }](https://colab.research.google.com/github/soniadas123/rs-gis-spatial-planner/blob/main/notebooks/04_15min_city.ipynb)
&nbsp; [View on GitHub](https://github.com/soniadas123/rs-gis-spatial-planner/blob/main/notebooks/04_15min_city.ipynb)

The 15-minute city puts daily needs within a short walk. You will measure real walking times along the street network in Koramangala, draw isochrones and map the access gaps for parks and schools.

## What you will learn

- Add walking time to every street segment
- Draw 5, 10 and 15-minute isochrones
- Calculate the walk from every intersection to the nearest park or school
- Map access gaps and work out a simple 15-minute score

## Key concepts

- **Isochrone**: the area reachable within a set time
- **Network distance** compared with straight-line distance
- **Access gap**: places beyond the target walking time

## What you will make

Maps of walking time to the nearest park and school, with red areas showing access gaps.

| | |
|---|---|
| **Packages** | osmnx, networkx, geopandas |
| **Data** | OpenStreetMap |
| **Time** | 30 to 45 minutes |

## Try it yourself

The end of the notebook includes these exercises:

1. Repeat for clinics and hospitals.
2. Use a slower walking speed for elderly people.
3. Compare with Electronic City.

---

[Previous: Lesson 3](03_street_network.md) | [Next: Lesson 5](05_urban_form.md)
