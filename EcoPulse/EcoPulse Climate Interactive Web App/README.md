# EcoPulse Climate Interactive Web App 
An interactive website developed using RStudio and Shiny Apps to engage users with climate change data through an educational and accessible platform. Featuring multiple tabs with interactive visualizations, in-depth data analysis, and clear explanations, the site empowers users to explore key aspects of climate change and understand its global impacts.

**Link to Project**: https://mecha.shinyapps.io/project-app-T3ch12et/

<img src="https://github.com/NomadCode33/git-lfs/blob/main/Climate%20Change%20Website.gif" img alt = "Climate Change Website GIF"/>

## How It's Made:

**Tech used:** <a href="https://www.r-project.org/about.html" target="_blank" rel="noreferrer"> <img alt="R Badge" src="https://img.shields.io/badge/-R-000000?style=flat&logo=R"></a> 
<a href="https://shiny.posit.co/" target="_blank" rel="noreferrer"> <img alt="R Shiny Apps Badge" src="https://img.shields.io/badge/-R Shiny Apps-000000?style=flat&logo=R"></a>
<a href="https://posit.co/download/rstudio-desktop/" target="_blank" rel="noreferrer"> <img alt="RStudio Badge" src="https://img.shields.io/badge/-RStudio-000000?style=flat&logo=rstudioide"></a>
<a href="https://www.git-scm.com/" target="_blank" rel="noreferrer"> <img alt="Git Badge" src="https://img.shields.io/badge/-Git-000000?style=flat&logo=GitHub"></a> 
<a href="https://github.com/" target="_blank" rel="noreferrer"> <img alt="GitHub Badge" src="https://img.shields.io/badge/-GitHub-000000?style=flat&logo=GitHub"></a> 

Creating an interactive website to allow people to engage with climate change data was an exciting project. We used RStudio and Shiny Apps to build this interactive site, which involved three main steps: designing the user interface (UI), fetching data from the server, and integrating everything into a cohesive structure similar to HTML. Here's a detailed breakdown of how we brought this project to life.

### App UI
Our Shiny app, aptly named "Climate Change," aims to educate users on the profound impacts of climate change through engaging visualizations and data analysis. It features multiple tabs, each focusing on a different aspect of climate change:

1. **Introduction**: This tab provides an overview of the app's goals and highlights the data sources used.
2. **Economic Damages**: Users can explore how CO2 emissions economically impact various countries, displaying the average economic damage as a percentage of Gross National Income (GNI).
3. **Anomaly**: This section visualizes the effect of carbon dioxide emissions on land and ocean temperature anomalies through interactive graphs.
4. **Greenhouse Gas Emissions**: Here, recent U.S. greenhouse gas emissions are compared to historical global emissions, with options to view data for different gases and years.
5. **Population**: This tab examines the effect of climate change on agricultural output and GDP across various countries.
6. **Summary of Greenhouse Gas Emission Contribution**: It highlights how different countries contribute to greenhouse gas emissions over time.
7. **Evaluation**: Summarizes the significance of understanding climate change factors and their impacts on economies, environments, and populations.

To enhance user engagement and comprehension, the app employs interactive elements such as radio buttons, select inputs, and sliders. It also integrates images, hyperlinks to data sources, and detailed explanations. The app is styled using the "cyborg" theme from shinythemes and utilizes libraries like `shiny`, `ggplot2`, `dplyr`, and `leaflet` in R.

### App Server
Here's a straightforward explanation of the server-side code used in our data visualization project with R:

1. **Installing Required Packages**:
   - Although commented out, the initial lines provide instructions to install essential packages if they aren't already installed. These include `shiny`, `dslabs`, `outliers`, and `reshape2`.

2. **Loading Required Libraries**:
   - We load various R libraries crucial for the project using the `library()` function. These libraries include `ggplot2`, `wbstats`, `dplyr`, `tidyr`, `maps`, `dslabs`, `knitr`, `RColorBrewer`, `outliers`, `httr`, `shiny`, and `reshape2`.

3. **Setting Options**:
   - The `options(scipen = 999)` setting ensures that scientific notation is avoided in plots and outputs.

4. **Fetching and Preparing Economic Damage Data**:
   - We retrieve data on economic damage due to CO2 emissions using the `wb()` function from the `wbstats` library. The data is cleaned by removing rows with missing values and converting the date column to numeric format. The average economic damage for each country is calculated and arranged in descending order.

5. **Selecting Top Countries**:
   - We identify the top 3, 5, and 10 countries based on average economic damage using the `top_n()` function.

6. **Preparing Emissions Anomaly Data**:
   - Data for carbon emissions and anomalies in land and ocean temperatures is selected and cleaned. The data is then transformed into a long format, making it easier to plot.

