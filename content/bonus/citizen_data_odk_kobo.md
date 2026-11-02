# Bonus: Collecting Citizen Data with ODK and KoboToolbox

<div class="question-box"><strong>Planning question:</strong> How can citizens report what satellites and maps cannot see?</div>

This bonus guide uses **no Python**. It shows you how to run a field survey on mobile phones and bring the results into
your maps. The worked example is a **citizen solid waste reporting survey** in Bengaluru.

[Download the full illustrated guide (PDF)](Field_Data_Collection_Carousel.pdf){ .md-button .md-button--primary }

## Why citizen data matters for planners

Satellite images show green cover and built-up land. OpenStreetMap shows roads and buildings. But neither can tell you:

- where garbage piles up on the street
- which footpaths are broken or blocked
- which streetlights are not working
- how residents actually use a park

**Citizen data**, collected by residents, volunteers or students with a phone, fills these gaps. It gives you
**ground truth**: real observations at real places. It also brings the community into the planning process.

## The tools

The guide uses four open-source tools. Each one does one job and hands the data to the next.

| Tool | Runs on | Job |
|---|---|---|
| [KoboToolbox](https://www.kobotoolbox.org) | Web browser | Design forms, then receive and review submissions |
| [ODK Collect](https://getodk.org) or KoboCollect | Android phone | Collect data offline, with GPS and photos |
| [QGIS](https://qgis.org) | Desktop | Clean, join, analyse and style the data |
| Dashboard | Web | A Leaflet map (see [Lesson 10](../lessons/10_site_suitability.md)) or a Streamlit app |

**ODK** stands for Open Data Kit. KoboToolbox is built on it, so forms made in Kobo work in both ODK Collect and KoboCollect.

A phone form gives a field team a lot that paper cannot:

- It **works offline**.
- It adds a **GPS point to every record**.
- **Photos** are attached to the record.
- There are **no paper sheets to re-type**.

## The pipeline

The work always runs in this order. **Start at step 1, not step 2.**

1. Plan storage
2. Design the form
3. Deploy
4. Connect the phones (ODK Collect)
5. Collect in the field
6. Review in Kobo
7. Archive
8. Analyse in QGIS
9. Build the dashboard and publish

## Step 1: Plan storage

Every KoboToolbox plan has a storage limit. Text submissions are tiny. **Photos are what fill it up.**

Do this sum before you start:

> **submissions you expect** x **photos per submission** x **photo size from your phones** = **storage you need**

Take a test photo on the phones your team will use and check its file size. Compare the total with your plan's limit,
and leave some headroom. Current plan limits are listed on [kobotoolbox.org](https://www.kobotoolbox.org).

To shrink photos before they upload, add this setting to the photo question's `parameters` column:

```
max-pixels=1024
```

It caps the longest side of each photo at 1,024 pixels. With photos resized like this, a 1 GB plan goes a long way.

!!! tip "Do the maths before fieldwork, not during it"
    If you go over the limit anyway, archive and clear old data (see Step 7) or buy more storage from Kobo.

## Step 2: Design the form

Start with the drag-and-drop **Formbuilder** in KoboToolbox. Once your form has more than about a dozen questions, switch to
**XLSForm**: a spreadsheet where **one row is one question**. It is easier to version, share and fix in bulk.

### Sample form: solid waste reporting in Bengaluru

**`survey` sheet**

| type | name | label | relevant | parameters |
|---|---|---|---|---|
| start | start | | | |
| end | end | | | |
| today | today | | | |
| select_one yesno | consent | Data will be published openly. Continue? | | |
| select_one_from_file sites.csv | site_id | Which site are you at? | `${consent} = 'yes'` | |
| geopoint | location | Stand at the site | `${consent} = 'yes'` | |
| select_one yesno | solid_waste | Is there solid waste? | `${consent} = 'yes'` | |
| image | photo | Photo of the site | `${solid_waste} = 'yes'` | max-pixels=1024 |

**`choices` sheet**

| list_name | name | label |
|---|---|---|
| yesno | yes | Yes |
| yesno | no | No |

`sites.csv` is a small file that you upload to the form as a media file. It holds a list of survey sites, with `name` and `label` columns,
for example one row per ward from [Lesson 1](../lessons/01_study_area.md).

### Form design tips

- **Geo questions:** `geopoint` records a point, `geotrace` a line and `geoshape` a polygon. Start with points.
- **Skip logic:** the `relevant` column hides a question until a condition is met. In the form above, nothing is asked
  unless the person gives consent, and the photo is only asked for when there is waste.
- **Clean names:** keep the `name` column short, lowercase and with underscores. These names become the column headers in QGIS and your dashboard.
- **Keep start, end and today:** the timestamps expose rushed or duplicate submissions.

## Steps 3 and 4: Deploy and connect the phones

When you sign up, Kobo asks you to pick a server: **Global** or **EU**. This decides where your data is stored.
Note which one you chose, because every phone must point to it.

**Deploy** makes the form live. After every edit, **Redeploy**, then update the form on every phone.

In ODK Collect or KoboCollect:

1. Choose **Configure server manually**, or go to **Settings > Project Management > Server**.
2. Paste the **server URL** from your project, found under **Form > Collect data**. It looks like
   `https://kc.kobotoolbox.org/your_username`. The EU server has a different URL, so always copy it from your own project.
3. Sign in with a **dedicated data collection account**, or allow anonymous submissions. **Never share your main login.**
4. **Download the form** and send one test submission from home.

## Step 5: Collect in the field

Brief volunteers on four things:

- **Stand at the site.** The GPS records where you are. Save once the accuracy drops below 5 to 10 m.
- **Finalise each form.** Don't leave it as a draft.
- **Tap Send** once you are back on a network.
- **Charge the phone** before going out.

Walk the route once with a test form before the team goes out.

!!! warning "Once the form is live, never rename a question"
    You can add questions mid-collection. Renaming or deleting old ones splits your data into mismatched columns.

## Steps 6 and 7: Review, then archive

Use Kobo's **Map view** as a quick GPS check. Mark each record **Approved**, **Not approved** or **On hold**.
That status travels into every export, so the dashboard can show approved records only.

Export two bundles:

- **GeoJSON export:** geometry and attributes in one open file, which loads straight into QGIS. Keep a CSV too.
- **Media ZIP:** the photo files. The photo column holds each file name, so they match up.

!!! danger "Deleted submissions and photos cannot be recovered from Kobo"
    **Verify, then delete:**

    1. The record count in the export matches Kobo.
    2. The photos in the ZIP match the non-empty photo values.
    3. A random handful of records show the right photo.
    4. You have two copies in two places, such as a local drive and the cloud.

    Or skip deleting altogether: Kobo sells monthly storage plans.

## Steps 8 and 9: Analyse and publish

Drag the GeoJSON or CSV onto the QGIS map. Then:

- **Join** the collected points to your base layer by a shared ID, for example the BBMP wards from [Lesson 1](../lessons/01_study_area.md)
- **Summarise** conditions per site or ward, for example the number of waste reports per ward
- **Overlay a DEM** to see which problems sit in low-lying ground (see the elevation data in [Lesson 10](../lessons/10_site_suitability.md))
- **Flag** poor GPS precision and records marked Not approved

**Keep the archive untouched, and work on copies.** Use the right format for each job:

| Use | Format |
|---|---|
| QGIS analysis | GeoPackage: geometry, attributes and styles in one file |
| Dashboard | GeoJSON for Leaflet, GeoParquet for faster Python |
| Web photos | Resized JPGs |
| Open data | CSV + GeoJSON + the XLSForm as a data dictionary, with personal information removed |

Build the dashboard in this order: **sketch charts in Colab**, **set the KPIs** (decide what to measure), then **build it**.

- **Leaflet:** a public map of finished data. One HTML file, with free hosting. Lesson 10 shows you how to make one.
- **Streamlit:** filters, charts, or live data from the Kobo API.

## Privacy and consent

Citizen data is about people and their neighbourhoods. Before you publish:

- Ask for **consent** at the start of the form, and say clearly that the data will be published.
- **Remove personal information**, such as names, phone numbers and faces in photos.
- Think about whether exact locations could identify a household. If they could, publish ward summaries instead of points.

## If you remember two things

1. **Plan storage before the form.** Resize photos to 1,024 pixels.
2. **Archive before you delete.** GeoJSON plus the media ZIP, verified, in two places.

Everything else in the pipeline can be fixed later. These two can't.

## The full guide

<object data="../Field_Data_Collection_Carousel.pdf" type="application/pdf" width="100%" height="800px">
  <p>Your browser cannot show the PDF here. <a href="../Field_Data_Collection_Carousel.pdf">Download the guide instead</a>.</p>
</object>

*Guide: "From Field Data Collection to Public Dashboard" by Sonia Das.*
