# SailLines: The 1779 Transatlantic Race
A stop-motion animation illustrating a race between two ships, El Rey and El Colon, as they navigate three distinct routes to determine the most efficient path. Designed to visualize comparative travel times, the animation blends storytelling with geographic insight to engage viewers in a dynamic exploration of maritime navigation.

<img src="./ShipRace Spain to Puerto Rico, 1770 720p.gif" img alt = "ShipRace GIF"/>

## How It's Made:

**Tech used:** <a href="https://www.esri.com/en-us/arcgis/products/arcgis-pro/overview" target="_blank" rel="noreferrer"> <img alt="ArcGIS Pro Badge" src="https://img.shields.io/badge/-ArcGIS Pro-000000?style=flat&logo=ArcGIS"></a>

The project opened with an animated display of interpolated ship paths, showing each ship’s movement frame by frame. To bring the animation to life, I needed to take several steps. First, I set up a per-feature filter using a range. This filter, connected to the "Hours_Travelled" field, allowed me to interactively filter the features on the map based on how long each ship had been at sea since leaving port. By synchronizing these filtered features with the exported video frames, I created the illusion of ships sailing across the ocean.

I navigated to the "Race Across the Atlantic" section in the bookmarks and selected the "Starting Line" bookmark. From there, I went to the "Logged Positions" layer in the Contents pane and opened the properties to add a range filter. I set the start field to "HOURS_TRAVELLED" and repeated this process for the "Interpolated Positions" layer. With the setup complete, a slider appeared on the side of the view and a "Range" tab on the ribbon. I activated the filter and set the maximum value to 24 and the span to 0, effectively showing a 24-hour snapshot of the journey. This allowed the animation to display each frame as a single day at sea, creating a stop-motion effect. 

Next, I used this range filter to build a stop-motion animation. I created individual images (frames) for each defined position of the ships. I zoomed to the "Starting Line" bookmark, reset the range slider, opened the Animation Timeline pane, and created the first keyframe. Then, I set the append time to display 25 states of the range slider per second and imported the remaining keyframes. This process generated an animation with 422 keyframes, one for each two-hour step, resulting in a total playtime of about 16.8 seconds, formatted for YouTube.

To mark the end of the race, I adjusted the final keyframes. I selected the 422nd keyframe and set up the camera to show the finish line. The fastest ship arrived after 29 days, meaning the keyframe for this moment was #349. I zoomed to keyframe 349, navigated to the "Finish Line" bookmark, and updated the camera. I verified the camera path, ensuring it tracked the ships smoothly by adjusting keyframes at intervals. Now, the camera followed the ships closely as they raced across the Atlantic.

With the animation set, I added lead-in and lead-out sections to provide context. To avoid a jarring start, I reset the animation to the beginning and added a three-second introduction. I zoomed to the "Overview" bookmark and clicked "Append" to create a smooth opening. To close, I added a three-second lead-out to highlight the race's conclusion.

Finally, I added title text and an overlay image to enhance viewer understanding. At keyframe 424, I selected all keyframes and added a title using the overlay tools. I adjusted the font for clarity and positioned it at the top center of the screen. I then included an image overlay, scaled to 40%, at the top left for additional context. After setting the final video options, I exported the completed animation.

This project transformed static data into a dynamic, engaging visual narrative, capturing the excitement of a race across the Atlantic and effectively communicating the story to the audience.

## Lessons Learned:

Throughout this project, I learned the importance of meticulous planning and attention to detail. Defining per-feature filters and synchronizing them with exported video frames taught me the value of precision in creating realistic animations. Handling a large volume of keyframes and ensuring smooth camera transitions highlighted the significance of methodical organization and iterative verification. Adding lead-in and lead-out sections, title text, and overlays emphasized the need to consider viewer engagement and comprehension. Overall, this project reinforced the importance of combining technical skills with effective organization to achieve successful results.

## Examples:
Take a look at these couple examples that I have in my own portfolio:

**TradeCurrents:** [TradeCurrents: Global Shipping in 1770](https://github.com/NomadCode33/NomadGeo/tree/main/CartoCraft/TradeCurrents)

**Lynnwood Right-of-Way:** [Lynnwood ROW Acquisition](https://github.com/NomadCode33/NomadGeo/tree/main/Furtado-Associates-Projects/Lynnwood%20ROW%20Acquisition)

**EcoPulse Report:** [EcoPulse Climate Analysis Report](https://github.com/NomadCode33/NomadGeo/tree/main/EcoPulse/EcoPulse%20Climate%20Analysis%20Report)

## Repositories
**Profile:** [NomadCode33](https://github.com/NomadCode33)

**Cartography Repository:** [CartoCraft](https://github.com/NomadCode33/NomadGeo/tree/main/CartoCraft)

**Main Repository:** [NomadGeo](https://github.com/NomadCode33/NomadGeo)
