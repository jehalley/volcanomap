---
title: "Leaflest Project"
author: "Jeff Halley"
date: "April 14, 2019"
output: html_document
---

```{r setup, include=FALSE}
knitr::opts_chunk$set(echo = TRUE)
```

## R Markdown
The map below shows the locations and names of all currently active volcanos. The location of the volcanos was taken from http://volcano.oregonstate.edu/volcano_table

```{r}
#volcano data from http://volcano.oregonstate.edu/volcano_table
volcanos<-read.csv("volcanos.csv")
library(leaflet)
volcanomap<-leaflet()%>%addTiles()%>%addMarkers(lat=volcanos$Lat,lng=volcanos$Long,popup=volcanos$Name)
volcanomap
```
