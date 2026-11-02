# RS & GIS for Spatial Planners

**Remote sensing and GIS with Python for architects and urban planners. Bengaluru is the case study throughout.**

Planners already ask spatial questions every day. Where is green space missing? Which streets are walkable?
Where is the city growing fastest? This course shows how to answer those questions with free data and short Python
notebooks that run in your web browser.

## Who this is for

- Architects, urban designers and planners who are curious about data-driven planning
- Students of architecture, planning and geography
- Anyone who has used Google Maps or QGIS and wants to go one step further

**You do not need to know Python.** Every notebook explains each step in plain words. You run the code by pressing a button.

## How it works

1. Pick a lesson from the list below.
2. Read the short lesson page to see the planning question and what you will learn.
3. Click **Open in Colab**. The notebook opens in Google Colab, a free online tool, so you install nothing on your computer.
4. Run the cells one by one and look at the maps.

New to Colab? Start with [Getting Started](setup.md).

## The course

| # | Lesson | Planning question | You will use |
|---|--------|-------------------|--------------|
| 1 | [Your Study Area](lessons/01_study_area.md) | What is my study area? | City and ward boundaries |
| 2 | [Mapping the City from OpenStreetMap](lessons/02_osm_city_map.md) | What exists on the ground? | Buildings, roads, amenities |
| 3 | [Street Network Analysis](lessons/03_street_network.md) | How connected and walkable are the streets? | Street networks |
| 4 | [The 15-Minute City](lessons/04_15min_city.md) | Who can walk to a park in 15 minutes? | Walking travel times |
| 5 | [Urban Form and Buildings](lessons/05_urban_form.md) | How dense is the fabric, and what shape is it? | Building footprints |
| 6 | [Satellite Imagery Basics](lessons/06_satellite_basics.md) | What does the city look like from space? | Sentinel-2 imagery |
| 7 | [Green Cover and Built-up Areas](lessons/07_green_builtup.md) | Where is green space lacking? | NDVI and NDBI indices |
| 8 | [Urban Heat Island](lessons/08_urban_heat.md) | Which neighbourhoods are hottest? | Landsat thermal data |
| 9 | [Urban Growth with Machine Learning](lessons/09_urban_growth.md) | How has the city expanded? | Land cover classification |
| 10 | [Site Suitability (Capstone)](lessons/10_site_suitability.md) | Where should a new park go? | Combining all layers, interactive web map |

## Learning path

- **Lessons 1 to 5: GIS.** Vector data (points, lines and polygons) from OpenStreetMap.
- **Lessons 6 to 9: remote sensing.** Raster data from satellite images.
- **Lesson 10: putting it together.** A suitability analysis that uses everything from the course.

Every lesson makes static maps, so you can focus on the analysis. **Interactive web maps** come at the end, in Lesson 10,
once you are comfortable with the data. There you turn your results into a Leaflet map that anyone can open, zoom and click in a web browser.

## Bonus material

[Collecting Citizen Data with ODK and KoboToolbox](bonus/citizen_data_odk_kobo.md) is a no-code guide to field surveys.
It goes from designing a phone form to putting citizen reports on a public map. Satellites and OpenStreetMap cannot tell you
where garbage piles up or which footpaths are broken. Citizens can.

## Data used

All data is free and open, and you do not need an account or API key.

- [OpenStreetMap](https://www.openstreetmap.org): roads, buildings, parks, schools
- [DataMeet Municipal Spatial Data](https://github.com/datameet/Municipal_Spatial_Data): BBMP ward boundaries
- [Sentinel-2](https://planetarycomputer.microsoft.com/dataset/sentinel-2-l2a): 10 m satellite imagery
- [Landsat 8 and 9](https://planetarycomputer.microsoft.com/dataset/landsat-c2-l2): land surface temperature
- [ESA WorldCover](https://planetarycomputer.microsoft.com/dataset/esa-worldcover): land cover map
- [Copernicus DEM](https://planetarycomputer.microsoft.com/dataset/cop-dem-glo-30): elevation

Satellite data is accessed through the [Microsoft Planetary Computer](https://planetarycomputer.microsoft.com).
