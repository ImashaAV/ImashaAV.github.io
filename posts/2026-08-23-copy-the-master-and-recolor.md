---
layout: default
title: "Copy the Master and Recolour it"
date: 2026-08-10
---

<link rel="stylesheet" href="/assets/style.css">

# Copy the Master and Recolour it

### Published: 23 August 2026

![Original visualisation](/images/module5.jpeg)
*Hawkins, E. (2024). #ShowYourStripes: Global. Show Your Stripes. [https://showyourstripes.info/c](https://showyourstripes.info/c)*

I picked this visualisation because it has a clear colour scheme and explored global temperature change over a range of years. I reproduced it using Python and recreated it using an alternate colour scheme. 

### Replication:  
The original visualisation uses a 1961-2010 baseline, but the raw data uses 1961-1990 as the baseline. So first, I calculated the anomaly relative to the 1961-2010 average so that my replicated bars would match the original.  
Then, at first I drew a simple bar graph. I used fig, ax instead of plt because, once I draw the graph using plt, I can't incrementally alter it. But since I have to change my graph to look like the original step by step, I stuck to fig, ax.  
The initial graph lacked certain features:  
* Colours of the original visualisation
* Y axis intervals were wrong
* Background colours were missing

Then, I added the background colour which was grey and coloured the x and y labels, ticks and axes spines in white. Then I used [imagecolorpicker](https://imagecolorpicker.com/) to get the hex values of the colours in the visualisation. I built a colour map using the hexadecimal values of the colours. Then I used TwoSlopeNorm which is a translator that converted my actual temperature values into 0-1 range values that the colour map needs. (Matplotlib, 2026).  
Then I added vcenter=0 to make sure that 0 °C is always in the exact middle of the colour scale even though data clearly isn't symmetric.  
Then the gap between the bars were removed to match the original.  
Then I added the topic "Global Temperature Change Relative to average of 1961-2010 [°C]". I manually placed this as a text using ax.text instead of ax.title to match the topic placement of the original visualisation.  
  
### Recolouring:
As for the colour, the original visualisation went with blue to red going from low temperatures to high. I agree with this colour scheme as it reflects the global temperature change that's being shown in the graph.  
For the recolouring, I wanted a colour scheme that goes from light to dark where the negative temperatures are shown by the light colour and the positive temperature changes are shown by the dark colour. Therefore, I went with the Yellow Red multi-hue colour scheme of Colour Brewer. 


### Replication
![Replication](/images/Replication.jpeg)


### Reconstruction with alternative colour scale
![Recolouring](/images/Recoloured.jpeg)

## Data card

| Field | Details |
|-|-|
| **Title** | Global Annual Temperature Change |
|**Summary**| This bar chart shows the global temperature anomalies from 1850 to 2025, relative to the average 1961-2010 period. Each bar represents a year. The height and color of the bar show that year’s temperature change.<br> This chart is a recreation of the “Show your Stripes” global warming stripes visualization by Hawkins in 2024, redesigned as a bar chart.|
|**Data Sources**| Met Office Hadley Centre & Climatic Research Unit. (2025). HadCRUT.5.1.0.0 data download [Data set]. Met Office. <br> [https://www.metoffice.gov.uk/hadobs/hadcrut5/data/HadCRUT.5.1.0.0/download.html](https://www.metoffice.gov.uk/hadobs/hadcrut5/data/HadCRUT.5.1.0.0/download.html) The specific file used is the “Global (NH+SH)/2 - Annual” CSV which is listed under “HadCRUT5 analysis time series: ensemble means and uncertainties" section of the download page above. <br>Morice, C. P., Kennedy, J. J., Rayner, N. A., Winn, J. P., Hogan, E., Killick, R. E., et al. (2021). An updated assessment of near-surface temperature change from 1850: the HadCRUT5 data set. Journal of Geophysical Research: Atmospheres, 126, e2019JD032361. [https://doi.org/10.1029/2019JD032361](https://doi.org/10.1029/2019JD032361)|
|**Mapping**| X axis: Year – Years from 1850 to 2025 with 25-year intervals <br>Y axis: Global mean temperature change in °C.|
|**Important Notes**| -Baseline mismatch: The Met Office’s HadCRUT5 csv file shows temperature changes relative to a 1961-1990 baseline. <br> The original Show Your Stripes visualization shows this same data to a 1961-2010 baseline (Hawkins et al., 2025).<br>As a result, the csv file values are less negative than the ones in the chart. To make sure my replication is comparable to the original, the downloaded values were re-baselined by subtracting the mean temperature for 1961-2010 from every year’s value.<br> -2026 excluded: The most recent year in the downloaded file (2026) was excluded from the replication as data for this year is still being collected.<br>-Ensemble based estimate: The values in the dataset aren’t single measurements. They are calculated by taking the average of 200 slightly different estimates (Morice et al., 2021).|
|**References**|Hawkins, E., Williams, R. G., Young, P. J., Berardelli, J., Burgess, S. N., Highwood, E., Randel, W., Roussenov, V., Smith, D., & Woods Placky, B. (2025). Warming stripes spark climate conversations: From the ocean to the stratosphere. Bulletin of the American Meteorological Society, 106(5). [https://doi.org/10.1175/BAMS-D-24-0212.1](https://doi.org/10.1175/BAMS-D-24-0212.1) <br> Morice, C. P., Kennedy, J. J., Rayner, N. A., Winn, J. P., Hogan, E., Killick, R. E., et al. (2021). An updated assessment of near-surface temperature change from 1850: the HadCRUT5 data set. Journal of Geophysical Research: Atmospheres, 126, e2019JD032361. [https://doi.org/10.1029/2019JD032361](https://doi.org/10.1029/2019JD032361)|
|**Access**|You can get a copy of the data used to build this visualization by downloading it from the Met Office HadCRUT5 page:<br>[https://www.metoffice.gov.uk/hadobs/hadcrut5/data/HadCRUT.5.1.0.0/download.html](https://www.metoffice.gov.uk/hadobs/hadcrut5/data/HadCRUT.5.1.0.0/download.html)<br>The specific dataset is “Global (NH+SH)/2, Annual CSV” under ensemble means and uncertainties table|

### References
Matplotlib. (2026). matplotlib.colors.TwoSlopeNorm. Matplotlib documentation. [https://matplotlib.org/stable/api/_as_gen/matplotlib.colors.TwoSlopeNorm.html](https://matplotlib.org/stable/api/_as_gen/matplotlib.colors.TwoSlopeNorm.html)

