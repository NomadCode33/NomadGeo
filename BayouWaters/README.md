# BayouWaters: A New Orleans Risk Model (Post Hurricane Data Analysis)
A collaborative mapping project analyzing hurricane-induced flooding in New Orleans, a city especially vulnerable due to its low-lying terrain and proximity to the Gulf of Mexico. Through advanced cartographic techniques, the project supports residents, emergency responders, and policymakers in improving preparedness and mitigation strategies—while emphasizing the importance of equitable investment in high-risk areas to avoid deepening existing socio-economic disparities.

**Link to Project:** https://nomadcode33.github.io/BayouWaters/

<img src="https://github.com/NomadCode33/git-lfs/blob/main/New%20Orleans%20Flood%20Risk.gif" img alt = "New Orleans Flood Risk Website"/>

## Introduction

For our project we will examine hurricane flooding in New Orleans. New Orleans is located just off of the Gulf of Mexico, a tropical storm generating body of water. Due to New Orleans location, and its general topography being relatively low with some areas below sea level, it is very vulnerable to hurricanes. In 2005, the city was hit by Hurricane Katrina, (facts here, discuss displacement and destruction). With the onset of global warming causing more extreme weather events around the world, it becomes increasingly important to equip cities like New Orleans with tools to mitigate and respond to these natural disasters which may become more frequent and intense with time. Using our skills as cartographers, we aim to examine the city and the risk posed by future hurricanes to provide a tool for potential damage mitigation and emergency response development.

The intended audience of the project are residents of the area, and also any emergency responding groups. City and state offices and policy-makers are likewise an important audience as a powerful agent in enacting fiscally sourced change such as infrastructure development.

Positive impacts of the project are better preparing residents of New Orleans for future hurricanes, as well as giving policy-makers and emergency responders better tools to understand the nature of hurricanes and flooding in New Orleans to better protect the population and reduce damage and risk to public safety. Impacts could also include the development of new infrastructure to better aid in emergency situations. Negative impacts could include policy-makers choosing to invest less in zones deemed at high risk for flooding, which could worsen socio-economic disparities in the city and put lives at greater risk. We could attempt to avoid this by emphasizing the need to invest in higher risk zones to bring down overall risk in the city.

## How It's Made:

**Tech used:** <a href="https://developer.mozilla.org/en-US/docs/Web/HTML" target="_blank" rel="noreferrer"> <img alt="HTML5 Badge" src="https://img.shields.io/badge/-HTML5-000000?style=flat&logo=HTML5"></a> 
<a href="https://developer.mozilla.org/en-US/docs/Web/CSS" target="_blank" rel="noreferrer"> <img alt="CSS3 Badge" src="https://img.shields.io/badge/-CSS3-000000?style=flat&logo=CSS"></a>
<a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript" target="_blank" rel="noreferrer"> <img alt="JavaScript Badge" src="https://img.shields.io/badge/-JavaScript-000000?style=flat&logo=JavaScript"></a>
<a href="https://code.visualstudio.com/" target="_blank" rel="noreferrer"> <img alt="Visual Studio Code Badge" src="https://img.shields.io/badge/-Visual Studio Code-000000?style=flat&logo=None"></a>
<a href="https://github.com/" target="_blank" rel="noreferrer"> <img alt="GitHub Badge" src="https://img.shields.io/badge/-GitHub-000000?style=flat&logo=GitHub"></a>
<a href="https://www.mapbox.com/" target="_blank" rel="noreferrer"> <img alt="Mapbox Badge" src="https://img.shields.io/badge/-Mapbox-000000?style=flat&logo=Mapbox"></a>
<a href="https://www.figma.com/" target="_blank" rel="noreferrer"> <img alt="Figma Badge" src="https://img.shields.io/badge/-Figma-000000?style=flat&logo=Figma"></a>

We began by outlining our project, focusing on flood risk in New Orleans. With the increasing impact of global warming causing more extreme weather events, it's crucial to equip cities like New Orleans with the tools to mitigate and respond to these natural disasters. As cartographers, we aimed to examine the city and the risk posed by future hurricanes to create a tool for damage mitigation and emergency response planning.

