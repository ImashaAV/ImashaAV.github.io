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

Then, I added the background colour which was grey and the coloured the x and y labels, ticks and axes spines in white. Then I used [imagecolorpicker](https://imagecolorpicker.com/) to get the hex values of the colours in the visualisation. I coloured the bars using those colours and got rid of the small gap between bars to match the original.

My replication looks very similar to Hawkin's visualisation. The placement of the title still isn't quite right. 
  
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
|**Data Sources**| Met Office Hadley Centre & Climatic Research Unit. (2025). HadCRUT.5.1.0.0 data download [Data set]. Met Office. <br> [https://www.metoffice.gov.uk/hadobs/hadcrut5/data/HadCRUT.5.1.0.0/download.html](https://www.metoffice.gov.uk/hadobs/hadcrut5/data/HadCRUT.5.1.0.0/download.html)
The specific file used is the “Global (NH+SH)/2 - Annual” CSV which is listed under “HadCRUT5 analysis time series: ensemble means and uncertainties" section of the download page above. <br>
Morice, C. P., Kennedy, J. J., Rayner, N. A., Winn, J. P., Hogan, E., Killick, R. E., et al. (2021). An updated assessment of near-surface temperature change from 1850: the HadCRUT5 data set. Journal of Geophysical Research: Atmospheres, 126, e2019JD032361. https://doi.org/10.1029/2019JD032361|



 

