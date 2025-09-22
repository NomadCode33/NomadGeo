# Sumner Jurisdiction Boundary
An independent mapping project focused on creating a comprehensive and accurate boundary map of the Sumner area using ArcGIS Pro. The workflow included defining the project boundary, collecting and cleaning relevant geospatial datasets, and integrating the data into Autodesk Civil 3D to enhance data management and visualization. The project concluded with the production of a high-resolution raster map, providing a detailed and visually rich representation of the Sumner region.

**Disclaimer:** Furtado & Associates maintains a policy of not allowing company property for personal use, so I don't have any documents or pictures of my project. However, I can describe the work I did and the process we followed.

## How It's Made:

**Tech used:** <a href="https://www.esri.com/en-us/arcgis/products/arcgis-pro/overview" target="_blank" rel="noreferrer"> <img alt="ArcGIS Pro Badge" src="https://img.shields.io/badge/-ArcGIS Pro-000000?style=flat&logo=ArcGIS"></a>  ArcGIS Online, Autodesk Civil 3D, Microsoft Excel, Office Database

### Sumner Boundary Map: A Journey Through Data Mapping

Creating the Sumner Boundary Map was one of my proudest achievements, a project I tackled independently without any outside assistance. The process began with opening ArcGIS Pro and understanding the project scope, which in this case, centered around the area of Sumner.

To ensure accuracy, I adjusted the coordinate system to align with Furtado’s specialized system, known for its precision. This meticulous approach is why many companies, including Sound Transit, prefer working with Furtado. They rely on our accurate and timely project completions.

I started by establishing the project boundary. Using ArcGIS’s polygon tool, I defined the boundary area and employed the Feature Class to Feature Class tool to incorporate and cleanse the data. This step is akin to inheriting older data and making it our own by refining and optimizing it for quicker loading and rendering, especially important for larger datasets. After adding the boundary to the database, I changed its color to red in the Symbology pane for clear visualization.

With the boundary set, the next step was gathering datasets. I scoured open sources like the county GIS portal and ArcGIS Online, searching for various data types, including GPS data, water systems, wastewater, storm drains, and other utilities. Verifying metadata was crucial, ensuring all data was accurate and relevant.

Using the ETL (Extract, Transform, Load) process, I cleaned and organized the data. The Feature Class to Feature Class tool helped transfer new data into my database for easy access. Checking the attribute table and metadata allowed me to filter data using the Select By Location and Selection By Attributes for Boundaries tools, ensuring only the relevant information was highlighted.

For example, to filter out culverts, I used the attribute table to select specific columns and create new layers from the selections. Each dataset had multiple types, necessitating further splitting for project clarity. Geographic coordinates were added when missing, using the Calculate Geometry Attributes tool to ensure accuracy.

The next phase involved integrating data from ArcGIS into Autodesk Civil 3D for better management and visualization. This integration allowed for precise area specifications and comprehensive project scopes. I used the Feature Class to Shapefile tool to export GIS data into Autodesk CAD software, organizing the data into specific folders for sanitary sewers, stormwater, and water, and further subdividing into points or line data.

In Autodesk Civil 3D, I imported shapefiles, starting with the map boundary, followed by other data types. Line values required plotting on the map, setting spatial filters, and assigning colors through the layer properties. Point values needed block standards assignment, ensuring each point type (e.g., hydrants, water valves) was correctly labeled and scaled for visibility.

Creating labels and pipes involved returning to ArcGIS Pro. I added new fields in the attribute table, calculated geometry attributes, and generated points along lines. These points were then exported to Excel for further processing. In Excel, new columns were added, merging data for easier label generation when transferred back to ArcGIS.

After refining the data, I imported it back into ArcGIS and matched everything to the original layers for label visibility in Autodesk Civil 3D. This meticulous process ensured each label was correctly placed and formatted. In Civil 3D, I finalized the labels, adjusting their properties, colors, and scales to match the utility classification layers.

### Creating the Raster Map

Next, I embarked on creating a raster map, which represented Sumner’s features and characteristics as a grid of pixels. I started by setting the map’s coordinate system in ArcGIS to Furtado’s custom system. Adding aerial data for Sumner and defining the project boundary with a bright red dashed line made it stand out.

