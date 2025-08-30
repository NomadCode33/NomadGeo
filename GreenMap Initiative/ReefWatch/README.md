# ReefWatch: Coral Reef Health Monitoring Dashboard
An interactive dashboard visualizing coral reef pollution and ecosystem health across local, regional, and global scales. Designed to support marine scientists, conservationists, and policymakers, the dashboard integrates multi-scale data to monitor reef conditions, identify pollution sources, and inform targeted preservation strategies.

<img alt = "Coral Reef Dashboard GIF" img src="./Coral Reef Bleaching Dashboard_EmekaEmeche (1).gif"/>

## How It's Made:

**Tech used:** <a href="https://www.esri.com/en-us/arcgis/products/arcgis-online/overview" target="_blank" rel="noreferrer"> <img alt="ArcGIS Online Badge" src="https://img.shields.io/badge/-ArcGIS Online-4d54b9?style=flat&logo=ArcGIS"></a>
<a href="https://www.esri.com/en-us/arcgis/products/arcgis-dashboards/overview" target="_blank" rel="noreferrer"> <img alt="ArcGIS Dashboards Badge" src="https://img.shields.io/badge/-ArcGIS Dashboards-e89204?style=flat&logo=ArcGIS"></a>

I began by diving into ArcGIS Online to search for the NOAA Coral Reef Watch data. Opening the data in Map Viewer, I carefully examined all the layers and features to prepare the web map for the dashboard. The attribute table revealed crucial information, such as Degree Heating Weeks and Alert Levels, which would be central to the dashboard's purpose. I selected the "Human Geography Dark Map" from the Basemap options and zoomed in to frame the coral monitoring areas perfectly. With the map view set, I saved the map and added all the necessary details before moving on to create a new dashboard. Choosing a dark theme to enhance visibility, I updated the header to display the dashboard's title.

Next, I wanted to show the monitoring status at each virtual station, so I added a list element that sorted them by the highest accumulated heat stress. Using the "Add Element" button, I selected "List" and positioned it on the left side of the dashboard. I linked the list to the layers from the Coral Reef Bleaching web map and expanded the NOAA Coral Reef Watch (CRW) Virtual Stations layer. Sorting by Degree Heating Weeks in descending order, I updated the list to dynamically display the monitoring status for each station, allowing viewers to see which reefs were experiencing the most stress.

To make the data more interactive, I enabled the "Show Pop-Up" option in the Actions tab for the Coral Reef Bleaching feature, so that a pop-up would display details whenever a location was selected. Then, I added a serial chart to visualize the number of virtual stations by alert level, ranging from 0 (no bleaching) to 4 (severe bleaching). I placed this chart beside the list, sourcing the data from the Coral Reef Bleaching web map and focusing on the NOAA Coral Reef Watch (CRW) Virtual Stations layer. I chose "Alert Level" as the Category Field, customized the x-axis labels, and set the y-axis to display the "Number of Coral Stations." To represent the severity of coral bleaching visually, I assigned different colors to the alert levels: light blue for "No Alert," light yellow for "Watch," peach for "Warning," light brown for "Level 1," and dark brown for "Level 2." These colors helped users quickly grasp the status of each reef.

To enhance the interactivity, I ensured that the elements shared a common data source. In the Actions tab, I set the Target Field to "Alert Level," so that clicking on a bar in the graph would highlight the corresponding locations on the map.

For a final touch, I added an indicator element at the top left corner of the map to display dynamic summary statistics. This indicator showed the number of virtual stations where the coral reef was at risk of bleaching. I linked it to the Coral Reef Bleaching web map from the NOAA Coral Reef Watch (CRW) Virtual Stations layer. Using the Data Options pane, I built an expression filter stating "Alert Level Greater Than Or Equal to 3" to highlight stations with Level 1 or 2 alerts. To provide context, I included the total number of stations in the reference section and chose "Statistic" as the reference type. The indicator now read, "Coral reefs at risk of bleaching" alongside the total station count, offering a clear and immediate understanding of the situation.

Lastly, I configured the actions to ensure that all the dashboard elements could interact seamlessly, creating a cohesive, engaging experience for viewers. With the dashboard complete, I had a powerful tool ready to monitor and raise awareness about the health of coral reefs worldwide.

## Lessons Learned:

I discovered how to source web maps from ArcGIS Online into ArcGIS Dashboards to create dynamic and interactive maps. By isolating specific layers, I ensured they were prominently displayed on the dashboard I was creating. Utilizing data points from these layers allowed the pop-ups to convey meaningful information, enhancing the viewing experience and inspiring people to take action. 

With a variety of customization options at my disposal, I could design a stylish and personalized layout on Dashboards. I was thrilled by the process and amazed at how even small actions could culminate in a tool that could help many people and drive societal change. The versatility of GIS continuously astonishes me, given its straightforward premise of creating maps for others to use.

Witnessing the interactivity between different apps on ArcGIS coming together to create fantastic products was both fascinating and gratifying. It’s incredible to see how these tools can seamlessly integrate to produce something impactful and beneficial.

## Examples:
Take a look at these couple examples that I have in my own portfolio:

**ImpactAtlas:** [ImpactAtlas: Climate Change Through Spatial Insight](https://github.com/NomadCode33/NomadGeo/tree/main/GreenMap%20Initiative/ImpactAtlas)

**Lynnwood Right-of-Way:** [Lynnwood ROW Acquisition](https://github.com/NomadCode33/NomadGeo/tree/main/Furtado-Associates-Projects/Lynnwood%20ROW%20Acquisition)

**COVID Rates Map:** [COViz: COVID Rates Interactive Map](https://github.com/NomadCode33/NomadGeo/tree/main/COViz/COViz-COVID%20Rates%20Index)

## Repositories
**Profile:** [NomadCode33](https://github.com/NomadCode33)

**Climate Action Repository:** [GreenMap Initiative](https://github.com/NomadCode33/NomadGeo/tree/main/GreenMap%20Initiative)

**Main Repository:** [NomadGeo](https://github.com/NomadCode33/NomadGeo)
