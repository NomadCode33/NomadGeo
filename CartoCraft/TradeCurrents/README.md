# TradeCurrents: Global Shipping in 1770
A 2D animation visualizing the maritime shipping routes of England, the Netherlands, and Spain in the year 1770. The animation dynamically unfolds over time, illustrating patterns of movement and trade to provide historical insight into 18th-century naval activity and colonial commerce.

<img src="./ShippingIn1770_gif_640x720p(3).gif" img alt = "Shipping in 1770 GIF"/>

## How It's Made:

**Tech used:** <a href="https://www.esri.com/en-us/arcgis/products/arcgis-pro/overview" target="_blank" rel="noreferrer"> <img alt="ArcGIS Pro Badge" src="https://img.shields.io/badge/-ArcGIS Pro-000000?style=flat&logo=ArcGIS"></a>

After downloading the data, I opened the map and navigated to the properties of the Ship Positions layer. In the Time tab, I selected "Filter Layer Content Based on Attribute Values" and set the Time Field to "ShipDate," confirming that each feature had a single time field. This enabled the time slider, which displayed a timeline from January 1, 1770, to December 31, 1770. To make the animation progress in weekly increments, I activated the Time Snapping option, set the units to days, and defined a span of 7 days.

Next, I enabled the Colonial Ports and Ship Paths layers in the Contents pane. The map was overly bright, making it difficult to discern details, so I adjusted the transparency settings: 50% for the Colonial Ports layer and 90% for the Ship Paths layer. These adjustments allowed the Ship Positions to stand out while the paths and ports faded into the background. To further enhance the map's appearance, I changed the background color to a custom dark gray, creating a more cohesive and visually calming effect.

With the map properly set, it was time to create temporal keyframes to illustrate the movement of ships throughout the year. I started by defining the change in temporal extent for each time step, setting the first keyframe in the animation. In the Time tab, I locked the Span to 7 days and verified that the Start field was set to January 1, 1770. I then moved to the View tab, clicked "Add Animation" in the Animation group, and opened the Animation Timeline pane. I created the first keyframe, then adjusted the spatial extent by panning the map to place Antarctica at the base of the frame, leaving space at the top for the title.

Initially, I chose the Twitter preset for the video export, but I switched to the YouTube preset for a wider resolution. Back in the Time tab, I confirmed the 7-day span was locked, and set the End field to December 31, 1770. Returning to the Animation Timeline pane, I clicked "Append Next Keyframe" to add a second keyframe and set the animation duration to 12 seconds to ensure a smooth and easy-to-follow playback.

To effectively communicate the changing dates, I added dynamic text overlays to the video. In the Overlay group, I updated the title to "World Shipping (1770)" and formatted the font for clarity. I then selected both keyframes in the Animation Timeline pane and added dynamic text using the predefined HTML tag `<dyntype="animation" property="endTime" format="short"/>`, which dynamically displayed the end date of each keyframe in the upper-left corner. As the animation played, the date updated in sync with the movement of the ships.

To simplify the display, I modified the dynamic text element to `<dyntype="animation" property="endTime" format="MMMM"/>` to show only the month name. I positioned this text at the bottom-center of the screen and adjusted the advanced text properties to remove the callout style, making the text easier to read during fast playback.

With everything in place, I exported the animation using the appropriate video settings, completing a dynamic visualization that captured the ebb and flow of global shipping routes in 1770. The final video effectively conveyed the story of maritime movement, bringing history to life through a compelling and engaging animation.

## Optimizations

The resolution could be slightly shorter, as the empty space risks breaking immersion. However, it could also be seen as part of the setpiece, ultimately making it inoffensive in the long run.

## Lessons Learned:

I relish the feeling of being a director creating my own movie. Through this process, I've gained a deeper understanding of how to make animation meaningful and informative for the viewer. It requires a great deal of foresight and planning to ensure that each frame is meticulously crafted, much like directing a flawless movie scene. Without these fundamental skills, an animation can easily become all style and no substance.

## Examples:
Take a look at these couple examples that I have in my own portfolio:

**StormChronicles:** [StormChronicles: Hurricanes since 1851](https://github.com/NomadCode33/NomadGeo/tree/main/CartoCraft/StormChronicles) 

**Sumner Jurisdiction Boundary:** [Sumner Jurisdiction Boundary](https://github.com/NomadCode33/NomadGeo/tree/main/Furtado-Associates-Projects/Sumner%20Jurisdiction%20Boundary)

**BayouWaters:** [BayouWaters: A New Orleans Risk Model](https://github.com/NomadCode33/NomadGeo/tree/main/BayouWaters)

## Repositories
**Profile:** [NomadCode33](https://github.com/NomadCode33)

**Cartography Repository:** [CartoCraft](https://github.com/NomadCode33/NomadGeo/tree/main/CartoCraft)

**Main Repository:** [NomadGeo](https://github.com/NomadCode33/NomadGeo)
