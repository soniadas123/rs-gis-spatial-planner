# RS & GIS for Spatial Planners

A beginner course in remote sensing and GIS with Python for architects and urban planners, with Bengaluru as the case study.

- Website: https://soniadas123.github.io/rs-gis-spatial-planner/
- Notebooks: `notebooks/` (each one opens in Google Colab from its lesson page)

## Support

[![GitHub stars](https://img.shields.io/github/stars/soniadas123/rs-gis-spatial-planner?style=social)](https://github.com/soniadas123/rs-gis-spatial-planner)

If this course helps you, please give it a star. It is free and takes one click, and it helps other architects and planners find the course.
Sharing it and [opening an issue](https://github.com/soniadas123/rs-gis-spatial-planner/issues) with problems or ideas helps too.

## Contributors

- **Sonia Das** ([@soniadas123](https://github.com/soniadas123)): course design, lessons and the field data collection guide. [Portfolio](https://soniadas123.github.io/soniadas/)

## Structure

```
mkdocs.yml                   site configuration (MkDocs Material)
content/                     website pages in Markdown
  lessons/                   one page per notebook
notebooks/                   10 Colab notebooks
.github/workflows/deploy.yml publishes the site to GitHub Pages on every push to main
```

## Preview the site locally

```
conda activate mkdocs
mkdocs serve
```

Then open http://127.0.0.1:8000.

## Publish

Push to the `main` branch of `soniadas123/rs-gis-spatial-planner`. The GitHub Action builds the site into the `gh-pages` branch.
In the repository settings, set **Pages > Source** to the `gh-pages` branch.