For larger project scopes, subdividing boundaries was necessary to manage data efficiently. I added a new field in the attribute table, subdivided the polygon, and measured distances to create equal parts. These subdivisions were essential for converting the map into manageable raster tiles, ensuring faster rendering times.

With the boundary set, I prepared to create raster map files. Turning off unnecessary layers, I focused on the Sumner Aerial data, zooming to the desired tile. Exporting the layout as a GeoTIFF, I opted for a high resolution of 1000 DPI with a 32-bit color depth and a transparent background. This high-quality output was saved to my office database’s raster folder, ensuring detailed and accurate visual representation of the area.

Through this intricate process, the Sumner Boundary Map came to life, a testament to meticulous planning, precise data handling, and seamless integration across multiple platforms. Each step was a blend of technical skill and creative problem-solving, ensuring the final product was not only accurate but also visually engaging and easy to interpret.

## Optimizations

Crafting the Sumner Boundary Map was a meticulous journey that demanded precision and a deep understanding of Geographic Information Systems (GIS). One of the first steps was aligning the project with Furtado’s specialized coordinate system. This alignment was crucial for achieving the high precision and accuracy required for reliable project outcomes, ensuring that every detail was mapped with exactness.

To manage and optimize the data efficiently, I employed the Extract, Transform, Load (ETL) process alongside the Feature Class to Feature Class tool. This combination was instrumental in cleaning and organizing the data, which significantly improved both the quality of the data and the speed at which it could be loaded and processed. 

Highlighting only the relevant information was another key optimization. By using the Select By Location and Selection By Attributes for Boundaries tools, I could filter the data effectively, making it more manageable and focused. This selective data highlighting ensured that the most pertinent information was readily accessible, streamlining the entire project.

Integrating the data into Autodesk Civil 3D was a transformative step. By exporting GIS data to Autodesk CAD software via the Feature Class to Shapefile tool, I optimized data management and visualization. This integration enabled precise area specifications and comprehensive project scopes, allowing for detailed and accurate visual representations of the mapped areas.

Creating the raster map involved subdividing boundaries and exporting high-resolution GeoTIFF files. This step was essential for faster rendering times and achieving a detailed visual representation of Sumner. The high-resolution output ensured that the final map was both visually appealing and highly usable, providing a clear and detailed overview of the area.

These optimizations collectively enhanced the project's efficiency, accuracy, and visual appeal. They were crucial in the successful creation of the Sumner Boundary Map, demonstrating a blend of technical prowess and creative problem-solving that brought the map to life.

## Lessons Learned:

One of the most significant lessons from the Sumner Boundary Map project was the importance of precision and attention to detail. Adjusting the coordinate system to align with Furtado’s specialized system ensured accuracy and reliability, which is why companies like Sound Transit trust our work. The meticulous approach to data handling, from gathering to cleansing and verifying metadata, highlighted the critical role of data integrity in mapping projects.

Another key lesson was the value of seamless integration across different platforms. The process of transferring data from ArcGIS to Autodesk Civil 3D demonstrated the necessity of compatibility and the benefits of using the right tools for specific tasks. This integration allowed for better management and visualization, making the project scope more precise and comprehensive.

Lastly, the project emphasized the importance of continuous learning and adaptation. Each step, from creating labels and pipes to generating raster map tiles, required a blend of technical skills and creative problem-solving. This experience underscored the need to stay updated with the latest tools and techniques in GIS and data mapping.

## Examples:
Take a look at these couple examples that I have in my own portfolio:

**Lynnwood Right-of-Way:** [Lynnwood ROW Acquisition](https://github.com/NomadCode33/NomadGeo/tree/main/Furtado-Associates-Projects/Lynnwood%20ROW%20Acquisition)

**BayState Map:** [BayState: Map of Massachusetts](https://github.com/NomadCode33/NomadGeo/tree/main/CartoCraft/BayState%20Map)

**COVID Rates Map:** [COViz: COVID Rates Interactive Map](https://github.com/NomadCode33/NomadGeo/tree/main/COViz/COViz-COVID%20Rates%20Index)

## Repositories
**Profile:** [NomadCode33](https://github.com/NomadCode33)

**Furtado & Associates Repository:** [Furtado & Associates Projects](https://github.com/NomadCode33/NomadGeo/tree/main/Furtado-Associates-Projects)

**Main Repository:** [NomadGeo](https://github.com/NomadCode33/NomadGeo)
