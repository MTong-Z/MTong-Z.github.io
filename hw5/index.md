---
layout: default
title: UFO Sightings in Space and Time
---

# UFO Sightings in Space and Time

This page shows two visualizations built from the UFO sightings dataset.

[The Data](https://github.com/UIUC-iSchool-DataViz/is445_data/raw/main/ufo-scrubbed-geocoded-time-standardized-00.csv)  
[The Analysis](https://github.com/MTong-Z/MTong-Z.github.io/blob/master/hw5/hw5.ipynb)

## Visualization 1: UFO Sightings Map

<iframe src="map_chart.html" width="750" height="450" frameborder="0"></iframe>

This visualization shows the geographic distribution of UFO sightings using longitude and latitude coordinates. Each point represents one sighting, so the main encoding is spatial position on the map. I also used color to encode UFO shape, which makes it easier to compare common categories such as light, circle, and triangle. I chose color for shape because shape is a categorical variable, and color helps separate categories visually without changing the map position. In the notebook, I cleaned the data by manually assigning column names, converting the datetime column into a proper date format, converting latitude and longitude to numeric values, removing rows with missing coordinates, and creating a year variable from the datetime column. I also limited the map to the most common UFO shapes so that the color scheme stays readable.

## Visualization 2: Number of UFO Sightings Over Time

<iframe src="time_chart.html" width="750" height="320" frameborder="0"></iframe>

This visualization shows the number of UFO sightings over time using a line chart. The x-axis represents year and the y-axis represents the total number of sightings in that year, so the main encoding is position. I used a line chart because it is a clear way to show trends over time and makes it easy to see periods when UFO reports increased or decreased. This plot required transforming the original dataset by extracting the year from the datetime field and then grouping the data by year to count the number of sightings. I did not use color in this plot because it shows one overall trend, and adding unnecessary colors would make the design less clear.

## Interactivity

I added interactivity in two ways. First, the map includes a dropdown menu that allows the viewer to focus on one UFO shape at a time, which makes it easier to compare the spatial pattern of a selected category. Second, the time series includes a brush selection across the x-axis. When a range of years is selected in the line chart, the map updates to show only sightings from those years. This makes the page more interactive and helps the viewer explore how the geographic pattern of sightings changes over time.