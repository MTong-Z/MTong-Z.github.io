---
layout: default
title: Where Does Urbana Spend Its Money?
---
## Group Member: Miantong Zhang, Mianchen Zhang

# Where Does Urbana Spend Its Money?

This page explores how the City of Urbana spends its public funds using official expenditure data. While city budgets affect everyday life, most people do not have a clear understanding of where the money actually goes. This article presents several visualizations to help the public better understand spending patterns, changes over time, and where the money ultimately ends up.

[The Data](https://data.illinois.gov/Local-Government/City-Of-Urbana-Open-Expenditures-Payment-Details/p34w-i7rn/about_data)

[The Analysis](https://github.com/MTong-Z/MTong-Z.github.io/blob/main/FP3/Workbook.ipynb)

## Visualization 1: Spending by Department

<iframe src="department_chart.html" width="750" height="450" frameborder="0"></iframe>

This visualization shows the top departments in Urbana based on total spending. Each bar represents a department, and the length of the bar encodes total expenditures. I used a bar chart because it allows for clear comparison across categories. The data was grouped by department and summed to calculate total spending.

From this chart, it is clear that a large portion of the city’s budget is concentrated in a few key departments. Public Works has the highest spending, followed by Community Development and Police. These departments are responsible for infrastructure, housing, and public safety, which are core functions of local government. This helps explain why they receive the largest share of funding.

## Visualization 2: Spending Over Time

<iframe src="time_chart.html" width="750" height="350" frameborder="0"></iframe>

This visualization shows how total city spending changes over time. The x-axis represents fiscal year, and the y-axis represents total expenditures. A line chart is used because it effectively shows trends and fluctuations across years.

The chart reveals that Urbana’s spending is not constant. There are noticeable peaks around 2014 and 2025, and a significant drop around 2019. These changes may reflect economic conditions, policy adjustments, or external events such as budget restructuring. Understanding these trends provides important context for interpreting the overall spending patterns.

## Visualization 3: Top Vendors Receiving Payments

<iframe src="vendor_chart.html" width="750" height="450" frameborder="0"></iframe>

This visualization highlights the vendors that receive the largest payments from the city. Each bar represents a vendor, and the chart shows the total amount of money paid to them.

One key insight from this chart is that “Employee Payroll” is by far the largest category. This indicates that a significant portion of city spending goes toward salaries and benefits for employees. Other major recipients include government-related organizations such as the Internal Revenue Service and healthcare providers. This visualization helps the public understand that city spending is not only about projects, but also about maintaining essential services and workforce operations.

## Visualization 4: Interactive Dashboard for Exploration

<iframe src="dashboard.html" width="750" height="900" frameborder="0"></iframe>

This interactive dashboard combines multiple views of the dataset and allows users to explore the data more deeply. The top chart shows spending over time, and users can select a range of years by dragging across the timeline. The department and vendor charts below will update automatically based on the selected time range.

This interaction helps users investigate specific periods and see how spending priorities change over time. For example, users can focus on a particular set of years and observe how department spending or vendor payments differ from the overall trend. This makes the visualization more engaging and allows for a more personalized exploration experience.

## Interactivity

Interactivity is incorporated through hover tooltips and dynamic filtering. Users can hover over charts to see exact values, and in the dashboard, they can select a time range to filter the other views. This interaction design helps users better understand the data without requiring technical knowledge, making the visualizations more accessible to the general public.
