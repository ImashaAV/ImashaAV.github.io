---
layout: default
title: "Multiplot it"
date: 2026-10-09
---

<link rel="stylesheet" href="/assets/style.css">

# Multiplot it

### Published: 9 October 2026


<iframe src="/temperature_stripes_multiplot2.html" width="100%" height="600" style="border:none;"></iframe>

For this exercise, I reused the temperature anomalies visualisation (Hawkins, 2024). At first, I loaded and cleaned both datasets: the annual and monthly csv files. Then the monthly data was prepared by making a list of month names for the x-axis and a lookup of each year's average anomaly. Then I used the same colour scale as the bars so each year's monthly line matches its bar. For every year, I stored the months, monthly values, 95% confidence limits, annual average and colours in a dictionary. I set 2025 as the default year that shows when the visualisation is initially loaded. 

Then, the interactive bar chart was plotted from the "Make it interactive" model. Then I created the multiplot layout using subplots, with two rows of equal height. O put the bar chart in the top row and the monthly chart at the bottom. The line chart has a shaded band which shows the 95% confidence range and a line with markers that show each month's value. They both have the same colour as that year's bar. When hovering over, the text shows each month's value and its confidence range. At this point, the bottom line chart still shows just one year.

Then I added the styling such as the grey background and axes value intervals.

Then, for linking the two charts, I used Javascript. Plotly in Python can't update a second plot when I hover in a HTML file, so I wrote a function that runs in the browser. When the mouse hovers over a bar, it swaps the bottom chart to that year's monthly data. Also, it outlines the hovered bar and updates the title of the bottom chart. 

Then the visualisation was exported as HTML file and hosted in my portfolio using iframe.

## Data card

| Field | Details |
|-|-|
| **Title** | Global Annual Temperature Change |
|**Summary**| This visualisation connects two charts to show how global temperatures have changed over time. The top chart has one bar for each year from 18500 to 2025, showing how far the global average temperature was from 1961-2010 average. Hovering over a bar updates the bottom chart.<br><br>The bottom chart is a line graph which shows that specific year's month-by-month anomaly as a line. It has a shaded band for 95% confidence range. The line and band are of the colour of that year's bar.|
|**Data Sources**| Met Office Hadley Centre & Climatic Research Unit. (2025). HadCRUT.5.1.0.0 data download [Data set]. Met Office. <br> [https://www.metoffice.gov.uk/hadobs/hadcrut5/data/HadCRUT.5.1.0.0/download.html](https://www.metoffice.gov.uk/hadobs/hadcrut5/data/HadCRUT.5.1.0.0/download.html) The specific files used are the **“Global (NH+SH)/2 - Annual”** and **Global (NH+SH)/2 - Monthly** CSVs which are listed under “HadCRUT5 analysis time series: ensemble means and uncertainties" section of the download page above.The annual file was used for the yearly bars and ht emonthly file was used for the line chart. <br><br>Morice, C. P., Kennedy, J. J., Rayner, N. A., Winn, J. P., Hogan, E., Killick, R. E., et al. (2021). An updated assessment of near-surface temperature change from 1850: the HadCRUT5 data set. Journal of Geophysical Research: Atmospheres, 126, e2019JD032361. [https://doi.org/10.1029/2019JD032361](https://doi.org/10.1029/2019JD032361)|
|**Mapping**| X axis: Year – Years from 1850 to 2025 with 25-year intervals <br>Y axis: Global mean temperature change in °C.|
|**Important Notes**| **-Baseline mismatch**: The Met Office’s HadCRUT5 csv file shows temperature changes relative to a 1961-1990 baseline. <br> The original Show Your Stripes visualization shows this same data to a 1961-2010 baseline (Hawkins et al., 2025).<br>As a result, the csv file values are less negative than the ones in the chart. To make sure my replication is comparable to the original, the downloaded values were re-baselined by subtracting the mean temperature for 1961-2010 from every year’s value.<br><br> **-2026 excluded**: The most recent year in the downloaded file (2026) was excluded from the replication as data for this year is still being collected.<br><br> **-Ensemble based estimate**: The values in the dataset aren’t single measurements. They are calculated by taking the average of 200 slightly different estimates (Morice et al., 2021).<br><br> **-The shaded band is uncertainity**: It's the 95% confidence range. It's wider in the early years, when there were fewer measurements, and narrower in the recent years.|
|**References**|Hawkins, E., Williams, R. G., Young, P. J., Berardelli, J., Burgess, S. N., Highwood, E., Randel, W., Roussenov, V., Smith, D., & Woods Placky, B. (2025). Warming stripes spark climate conversations: From the ocean to the stratosphere. Bulletin of the American Meteorological Society, 106(5). [https://doi.org/10.1175/BAMS-D-24-0212.1](https://doi.org/10.1175/BAMS-D-24-0212.1) <br><br> Morice, C. P., Kennedy, J. J., Rayner, N. A., Winn, J. P., Hogan, E., Killick, R. E., et al. (2021). An updated assessment of near-surface temperature change from 1850: the HadCRUT5 data set. Journal of Geophysical Research: Atmospheres, 126, e2019JD032361. [https://doi.org/10.1029/2019JD032361](https://doi.org/10.1029/2019JD032361)|
|**Access**|You can get a copy of the data used to build this visualization by downloading it from the Met Office HadCRUT5 page:<br>[https://www.metoffice.gov.uk/hadobs/hadcrut5/data/HadCRUT.5.1.0.0/download.html](https://www.metoffice.gov.uk/hadobs/hadcrut5/data/HadCRUT.5.1.0.0/download.html)<br>The specific dataset is “Global (NH+SH)/2, Annual CSV” under ensemble means and uncertainties table|


### References
*Hawkins, E. (2024). #ShowYourStripes: Global. Show Your Stripes. [https://showyourstripes.info/c](https://showyourstripes.info/c)*

