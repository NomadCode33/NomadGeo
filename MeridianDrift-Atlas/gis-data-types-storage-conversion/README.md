# GIS Data Types, Storage, and Conversion

An exploration of geospatial data management focused on reading, writing, and converting between core GIS data formats using Python. Working with vector and raster data — Shapefiles, GeoJSON, and GeoTIFF — this project covers how to use Python geospatial libraries to open, inspect, plot, and convert spatial datasets sourced from both local files and remote databases.

## How It's Made:

**Tech used:** Python, GeoPandas, Fiona, OGR/GDAL, Rasterio, Matplotlib, JupyterLab

We started by setting up the environment and installing the libraries needed to handle the different data types covered in the project. From there, we downloaded the Natural Earth Quick Start Kit and organized the data into subfolders — `10m_cultural`, `50m_raster`, and `110m_cultural` — uploading each dataset into Jupyter before writing any code.

The project was structured around three core workflows. The first was reading and writing vector data with GeoPandas. We loaded a shapefile of world land boundary lines, inspected the attribute table with `df.head()`, checked the geometry types, and verified the coordinate reference system (EPSG:4326 / WGS 84). We then reprojected the data into a Mercator projection using `df.to_crs('epsg:3395')`, converted it to JSON with `df.to_json()`, and wrote it out as a new GeoJSON file using `df.to_file()`. The second workflow was reading and writing vector data with OGR. We pulled down MTBS wildfire point data and used the `osgeo.ogr` library to open the shapefile and extract its schema, comparing the OGR approach side-by-side with the GeoPandas one. We also used `!ogrinfo --formats` to list all available OGR-supported formats. The third workflow was reading and writing raster data with Rasterio and GDAL. We opened a GeoTIFF of the world (`NE1_50M_SR_W.tif`), inspected its band count, pixel dimensions (10800 x 5400), bounding box, and CRS, then read and plotted band 1 using Matplotlib. On the GDAL side, we used `!gdalinfo` to pull raster metadata and `!gdal_translate` to convert the GeoTIFF into a JPEG format.

For the independent section, I wrote the GeoJSON file created earlier back out using `df.to_file()`, then read it back in with GeoPandas and plotted it with `my_geojson.plot(color='black')`.

## Optimizations

One challenge that came up early was that `df.to_file()` threw a CRSError when trying to write the GeoJSON — the projection info wasn't being handled cleanly in the environment. Rather than blocking progress on the rest of the project, I flagged it with a comment and returned to resolve it in the independent section once the overall workflow was clearer. Working through the three libraries — GeoPandas, OGR, and Rasterio/GDAL — back to back made it easy to see where each one has an edge: GeoPandas is much more readable for attribute-table work, while OGR and GDAL give you lower-level control that's useful for format conversion and raster inspection. Using the `!` prefix inside Jupyter to run `ogrinfo` and `gdalinfo` directly from cells was also a cleaner approach than switching between the notebook and a terminal.

## Lessons Learned:

This project made it clear that knowing multiple tools for the same task is genuinely useful in GIS work — you're not always going to have the luxury of picking one library and sticking with it. GeoPandas makes reading and plotting shapefiles straightforward, but when you need to dig into schema structure or convert raster formats at the command level, OGR and GDAL are the right tools. Getting comfortable with how CRS information travels through a workflow — checking it, reprojecting it, and making sure it's preserved when writing to a new format — was probably the most practically useful takeaway. It's the kind of thing that causes silent errors downstream if you're not paying attention to it upfront.
