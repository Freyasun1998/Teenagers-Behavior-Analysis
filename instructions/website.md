# Website 

The output of the project will be delivered through a self-contained website in the `website/` subdirectory, having `index.html` as the starting point. You will build the website incrementally over the milestones.

The code to build the website will be in the `website-source/` directory.

## Structure 

The website must have the following structure:

* Landing and project description page - website/index.html - You are populating this site during the final submission
* Exploratory data analysis page - website/eda.html - You are populating this site during the final submission
* NLP page - website/nlp.html - You are populating this site during milestone 2
* ML page  - website/ml.html - You are populating this site during milestone 3
* Conclusion page - website/conclusion.html - You are populating this site during the final submission


## Requirements

* Your website **must be accessible via an `index.html` file in the `website/`folder.** You can build the website using the tool(s) of your preference. choose however you would like to build your website (using `Rmarkdown`, editing HTML directly, any other framework, etc.)
* You can use CSS frameworks, such as [Bootstrap](https://getbootstrap.com/), [Materialize](https://materializecss.com/), or [Distill](https://distill.pub/about/) and include external libraries (jQuery, leaflet.js, moment.js, etc.).  Layers such as NVD3, Vega-lite, Highcharts, etc. are allowed. Many of these have wrapper packages in R and Python. For example, the package `altair` (in both [R](https://vegawidget.github.io/altair/) and [Python](https://altair-viz.github.io)) wraps Vega-lite, and the package `plotly` (in both [R](https://plotly.com/r) and [Python](https://plotly.com/python)), among other packages, wraps D3. Other packages you may use are any of the [`htmlwidgets`](https://www.htmlwidgets.org) packages in R, [`bokeh`](https://bokeh.org) or [`holoviz`](https://holoviz.org) (and it's accompanying ecosystem) in Python, as well as specialized packages for geospatial ([`leaflet`](https://rstudio.github.io/leaflet/), [`tmap`](https://geocompr.robinlovelace.net/adv-map.html) in R, [`folium`](https://python-visualization.github.io/folium/index.html) in Python) and networks ([`igraph`](https://igraph.org), [`NetworkX`](https://networkx.org), `bokeh`, `plotly`). 
* You do not need to make the site public as we will look at it from the repository. You may make it public (just the website sub-directory) using your preferred method. However, the naming convention of `website/` as the directory may not work. 
* No custom backends (Node.js, Python, etc) and database systems, such as Postgres or MySQL.
* The communication needs to be effective with clean aesthetics, but you do not need to get too fancy.
* You may include the `html` exports of notebooks



