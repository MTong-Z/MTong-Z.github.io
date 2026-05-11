---
layout: default
title: Final Project
---

#### Group Member: Miantong Zhang, Mianchen Zhang

# How Does Urbana’s Spending Relate to Community Development Activity?

## Introduction

Urbana, Illinois is a small city, but like any city, it runs on public money. Every year, the city government allocates funds across departments to keep essential services running and neighborhoods functioning. For residents, these spending decisions shape the places they live in. But how well does the city's spending actually reflect what is happening on the ground?
This project focuses on one specific question: does Urbana's spending on community development and public works track real development activity in the city?
To answer this, we combine two public datasets. The first is the City of Urbana's open expenditure records, which detail how much money each city department spends each year. Among all departments, we focus on Community Development and Public Works, two departments whose core responsibilities directly involve building, maintaining, and regulating the city's physical environment. The second dataset is Urbana's Community Development Permits, which tracks the number of building and development permits issued over time. We chose this as our context dataset because permits are a direct, on-the-ground measure of the activity that these two departments are meant to support. If spending in these departments is working as intended, we might reasonably expect permit activity to follow.
But our analysis suggests the relationship is more complicated. Permit issuance in Urbana climbed steadily from 2013 to 2024, while Community Development department spending was far more volatile, spiking in certain years and dropping sharply in others. Rather than moving together, the two trends frequently diverge, which raises a natural question: what is driving the gap, and what does it tell us about how Urbana prioritizes its resources?

## Data Overview

This project draws on two publicly available datasets from the Illinois open data portal.
The primary dataset is the City of Urbana Open Expenditures, which records individual payment transactions made by the city government from July 2012 through December 2025, totaling approximately 174,941 entries. Each record represents a single payment, including the department responsible and the amount spent. For this project, we focus specifically on the Community Development and Public Works departments, as their spending most directly relates to the city's physical development activity.
The context dataset is the City of Urbana Community Development Permits Issued, which logs building and development permits approved by the city from January 1999 through April 2026, with approximately 48,551 records. We use annual permit counts as a proxy for real-world development activity, providing a ground-level measure of whether development is actually happening in Urbana, independent of what the city budget says.

