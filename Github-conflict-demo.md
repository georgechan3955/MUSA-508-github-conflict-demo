---
title: "Github Conflict Demo"
author: "Anna Duan"
date: "2024-02-02"
output:
  html_document:
    keep_md: yes
    toc: yes
    theme: flatly
    toc_float: yes
    code_folding: hide
    number_sections: no
  pdf_document:
    toc: yes
---

## Setup 
First let's set up our chunk options and required libraries. This will minimize clutter and remove unnecessary messages and warnings. 


## Load data
Next we load our dataset from OpenDataPhilly.org. This dataset is a GeoJSON of all the parks in Philadelphia. We use sf::st_read() to read in spatial data like this.


## Preview data
### I don't want to preview the data
Let's preview our data. Using mapview::mapview(), we can quickly check what the data looks like. This is useful for when you are manipulating spatial data and need to check if things look right at each step.

```r
mapview(parks, col.regions = "chartreuse3", map.types = "CartoDB.DarkMatter")
```

```{=html}
<div class="leaflet html-widget html-fill-item-overflow-hidden html-fill-item" id="htmlwidget-5e1912bb0888a361ca38" style="width:672px;height:480px;"></div>
```
## Map the data
Finally, let's map using ggplot2. Add your name as a subtitle in the labs() function. Also feel free to change the colors and other aesthetics. Once you're satisfied, save and commit. 

```r
ggplot() +
  geom_sf(data = parks, fill = "chartreuse4", color = "transparent") +
  labs(title = "Philadelphia Park System, 2023") + 
  theme_void()
```

![](Github-conflict-demo_files/figure-html/map data-1.png)<!-- -->