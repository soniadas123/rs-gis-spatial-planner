# Lesson 6: Satellite Imagery Basics

<div class="question-box"><strong>Planning question:</strong> What does the city look like from space?</div>

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg){ .colab-badge }](https://colab.research.google.com/github/soniadas123/rs-gis-spatial-planner/blob/main/notebooks/06_satellite_basics.ipynb)
&nbsp; [View on GitHub](https://github.com/soniadas123/rs-gis-spatial-planner/blob/main/notebooks/06_satellite_basics.ipynb)

Free satellite images show any city as it is today. You will search the Sentinel-2 catalogue, choose a cloud-free image of central Bengaluru, make true and false colour images, and compare the spectral signatures of water, trees and buildings.

## What you will learn

- Search a STAC catalogue by place, date and cloud cover
- Load satellite bands as an xarray dataset
- Convert raw values to reflectance
- Make true colour and false colour composites
- Plot spectral signatures

## Key concepts

- **Bands**: each records one colour of light
- **Reflectance**: the share of sunlight bounced back
- **False colour**: showing invisible light, such as near-infrared, to reveal vegetation

## What you will make

True colour and false colour images of central Bengaluru, and a spectral signature chart.

| | |
|---|---|
| **Packages** | pystac-client, odc-stac, rioxarray |
| **Data** | Sentinel-2 L2A (Microsoft Planetary Computer) |
| **Time** | 30 to 45 minutes |

## Try it yourself

The end of the notebook includes these exercises:

1. Compare 2019 with 2024.
2. Move the box to the airport.
3. Add a point for Bellandur Lake.

---

[Previous: Lesson 5](05_urban_form.md) | [Next: Lesson 7](07_green_builtup.md)
