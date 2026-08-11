---
layout: default
title: "Verifying Data Integrity: HowMuch.net's U.S. Rent Price Map"
date: 2026-08-10
---

<link rel="stylesheet" href="/assets/style.css">

![HowMuch.net map showing the top 10 U.S. cities with the fastest growing and declining two-bedroom rent prices, April 2020 to April 2021](/images/module3.jpeg)
*Figure 1. Top 10 U.S. cities by fastest growing and declining rent prices (HowMuch.net, 2021).*

## Objective
For this exercise, I did verification of a data visualisation published by HowMuch.net. We examined a chart by this site in class and discovered significant data errors. The goal was to select a different visualisation from HowMuch.net, track down its original data source, and verify the source values against the values in the chart. I also identified variables in the chart, assessed whether the data aligned with the question and evaluated how reliable the source is.

I chose HowMuch.net's *"Top 10 U.S. Cities by Fastest Growing and Declining Rent Prices"* (2021). This is a map showing the 10 U.S. cities with he largest percentage change in two-bedroom apartment rent prices, both increasing and decreasing.  
The reason I chose this visualisation is, I was interested in rent fluctuation as I myself live in a two-bedroom apartment in Melbourne. 

## Finding the original data source

HowMuch.net’s article cites its data sources in two places. I checked both but neither point cleanly to the correct report. First, there was a general “Article & Sources” box near the end of the article that said “Apartment Guide-apartmentguide.com”. This linked to a bare homepage which didn't’ have any specific report. Second, and more specifically, the article’s body text states this: “For out data presented, city average rent price trends and percentages were gathered from the Apartment Guide’s Rent Report, May 2021: The State of the Rental Market,” with the words “The State of the Rental Market” hyperlinked to [https://www.rent.com/research/average-rent-price-report/](https://www.rent.com/research/average-rent-price-report/). 
I followed this in-text hyperlink but it didn’t lead to the May 2021 report. Instead, it directed me to Rent.com’s February 2025 Average Rent Report (“Rent Rises as Construction Slows”). This didn’t match the April 2020-April 2021 period described in HowMuch.net’s own visualization.

Since the cited link was unreliable, I carried out a manual search for Apartment Guide reports published around the relevant time period. I found out an “April 2021” report [https://www.apartmentguide.com/blog/rent-report-april-2021/](https://www.apartmentguide.com/blog/rent-report-april-2021/). This looked promising at first. However, it was stated that the data was based on March 2021 rental data compared against March 2020 which is one month earlier than the period in HowMuch.net. Then I checked a few values in this report to confirm that it wasn’t the correct source.
For example, this report listed Las Vegas, NV at a 31.1% two-bedroom rent increase and did not include Scottsdale, AZ or Tucson, AZ in its top 10 increases at all. Both those figures were clearly inconsistent with HowMuch.net’s reported 45.6 (Las Vegas) and 36.8% (Scottsdale) 

Then continuing the search led to the correct report: the “May 2021” report [https://www.apartmentguide.com/blog/rent-report-may-2021/](https://www.apartmentguide.com/blog/rent-report-may-2021/). Its stated methodology matched HowMuch.net’s description exactly which was April 2020 data against April 2021 data. I cross-checked a few values in this report directly against HowMuch.net’s visualisation and all five of HowMuch.net’s top increasing cities (Las Vegas, Buffalo, Scottsdale, Detroit, Tucson) and all five top decreasing cities (Seattle, Miami, Philadelphia, Lexington, San Jose) matched the May 2021 report’s figures exactly, down to decimal percentages. 

In summary, locating the correct source required more than looking up HowMuch.net’s own citation which pointed to an outdated URL. Instead, I had to use the report’s title and stated period to verify the correct report manually. 


## Visually encoded variables

| Variable | How it’s visually encoded | Unit | Level of measurement |
|---|---|---|---|
| City | Text above each large circle | None | Nominal |
| State | Text label below city name | None | Nominal |
Rank (1-10)	Number before each city name, for both increase and decrease groups	None (ordinal position)	Ordinal
Geographic location	Small coloured dots on the map	None 	Nominal
One-year % change in rent 
(Apr 2020- Apr 2021)	Colour of both the small dot on map and large circle. Two colour scales are used.
(pink -> dark maroon for increases,
light blue -> dark blue for decreases)
Exact percentage value is written as text inside the circle	Percent (%)	Ratio
Average rent price, April 2021	Size of the large circle (larger circle = higher price).
Exact value written as text inside the circle	US dollars ($) 	Ratio


•	City and state and nominal because they are category labels with no order or numeric meaning.
•	Rank is ordinal because it has a meaningful order (1st biggest increase, 2nd biggest increase etc.). But the gap between rank 1 and rank 2 isn’t necessarily equal to the gap between rank 2 and rank 3.
•	% change and rent price ($) are ratio because they both have a meaning zero (0% means no change and $0 means no rent).


