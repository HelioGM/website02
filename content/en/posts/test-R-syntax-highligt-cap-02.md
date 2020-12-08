---
title: "R Syntax highlighting cap 02"
subtitle: "Subtitulo"
date: 2020-12-03T10:33:41+09:00
description: "Syntax highlighting test"
draft: false
hideToc: false
enableToc: true
enableTocContent: false
author: Helio
authorEmoji: 🎅
pinned: false
tags:
- hugo
series:
-
categories:
- hugo
image: images/feature2/color-palette.png
---

## Code Syntax Highlighting

Verify the following code blocks render as code blocks and highlight properly. 

More about tuning syntax highlighting is the [Hugo documentation](https://gohugo.io/content-management/syntax-highlighting/).

### R

``` r {hl_lines=[4,"6-7"]}

library(readr)
library(mosaic)
library(FSA)
library("ggplot2")
library(readxl)
library(knitr)
library(doBy)
library(agricolae)

options(scipen=999, digits = 0)

mydata <- read_excel("./data/2016-Solanum-01-11_Isolates(Germplasms).xlsx")

## getwd()


## Load all the libraries needed and the data

```


