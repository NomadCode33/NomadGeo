# StormChronicles: Hurricanes since 1851
A detailed map projection showcasing the projected paths and frequencies of hurricanes worldwide since 1851, providing a comprehensive view of historical hurricane patterns to analyze trends.

<img alt = "Hurricane" img src="./Hurricane_Projection_EmekaEmeche.jpg"/>

## How It's Made:

**Tech used:** <a href="https://www.esri.com/en-us/arcgis/products/arcgis-pro/overview" target="_blank" rel="noreferrer"> <img alt="ArcGIS Pro Badge" src="https://img.shields.io/badge/-ArcGIS Pro-000000?style=flat&logo=ArcGIS"></a>

I began by gathering four key datasets: the NASA basemap image, NOAA's historic hurricane data, coastlines and graticules, and a collection of Firefly icon images. To create a captivating visual experience, I chose the South Pole Stereographic Projection. This projection accentuates the circular patterns of storms across the globe, drawing attention to the storm density in the Northern Hemisphere.

To make the hurricane points stand out, I modified the basemap, darkening it and boosting its saturation to enhance contrast. I also adjusted the grayscale of the basemap to be slightly transparent, allowing subtle colors to peek through and adding depth to the map.

Next, I incorporated the Firefly icons in the Content pane, linking them to the hurricane data points to create a dynamic visual effect. To draw the viewer's focus to the center, I added a vignette, which softly darkens the edges of the map.

At the bottom of the map, I placed a bar chart that compares hurricane occurrences by year. Beneath the chart, I added annotation text that provides context about the history of hurricanes and explains how measurement methods have evolved over time. This combination of striking visuals and informative text creates a comprehensive and engaging representation of the data, inviting viewers to explore and understand the story of hurricanes worldwide.

## Optimizations

Increasing the font size for the title could help draw more attention to it without detracting from the map. This adjustment is subtle and should be unobtrusive, enhancing the overall presentation without overwhelming the visual elements.

## Lessons Learned:

What I've learned here is the importance of going beyond the basics and experimenting. When creating a map, I considered it from a viewer's perspective. If I had made a basic map of hurricanes with only minor quality-of-life changes, it would have been readable but dull, and the impact of the information would have been lost. Instead of presenting mere data points, I aimed to create a map that vividly depicts roaring hurricanes.

While the basics are crucial, art and presentation significantly enhance how the message is conveyed to viewers. This approach can inspire curiosity about the topic and even motivate action. Small details can make a big difference in effective storytelling through maps. The skills I've learned in basemap and icon construction have taught me to be intentional in my mapmaking, ensuring that every element contributes to a compelling and informative visual narrative.

## Examples:
Take a look at these couple examples that I have in my own portfolio:

**SpilView:** [SpilView: Seeing the World Through Oceans](https://github.com/NomadCode33/NomadGeo/tree/main/CartoCraft/SpilView)

**DemoGraphIt Map:** [DemoGraphIt: Interactive Census Mapping Tool](https://github.com/NomadCode33/NomadGeo/tree/main/DemoGraphIt)

**West Seattle Light Rail Survey:** [West Seattle Light Rail Survey](https://github.com/NomadCode33/NomadGeo/tree/main/Furtado-Associates-Projects/West%20Seattle%20Light%20Rail%20Survey)

## Repositories
**Profile:** [NomadCode33](https://github.com/NomadCode33)

**Cartography Repository:** [CartoCraft](https://github.com/NomadCode33/NomadGeo/tree/main/CartoCraft)

**Main Repository:** [NomadGeo](https://github.com/NomadCode33/NomadGeo)
