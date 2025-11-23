---
name: IS 455 Homework 5
tools: [Python, HTML, vega-lite]
image: assets/pngs/h5_licenses.png
description: Practice with Altair + Jekyll using IDFPR Professional License data
custom_js:
  - vega.min
  - vega-lite.min
  - vega-embed.min
  - justcharts
---

# IS 455 Homework 5



<!-- Combined interactive chart -->
<vegachart schema-url="{{ site.baseurl }}/assets/json/licenses_plots.json" style="width: 100%"></vegachart>

## Plot 1: Number of Professional Licenses Issued (2000 - 2021)
The plot shows the number of professional licenses issued each year from 2000 to 2021. To create it I filtered the dataset to only include licenses originally issued within the year range and grouped by the 'Issue Year' to get the total number of licenses issued each year. Since I am displaying discrete yearly counts I chose to go with a bar chart, with the issue year on the x-axis encoded as ordinal (since year is nominal in this context but the order matters) and the 'Number of Licenses' on the y-axis, encoded as quantitative beacuse it is a count. The color is meant to help with the interaction aspect so the user can tell which bar they have selected, displayed in dark blue vs. light blue for the unselected bars.  

## Plot 2: License type Distribution (Selected Year)
The second plot gives a breakdown of the types of licenses issued in the year selected from the bar chart, as percentage of all licenses issued in that year. I grouped the original data by the 'Issue Year' and 'License Type' to obtain a count of licenses of each type for each year, then divided by the total number of licenses issued in that year to get the percentages. Here, I chose to go with a horizontal bar graph because I am displaying nominal categories, there is no order to the type of license (& to not do a pie chart:). The 'Percentage' is encoded on the x-axis as quantitative and formated as a percentage and the 'License Type' is on the y-axis encoded as nominal and sorted by the descending order of the x-axis, to show the largest "contributor" first. I did not use any colormap here because I feel like the bar length and order in which the information is displayed already communicates the intended message. 


## Interactivity
These two plots are linked through a year selection defined in Altair. When a bar on Plot 1 gets selected, it stores the year as a selection and Plot 2 updates to show the License type distribution for that year. It lets you dynamically see the composition of license types changes from year to year.
---

## The Data & The Analysis

<div class="left">
  {% include elements/button.html
     link="https://github.com/UIUC-iSchool-DataViz/is445_data/raw/main/licenses_fall2022.csv"
     text="The Data" %}
</div>

<div class="right">
  {% include elements/button.html
     link="https://github.com/manuelarodr/manuelarodr.github.io/blob/main/python_notebooks/Workbook.ipynb"
     text="The Analysis" %}
</div>
