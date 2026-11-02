# Data

## Start with your research question

**Your research question is the most important part of any spatial analysis.** It decides what data you need,
for which area, from which years and at what level of detail. People often start by downloading interesting data and then
look for a question to fit it. That leads to hours of downloads and a weak result.

Turn it around. Write the planning question down in one sentence first, then ask:
**what do I need to measure to answer it?** Only then go looking for data.

| Planning question | What you need to measure | Type of data | Example source |
|---|---|---|---|
| Where is green space lacking? | Vegetation cover per ward | Satellite image (NDVI) + ward boundaries | Sentinel-2, DataMeet |
| Which neighbourhoods are hottest? | Land surface temperature | Thermal satellite image | Landsat 8/9 |
| Who can walk to a park in 15 minutes? | Street network, park locations | Vector map data | OpenStreetMap |
| How many people lack access to a school? | Population by area | Population grid or census | WorldPop, Census of India |
| How has the city expanded since the 1970s? | Built-up area over time | Historical and recent imagery | CORONA, Landsat |
| Which areas flood after heavy rain? | Elevation, low-lying land, rainfall | DEM + rainfall data | Copernicus DEM, CHIRPS |

### Answer these before you search

- **Where?** Your exact study area: a site, a ward, a city or a region.
- **When?** A single date, a season, or a change over several years.
- **How detailed?** A building needs data with pixels of 1 m or less. A neighbourhood needs about 10 to 30 m, and a whole city about 100 m to 1 km.
- **How often?** Is one snapshot enough, or do you need regular updates?
- **Can I use it?** Check the licence, especially if you will publish the results.

Once you have these answers, here are some good places to find data.

## Satellite imagery

