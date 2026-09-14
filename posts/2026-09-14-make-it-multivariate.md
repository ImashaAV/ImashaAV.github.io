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

I decided to add **World region** as the third variable as it would be meaningful to know which areas in the world are responsible for the CO2 emissions shown in the chart. I decided to classify the regions into 6 by continents: North America, South America, Europe, Africa, Asia and Oceania.

I inspected the dataset downloaded from Our World in Data (OWID) and found out that it contained the CO2 emissions for every country. So I can use this dataset itself to incorporate the third variable into the visualisation.   
Upon further inspection I realised that the continents were aggregated in two ways:
"Europe" and "Europe (GCP)" appeared as separate entities. The plain continent entities (e.g. "Europe", coded OWID_EUR) had data across all three columns.  
However, the "(GCP)" entities were missing both the Land-use change and Total columns entirely.  
Since my visualisation needs both fossil fuel and land-use values, I decided to use the plain OWID continent entities rather than the GCP ones.

I filtered the dataset down to the six regions I want. Then I removed the 'Total' column as it was redundant data because it is the sum of fossil fuel emissions and land-use change emissions. 

I started by drawing the faceted chart outline. Then I visualised my data. Each column facet corresponded to a region. The two column facets showed the two categories (Fossil fuels and land-use). X axis within each panel showed the year and y axis within each panel showed emissions in tonnes.

Then I added the title and X and Y axis labels. To get rid of the scientific notations in the y axis, I changed the unit of emissions from tonnes to billion tonnes. The strict boundaries around each facet made it look like separate charts. Therefore, I added a common gridline to each facet
