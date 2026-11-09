# Geospatial Visualization in Python

Hands-on notebook for Lecture 27 of GEOG 213/313 Advanced Geospatial Analytics with Python at Clark University. The concepts are covered in [Lecture 26: Communicating with Maps and Visualizations](https://hamedalemo.github.io/advanced-geo-python/lectures/26_visualization_principles.html) on the [course website](https://hamedalemo.github.io/advanced-geo-python/intro.html).

## What you will do

1. Compare rainbow (`jet`) and perceptually uniform colormaps, measure their lightness and simulate color vision deficiency.
2. Build choropleth maps that normalize, classify (`mapclassify`) and project the data on purpose.
3. Make interactive maps with GeoPandas `.explore()` and [Lonboard](https://developmentseed.org/lonboard/).
4. Look inside map tiles: read a remote [PMTiles](https://docs.protomaps.com/pmtiles/) file with HTTP range requests, decode a vector tile, write your own PMTiles with GeoPandas, and display PMTiles with leafmap and Lonboard.
5. Fix a bad map.

## Setup

Install [pixi](https://pixi.sh), then from this folder:

```bash
pixi install
pixi run lab
```

The first run downloads about 65 MB of data into `data/` (ignored by git).

## Data

All data are downloaded by the notebook from GitHub:

- [Natural Earth](https://www.naturalearthdata.com/) countries, populated places and roads, via [nvkelso/natural-earth-vector](https://github.com/nvkelso/natural-earth-vector) (public domain).
- NCEP reanalysis air temperature from the [Xarray tutorial data](https://github.com/pydata/xarray-data).
- PMTiles test archives from [protomaps/PMTiles](https://github.com/protomaps/PMTiles) (Florence vector tiles: OpenStreetMap, ODbL; Mount Whitney imagery: USGS).
- A digital elevation model bundled with Matplotlib.

## Notes

- The interactive maps (Lonboard and leafmap) need a running Jupyter session and an internet connection for basemaps.
- `ipyvuetify` is pinned below 3 because leafmap's MapLibre widget does not yet work with ipyvuetify 3.