[Main Dataset](https://data.illinois.gov/Local-Government/City-Of-Urbana-Open-Expenditures-Payment-Details/p34w-i7rn/about_data)

[Context Dataset](https://data.illinois.gov/Local-Government/City-of-Urbana-Community-Development-Permits-Issue/dvw9-7wyx/about_data)

[The Analysis](https://github.com/MTong-Z/MTong-Z.github.io/blob/master/projects/FP3/Workbook.ipynb)

## Visualization 1: Overall Spending by Department

<iframe src="overall_spending_by_department.html" width="750" height="450" frameborder="0"></iframe>

This visualization shows the top departments in Urbana based on total spending. Each bar represents a department, and the length of the bar encodes total expenditures. A bar chart is appropriate here because it allows for a clear comparison across categories, making it easy to identify which departments account for the largest shares of city spending.

Public Works and Community Development deserve special attention because they account for the largest spending totals while representing different public priorities. Public Works reflects the cost of maintaining streets, facilities, utilities, and other basic infrastructure that residents depend on every day, so changes in this department can affect the city broadly and immediately. Community Development is important for a different reason: it captures spending connected to housing, redevelopment, and neighborhood improvement, which shapes longer-term growth and quality of life. Together, these two departments highlight both the city’s day-to-day operating responsibilities and its longer-term investment strategy.

## Visualization 2: Development-Related Spending Over Time

<iframe src="development_related_spending_over_time.html" width="750" height="450" frameborder="0"></iframe>

This visualization compares yearly spending in Community Development and Public Works. The x-axis represents fiscal year, and the y-axis represents total expenditures. A line chart is used because it effectively shows how each department’s spending changes over time and makes it easier to compare their trends side by side.

This chart focuses on Community Development and Public Works because they represent two important but different kinds of development-related spending. Public Works stays above Community Development in most years, suggesting that infrastructure and maintenance create a larger and more consistent budget commitment. Community Development is more volatile, with especially large spikes in 2014, 2015, and 2025, which may reflect periods of concentrated redevelopment, housing, or neighborhood investment. Looking at these two departments together helps separate steady infrastructure spending from more project-driven development activity.

## Transition to Context Dataset

Spending trends alone cannot explain actual development activity. A department may spend more money in a given year, but that does not automatically show how many projects were started, what kinds of construction were taking place, or whether development activity increased across the city. To add that missing context, I use the Urbana permits dataset, which records permit issuance related to building and other development work. This context dataset makes it possible to connect financial patterns in the expenditures data to evidence of real development activity on the ground.

## Visualization 3: Community Development Permits Over Time

<iframe src="community_development_permits_over_time.html" width="750" height="450" frameborder="0"></iframe>

This chart uses the permits dataset to track development activity more directly than spending alone. Permit issuance was higher in the early 2000s, declined through the late 2000s and early 2010s, and then strengthened again after 2021, exceeding 2,000 permits in both 2023 and 2024. That rebound suggests recent development activity has picked up even when expenditure totals are harder to interpret by themselves. The drop in 2026 should be read cautiously because the file appears to have been downloaded on May 10, 2026, so the 2026 count likely reflects only part of the year.

## Visualization 4: Development Activity and Public Spending Trends

<iframe src="development_activity_and_public_spending_trends.html" width="1000" height="520" frameborder="0"></iframe>

To better compare the two datasets despite their different units, both Community Development spending and permit activity were converted into indexed relative values using 2013 as the baseline year (2013 = 100). This allows the visualization to focus on relative change over time rather than raw dollar amounts or permit counts.

The indexed chart shows that Community Development spending experienced a sharp early spike, especially around 2014, but later remained below the 2013 baseline for much of the period. In contrast, permit activity gradually increased after the baseline year and rose especially strongly after 2021. This divergence suggests that Community Development spending does not directly track the number of permits issued each year. Instead, spending may reflect longer-term planning cycles, staffing or administrative costs, infrastructure preparation, maintenance needs, inflation, or delayed responses to development activity. Overall, the comparison suggests that Urbana’s spending relates to community development activity, but not in a simple one-to-one way.

## Visualization 5: What Drives Development-Related Spending in Urbana?

<iframe src="what_drives_development_related_spending_dashboard.html" width="1100" height="980" frameborder="0"></iframe>

After comparing development activity and public spending trends over time, this dashboard shifts the analysis from overall patterns to the composition of spending itself. Rather than focusing only on whether spending rises or falls alongside permit activity, the dashboard helps identify where development-related funding is actually going. By filtering by year and department, it becomes possible to examine which spending categories, projects, and vendors account for the largest shares of Community Development and Public Works expenditures.

This deeper breakdown helps explain why spending may not directly follow permit counts each year, since development-related expenditures can also be shaped by infrastructure projects, contractual services, maintenance needs, staffing, administrative costs, or long-term planning priorities. In this way, the dashboard extends the project’s central question by investigating what may drive Urbana’s development-related spending beyond permit activity alone.

## Interactivity

Interactivity is incorporated through hover tooltips, zooming, and dynamic filtering. Users can hover over the charts to see exact values, and several of the visualizations allow scale-based exploration through interactive navigation. The dashboard provides the richest interaction: users can filter by year and by department option to compare Community Development, Public Works, or both combined. This interaction design makes the analysis more transparent and helps users move from broad trends to the specific spending categories and vendors that drive those patterns.

## Discussion

The comparison between Urbana’s development-related spending and permit activity suggests that the relationship between government expenditures and real development activity is more complex than a direct one-to-one connection. Although permit activity increased steadily after 2021, Community Development spending remained uneven across the same period. This suggests that public spending may reflect planning cycles, infrastructure preparation, staffing costs, administrative operations, and delayed investment patterns instead of immediate development activity alone.

The dashboard analysis also supports this interpretation by showing that much of the development-related spending is connected to infrastructure projects, maintenance services, vendors, and operational categories that do not directly match yearly permit counts. Permit issuance captures visible development activity in the city, while expenditure records reflect the broader financial responsibilities involved in managing and maintaining urban systems over time.

There are several limitations in the datasets used for this project. Permit counts do not represent all forms of development activity because permits vary in size and importance. One permit may represent a small residential repair, while another may represent a large construction project. The expenditure dataset also records individual payment transactions rather than complete project budgets, so spending patterns may appear uneven when projects continue across multiple years or payments are processed at different times. In addition, this analysis does not account for inflation, population growth, or economic conditions that may influence both spending and development activity.

This project also highlights the value of public financial transparency and civic data visualization. Residents may expect increases in government spending to directly correspond to visible development in the city, but the visualizations suggest that public investment priorities often operate on longer timelines. By combining expenditure data with permit activity, the project provides a broader view of how Urbana allocates resources and supports development over time.

## Conclusion

This project explored whether Urbana’s spending on Community Development and Public Works aligns with community development activity over time. By combining open expenditure records with permit issuance data, the analysis showed that development activity and government spending are related, but not in a direct or proportional way.

The visualizations showed that Public Works spending remained consistently high across most years, while Community Development spending changed more dramatically. Permit activity generally increased over time, especially after 2021. When both datasets were compared using indexed values, the trends often diverged instead of moving together.

These findings suggest that development-related spending reflects broader planning, infrastructure, and operational priorities beyond the number of permits issued each year. Government spending may support long-term maintenance and future development in ways that are not immediately visible through yearly permit activity alone.

Future work could expand this analysis by separating residential and commercial permits, adjusting expenditures for inflation, comparing Urbana with nearby cities, or examining spending patterns across neighborhoods. Additional datasets related to housing or transportation could also help provide a more detailed understanding of how public spending influences community development over time.