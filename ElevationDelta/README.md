# ElevationDelta — Raster Analysis of Pre- and Post-Flood Terrain Change

An exploration of raster data processing focused on opening, inspecting, classifying, and comparing lidar-derived raster datasets using Python. Working with Digital Terrain Models (DTM), Digital Surface Models (DSM), and Canopy Height Models (CHM) — all in GeoTIFF format — this project covers how to use Python geospatial libraries to read raster data, handle no data values, perform raster math, and produce classified raster maps that visualize change over time. The dataset is lidar-derived NEON data from Boulder, Colorado, capturing terrain and vegetation conditions before and after the 2013 flood.

---

## How It's Made:

**Tech used:** Python, rioxarray, xarray, NumPy, GeoPandas, EarthPy, Matplotlib, Seaborn, JupyterLab

The project started with installing and importing the required libraries — `rioxarray`, `earthpy`, and `GeoPandas` — and downloading the Colorado Flood dataset using `et.data.get_data()`. The working directory was set using `os.chdir()` to point into the `earth-analytics/data` folder where all the raster files live.

The project was structured around two core workflows.

**Q1 — Inspecting a raster file:** The pre-flood Canopy Height Model (`lidar_chm.tiff`) was opened using `rxr.open_rasterio()` with `masked=True` and `.squeeze()` to remove the extra band dimension that would otherwise cause plotting issues. From there, the CRS and no data values were printed for both the DEM and DSM versions of the raster file to verify the spatial metadata. The CRS came back correct, but the no data value returned `nan` rather than a properly defined value — meaning it wasn't cleanly set in the raster file's metadata. The spatial extents and resolutions of the two raster layers were then compared using `.rio.bounds()` and `.rio.resolution()` to confirm they matched before any raster math was attempted. A CHM was calculated by subtracting the DTM from the DSM and plotted using a Greens colormap. Because the `lidar_chm.tiff` file didn't have distinct classified layers, the output rendered as a single-tone green raster rather than a multi-class map.

**Q2 — Plotting change over time:** This section involved working with four raster files — pre- and post-flood versions of both the DTM (`pre_DTM.tif`, `post_DTM.tif`) and DSM (`pre_DSM.tif`, `post_DSM.tif`). Each was opened using `rxr.open_rasterio()` with masking and squeezing applied. Pre-flood and post-flood CHMs were derived separately by subtracting the DTM from the DSM for each time period. The two CHMs were then subtracted from each other to produce a difference raster capturing how canopy height changed as a result of the flood. The same workflow was repeated using just the DTM layers to isolate terrain-level change independent of vegetation.

Both difference rasters were classified using `np.digitize` through `xr.apply_ufunc()`, with class bins set at `[-np.inf, 2, 7, 12, np.inf]` to separate short, medium, tall, and really tall tree height categories. Missing data pixels (classified as value 5 from the digitize output) were masked out using `.where()`. Final classified raster maps were produced using `ListedColormap` and `BoundaryNorm` for discrete color bins, with custom legends added via `ep.draw_legend()` from EarthPy, and titles set on each plot.

The CHM change map showed that before and after the flood, medium and tall trees dominated the left side of the study area, with that cluster appearing largely undisturbed post-flood. The terrain change map told a different story — the majority of the post-flood raster shifted toward short tree classifications, with medium, tall, and really tall categories becoming sparse and scattered, suggesting significant vegetation and ground surface disruption across much of the area.

---

## Optimizations

One issue that came up early in Q1 was that the no data value for the raster wasn't properly defined — it printed as `nan` rather than a recognized nodata flag. This is the kind of thing that can quietly break raster calculations or skew color scales without throwing an obvious error, so catching it early by explicitly printing `rio.nodata` before doing anything else was the right call.

Checking that the spatial extent and resolution of the raster layers matched before subtracting them was also important. Raster math in Python is matrix subtraction — if the dimensions don't line up perfectly, the results won't make sense. Using `.rio.bounds()` and `.rio.resolution()` to confirm alignment before running the CHM calculation kept that from becoming a problem.

Using `masked=True` and `.squeeze()` together every time a raster was opened became the consistent pattern throughout the project. `masked=True` ensures no data values don't pollute calculations, and `.squeeze()` drops the extra band dimension that rioxarray adds by default — both are easy to forget and both cause downstream issues if skipped.

---

## Lessons Learned

This project made it clear that raster data processing is a lot more than just opening a file and making a plot. Getting to a meaningful classified raster map required understanding the structure of the data — what the band dimension is, why no data values matter, how CRS travels through a workflow, and why spatial alignment between layers has to be verified before any math happens.

The raster subtraction approach for deriving change over time (CHM difference, terrain difference) is straightforward in concept but requires all the upstream steps to be correct. If the rasters aren't masked properly, or their extents don't match, or the no data value is undefined, the difference raster will contain garbage values and any classification you apply on top of that will be meaningless.

The classification step using `np.digitize` was a good example of how raster reclassification works in practice — assigning pixel values to bins based on defined breakpoints and mapping those bins to discrete categories. The extra class that digitize creates for values below the lowest bin is easy to miss and leads to a visually confusing plot until you mask it out with `.where()`.

Working through both the canopy height and terrain change analyses side by side also made it easier to see what the flood actually did to the landscape — the CHM map captured what happened to the trees, while the DTM map showed what happened to the ground itself.