| Source | What you get | Detail and coverage | Access |
|---|---|---|---|
| [USGS EarthExplorer](https://earthexplorer.usgs.gov) | **Landsat** imagery since 1972, and much more | 30 m (15 m panchromatic), global | Free account |
| [USGS EarthExplorer](https://earthexplorer.usgs.gov), Declassified Data | **CORONA** spy satellite photos from 1960 to 1972 | About 2 to 12 m, black and white film | Free account |
| [Bhoonidhi (ISRO / NRSC)](https://bhoonidhi.nrsc.gov.in) | **Indian satellite data**: Resourcesat (LISS-III, LISS-IV, AWiFS), Cartosat, Oceansat and more | 5.8 m to 56 m, with India in focus | Free account; some products are paid |
| [Copernicus Browser](https://browser.dataspace.copernicus.eu) | **Sentinel-2** optical and **Sentinel-1** radar imagery | 10 m, every 5 days, global | Free account |
| [Microsoft Planetary Computer](https://planetarycomputer.microsoft.com) | Sentinel, Landsat, DEMs, land cover and more, through STAC | Global | Free, no account needed. **Used in this course.** |
| [Google Earth Engine](https://earthengine.google.com) | A huge catalogue, with processing in the cloud | Global | Free for research and education |

!!! tip "CORONA for urban history"
    CORONA images show Indian cities as they were around 1965 to 1972, long before the IT boom.
    Comparing them with today's Sentinel-2 images is a powerful way to show urban growth, lost lakes and vanished farmland.

## Elevation (DEM)

| Source | What you get | Detail | Access |
|---|---|---|---|
| [USGS EarthExplorer](https://earthexplorer.usgs.gov) | **SRTM** and **ASTER GDEM** elevation | 30 m, global | Free account |
| [Copernicus DEM](https://dataspace.copernicus.eu/explore-data/data-collections/copernicus-contributing-missions/collections-description/COP-DEM) | GLO-30 elevation | 30 m, global | Free. **Used in Lesson 10** (via Planetary Computer) |
| [Bhuvan](https://bhuvan.nrsc.gov.in) / [Bhoonidhi](https://bhoonidhi.nrsc.gov.in) | **CartoDEM**, made by ISRO from Cartosat-1 | 30 m, India | Free account |
| [ALOS World 3D (JAXA)](https://www.eorc.jaxa.jp/ALOS/en/dataset/aw3d30/aw3d30_e.htm) | AW3D30 elevation | 30 m, global | Free account |

## Land cover and land use

| Source | What you get | Detail | Access |
|---|---|---|---|
| [ESA WorldCover](https://esa-worldcover.org) | 11 land cover classes for 2020 and 2021 | 10 m, global | Free. **Used in Lessons 9 and 10** |
| [Dynamic World](https://dynamicworld.app) | Near real-time land cover from Sentinel-2 | 10 m, global | Free (Google Earth Engine) |
| [Bhuvan](https://bhuvan.nrsc.gov.in) | Land use / land cover maps of India | Various scales | Free account |

## Base maps, roads and buildings

| Source | What you get | Detail | Access |
|---|---|---|---|
| [OpenStreetMap](https://www.openstreetmap.org) | Roads, buildings, parks, amenities, land use | Street level, global | Free (ODbL licence). **Used in Lessons 1 to 5 and 10** |
| [Geofabrik](https://download.geofabrik.de/asia/india.html) | Ready-made OSM downloads for India and its states | Street level | Free |
| [Overture Maps](https://overturemaps.org) | Cleaned, combined open map data: buildings, places, transport | Global | Free |
| [Google Open Buildings](https://sites.research.google/gr/open-buildings/) | Building footprints detected by AI, including heights in the 2.5D version | Africa, South and Southeast Asia, Latin America | Free |
| [Microsoft Building Footprints](https://github.com/microsoft/GlobalMLBuildingFootprints) | Building footprints detected by AI | Global | Free |

## Population and settlements

| Source | What you get | Detail | Access |
|---|---|---|---|
| [WorldPop](https://www.worldpop.org) | Estimated population per grid cell, by age and sex | 100 m, global, yearly | Free |
| [GHSL (Global Human Settlement Layer)](https://human-settlement.emergency.copernicus.eu) | Built-up area, population and settlement type since 1975 | 10 m to 1 km, global | Free |
| [Census of India](https://censusindia.gov.in) | Official population and housing tables, down to wards and villages | Administrative units | Free |
| [Meta High Resolution Population Density](https://data.humdata.org/organization/meta) | Population estimates from satellite imagery | 30 m | Free (Humanitarian Data Exchange) |

## Climate and environment

| Source | What you get | Detail | Access |
|---|---|---|---|
| [NASA POWER](https://power.larc.nasa.gov) | Daily temperature, rainfall, solar radiation and wind | About 50 km, global | Free |
| [CHIRPS](https://www.chc.ucsb.edu/data/chirps) | Daily and monthly rainfall since 1981 | About 5 km | Free |
| [Copernicus Climate Data Store (ERA5)](https://cds.climate.copernicus.eu) | Hourly climate reanalysis since 1940 | About 30 km | Free account |
| [VIIRS Night Lights](https://eogdata.mines.edu/products/vnl/) | Night-time light, a proxy for urban activity and growth | About 500 m | Free account |

## Indian government and community portals

| Source | What you get | Access |
|---|---|---|
| [Bhuvan (ISRO / NRSC)](https://bhuvan.nrsc.gov.in) | Thematic maps of India: land use, wastelands, urban sprawl, DEMs | Free account |
| [Open Government Data Platform](https://data.gov.in) | Datasets from Indian ministries and states | Free |
| [Survey of India](https://onlinemaps.surveyofindia.gov.in) | Official topographic maps | Free account |
| [India-WRIS](https://indiawris.gov.in) | Water resources: rivers, watersheds, groundwater, reservoirs | Free |
| [DataMeet](https://github.com/datameet) | Community-made open data: ward boundaries, constituencies, pin codes. **Used in Lessons 1, 7 and 8** | Free |

## Your own data

Sometimes the data you need does not exist, for example garbage dumps, broken footpaths or streetlights that do not work.
Then you collect it yourself. See the bonus guide [Collecting Citizen Data with ODK and KoboToolbox](bonus/citizen_data_odk_kobo.md).

## Before you download

- **Licence and citation:** can you share or publish the results? Who should you credit?
- **Date and season:** compare like with like. For example, compare dry season with dry season in each year.
- **Cloud cover:** for optical imagery, filter for scenes with little cloud.
- **Coordinate system (CRS):** make sure all layers line up. Reproject if needed.
- **Detail compared with your question:** 30 m pixels cannot show a single building, and street-level data may be far too much for a state-wide study.

!!! tip "Accounts"
    USGS EarthExplorer, Bhoonidhi, Bhuvan and the Copernicus Browser all need a free account. Register before your workshop or fieldwork,
    because approval for some products can take a day or two.

## Data used in this course

| Lessons | Data | Source |
|---|---|---|
| 1, 7, 8 | BBMP ward boundaries | [DataMeet](https://github.com/datameet/Municipal_Spatial_Data) |
| 1 to 5, 10 | Roads, buildings, parks, amenities | [OpenStreetMap](https://www.openstreetmap.org) |
| 6, 7, 9 | Sentinel-2 imagery | [Planetary Computer](https://planetarycomputer.microsoft.com/dataset/sentinel-2-l2a) |
| 8, 10 | Landsat 8/9 thermal and optical | [Planetary Computer](https://planetarycomputer.microsoft.com/dataset/landsat-c2-l2) |
| 9, 10 | ESA WorldCover 2021 | [Planetary Computer](https://planetarycomputer.microsoft.com/dataset/esa-worldcover) |
| 10 | Copernicus DEM GLO-30 | [Planetary Computer](https://planetarycomputer.microsoft.com/dataset/cop-dem-glo-30) |

All of it is free and open, and the notebooks download it automatically, with no account needed.
