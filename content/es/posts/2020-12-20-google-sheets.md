---
title: "Google Sheets"
date: 2020-12-19T19:12:10-08:00
description: Google Sheets
authorEmoji: 📡
draft: false
hideToc: false
enableToc: true
enableTocContent: false
tocPosition: inner
tocLevels: ["h2", "h3", "h4"]
tags:
-
series:
-
categories:
-
image: https://upload.wikimedia.org/wikipedia/commons/thumb/0/08/Google_Sheets_logo.svg/1200px-Google_Sheets_logo.svg.png
---

```{r LoadPackages, message = FALSE, warning = FALSE, fig.cap='Figure caption'}   

library(readr)
library(mosaic)
library(FSA)
library("ggplot2")
library(readxl)
library(knitr)
library(doBy)
library(agricolae)
options(scipen=999, digits = 0)
## Load all the libraries needed and the data

```



<iframe src="https://docs.google.com/spreadsheets/d/e/2PACX-1vTADEwnTfsuU0PipEXHK1FVtoJjljwQCvOzkUbdo5PiAJ5w9kBWGSxg389vSE5xhzifbBOGecjByTAn/pubhtml?widget=true&amp;headers=false" width="420" height="300"></iframe>


[Datos](https://docs.google.com/spreadsheets/d/e/2PACX-1vTADEwnTfsuU0PipEXHK1FVtoJjljwQCvOzkUbdo5PiAJ5w9kBWGSxg389vSE5xhzifbBOGecjByTAn/pub?output=xlsx)


```{r LoadFiles, message = FALSE, warning = FALSE, fig.cap='Figure caption'}   

mydata <- read_excel("https://docs.google.com/spreadsheets/d/e/2PACX-1vTADEwnTfsuU0PipEXHK1FVtoJjljwQCvOzkUbdo5PiAJ5w9kBWGSxg389vSE5xhzifbBOGecjByTAn/pub?output=xlsx")

```
.