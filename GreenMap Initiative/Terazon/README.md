# Terazon: Visualizing Land Cover Change in Rondonia
An interactive app visualizing land cover change in Rondônia, Brazil, from 1992 to 2020, emphasizing the transformation of forested areas into cropland and urban zones due to ongoing deforestation. Designed to inform environmental researchers, policymakers, and the public, the app presents temporal trends and spatial patterns to support awareness and conservation efforts.

<img alt = "Rondonia Land Cover Change GIF" img src="./Rondonia Land Cover Change from 1992 to 2020 Emeka Emeche - Google Chrome 2024-06-13 20-58-03.gif"/>

## How It's Made:

**Tech used:** <a href="https://www.esri.com/en-us/arcgis/products/arcgis-online/overview" target="_blank" rel="noreferrer"> <img alt="ArcGIS Online Badge" src="https://img.shields.io/badge/-ArcGIS Online-4d54b9?style=flat&logo=ArcGIS"></a>
<a href="https://www.esri.com/en-us/arcgis/products/arcgis-instant-apps/trial" target="_blank" rel="noreferrer"> <img alt="ArcGIS Instant Apps Badge" src="https://img.shields.io/badge/-ArcGIS Instant Apps-8FA17A?style=flat&logo=ArcGIS"></a>

I started by searching ArcGIS Online for a suitable web map and discovered the "Rondonia Land Cover Change from 1992 to 2020." It was the perfect foundation for my project. With this map in hand, I moved to ArcGIS Instant Apps, choosing the Media Map template—a great choice for allowing users to interact with and compare the data over time.

In the Search Settings, I enabled the Swipe tool, turning off the Express Mode window for more customization. For the Leading Layers pane, I selected "Rondonia Land Cover 2020_CLIM," and for the Trailing Layers pane, I chose "Rondonia Land Cover 1992_CLIM." This setup allowed for a side-by-side comparison of the maps using a slider tool, which I positioned at a starting point of 15 to give a clear view of the differences.

Moving to the Configuration panel, I switched the theme to dark under the Theme & Layout settings to enhance visual contrast and fixed the header to prominently display the app title. To make the web app accessible to a wider audience, I added multiple language options.

With everything in place, I published the web app, creating an interactive and visually compelling tool that invites users to explore the dramatic land cover changes in Rondonia over nearly three decades.

## Lessons Learned:

I discovered the process of sourcing web maps into an interactive app using ArcGIS Instant Apps. This tool proved to be incredibly handy, requiring minimal maintenance and allowing for quick creation. I felt a sense of accomplishment, much like a front-end developer, as I built and sustained an app that was up-to-date, functional, and user-friendly.

Moreover, I was thrilled to learn something new, expanding my skill set and eagerly anticipating future opportunities to apply these skills. The experience was both empowering and exciting, opening new avenues for creativity and professional growth.

## Examples:
Take a look at these couple examples that I have in my own portfolio:

**SeaRise3D:** [SeaRise3D: Miami Beach](https://github.com/NomadCode33/NomadGeo/tree/main/GreenMap%20Initiative/SeaRise3D)

**SailLines:** [SailLines: The 1779 Transatlantic Race](https://github.com/NomadCode33/NomadGeo/tree/main/CartoCraft/SailLines)

**COVID Cases Map:** [COViz: COVID Cases Interactive Map](https://github.com/NomadCode33/NomadGeo/tree/main/COViz/COViz-COVID%20Case%20Map)

## Repositories
**Profile:** [NomadCode33](https://github.com/NomadCode33)

**Climate Action Repository:** [GreenMap Initiative](https://github.com/NomadCode33/NomadGeo/tree/main/GreenMap%20Initiative)

**Main Repository:** [NomadGeo](https://github.com/NomadCode33/NomadGeo)
