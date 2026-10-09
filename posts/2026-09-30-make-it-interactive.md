---
layout: default
title: "Make it interactive"
date: 2026-09-30
---

<link rel="stylesheet" href="/assets/style.css">

# Make it interactive

### Published: 30 September 2026

<iframe src="/interactive.html" width="100%" height="600" style="border:none;"></iframe>

For this exercise, I decided to reuse the master visualisation I did for "Copying the Master". The visualisation contains bars showing the temperature anomalies from 1859 to 2025, rebaselined against the 1961-2010 average.

First I drew the graph using plotly without any interactivity. The graph was drawn according to plotly's default styling and didn't really mimic the original visualisation I was going for. I made some changes by removing the legend and making the background dark.

For interactivity, I added the hover feature where when hovering over the bars, it shows the exact year and the temperature change value. 
The second component of interactivity was, a slider which can be adjusted to a specific year range so that the user can inspect a specific time period they're interested in.

## Data card

| Field | Details |
|-|-|
| **Title** | Global Annual Temperature Change |
|**Summary**| This bar chart shows the global temperature anomalies from 1850 to 2025, relative to the average 1961-2010 period. Each bar represents a year. The height and color of the bar show that year’s temperature change.<br><br>This visualization is interactive, such that hovering over shows the exact year and the temperature anomaly for each bar. There is also a slider which can be adjusted to show a particular range of years.<br><br>The static version of this chart is a recreation of the “Show your Stripes” global warming stripes visualization by Hawkins in 2024, redesigned as a bar chart. |
|**Data Sources**| Met Office Hadley Centre & Climatic Research Unit. (2025). HadCRUT.5.1.0.0 data download [Data set]. Met Office. <br> [https://www.metoffice.gov.uk/hadobs/hadcrut5/data/HadCRUT.5.1.0.0/download.html](https://www.metoffice.gov.uk/hadobs/hadcrut5/data/HadCRUT.5.1.0.0/download.html) The specific file used is the **“Global (NH+SH)/2 - Annual”** CSV which is listed under “HadCRUT5 analysis time series: ensemble means and uncertainties" section of the download page above. <br><br>Morice, C. P., Kennedy, J. J., Rayner, N. A., Winn, J. P., Hogan, E., Killick, R. E., et al. (2021). An updated assessment of near-surface temperature change from 1850: the HadCRUT5 data set. Journal of Geophysical Research: Atmospheres, 126, e2019JD032361. [https://doi.org/10.1029/2019JD032361](https://doi.org/10.1029/2019JD032361)|
|**Mapping**| X axis: Year – Years from 1850 to 2025 with 25-year intervals <br>Y axis: Global mean temperature change in °C.|
|**Important Notes**| **-Baseline mismatch**: The Met Office’s HadCRUT5 csv file shows temperature changes relative to a 1961-1990 baseline. <br> The original Show Your Stripes visualization shows this same data to a 1961-2010 baseline (Hawkins et al., 2025).<br>As a result, the csv file values are less negative than the ones in the chart. To make sure my replication is comparable to the original, the downloaded values were re-baselined by subtracting the mean temperature for 1961-2010 from every year’s value.<br><br> **-2026 excluded**: The most recent year in the downloaded file (2026) was excluded from the replication as data for this year is still being collected.<br><br>**-Ensemble based estimate**: The values in the dataset aren’t single measurements. They are calculated by taking the average of 200 slightly different estimates (Morice et al., 2021).|
|**References**|Hawkins, E., Williams, R. G., Young, P. J., Berardelli, J., Burgess, S. N., Highwood, E., Randel, W., Roussenov, V., Smith, D., & Woods Placky, B. (2025). Warming stripes spark climate conversations: From the ocean to the stratosphere. Bulletin of the American Meteorological Society, 106(5). [https://doi.org/10.1175/BAMS-D-24-0212.1](https://doi.org/10.1175/BAMS-D-24-0212.1) <br><br> Morice, C. P., Kennedy, J. J., Rayner, N. A., Winn, J. P., Hogan, E., Killick, R. E., et al. (2021). An updated assessment of near-surface temperature change from 1850: the HadCRUT5 data set. Journal of Geophysical Research: Atmospheres, 126, e2019JD032361. [https://doi.org/10.1029/2019JD032361](https://doi.org/10.1029/2019JD032361)|
|**Access**|You can get a copy of the data used to build this visualization by downloading it from the Met Office HadCRUT5 page:<br>[https://www.metoffice.gov.uk/hadobs/hadcrut5/data/HadCRUT.5.1.0.0/download.html](https://www.metoffice.gov.uk/hadobs/hadcrut5/data/HadCRUT.5.1.0.0/download.html)<br>The specific dataset is “Global (NH+SH)/2, Annual CSV” under ensemble means and uncertainties table|


### References
Hawkins, E. (n.d.). Professor Ed Hawkins. National Centre for Atmospheric Science. [https://ncas.ac.uk/people/10077/ed-hawkins/](https://ncas.ac.uk/people/10077/ed-hawkins/)
