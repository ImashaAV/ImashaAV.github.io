---
layout: default
title: "Make it multivariate"
date: 2026-09-14
---

<link rel="stylesheet" href="/assets/style.css">

# Make it multivariate

### Published: 14 September 2026

## Data Visualisation after made multivariate
![Multivariate](/images/multivariate.jpeg)

I decided to add **World region** as the third variable as it would be meaningful to know which areas in the world are responsible for the CO2 emissions shown in the chart. I classified the regions into 6 by continents: North America, South America, Europe, Africa, Asia and Oceania.

I inspected the dataset downloaded from Our World in Data (OWID) and found out that it contained the CO2 emissions for all the continents. So I can use this dataset itself to incorporate the third variable into the visualisation.   
Upon further inspection I realised that the continents were aggregated in two ways:
"Europe" and "Europe (GCP)" appeared as separate entities. The plain continent entities (e.g. "Europe", coded OWID_EUR) had data across all three columns.  
However, the "(GCP)" entities were missing both the Land-use change and Total columns entirely.  
Since my visualisation needs both fossil fuel and land-use values, I decided to use the plain OWID continent entities rather than the GCP ones.

I filtered the dataset down to the six regions I want. Then I removed the 'Total' column as it was redundant data because it is the sum of fossil fuel emissions and land-use change emissions. 

I started by drawing the faceted chart outline. Then I visualised my data. Each column facet corresponded to a region. The two column facets showed the two categories (Fossil fuels and land-use). X axis within each panel showed the year and y axis within each panel showed emissions in tonnes.

Then I added the title and X and Y axis labels. To get rid of the scientific notations in the y axis, I changed the unit of emissions from tonnes to billion tonnes. The strict boundaries around each facet made it look like separate charts. Therefore, I added a common gridline to each facet

## Test table
|Header one|Header two|
|-|-|

## Data card
|Field|Details|
|-|-|
|**Title** | CO2 emissions from fossil fuels and land use change by region over time (1850-2024)|
|**Summary** | This line chart shows the CO2 emissions from 1850 to 2024 categorized by world region. Global emissions are broken into two categories: fossil fuels and land-use change.|
|**Data Sources** | Our World in Data. (2026). CO₂ emissions from fossil fuels and land-use change [Data set]. [https://ourworldindata.org/grapher/co2-fossil-plus-land-use](https://ourworldindata.org/grapher/co2-fossil-plus-land-use) Gcarbonproject. (n.d.). Home. Retrieved from [https://globalcarbonbudget.org/](https://globalcarbonbudget.org/) All data was retrieved from OWID’s own csv download for the chart.|
|**Mapping** | Column facet – World region Raw facet – Catrgory (Fossil fuels, Land use change) X axis within each panel – Year (1850-2024) Y axis within each panel – Emissions (billion tones)|
|**Important Notes** | Total emissions (fossil fuels + land-use change combined) was removed from the final chart as it’s redundant with the sum of the other two categories. The dataset has two different aggregations per continent: (e.g.: “Europe”, coded OWID_EUR and a separate “Europe (GCP)”). Only the plain OWID continent entities were used because the “(GCP)” versions are missing the lan0use change and total columns entirely. Fossil fuel emission data is missing for Africa and Asia between 1850 and 1880s. Because each row shares one y-axis scale across all six regions, Asia’s fossil fuel emissions visually compress the other five lines in that row. This is an honest representation of the data, not a chart error.|
|**Access** | Original visualization: [https://ourworldindata.org/grapher/co2-fossil-plus-land-use](https://ourworldindata.org/grapher/co2-fossil-plus-land-use) Data download: Available directly from the “Download” icon on the same OWID chart page|

