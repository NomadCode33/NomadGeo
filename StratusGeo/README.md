# StratusGeo — Serverless Geospatial Analytics and Machine Learning with AWS and CARTO

An exploration of cloud-native geospatial analytics focused on enabling spatial queries, third-party data integration, and machine learning directly inside a cloud data warehouse. Working with Amazon Redshift, AWS Data Exchange, and CARTO, this project covers how to subscribe to geospatial datasets in the cloud, run spatial joins and built-in spatial functions using SQL, and build machine learning models on spatial data — all without leaving the cloud environment.

## How It's Made:

**Tech used:** <a href="https://aws.amazon.com/redshift/" target="_blank" rel="noreferrer"> <img alt="Amazon Redshift Badge" src="https://img.shields.io/badge/-Amazon Redshift-000000?style=flat&logo=None"></a> <a href="https://aws.amazon.com/data-exchange/" target="_blank" rel="noreferrer"> <img alt="AWS Data Exchange Badge" src="https://img.shields.io/badge/-AWS Data Exchange-000000?style=flat&logo=None"></a>
<a href="https://carto.com/" target="_blank" rel="noreferrer"> <img alt="CARTO Badge" src="https://img.shields.io/badge/-CARTO-000000?style=flat&logo=Carto"></a>
<a href="https://www.ibm.com/think/topics/structured-query-language" target="_blank" rel="noreferrer"> <img alt="SQL Badge" src="https://img.shields.io/badge/-SQL-000000?style=flat&logo=None"></a> 
<a href="https://aws.amazon.com/redshift/features/redshift-ml/" target="_blank" rel="noreferrer"> <img alt="Redshift ML Badge" src="https://img.shields.io/badge/-Redshift ML-000000?style=flat&logo=None"></a>
<a href="https://www.databricks.com/discover/data-warehouse/cloud" target="_blank" rel="noreferrer"> <img alt="Cloud Data Warehouse Badge" src="https://img.shields.io/badge/-Cloud Data Warehouse-000000?style=flat&logo=None"></a>

The project started with setting up access to Amazon Redshift and connecting it to AWS Data Exchange, which serves as the entry point for third-party geospatial datasets. Rather than downloading and managing data locally, AWS Data Exchange allows you to find, subscribe to, and query external datasets directly alongside your own first-party data inside Redshift — keeping everything in one place and eliminating the data movement that typically slows down geospatial workflows.

With the data in place inside Amazon Redshift, the work was structured around three core capabilities.

The first was running spatial queries using SQL. Amazon Redshift has built-in spatial functions that let you perform operations like spatial joins, point-in-polygon lookups, and proximity analysis directly in the data warehouse using standard SQL syntax. This is significant because it means analysts who already know SQL can run geospatial queries without needing to learn a separate GIS toolchain or spin up a dedicated spatial database like PostGIS.

The second was integrating third-party geospatial data through AWS Data Exchange. By subscribing to external datasets through the exchange, those datasets become immediately queryable inside Redshift without any manual export or transformation step. This makes it straightforward to combine external geospatial data — things like demographic boundaries, points of interest, or environmental datasets — with internal first-party data and run spatial joins across both in a single query.

The third was applying machine learning to spatial data using Redshift ML. Rather than exporting data to a separate environment to train and run models, Redshift ML allows you to create and apply ML models on your data in place using SQL. This keeps the spatial data in the cloud data warehouse throughout the entire workflow — from ingestion to analysis to prediction — without any data movement between systems.

CARTO was used as the visualization and spatial analytics layer on top of Redshift, providing a way to surface the results of cloud-based spatial queries as interactive maps and dashboards. This combination — Redshift for storage, querying, and ML, and CARTO for visualization — covers most geospatial use cases entirely within the cloud.

## Optimizations

One of the main advantages of this cloud-native approach is that the data never has to leave Amazon Redshift. Traditional geospatial workflows often involve pulling data out of a database, processing it in a desktop GIS tool or Python environment, and then either loading the results back in or exporting them elsewhere. Each of those handoffs introduces latency, potential data inconsistency, and additional infrastructure to manage. By keeping everything inside Redshift — including the ML models — that overhead is eliminated.

AWS Data Exchange also removes the typical friction of working with third-party geospatial data. Instead of downloading files, managing local copies, and figuring out how to load them into a database, the data is available directly in Redshift as soon as you subscribe. That makes it much faster to get to the actual analysis.

Using SQL as the primary interface throughout — for spatial joins, spatial functions, and ML model creation — is also a meaningful optimization from a workflow standpoint. It lowers the barrier to entry for analysts who aren't GIS specialists, and it means spatial analysis can happen inside the same environment where the rest of the business data already lives.

## Lessons Learned

This project made it clear that the biggest bottleneck in geospatial analytics is usually not the analysis itself — it's everything that has to happen before and after. Getting data into the right format, moving it between systems, and managing infrastructure for spatial processing can easily consume more time than the actual spatial queries. A cloud data warehouse like Amazon Redshift, combined with a data marketplace like AWS Data Exchange, removes most of that friction by treating geospatial data the same way it treats any other structured data.

The ability to run machine learning directly inside Redshift using SQL was probably the most unexpected takeaway. The typical assumption is that ML requires a separate pipeline — export the data, train a model in a notebook or dedicated platform, deploy it somewhere, and then figure out how to get predictions back into your analysis environment. Redshift ML collapses that into a single SQL statement, which changes what's practical to do with spatial data at scale.

The CARTO integration also reinforced that cloud-native geospatial work doesn't have to sacrifice visualization quality. Having a direct connection from the data warehouse to an interactive mapping platform means the output of a spatial query can be on a map in seconds, rather than going through an export-and-import cycle just to see what the data looks like spatially.

## Examples:

Take a look at these couple examples that I have in my own portfolio:

**ImpactAtlas:** [ImpactAtlas: Climate Change Through Spatial Insight](https://github.com/NomadCode33/NomadGeo/tree/main/GreenMap%20Initiative/ImpactAtlas)

**EmpireMap:** [EmpireMap: New York in Layers](https://github.com/NomadCode33/NomadGeo/tree/main/CartoCraft/EmpireMap)

**North Bothell Bus Base:** [North Bothell Bus Base](https://github.com/NomadCode33/NomadGeo/tree/main/Furtado-Associates-Projects/North%20Bothell%20Bus%20Base)

## Repositories

**Profile:** [NomadCode33](https://github.com/NomadCode33)

**Main Repository:** [NomadGeo](https://github.com/NomadCode33/NomadGeo)