7. **Fetching and Preparing Gas Emission Data**:
   - We retrieve data on CO2, Methane, and Nitrous Oxide emissions in the USA, clean it, and transform it into a long format for easier plotting.

8. **Creating Plots**:
   - Several `ggplot2` plots are created to visualize the data. These include:
     - A bar chart showing economic damage by country.
     - A line chart depicting the impact of carbon emissions on land and ocean temperature anomalies.
     - Visualizations of greenhouse gas emissions in the US over time.
     - Plots showing climate change effects on population and markets in different countries.

9. **Setting Up Shiny Server**:
   - The `server` function is defined to render various plots and outputs based on user inputs in the Shiny app. The plots and text outputs are dynamically generated, allowing users to interact with the data and customize their visualizations.

10. **Example Plots**:
   - Example plots include a bar chart illustrating average economic damage by country, a line chart showing the impact of carbon emissions, and various visualizations of greenhouse gas emissions and climate change effects.

Overall, this code fetches, cleans, and visualizes data on economic damage from CO2 emissions, land and ocean temperature anomalies, and greenhouse gas emissions using R and the Shiny package for interactive web applications.

### App Integration
Finally, to bring it all together, we set up and run the Shiny web application using R:

1. **Loading Required Libraries**:
   - We load the `shiny` and `plotly` libraries. `shiny` creates interactive web applications in R, while `plotly` adds interactive plotting capabilities.

2. **Sourcing External Files**:
   - The `source()` function runs the code from "app_server.R" and "app_ui.R" files. These files contain the server-side logic and the user interface definitions for the Shiny app, respectively.

3. **Creating and Running the Shiny App**:
   - The `shinyApp(ui = ui, server = server)` function creates a new Shiny application using the `ui` and `server` variables defined in the sourced files. The `ui` defines the app's layout and appearance, while the `server` manages the app's behavior and responses to user inputs.

In summary, this code initializes and runs a Shiny app by loading the necessary libraries, executing external files for the UI and server logic, and then creating the app using the specified components. Through this process, we created a dynamic and interactive website that allows users to explore and understand climate change data in an engaging way.

## Optimizations

Exploring the website, several optimizations stand out that enhance user engagement and data comprehension. The app’s layout is well-organized, with each tab focusing on a specific aspect of climate change, making navigation intuitive. The use of interactive elements like radio buttons, select inputs, and sliders ensures users can tailor the data visualizations to their interests. Styling with the "cyborg" theme from shinythemes gives the app a sleek, modern look, while incorporating images and hyperlinks enriches the educational content. Libraries such as ggplot2 and leaflet were effectively utilized to create visually appealing and informative plots. These thoughtful design choices collectively elevate the user experience and educational value of the app.

The app is robust and informative, but there are areas where enhancements could elevate its impact. Integrating real-time data would make the visualizations more current and relevant. Improving mobile responsiveness would ensure a seamless user experience across all devices. Implementing advanced data filtering options would allow users to dive deeper into specific data subsets, providing a more personalized exploration. On the population tab, which I worked on, the data visualization could have been more robust and intuitive. My goal was to create a visualization similar to the one in question 4 of the report, but despite a workaround, the bar graph appears too large. Additionally, one of the buttons does not switch to the Population Affected % effectively, and not all graphs switch to the Population Affected %, which can make the user experience clunky. Incorporating user feedback mechanisms could help identify areas for further improvement and make the app more user-centric. These optimizations would refine the app's functionality and increase its appeal and usability.

## Lessons Learned:

Creating the interactive website deepened my understanding of climate change and honed my technical skills. I learned the importance of designing intuitive user interfaces and the intricacies of fetching and integrating data from diverse sources. This project underscored the power of interactive visualizations in making complex data accessible and engaging for users. Moreover, it highlighted the necessity of clear communication and meticulous attention to detail, from coding to final presentation.

## Examples:
Take a look at these couple examples that I have in my own portfolio:

**Terazon:** [Terazon: Visualizing Land Cover Change in Rondonia](https://github.com/NomadCode33/NomadGeo/tree/main/GreenMap%20Initiative/Terazon)

**Sumner Jurisdiction Boundary:** [Sumner Jurisdiction Boundary](https://github.com/NomadCode33/NomadGeo/tree/main/Furtado-Associates-Projects/Sumner%20Jurisdiction%20Boundary)

**North Bothell Bus Base:** [North Bothell Bus Base](https://github.com/NomadCode33/NomadGeo/tree/main/Furtado-Associates-Projects/North%20Bothell%20Bus%20Base)

## Repositories
**Profile:** [NomadCode33](https://github.com/NomadCode33)

**EcoPulse Repository:** [EcoPulse](https://github.com/NomadCode33/NomadGeo/tree/main/EcoPulse)

**Main Repository:** [NomadGeo](https://github.com/NomadCode33/NomadGeo)
