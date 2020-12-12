---
title: "Resaltador de sintaxis"
subtutle: "Archivo MD"
date: 2020-12-11T23:45:00-08:00
description: "Prueba de resaltador de sintaxis con archivos en formato MD"
draft: false
hideToc: false
enableToc: true
enableTocContent: false
author: Helio
authorEmoji: 👽
pinned: false
tags:
- Markdown
series:
- Pruebas
- Markdown
categories:
- Programación
image: https://images.unsplash.com/photo-1515879218367-8466d910aaa4?ixlib=rb-1.2.1&q=80&fm=jpg&crop=entropy&cs=tinysrgb&w=2000&fit=max&ixid=eyJhcHBfaWQiOjExNzczfQ
---



## Resaltador de sintaxis de codigo



### Markdown

``` markdown
**bold** 
*italics* 
[link](www.example.com)
```

### R

```r
## Load all the libraries needed and the data
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
####Eggs PER PLANT ####
##Create a subset of the desire variable
Sub.Eggs <- subset(mydata,
                   select=c(Nger, 
                            Isolate, 
                            EggsP) ) 
####Isolate: MIAd####
Sub.Eggs.MIAd <- subset(Sub.Eggs, Isolate == "MIAd", select=c(Nger, EggsP)) 
Sub.Eggs.MIAd$Nger = factor (Sub.Eggs.MIAd$Nger, labels=c("EC", "TB", "TE", "TS", "TT")) 
###Descriptive statistics calculation###
Sub.Eggs.MIAd.EC <- subset(Sub.Eggs.MIAd, Nger == "EC", select=c(Nger,EggsP))
Me.EP.MIAd.EC <- mean(Sub.Eggs.MIAd.EC$EggsP, na.mr=FALSE)
Me.EP.MIAd.EC <- round(Me.EP.MIAd.EC, digits=2)
Se.EP.MIAd.EC <- se(Sub.Eggs.MIAd.EC$EggsP)
Se.EP.MIAd.EC <- round(Se.EP.MIAd.EC, digits=2)
Sub.Eggs.MIAd.SB <- subset(Sub.Eggs.MIAd, Nger == "TB", select=c(Nger,EggsP))
Me.EP.MIAd.TB <- mean(Sub.Eggs.MIAd.SB$EggsP, na.mr=FALSE)
Me.EP.MIAd.TB <- round(Me.EP.MIAd.TB, digits=2)
Se.EP.MIAd.TB <- se(Sub.Eggs.MIAd.SB$EggsP)
Se.EP.MIAd.TB <- round(Se.EP.MIAd.TB, digits=2)
Sub.Eggs.MIAd.SB <- subset(Sub.Eggs.MIAd, Nger == "TE", select=c(Nger,EggsP))
Me.EP.MIAd.TE <- mean(Sub.Eggs.MIAd.SB$EggsP, na.mr=FALSE)
Me.EP.MIAd.TE <- round(Me.EP.MIAd.TE, digits=2)
Se.EP.MIAd.TE <- se(Sub.Eggs.MIAd.SB$EggsP)
Se.EP.MIAd.TE <- round(Se.EP.MIAd.TE, digits=2)
Sub.Eggs.MIAd.SB <- subset(Sub.Eggs.MIAd, Nger == "TS", select=c(Nger,EggsP))
Me.EP.MIAd.TS <- mean(Sub.Eggs.MIAd.SB$EggsP, na.mr=FALSE)
Me.EP.MIAd.TS <- round(Me.EP.MIAd.TS, digits=2)
Se.EP.MIAd.TS <- se(Sub.Eggs.MIAd.SB$EggsP)
Se.EP.MIAd.TS <- round(Se.EP.MIAd.TS, digits=2)
Sub.Eggs.MIAd.SB <- subset(Sub.Eggs.MIAd, Nger == "TT", select=c(Nger,EggsP))
Me.EP.MIAd.TT <- mean(Sub.Eggs.MIAd.SB$EggsP, na.mr=FALSE)
Me.EP.MIAd.TT <- round(Me.EP.MIAd.TT, digits=2)
Se.EP.MIAd.TT <- se(Sub.Eggs.MIAd.SB$EggsP)
Se.EP.MIAd.TT <- round(Se.EP.MIAd.TT, digits=2)
####Kruskall-Wallis test calculation####
KTMIAd = kruskal.test(Sub.Eggs.MIAd$EggsP ~ Sub.Eggs.MIAd$Nger)
####Dunn test calculation####
DTMIAd = dunnTest(Sub.Eggs.MIAd$EggsP ~ Sub.Eggs.MIAd$Nger, method="bonferroni")
DTMIAd.Comparison <- DTMIAd$res$Comparison
DTMIAd.Padj <- round (DTMIAd$res$P.adj, digits=5)
KrusData = data.frame(DTMIAd.Comparison, DTMIAd.Padj)
RND = nrow(DTMIAd$res)
krustable=kable(KrusData[1:RND,])
if (KTMIAd$p.value>0.05) {
dif="There is no significative differences (P<0.05) between treatments (P<0.05)"
krustable="0"
} else {
dif="There is significative differences between treatments (P<0.05)."
krustable=kable(KrusData[1:RND,])
boxplot(Sub.Eggs.MIAd$EggsP ~ Sub.Eggs.MIAd$Nger, main = "MIAd", xlab = "Germplasm", ylab = "Eggs per plant")
DTMIAd$dtres

}
```





