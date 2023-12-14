# 2021 Houston Power Outage: Socioecnomic Analysis on Recovery

![image](https://github.com/hazelvaq/2021-Texas-Power-Crisis/assets/108312152/df9b7be4-c77b-4ece-93f5-1a1b7e51fe5f)

[*Houston night lights after Feb 16, 2021 storm*](https://en.wikipedia.org/wiki/2021_Texas_power_crisis#/media/File:Houston_bmhd_2021047_lrg_Feb_16_2021.jpg)

This project analyzes how socioeconomic status affected recovery from the 2021 Houston snowstorm that caused power outages for more than 4.5 million homes. Using `R` 
I analyzed spatial data on remotely-sensed night light raster from highways and homes to determine which census blocks were affected the power outage. And pinpointing 
how many homes where affected by the storm. As well as the income distribution of the homes affected. Highlighted steps for this analysis include:

1. Raster manipulation with `stars` package
2. Raster reclassification
3. Highway removal through buffering
4. `SQL`data selection
5. `dplyr` summary statistics
6. Raster map development `ggplot2`

Additional information can be found in `texas_power.Rmd` and at my [blog.](https://hazelvaq.github.io/blog/2023-12-13-houston-power-outage/texas_power.html)


## Data Citations
Data was obtained from:
[Visible Infrared Imaging Radiometer Suite](https://ladsweb.modaps.eosdis.nasa.gov/missions-and-measurements/products/VNP46A1/)
[OpenStreetMap](https://www.openstreetmap.org/#map=4/38.01/-95.84)
[U.S. Census Bureau's American Community Survey](https://www.census.gov/programs-surveys/acs)

Data is currently not included in the repo and is included in the `.gitignore`

## File Structure

``` markdown
├── 2021-Texas-Power-Crisis.Rproj
├── data
│   ├── ACS_2019_5YR_TRACT_48_TEXAS.gdb
│   │    └── ACS_2019_5YR_TRACT_48_TEXAS.gdb
│   ├── gis_osm_buildings_a_free_1.gpkg
│   ├── gis_osm_roads_free_1.gpkg
│   └── VNP46A1
│       │   └── VNP46A1
│       ├── VNP46A1.A2021038.h08v05.001.2021039064328.tif
│       ├── VNP46A1.A2021038.h08v06.001.2021039064329.tif
│       ├── VNP46A1.A2021047.h08v05.001.2021048091106.tif
│       └── VNP46A1.A2021047.h08v06.001.2021048091105.tif
├── images
│   └── income_census.png
├── README.md
├── texas_power.html
└── texas_power.Rmd
```