To support our claims, we researched key sources, developing plans to help policymakers invest in preventative measures. We used data on hurricane water levels, SRTM elevation for flood risk zones, New Orleans lot data from the Open Data portal, population by block group, income census tracts, information from NOLA Ready about hazards and coastal erosion, details on levee failures, and the locations of emergency shelters. We drafted a preliminary outline, available in our [New Orleans Draft Outline](https://www.figma.com/file/aFlpzHJg4MToRVFaCkaqFC/Project-Design?type=design&node-id=0-1&mode=design).

We faced challenges during the project. With limited flood data available, we had to create a map ourselves using Mapbox. Finding emergency shelter locations was difficult until I found the necessary data on the Red Cross website.

We then created our website using HTML, CSS, and JavaScript using Visual Studio. Here’s how the site was structured:

1. **Document Type and Structure**:
   - `<!DOCTYPE html>` declares the document as HTML5.
   - The `<html>`, `<head>`, and `<body>` tags define the structure.

2. **Metadata**:
   - `<meta>` tags provide document metadata, such as character encoding (`utf-8`), description, compatibility, and viewport settings for responsive design.

3. **Title and Favicon**:
   - `<title>` sets the webpage title to "New Orleans Flood Analysis".
   - `<link>` with `rel="icon"` specifies the favicon for the website.

4. **Styling and Scripts**:
   - External CSS (`main.css`) and JavaScript libraries (`scrollama` and `mapbox-gl`) enable interactive scrolling and map rendering.

5. **Content Sections**:
   - **Introduction (`<section id="cover">`)**: An engaging introduction with a background image of New Orleans and text describing its vulnerability to hurricanes and flood protection measures. The team members are also introduced here.
   - **Hurricane Impact (`<section id="damage_section">`)**: Detailed information on hurricanes Katrina and Ida, illustrated with before-and-after images and external source attributions. The section highlights Katrina's devastation and the ongoing threat to the city.
   - **Geonarrative (`<section id="geonarrative">`)**: Interactive maps and narratives covering emergency plans, demographic comparisons, flood risk mapping, and environmental impacts. Each scene includes detailed text and interactive elements managed by JavaScript.
   - **Conclusion (`<section id="footer">`)**: Summarizes the project and provides additional information. It includes an image, explanations of geographical challenges, and a call-to-action for future flood mitigation efforts.

6. **JavaScript Interaction**:
   - JavaScript code initializes and configures interactive elements like maps, adjusts layouts based on window resizing, and manages scroll-based interactions.

Our website seamlessly integrates text, images, styling, and interactive elements to create an engaging and informative experience. It highlights New Orleans' complex relationship with water and the ongoing battle against natural disasters. Through dynamic maps and interactive features, the site educates and inspires action towards building more sustainable and resilient cities in the face of a changing climate.

## Optimizations

During the project, we implemented several optimizations to enhance efficiency and accuracy. Initially, we faced challenges with limited flood data, which led us to create custom maps using Mapbox, ensuring our flood risk assessments were precise and up-to-date. To streamline the integration of diverse data sources, we developed a methodical approach to data aggregation, combining hurricane water level information, SRTM elevation data, and New Orleans lot and population data. This allowed us to produce a detailed and multi-faceted flood risk map. In terms of technical development, we optimized our website by linking external CSS and JavaScript libraries, such as scrollama and mapbox-gl, to enable interactive scrolling and map rendering. We also ensured the website's responsiveness across different devices by carefully configuring metadata and viewport settings. Additionally, by embedding interactive maps and narratives within the site, we created an engaging user experience that effectively communicated our findings and facilitated user interaction with the data. These optimizations not only improved the functionality of our project but also made the final product more accessible and informative for policymakers and the general public.

## Lessons Learned:

Throughout this project, we gained invaluable insights into the complexities of flood risk management in New Orleans. We began by meticulously outlining our objectives, emphasizing the importance of addressing the heightened risk of extreme weather events due to global warming. As cartographers, our goal was to assess the city's vulnerability to future hurricanes and develop a tool for effective damage mitigation and emergency response. This project underscored the necessity of thorough research and data analysis, as we explored sources ranging from hurricane water levels to population demographics and income data. Despite facing challenges such as limited flood data, we adapted by creating our own maps using Mapbox and locating emergency shelter information through persistent efforts. The process of building our website with HTML, CSS, and JavaScript further reinforced the importance of integrating technical skills with subject matter expertise. Ultimately, this project highlighted the critical role of comprehensive planning and innovative solutions in enhancing urban resilience against natural disasters.

## Data Sources
* Nola Hurricane water level increase and flood data - for developing risk zone levels [Nola Storm Surge](https://ready.nola.gov/hazard-mitigation/hazards/storm-surge-and-coastal-flooding/#:~:text=The%20damages%20caused%20by%20Hurricane%20Katrina%20demonstrate%20that,the%20south%20shore%20in%20Jefferson%20and%20Orleans%20Parishes)

* SRTM elevation data - for use in applying flood risk zones to New Orleans (assets)

* New Orleans lot data - for development of flood risk map, sourced from [New Orleans Open Data](https://data.nola.gov/dataset/Lots/m5br-772y) (assets)

* [NOLA population by block group](https://data.census.gov/cedsci/table?q=census%20tract&t=Populations%20and%20People&g=0500000US22071%241500000&tid=ACSDT5Y2020.B01003) - population analysis

* [Income Dataset](https://data.census.gov/cedsci/all/tables?q=census%20tract&t=Income%20and%20Poverty&g=310XX00US35380)

* [NOLA Ready](https://ready.nola.gov/hazard-mitigation/hazards/coastal-erosion/)

* [Failure of Levees](https://www.jstor.org/stable/4624679)

* [New Orleans FloodWalls](https://sgp.fas.org/crs/misc/RS22238.pdf)

* [New Orleans History](https://www.britannica.com/place/New-Orleans-Louisiana)

* [New Orleans Topography](https://en-us.topographic-map.com/maps/q8su/New-Orleans/#:~:text=Name%3A%20New%20Orleans%20topographic%20map%2C%20elevation%2C%20relief.%20Coordinates%3A,Maximum%20elevation%3A%20821%20ft%20Average%20elevation%3A%203%20ft)

## Examples:
Take a look at these couple examples that I have in my own portfolio:

**OsoShift:** [OsoShift: Oso Landslide Story](https://github.com/NomadCode33/NomadGeo/tree/main/CartoCraft/OsoShift)

**DemoGraphIt Map:** [DemoGraphIt: Interactive Census Mapping Tool](https://github.com/NomadCode33/NomadGeo/tree/main/DemoGraphIt)

**EcoPulse Web App:** [EcoPulse Climate Interactive Web App](https://github.com/NomadCode33/NomadGeo/tree/main/EcoPulse/EcoPulse%20Climate%20Interactive%20Web%20App)

## Repositories
**Profile:** [NomadCode33](https://github.com/NomadCode33)

**Main Repository:** [NomadGeo](https://github.com/NomadCode33/NomadGeo)
