# 1m Water Balance model for WBP core area analysis


https://github.com/user-attachments/assets/c366ca37-40a1-4cf6-9676-012ead12c62b

2002-2022 Average Annual Climatic Water Deficit - Surprise and Amphitheater, GRTE

# Site Setup
Create a directory in data/input with the desired site name, i.e., `/data/input/holly_lake_small`
Create subdirectories dem and soil

dem, aspect, slope, hillshade layers are created manually, as well as soils gpkg with soil polygons (in QGIS)
run `01_resample_layers.R` to create resampled versions of `1980_dayl` (not needed? may be able to skip this file),
jennings, soil_whc layers.

Add site id and lat long coordinates to `sites.csv`.  The whole site will be simulated with the climate at that point
Run `00_clim_data.R` to pull climate data for that site.  

```
burroughs/
├── 1980_dayl_resampled.nc4
├── dem
│   ├── aspect_nad83.tif
│   ├── dem_nad83.tif
│   ├── hillshade_nad83.tif
│   └── slope_nad83.tif
├── gridmet_1979_2023.csv
├── jennings_t50_coefficients.tif
├── macav2metdata_2006_2099.csv
└── soil
    ├── soil_whc_025.tif
    ├── soil_whc_100.tif
    └── ssurgo_soils.gpkg
```

Example site data available at https://huysman.net/research/core_areas/data.zip