### Latex

```latex
\documentclass[11pt,twoside,a4paper,openright]{report}


%%%%% packages %%%%%

\usepackage{adjustbox}
\usepackage{amsmath}
\usepackage{array}

\usepackage[backend=biber, style=chicago-authordate, natbib=true, maxcitenames=2, maxbibnames=6, minbibnames=6,sorting=nyt, firstinits=true]{biblatex}
\usepackage{caption}
\usepackage[english]{babel}
\usepackage{fancyhdr}
\usepackage{float}
\usepackage{gensymb}
\usepackage[a4paper,width=150mm,top=25mm,bottom=25mm,bindingoffset=6mm]{geometry}
\usepackage{graphicx}
\usepackage[utf8]{inputenc}
\usepackage{makecell}
\usepackage{multicol}
\usepackage{pgfplots, pgfplotstable}
\usepackage{rotating}
\usepackage{subcaption}
\usepackage{tikz}
\usepackage{wrapfig}
\usepackage{wallpaper}

%\usepackage[scaled=0.92]{helvet}

%%%%% Config %%%%%

\graphicspath{ {images/} }

\pagestyle{fancy}
%\fancyhead[LE,RO]{\scriptsize \slshape PhD dissertation}
%\fancyhead[LO,RE]{\tiny \slshape \leftmark}
\fancyhead[LE,RO]{}
\fancyhead[LO,RE]{}
\fancyhead[C]{\small \slshape Chapter \thechapter: \leftmark}
\fancyfoot[C]{\thepage}
\fancyfoot[RO,LE]{\footnotesize \slshape Garc\'ia-Mend\'ivil et al., 2019}
\fancyfoot[LO,RE]{\footnotesize \slshape \rightmark}
\renewcommand{\chaptermark}[1]{ \markboth{#1}{} }
\renewcommand{\sectionmark}[1]{ \markright{#1}{} }

\renewcommand{\headrulewidth}{0.7pt}
\renewcommand{\footrulewidth}{0.7pt}

\fancypagestyle{plain2}{
	\fancyhf{} % clear all header and footer fields
	\fancyfoot[C]{\thepage} % except the center
	\renewcommand{\headrulewidth}{0.7pt}\renewcommand{\footrulewidth}{0.7pt}}



\usetikzlibrary{calc}
\usetikzlibrary{arrows}
\usetikzlibrary{shapes,snakes}

\pgfplotsset{compat=1.10}

\addbibresource{MyCollection.bib}

\DeclareFieldFormat
[article,inbook,incollection,inproceedings,patent,thesis,unpublished,online,misc]
{title}{#1\isdot}



\title{Durability of resistance to \textit{Meloidogyne} mediated by R-genes in Solanaceae and Cucurbitaceae crops}
\author{Helio A. Garc\'ia Mend\'ivil}
\date{Day Month Year}


%%%%% Data tables %%%%%

\pgfplotstableread{
	x y label
	1	4.739572344 a
	1.618048097	4.415021645 a
	2.190331698	4.201026904 a
	2.229169703	3.469661305 a
	2.340444115	3.611902669 a
	2.36361198	3.533531071 a
	2.386498966	3.336134957 a
	2.519171464	3.385089538 a
	2.574609941	3.117778657 a
	2.737590166	2.889857625 a
}\datatable

\pgfplotstableread{
	x y label
	1	4.739572344	a
	1.618048097	4.415021645	a
	2.209750701	3.835344105	a
	2.363518354	3.493856232	a
	2.519171464	3.385089538	a
	2.574609941	3.117778657	a
	2.737590166	2.889857625	a
}\dataEC

\pgfplotstableread{
	x y label
	1	1.991226076	a
	1.618048097	1.997375856	a
	2.209750701	1.455829278	a
	2.363518354	1.426557085	a
	2.519171464	1.472054612	a
	2.574609941	0.310751279	a
	2.737590166	0.392743602	a
}\dataTB

\pgfplotstableread{
	x y label
	1	2.704836606	a
	1.618048097	2.279798835	a
	2.209750701	1.513852201	a
	2.363518354	1.775448939	a
	2.519171464	1.512317792	a
	2.574609941	0.408113446	a
	2.737590166	1.081953769	a
}\dataTE

\pgfplotstableread{
	x y label
	1	2.324693914	a
	1.618048097	2.046593879	a
	2.190331698	1.662635993	a
	2.284806909	1.527292047	a
	2.375055473	1.536458041	a
	2.519171464	1.486866491	a
	2.574609941	0.945480387	a
	2.737590166	1.019805863	a
}\dataTS

\pgfplotstableread{
	x y label
	1	2.239049093	a
	1.618048097	1.859073158	a
	2.209750701	1.690613336	a
	2.363518354	1.435091922	a
	2.519171464	0.346524596	a
	2.574609941	0.428850591	a
	2.737590166	0.945096312	a
}\dataTT

\pgfplotstableread{
	x y label
	1.62065648	3.043458759	a
	1.707570176	2.173243416	a
	1.838849091	1.633907359	a
	2.012981416	2.29939005	a
	2.16879202	1.98058107	a
	2.205475037	1.721895326	a
	2.386948459	1.770517672	a
	2.574031268	0.781611782	a
	2.717254313	1.424884767	a
	2.92505412	0.413003755	a
}\dataECa

\pgfplotstableread{
	x y label
	1.62065648	1.827740624	a
	1.707570176	0.790740378	a
	1.838849091	.	a
	2.012981416	0.726846827	a
	2.16879202	1.140838147	a
	2.205475037	0.367396565	a
	2.386948459	0.983959489	a
	2.574031268	0.526339277	a
	2.717254313	0.63163441	a
	2.92505412	0.454795058	a
}\dataTBa

\pgfplotstableread{
	x y label
	1.62065648	1.856464775	a
	1.707570176	0.770996319	a
	1.838849091	0.893544669	a
	2.012981416	0.910972831	a
	2.16879202	0.709729775	a
	2.205475037	0.744402667	a
	2.386948459	0.526763706	a
	2.574031268	0.319175485	a
	2.717254313	0.626154281	a
	2.92505412	.	a
}\dataTEa

\pgfplotstableread{
	x y label
	1.62065648	1.400532819	a
	1.707570176	0.927913571	a
	1.838849091	1.171874775	a
	2.012981416	0.698248879	a
	2.16879202	0.927422565	a
	2.205475037	0.550399819	a
	2.386948459	0.197167596	a
	2.574031268	.	a
	2.717254313	0.592375855	a
	2.92505412	0.353699481	a
}\dataTSa

\pgfplotstableread{
	x y label
	1.62065648	2.271438123	a
	1.707570176	1.566587673	a
	1.838849091	1.129633858	a
	2.012981416	1.464300922	a
	2.16879202	1.274470967	a
	2.205475037	1.529484725	a
	2.386948459	0.636176779	a
	2.574031268	-0.045114567	a
	2.717254313	0.593226579	a
	2.92505412	.	a
}\dataTTa


\AtBeginBibliography{\footnotesize}

%%%% Document %%%%%

\begin{document}


.
.
.

.
.
.
\end{document}

```
