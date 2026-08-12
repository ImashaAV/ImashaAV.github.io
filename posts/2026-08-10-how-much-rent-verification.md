---
layout: default
title: "Verifying Data Integrity: HowMuch.net's U.S. Rent Price Map"
date: 2026-08-10
---

<link rel="stylesheet" href="/assets/style.css">

# Verify It !: Verifying source data against chart data

### Published: 10 August 2026

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
| Rank (1-10) |	Number before each city name, for both increase and decrease groups |	None| Ordinal |
| Geographic location	| Small coloured dots on the map |	None |	Nominal |
| One-year % change in rent (Apr 2020- Apr 2021) |	Colour of both the small dot on map and large circle. Two colour scales are used. (pink -> dark maroon for increases, light blue -> dark blue for decreases) Exact percentage value is written as text inside the circle |	Percent (%)	| Ratio |
| Average rent price, April 2021 | Size of the large circle (larger circle = higher price). Exact value written as text inside the circle	| US dollars ($) | 	Ratio |


•	City and state and nominal because they are category labels with no order or numeric meaning.  
•	Rank is ordinal because it has a meaningful order (1st biggest increase, 2nd biggest increase etc.). But the gap between rank 1 and rank 2 isn’t necessarily equal to the gap between rank 2 and rank 3.  
•	% change and rent price ($) are ratio because they both have a meaning zero (0% means no change and $0 means no rent).

## Alignment of data and question

HowMuch.net’s visualization doesn’t explicitly state a research question. So, I decided that the implied question inferred from its title should be: *“Which US cities experienced the fastest increasing and decreasing rent prices over the past year?”*

The data used to answer this is the percentage change across a year in average two-bedroom apartment rent prices from April 2020 to April 2021. This is calculated for the 100 most populated cities in the US, sourced from Apartment Guide’s May 2021 Rent Report.

Overall, there is a strong alignment between the data and the question, but I will explore this on a few specific points.  

•	**Apartment size**: The question is broadly around “rent prices”, but the data only covers two-bedroom apartments. There could be different rent trends for other apartment types like studios, one-bedrooms or larger units. So, the chart technically answers a narrower question than what its title suggests.  

•	**Sample of selected cities**: The data is limited to the 100 most populated US cities. This is understandable in practical sense, but it means the chart cannot claim to represent all US cities.  

•	**Time period**: The one-year window considered in this visualization (April 2020-April 2021) is a volatile period in the market. The Airbnb market was affected by pandemic related remote work and migration. This actually suits the question well, because it captures a period of extreme change. But we should keep in mind that these swings may not reflect a typical year for rent prices.

Overall, I think the data is a direct match for the question. The data doesn’t measure something entirely different from what it claims to show. The main issue is that the title talks broadly about “rent prices” and “US cities” but the data considers only two-bedroom apartments, and only in the 100 biggest cities. So, it’s more of a scope not being addressed properly than the data being wrong.

## Verifying the values

