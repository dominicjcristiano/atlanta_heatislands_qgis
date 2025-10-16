# atlanta_heatislands_qgis
Mapping summer 2025 mean temperatures for the five counties of Metro Atlanta, using MODIS data

This project looks at the mean temperatures from June - August 2025 of the greater Atlanta, GA, USA area.
# Data Files
  The data files used for this project can be found here:
  MODIS: https://lpdaac.usgs.gov/products/mod11a2v006/
  Census tracts: https://www.census.gov/geographies/mapping-files/time-series/geo/tiger-line-file.html

# Methods
  
Data obtained and added to QGIS project

MODIS files were converted from hdf to tif using gdal 

Reprojected tifs to the correct format using GDAL → Raster projections → warp (reproject) → batch → nearest neighbor

Clipped tifs to the boundary of the 5 atlanta counties (Fulton, DeKalb, Cobb, Clayton, Gwinnet)

Converted data in tifs from K to C by subtracting 273.15 

Aggregated 26 rasters to get average value for each pixel (GRASS r.series)

Added “ironbow” color pallete to show brighter colors as the higher temperatures

Created map layout and exported PDF
