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
<vegachart schema-url="{{ site.baseurl }}/assets/json/licenses_charts.json" style="width: 100%"></vegachart>

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
