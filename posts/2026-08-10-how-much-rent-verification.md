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


I chose HowMuch.net's *"Top 10 U.S. Cities by Fastest Growing and Declining Rent Prices"* (2021). This is a map showing the 10 U.S. cities with the largest percentage change in two-bedroom apartment rent prices, both increasing and decreasing.  
The reason I chose this visualisation is, I was interested in rent fluctuation as I myself live in a two-bedroom apartment in Melbourne. 

## 4.2 

Apartment Guide. (2021, May 28). Rent report, May 2021: The state of the rental market. [https://www.apartmentguide.com/blog/rent-report-may-2021/](https://www.apartmentguide.com/blog/rent-report-may-2021/)

## 4.3

 | Variable | How it’s visually encoded | Unit | Level of measurement |
|---|---|---|---|
| City | Text above each large circle | None | Nominal |
| State | Text label below city name | None | Nominal |
| Rank (1-10) |	Number before each city name, for both increase and decrease groups |	None| Ordinal |
| Geographic location	| Small coloured dots on the map |	None |	Nominal |
| One-year % change in rent (Apr 2020- Apr 2021) |	Colour of both the small dot on map and large circle. Two colour scales are used. (pink -> dark maroon for increases, light blue -> dark blue for decreases) Exact percentage value is written as text inside the circle |	Percent (%)	| Ratio |
| Average rent price, April 2021 | Size of the large circle. Exact value written as text inside the circle	| US dollars ($) | 	Ratio |


