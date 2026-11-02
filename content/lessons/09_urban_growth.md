# Lesson 9: Urban Growth with Machine Learning

<div class="question-box"><strong>Planning question:</strong> How has the city expanded?</div>

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg){ .colab-badge }](https://colab.research.google.com/github/soniadas123/rs-gis-spatial-planner/blob/main/notebooks/09_urban_growth.ipynb)
&nbsp; [View on GitHub](https://github.com/soniadas123/rs-gis-spatial-planner/blob/main/notebooks/09_urban_growth.ipynb)

East Bengaluru has grown rapidly along its IT corridors. You will train a Random Forest classifier with ESA WorldCover labels, map land cover in 2019 and 2024, and measure the new built-up area.

## What you will learn

- Turn satellite images into a table of pixels and features
- Train and test a Random Forest classifier
- Read precision, recall and the confusion matrix
- Classify two years and map the change

## Key concepts

- **Supervised classification**: learning from labelled examples
- **Training and test sets**: checking the model on unseen data
- **Change detection**: comparing classified maps over time

## What you will make

Land cover maps for 2019 and 2024, and a map of new built-up areas.

| | |
|---|---|
| **Packages** | scikit-learn, odc-stac, xarray |
| **Data** | Sentinel-2 L2A, ESA WorldCover 2021 |
| **Time** | 30 to 45 minutes |

## Try it yourself

The end of the notebook includes these exercises:

1. Study the airport area.
2. Train without the indices.
3. Use fewer trees.

*Enjoying the course? Support it with a [star on GitHub](https://github.com/soniadas123/rs-gis-spatial-planner).*

---

[Previous: Lesson 8](08_urban_heat.md) | [Next: Lesson 10](10_site_suitability.md)
