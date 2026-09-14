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
| Field | Details |
|-|-|
| **Title** | Global Annual Temperature Change |
|**Summary**| This bar chart shows the global temperature anomalies from 1850 to 2025, relative to the average 1961-2010 period. Each bar represents a year. The height and color of the bar show that year’s temperature change.<br> This chart is a recreation of the “Show your Stripes” global warming stripes visualization by Hawkins in 2024, redesigned as a bar chart.|
|**Data Sources**| Met Office Hadley Centre & Climatic Research Unit. (2025). HadCRUT.5.1.0.0 data download [Data set]. Met Office. <br> [https://www.metoffice.gov.uk/hadobs/hadcrut5/data/HadCRUT.5.1.0.0/download.html](https://www.metoffice.gov.uk/hadobs/hadcrut5/data/HadCRUT.5.1.0.0/download.html) The specific file used is the **“Global (NH+SH)/2 - Annual”** CSV which is listed under “HadCRUT5 analysis time series: ensemble means and uncertainties" section of the download page above. <br><br>Morice, C. P., Kennedy, J. J., Rayner, N. A., Winn, J. P., Hogan, E., Killick, R. E., et al. (2021). An updated assessment of near-surface temperature change from 1850: the HadCRUT5 data set. Journal of Geophysical Research: Atmospheres, 126, e2019JD032361. [https://doi.org/10.1029/2019JD032361](https://doi.org/10.1029/2019JD032361)|
|**Mapping**| X axis: Year – Years from 1850 to 2025 with 25-year intervals <br>Y axis: Global mean temperature change in °C.|
|**Important Notes**| **-Baseline mismatch**: The Met Office’s HadCRUT5 csv file shows temperature changes relative to a 1961-1990 baseline. <br> The original Show Your Stripes visualization shows this same data to a 1961-2010 baseline (Hawkins et al., 2025).<br>As a result, the csv file values are less negative than the ones in the chart. To make sure my replication is comparable to the original, the downloaded values were re-baselined by subtracting the mean temperature for 1961-2010 from every year’s value.<br><br> **-2026 excluded**: The most recent year in the downloaded file (2026) was excluded from the replication as data for this year is still being collected.<br><br>**-Ensemble based estimate**: The values in the dataset aren’t single measurements. They are calculated by taking the average of 200 slightly different estimates (Morice et al., 2021).|
|**References**|Hawkins, E., Williams, R. G., Young, P. J., Berardelli, J., Burgess, S. N., Highwood, E., Randel, W., Roussenov, V., Smith, D., & Woods Placky, B. (2025). Warming stripes spark climate conversations: From the ocean to the stratosphere. Bulletin of the American Meteorological Society, 106(5). [https://doi.org/10.1175/BAMS-D-24-0212.1](https://doi.org/10.1175/BAMS-D-24-0212.1) <br><br> Morice, C. P., Kennedy, J. J., Rayner, N. A., Winn, J. P., Hogan, E., Killick, R. E., et al. (2021). An updated assessment of near-surface temperature change from 1850: the HadCRUT5 data set. Journal of Geophysical Research: Atmospheres, 126, e2019JD032361. [https://doi.org/10.1029/2019JD032361](https://doi.org/10.1029/2019JD032361)|
|**Access**|You can get a copy of the data used to build this visualization by downloading it from the Met Office HadCRUT5 page:<br>[https://www.metoffice.gov.uk/hadobs/hadcrut5/data/HadCRUT.5.1.0.0/download.html](https://www.metoffice.gov.uk/hadobs/hadcrut5/data/HadCRUT.5.1.0.0/download.html)<br>The specific dataset is “Global (NH+SH)/2, Annual CSV” under ensemble means and uncertainties table|

## Data card
|Field|Details|
|-|-|
|**Title** | CO2 emissions from fossil fuels and land use change by region over time (1850-2024)|
|**Summary** | This line chart shows the CO2 emissions from 1850 to 2024 categorized by world region. Global emissions are broken into two categories: fossil fuels and land-use change.|
|**Data Sources** | Our World in Data. (2026). CO₂ emissions from fossil fuels and land-use change [Data set]. [https://ourworldindata.org/grapher/co2-fossil-plus-land-use](https://ourworldindata.org/grapher/co2-fossil-plus-land-use) Gcarbonproject. (n.d.). Home. Retrieved from [https://globalcarbonbudget.org/](https://globalcarbonbudget.org/) All data was retrieved from OWID’s own csv download for the chart.|
|**Mapping** | Column facet – World region Raw facet – Catrgory (Fossil fuels, Land use change) X axis within each panel – Year (1850-2024) Y axis within each panel – Emissions (billion tones)|
|**Important Notes** | Total emissions (fossil fuels + land-use change combined) was removed from the final chart as it’s redundant with the sum of the other two categories. The dataset has two different aggregations per continent: (e.g.: “Europe”, coded OWID_EUR and a separate “Europe (GCP)”). Only the plain OWID continent entities were used because the “(GCP)” versions are missing the lan0use change and total columns entirely. Fossil fuel emission data is missing for Africa and Asia between 1850 and 1880s. Because each row shares one y-axis scale across all six regions, Asia’s fossil fuel emissions visually compress the other five lines in that row. This is an honest representation of the data, not a chart error.|
|**Access** | Original visualization: [https://ourworldindata.org/grapher/co2-fossil-plus-land-use](https://ourworldindata.org/grapher/co2-fossil-plus-land-use) Data download: Available directly from the “Download” icon on the same OWID chart page|

