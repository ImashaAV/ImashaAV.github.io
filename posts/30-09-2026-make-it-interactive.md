---
layout: default
title: "Make it interactive"
date: 2026-09-30
---

<link rel="stylesheet" href="/assets/style.css">

# Make it interactive

### Published: 30 September 2026

<iframe src="/temperature_stripes_new.html" width="100%" height="600" style="border:none;"></iframe>

For this exercise, I decided to reuse the master visualisation I did for "Copying the Master". The visualisation contains bars showing the temperature anomalies from 1859 to 2025, rebaselined against the 1961-2010 average.

First I drew the graph using plotly without any interactivity. The graph was drawn according to plotly's default styling and didn't really mimic the original visualisation I was going for. I made some changes by removing the legend and making the background dark.

For interactivity, I added the hover feature where when hovering over the bars, it shows the exact year and the temperature change value. 
The second component of interactivity was, a slider which can be adjusted to a specific year range so that the user can inspect a specific time period they're interested in.
