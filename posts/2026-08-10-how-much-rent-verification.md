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
For this exercise, I did verification of a data visualisation published by HowMuch.net. The goal was to select a visualisation from HowMuch.net, track down its original data source, and verify the source values against the values in the chart. I also identified variables in the chart, assessed whether the data aligned with the question and evaluated how reliable the source is.

I chose HowMuch.net's *"Top 10 U.S. Cities by Fastest Growing and Declining Rent Prices"* (2021). This is a map showing the 10 U.S. cities with the largest percentage change in two-bedroom apartment rent prices, both increasing and decreasing.  
The reason I chose this visualisation is because I was interested in rent fluctuation as I too live in a two-bedroom apartment in Melbourne. 

## Data source

Apartment Guide. (2021, May 28). Rent report, May 2021: The state of the rental market. [https://www.apartmentguide.com/blog/rent-report-may-2021/](https://www.apartmentguide.com/blog/rent-report-may-2021/)

## Visually encoded variables

 | Variable | How it’s visually encoded | Unit | Level of measurement |
|---|---|---|---|
| City | Text above each large circle | None | Nominal |
| State | Text below city name | None | Nominal |
| Rank (1-10) |	Number before each city name, for both increase and decrease groups |	None| Ordinal |
| Geographic location	| Small coloured dots on the map |	None |	Nominal |
| One-year % change in rent (Apr 2020- Apr 2021) |	Colour of both the small dot on map and large circle. Two colour scales are used. (pink -> dark maroon for increases, light blue -> dark blue for decreases) Exact percentage value is written as text inside the circle |	Percent (%)	| Ratio |
| Average rent price, April 2021 | Size of the large circle. Exact value written as text inside the circle	| US dollars ($) | 	Ratio |

•	City and state are nominal because they are category labels with no order or numerical meaning.  
•	Rank is ordinal because it has a meaningful order. But the gap between 1st and 2nd isn't necessarily equal to the gap between 2nd and 3rd).  
•	% Change and rent price ($) are ratio because they both have a meaningful zero (0% means no change and $0 means no rent). 

## Alignment of data and the question

HowMuch.net’s visualisation doesn’t explicitly ask a research question. So, I decided that the implied question from the title must be: “Which US cities have the fastest increasing and decreasing rent prices over the past year?” 

The data used to answer this is the percentage change across a year in average two-bedroom apartment rent prices from April 2020 to April 2021. This is calculated for the 100 most populated cities in the US, sourced from Apartment Guide’s May 2021 Rent Report. 

Overall, there is a strong alignment between the data and the question.  
However, there are two points which could use better alignment:

•	**Apartment size**: The question is around “rent prices”, but the data only covers two-bedroom apartments. There could be different rent trends for other apartment types like studios or one-bedroom apartments. So, the chart technically answers a narrower question than what the title suggests.  

•	**Sample of selected cities**:  The data is limited to the 100 most populated US cities. This is understandable in practical sense, but it means the chart cannot claim to represent all US cities. 

Overall, I think the data is a direct match for the question. The data doesn’t measure something entirely different from what it claims to show. The main issue is that the title talks about “rent prices” and “US cities”, but the data considers only two-bedroom apartments, and only in the 100 biggest cities. So, it’s more of the scope not being addressed properly than the data being wrong. 

## Verifying source data with visually encoded values

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

According to the above table, all 20 cities’ percentage and dollar values match the source exactly. Therefore, all data points in the HowMuch.net visualisation are successfully verified against Apartment Guide’s May 2021 Report. There are no discrepancies, not even rounding differences. 

The values in HowMuch.net are consistent with the original source. The only issue I identified was not with the data itself, but with finding the correct source. The in-text hyperlink to the source was incorrect and, at the time I checked, redirected to an unrelated report. This means that a reader following the published citation wouldn’t lan on the correct data. 

Given that every value matched perfectly, I am highly confident about the data accuracy in this visualisation. 

## Examining the quality of the data source

The data source, which is Apartment Guide, is a large online apartment listing platform which has published its Rent Report monthly for several years. Since its a consistent website that publishes information regularly, I consider it to be a reputable source. 

**Limitations**: 

•	**It’s a commercial source, not a government one**: Apartment Guide is not a government owned source. It’s owned by Redfin, operated through Rent group INC (Redfin Corporation, 2021). This means the data could be influenced by which landlords decide to list with Apartment Guide rather than representing the entire rental market in the city. 

 •	**“Average” rent is based on available listings, not all rented units**: The figures show the asking prices for available apartments at a point in time, not the actual rents being paid across all occupied units in a city. Therefore, it can produce different results from a government source which uses census information. 

Overall, Apartment Guide can be considered a reputable source for this purpose, This is mostly because of the accuracy confirmed during verification. However, it shouldn’t be considered equivalent to a government dataset. That is because the figures in the site represent listed apartments from a private platform, and not a full census of the rental market in the US.  

 
**References**
Redfin Corporation. (2021, February 19). Redfin announces agreement to acquire RentPath for $608 million [Press release]. U.S. Securities and Exchange Commission. 
[https://www.sec.gov/Archives/edgar/data/1382821/000138282121000023/rushmorepressrelease.htm](https://www.sec.gov/Archives/edgar/data/1382821/000138282121000023/rushmorepressrelease.htm)