| Rank | City, State | HowMuch.net % | Source % | HowMuch.net $ | Source $ | Match? |
|-|-|-|-|-|-|-|
| 1 | Las Vegas, NV | 45.6% | 45.6% | $1,997 | $1,997 | ✓ |
| 2 | Buffalo, NY | 41.8% | 41.8% | $1,853 | $1,853 | ✓ |
| 3 | Scottsdale, AZ | 36.8% | 36.8% | $3,125 | $3,125 | ✓ |
| 4 | Detroit, MI | 31.4% | 31.4% | $2,320 | $2,320 | ✓ |
| 5 | Tucson, AZ | 28.8% | 28.8% | $1,366 | $1,366 | ✓ |
| 6 | Arlington, TX | 27.0% | 27.0% | $1,667 | $1,667 | ✓ |
| 7 | Virginia Beach, VA | 24.6% | 24.6% | $1,671 | $1,671 | ✓ |
| 8 | Orlando, FL | 23.6% | 23.6% | $2,229 | $2,229 | ✓ |
| 9 | Henderson, NV | 22.1% | 22.1% | $1,897 | $1,897 | ✓ |
| 10 | Sacramento, CA | 21.2% | 21.2% | $2,521 | $2,521 | ✓ |
| 1 | Seattle, WA | -26.3% | -26.3% | $2,884 | $2,884 | ✓ |
| 2 | Miami, FL | -20.5% | -20.5% | $2,383 | $2,383 | ✓ |
| 3 | Philadelphia, PA | -20.3% | -20.3% | $2,423 | $2,423 | ✓ |
| 4 | Lexington, KY | -17.7% | -17.7% | $976 | $976 | ✓ |
| 5 | San Jose, CA | -14.7% | -14.7% | $3,054 | $3,054 | ✓ |
| 6 | Fort Wayne, IN | -14.5% | -14.5% | $839 | $839 | ✓ |
| 7 | San Antonio, TX | -14.2% | -14.2% | $1,216 | $1,216 | ✓ |
| 8 | Fort Worth, TX | -14.1% | -14.1% | $1,335 | $1,335 | ✓ |
| 9 | St. Petersburg, FL | -12.8% | -12.8% | $1,474 | $1,474 | ✓ |
| 10 | Garland, TX | -12.7% | -12.7% | $1,423 | $1,423 | ✓ |

Looking at the above table, it’s clear that all 20 cities’ both percentage and the dollar figure match the source exactly.

All 20 data points in the visualization in HowMuch.net’s map were successfully verified against Apartment Guide’s May 2021 Rent Report. Every value matched exactly, and there are no discrepancies, not even rounding differences.

The numbers reported by HowMuch.net are fully accurate and consistent with the original source. The only issue I identified was not with the data itself, but with finding the citation error. The in-text hyperlink to the source was incorrect and, at the time I checked, redirected to unrelated reports (Step 4.1). This means,  a reader following the published citation wouldn’t land on the correct data.

Given that every value checked out precisely, I have high confidence with the data accuracy in this visualization. The verification process confirms that HowMuch.net recorded the source figures correctly, and did not round inappropriately, or alter any values when producing the chart.


## Quality of data source and limitations

The data source which is Apartment Guide is a large online apartment listing platform operating across the United States. Part of the same corporate family is established as Rent.com. Apartment Guide has published its Rent Report monthly for several years using a clearly stated methodology which is, a weighted average formula applied across a fixed set of the 100 most populated US cities. Since its consistent in the methodology used, I think it’s a reasonably reputable source.
Limitations:

•	**It’s a commercial source, not a government one**: Apartment Guide is a rental listings company, and its data reflect the listings on its own platform (and Rent.com’s) rather than an independently conducted census of the rental market. This means the data could be influenced by which landlords choose to list with Apartment Guide/Rent.com rather than representing the entire rental market in the city.

•	**“Average” rent is based on available listings, not all rented units**: The figures show the asking prices for available apartments at a point in time, not the actual rents being paid across all occupied units in a city. Therefore, it can produce different results to a government source which uses census information.


Overall, Apartment Guide can be considered a reasonably reputable source for this purpose. This is particularly because of the accuracy confirmed during verification (Step 4.5) However, it shouldn’t be treated as equivalent to a government dataset. Readers should understand that the figures in this site represent listed apartments from a private industry platform, and not a full census of the rental market in the US.


## References

Apartment Guide. (2021, May 28). *Rent report, May 2021: The state of the rental market*.[https://www.apartmentguide.com/blog/rent-report-may-2021/](https://www.apartmentguide.com/blog/rent-report-may-2021/)

HowMuch.net. (2021, June 4). *Top 10 U.S. cities by fastest growing and declining rent prices*. [https://howmuch.net/articles/top-10-us-cities-by-fastest-growing-or-declining-rent-prices](https://howmuch.net/articles/top-10-us-cities-by-fastest-growing-or-declining-rent-prices)
