# Climate Action For Improved Respiratory Health: Mapping Benefits Across Scotland’s NHS Boards
This repository reflects my entry for the DataLabs Data Visualisation Contest 2025, showcasing spatial‑temporal storytelling using open data and open‑source tools.
The project explores **the yearly projected monetary value saved** from respiratory‑health-related co‑benefits across NHS Boards in Scotland. The core output is a **temporal map visualisation** created using QGIS, showing how benefits evolve over time across geographic areas.

## Project Overview
Using the co-benefits atlas data provided by the team at Edinburgh Climate Change Institute (ECCI), I mapped five co-benefit pathways that translate environmental improvement directly into respiratory health improvement and NHS savings: 
### Co-Benefit Pathways
| **Co‑Benefit** | **Damage Pathway** | **Damage Type** | **Value** |
|---------------|--------------------|-----------------|-------------|
| Air quality | Reduced mortality | Health | Lower air pollution reduces respiratory disease and prevents premature deaths. |
| Dampness | NHS | Non‑health | Fewer GP visits and lower NHS treatment costs for respiratory and other infections. |
| Dampness | QALY | Health | Healthier indoor environments improve quality of life by reducing damp‑related illness. |
| Excess cold | NHS | Non‑health | Warmer homes reduce hospital admissions and NHS costs for cold‑related illnesses. |
| Excess cold | QALY | Health | Adequate heating prevents cold‑related issues and supports immunity and wellbeing. |

For each Scottish Data Zone:

1. The yearly projected monetary benefit of the selected co‑benefit or damage pathway was obtained.
2. This value was multiplied by the Data Zone’s population.
3. Values were then aggregated to the level of NHS Board areas.

These aggregated values were animated spatially using QGIS’s Temporal Controller, producing a frame‑by‑frame view of how monetary benefits accumulate over time.

## Tools and Technologies
QGIS (spatial joins, temporal controller, vector styling)<br>
Python / Jupyter Notebook (data exploring, cleaning, combining)<br>
HTML + CSS (basic webpage for submission)

## Data Sources
### Co-Benefit Atlas Data
The primary dataset used for this analysis is the data used to power The UK Co-Benefits Atlas. This data was provided by the team at [Edinburgh Climate Change Institute (ECCI)](https://edinburghcentre.org/) for [The Data Lab’s Data Visualisation Competition 2025](https://thedatalab.com/data-visualisation-competition-2025/?utm_source=campaign&utm_medium=email&utm_campaign=campaign_2970972&utm_content=data_visualisation_competition). This data contains values which are estimates of wider socio-economic impacts from the UK reaching net zero by 2050, and the data represents the value to individuals and society across 11 co-benefit types from following the actions set out by the UK Climate Change Committee. The data is provided in three different levels of complexity, for this analysis and exploration the level 3 data was used. A **lookup** file and **shapefile** were also provided which were combined with the main data.

### Respiratory Illness Data (Exploration only)
The respiratory illness data used was the [Weekly Cases for COVID-19, Influenza and RSV by Health Board](https://opendata.scot/datasets/public+health+scotland-viral+respiratory+diseases+%2528including+influenza+and+covid-19%2529+data+in+scotland/ ) data from Open Data Scotland, which contains public sector information licensed under the [UK Open Government Licence v3.0](https://www.nationalarchives.gov.uk/doc/open-government-licence/version/3/). This data contains weekly recorded respiratory cases for COVID-19, Influenza and RSV and contains historical records from 2016 to up to the current year and first week in January 2026 when this analysis was conducted. For the purposes of this analysis, only the data from 2017-2025 was used from this dataset.

### Scottish NHS board boundaries
[The NHS health boards (scotland)](https://data-stirling-council.hub.arcgis.com/datasets/stirling-council::open-data-nhs-health-boards-scotland/about) data was obtained for Stirling Council via its Open Data portal. This data contains the boundaries of each health board area and was used as a vector layer in QGIS. This datas contains public sector information licensed under the [UK Open Government Licence v3.0](https://www.nationalarchives.gov.uk/doc/open-government-licence/version/3/) and contains Ordnance Survey data © Crown copyright and database right 2024.
