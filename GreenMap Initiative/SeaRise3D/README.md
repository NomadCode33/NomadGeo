# SeaRise3D: Miami Beach
A dynamic 3D map highlighting buildings in Miami, Florida projected to be at risk from sea level rise by 2030, 2050, and 2090, using spatial analysis to identify vulnerable infrastructure and enable city officials, developers, and climate resilience teams to prioritize mitigation and long-term adaptation efforts.

<img alt = "Sea Level Rise GIF" img src="./ArcGIS - City of Miami Beach Sea Level Rise_EmekaEmeche (3).gif"/>

## How It's Made:

**Tech used:** <a href="https://www.esri.com/en-us/arcgis/products/arcgis-pro/overview" target="_blank" rel="noreferrer"> <img alt="ArcGIS Pro Badge" src="https://img.shields.io/badge/-ArcGIS Pro-000000?style=flat&logo=ArcGIS"></a>
<a href="https://www.esri.com/en-us/arcgis/products/arcgis-online/overview" target="_blank" rel="noreferrer"> <img alt="ArcGIS Online Badge" src="https://img.shields.io/badge/-ArcGIS Online-4d54b9?style=flat&logo=ArcGIS"></a>
<a href="https://livingatlas.arcgis.com/en/home/" target="_blank" rel="noreferrer"> <img alt="ArcGIS Living Atlas Badge" src="https://img.shields.io/badge/-ArcGIS Living Atlas-43A047?style=flat&logo=ArcGIS"></a>
<img alt="Phone Number Badge" src="https://img.shields.io/badge/-ArcGIS 3D Analyst Extension-000000?style=flat&logo=None">

I started by downloading a dataset of Miami and transforming a flat 2D map into an immersive 3D display. My first challenge was to set the extrusion of the buildings. Initially, all structures appeared uniform in height, so I used the join field tool to merge tables, transferring accurate height attributes to reflect the city's varied skyline. To make the buildings even more realistic, I created multipatch layers and applied textures using the symbology pane and a rule package file (RPK). This added details like windows and modified roof shapes for a more lifelike appearance. Next, I incorporated water data to create a dynamic 3D effect and adjusted the lighting to mimic the glow of an 8 AM sunrise.

With the foundational elements in place, I turned my attention to sea level rise. I sourced data from the ArcGIS Living Atlas of the World, specifically layers showing intermediate-high sea level rise projections for 2030, 2050, and 2090 from NOAA's Digital Coast. I used the Environments Geoprocessing tool to configure this data, converting it from raster to polygons for better interactivity.

Next, I assessed the impact of rising sea levels on Miami's buildings. I filtered the building layer using the Select by Location tool with sea level rise data for 2030, 2050, and 2090. To show when each building might be affected, I added a column in the attribute table named "Inundated_Year." I then used the symbology pane to assign colors indicating risk levels: green for safe, light orange for 2030, dark orange for 2050, and red for 2090.

To deepen my analysis, I used the Elevation Profile tool to measure the heights of buildings. This revealed that those at lower elevations were more vulnerable, highlighting the critical need for future developments to account for sea level rise.

Finally, I uploaded the completed 3D map to ArcGIS Online, making it accessible for public viewing and engagement.

## Optimizations

To enhance this project, incorporating a web app would be highly beneficial. This web app would allow the community and decision-makers in Miami Beach to interact with the analysis results and visualize the impact of rising sea levels over time. By providing an accessible and user-friendly platform, stakeholders can better understand the data, explore different scenarios, and make informed decisions to address the challenges posed by sea level rise.

## Lessons Learned:

I never would have imagined I could create a map like this; it was definitely a rewarding learning experience. Throughout the process of developing this 3D map, I was thrilled to see it improve over time. I mastered valuable tools such as the environments geoprocessing tool, raster to polygon conversion, and the use of RPK files, among others. The end result was impressive, and I gained a deeper understanding of the many ways GIS can be used to convey complex topics. With this newfound knowledge, I am now equipped to create more detailed and impactful 3D maps to address various global issues.

## Examples:
Take a look at these couple examples that I have in my own portfolio:

**ThermaRisk:** [ThermaRisk: Mapping Urban Heat Risk in Athens](https://github.com/NomadCode33/NomadGeo/tree/main/GreenMap%20Initiative/ThermaRisk)

**OsoShift:** [OsoShift: Oso Landslide Story](https://github.com/NomadCode33/NomadGeo/tree/main/CartoCraft/OsoShift)

**West Seattle Light Rail Survey:** [West Seattle Light Rail Survey](https://github.com/NomadCode33/NomadGeo/tree/main/Furtado-Associates-Projects/West%20Seattle%20Light%20Rail%20Survey)

## Repositories
**Profile:** [NomadCode33](https://github.com/NomadCode33)

**Climate Action Repository:** [GreenMap Initiative](https://github.com/NomadCode33/NomadGeo/tree/main/GreenMap%20Initiative)

**Main Repository:** [NomadGeo](https://github.com/NomadCode33/NomadGeo)
