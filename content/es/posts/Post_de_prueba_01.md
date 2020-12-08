---
title: "Post de prueba"
date: 2010-12-05
description: "Post de prueba"
draft: false
hideToc: false
enableToc: true
enableTocContent: false
author: Helio
authorEmoji: 🎅
pinned: true
tags:
- Test
series:
-
categories:
- Test
image: images/feature2/color-palette.png
---

<div id="fb-root"></div>
<script async defer crossorigin="anonymous" src="https://connect.facebook.net/es_ES/sdk.js#xfbml=1&version=v9.0" nonce="hkmYU9qu"></script>


## Code Syntax Highlighting

Verify the following code blocks render as code blocks and highlight properly. 

More about tuning syntax highlighting is the [Hugo documentation](https://gohugo.io/content-management/syntax-highlighting/).


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





### Latex Equation

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





%\maketitle

\input{titlepage}
\pagenumbering{roman}
%\chapter*{Dedication}
%To mum and dad

\include{chapters/Declaration}
%I declare that..



%\chapter*{Acknowledgements}
%I want to thank...
%\newcommand\blankpage{% comando pagina vuota
	%\clearpage
	%\null
	%\thispagestyle{empty}%
	%\addtocounter{page}{-1}%
	%\clearpage
%}
%\blankpage
%\clearpage
%\null
%\thispagestyle{empty}
%\ThisULCornerWallPaper{1.05}{Melo01}
%\clearpage
\tableofcontents
\thispagestyle{plain2}


\newpage
\input{abstract}

%\clearpage
%\null
%\thispagestyle{empty}
%\ThisULCornerWallPaper{1.05}{Melo05}
%\clearpage

\include{chapters/Chapter01}

%\blankpage
%\include{Objectives}

\include{chapters/chapter02}


\include{chapters/chapter03}

\clearpage
\null
\thispagestyle{empty}
\ThisULCornerWallPaper{1.05}{Melo04}
\clearpage

\include{chapters/chapter04}

%\blankpage
%\clearpage
%\null
%\thispagestyle{empty}
%\ThisULCornerWallPaper{1.05}{Melo01}
%\clearpage

\clearpage
\null
\thispagestyle{empty}
\ThisULCornerWallPaper{1.05}{Melo02}
\clearpage

\include{chapters/Chapter05}

\clearpage
\null
\thispagestyle{empty}
\ThisULCornerWallPaper{1.05}{Melo05}
\clearpage

\include{chapters/discusion}

\include{chapters/Conclusions}
%\input{chapters/conclusion}

%\appendix
%\chapter{Appendix Title}
%\input{chapters/appendix}
%\chapter*{Cronogr\'ama de actividades}
%\input{chapters/cronograma}


%\printbibliography
% One or more words can be kept together on the one line with the standard LaTeX command: \mbox{text}
% to separate letter too close: \Large Not shelfful\\
% but shelf{}ful

\begin{multicols}{2}
\thispagestyle{plain2}	
	\printbibliography[title={References}] \addcontentsline{toc}{chapter}{References}
\thispagestyle{plain2}	
\end{multicols}
\thispagestyle{plain2}	
\clearpage
\null
\thispagestyle{empty}
\ThisULCornerWallPaper{1.05}{Melo07}
\clearpage
\thispagestyle{plain2}	
\listoftables \addcontentsline{toc}{chapter}{List of tables}
\thispagestyle{plain2}	
\listoffigures\addcontentsline{toc}{chapter}{List of figures}
\thispagestyle{plain2}	
%\blankpage
%\clearpage
%\null
%\thispagestyle{empty}
%\ThisULCornerWallPaper{1.05}{Melo02}
\thispagestyle{plain2}	
%\chapter{Appendix Title}


\end{document}

```


## Ejemplos de contenido que es posible incrustar:

### Lista de reproducción de SoundCloud:

<iframe width="100%" height="450" scrolling="no" frameborder="no" allow="autoplay" src="https://w.soundcloud.com/player/?url=https%3A//api.soundcloud.com/playlists/700244739&color=%23e1ebec&auto_play=false&hide_related=false&show_comments=true&show_user=true&show_reposts=false&show_teaser=true"></iframe><div style="font-size: 10px; color: #cccccc;line-break: anywhere;word-break: normal;overflow: hidden;white-space: nowrap;text-overflow: ellipsis; font-family: Interstate,Lucida Grande,Lucida Sans Unicode,Lucida Sans,Garuda,Verdana,Tahoma,sans-serif;font-weight: 100;"><a href="https://soundcloud.com/helio4gm" title="Helio" target="_blank" style="color: #cccccc; text-decoration: none;">Helio</a> · <a href="https://soundcloud.com/helio4gm/sets/03-a" title="[03]" target="_blank" style="color: #cccccc; text-decoration: none;">[03]</a></div>


### Documento PDF de Google Drive:

<iframe src="https://drive.google.com/file/d/1FfZiVSoM-lGF8luHayFT4cbWj8JoafAA/preview" width="100%" height="480"></iframe>  
<hr />

### Album de fotografías de Google Photos:

<script src="https://cdn.jsdelivr.net/npm/publicalbum@latest/embed-ui.min.js" async></script>
<div class="pa-gallery-player-widget" style="width:100%; height:480px; display:none;"
  data-link="https://photos.app.goo.gl/82UwYc5t4M4wnvnD6"
  data-title="Castelldefels 01"
  data-description="8 new photos added to shared album">
  <object data="https://lh3.googleusercontent.com/X0XKuvQ0RhArAbnBg70BeyYGYZ92Ns-0rxXWuTlnA2KmBAV-4GG18ndKxAqMxcgFVcJCF0iujOtPCXz_ZBQ9NzY3IzTFL5PnmMTfHDF216L_2GBCGb6bCsgfhhlNkM7Rfzg4Ar6O=w1920-h1080"></object>
  <object data="https://lh3.googleusercontent.com/ctqQVFjpo1W5YXz_CZMTcABEBIx9BxBl_3QdSTaBJDKlLIX5QAIjeH3CfS-dbGjdbqutPEOzTJAOrHi1lbBSTFh_whuHfwFCb58DCxVnDmltJDu0NvvC4XAKGq2BBJaxnaulq6s5=w1920-h1080"></object>
  <object data="https://lh3.googleusercontent.com/eKqxYDzVjnuUoAGbPWOm-xsWYu83FrdmxsKhOrK_0aKQaXJhfik0_axYlAS_h5ehgq-MYYwBemKCPdMBlIdtgbXXLMzWYwfRjX6Zp13UPZxnWLPQjHWf3msJFdeLxsQ1sXQ8RARb=w1920-h1080"></object>
  <object data="https://lh3.googleusercontent.com/He4ZKJWPJ1YQ8N-gN36elZU2EeuQ04zlyuS467eH3OWj_OxMuMx0EQ9pBOuYuYaGe5taoXkbgieHve8EESabQ8tGl4YhI2rrzZD8jIJbxFz1Sv-oRlbCSpd6EVcEiGK-VrcX5VmA=w1920-h1080"></object>
  <object data="https://lh3.googleusercontent.com/CqE0yaOWn77uRpc6bR4q5G-6DxakPAliAk_7ToqoqyYi4G7o76pkmbLCS4-7qeXbTRA7pSyessoHDaIiBserWpStYcswwc2eX7nMANfIXDeZYGQzEqzazEigK9KH8kMX2LWhdgkV=w1920-h1080"></object>
  <object data="https://lh3.googleusercontent.com/FA8e-PstQcyVUNshvwANaowzAzulh45evJ2fzcPghomRFslH_WsW_mgRTOWee_Z8-YiBfWQPO4rSRxfkXWVAdoaqZax0ffRO32dzUIDr6xpT2JPwTi9fcBSNeveOInHBxA6BKigU=w1920-h1080"></object>
  <object data="https://lh3.googleusercontent.com/lUD2TQoBWYWM2mjN9j0zX1vKPK_a0eYYWRGjFCyDK0M2DpyFR13-gUyiTaP89YoCEW_xZ8pTAUjpfXp1pmMNLBaW3grk1TM0X1M5-PRyS3JwoPvBhGja6htzbKejgXpnRe4aV8Ks=w1920-h1080"></object>
  <object data="https://lh3.googleusercontent.com/TMlfZ6GDc6do9t1O66WVQvQQ0qvtyboF5H5OCaHEmVbedT8qrOg5JBvMX5NB5tHAoFidOjBgBQl86wXj4OYO0T3HRA9U13-uvIOpqhdg8dbDdEGxeDLAG3twHQ7L0yNr8n9IN-VQ=w1920-h1080"></object>
</div>

### Fotografía de Google Photos:

<div style="width:100%;height:480px;background-color:black;text-align:center;">
  <a href="https://lh3.googleusercontent.com/KdJx-FSM-F84dh0cGyHM7NA8D_yqKvwbAR31sSZDpJyiRdktKECiobIXoh5-btb0UdBz46xFUfzpCUfsEzaWjL_itIHeBgZrLAPCNUcesGp0Ril4bnAMv0bispbs4UtgyCgKgJEx=w1920-h1080" target="_blank">
    <img style="height:100%;border:0;" src="https://lh3.googleusercontent.com/KdJx-FSM-F84dh0cGyHM7NA8D_yqKvwbAR31sSZDpJyiRdktKECiobIXoh5-btb0UdBz46xFUfzpCUfsEzaWjL_itIHeBgZrLAPCNUcesGp0Ril4bnAMv0bispbs4UtgyCgKgJEx=h480" />
  </a>
</div>

### Video de Facebook:

<iframe src="https://www.facebook.com/plugins/video.php?height=314&href=https%3A%2F%2Fwww.facebook.com%2Fhelio.irie%2Fvideos%2F2469638623085198%2F&show_text=false" width="100%" height="400" style="border:none;overflow:hidden" scrolling="no" frameborder="0" allowfullscreen="true" allow="autoplay; clipboard-write; encrypted-media; picture-in-picture; web-share" allowFullScreen="true"></iframe>

### Video de Facebook con funciones:

<iframe src="https://www.facebook.com/plugins/video.php?height=314&href=https%3A%2F%2Fwww.facebook.com%2Fhelio.irie%2Fvideos%2F2469638623085198%2F&show_text=true" width="100%" height="480" style="border:none;overflow:hidden" scrolling="no" frameborder="0" allowfullscreen="true" allow="autoplay; clipboard-write; encrypted-media; picture-in-picture; web-share" allowFullScreen="true"></iframe>

### Otro video Video de Facebook, porque gracioso:

<iframe src="https://www.facebook.com/plugins/video.php?height=314&href=https%3A%2F%2Fwww.facebook.com%2Fhelio.irie%2Fvideos%2F3144207428961644%2F&show_text=true" width="100%" height="480" style="border:none;overflow:hidden" scrolling="no" frameborder="0" allowfullscreen="true" allow="autoplay; clipboard-write; encrypted-media; picture-in-picture; web-share" allowFullScreen="true"></iframe>

### Video de YouTube

<iframe width="100%" height="430" src="https://www.youtube.com/embed/n-KudQDVpR0" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

### Tweet

<blockquote class="twitter-tweet"><p lang="en" dir="ltr">WTF! White fragility! <a href="https://t.co/QgRY3mv1Ez">https://t.co/QgRY3mv1Ez</a></p>&mdash; Gad Saad (@GadSaad) <a href="https://twitter.com/GadSaad/status/1306566054869700611?ref_src=twsrc%5Etfw">September 17, 2020</a></blockquote> <script async src="https://platform.twitter.com/widgets.js" charset="utf-8"></script> 

### Post de Tumblr

 <div class="tumblr-post" data-href="https://embed.tumblr.com/embed/post/lNvfxVmZY1u_QqdqNGCjbg/636618977925382144" data-did="c3cc989fd1f53548b98d713e9a22492b6cb4c57f"><a href="https://neurosciencestuff.tumblr.com/post/636618977925382144/how-waves-of-clutches-in-the-motor-cortex-help">https://neurosciencestuff.tumblr.com/post/636618977925382144/how-waves-of-clutches-in-the-motor-cortex-help</a></div>  <script async src="https://assets.tumblr.com/post.js"></script>

### Otro post de Tumblr (Meme)

 <div class="tumblr-post" data-href="https://embed.tumblr.com/embed/post/wKJaCnMR-HSRGld6lqnMcA/636611572742209536" data-did="da39a3ee5e6b4b0d3255bfef95601890afd80709"><a href="https://en.futubandera.cl/post/636611572742209536">https://en.futubandera.cl/post/636611572742209536</a></div>  <script async src="https://assets.tumblr.com/post.js"></script>

### Feed de Twitter

<a class="twitter-timeline" data-height="480" data-theme="dark" href="https://twitter.com/Helio0401?ref_src=twsrc%5Etfw">Tweets by Helio0401</a> <script async src="https://platform.twitter.com/widgets.js" charset="utf-8"></script> 
 
 
### Una publicación de Facebook

<div class="fb-post" data-href="https://www.facebook.com/helio.irie/posts/3397644883617896" data-show-text="true" data-width=""><blockquote cite="https://www.facebook.com/helio.irie/posts/3397644883617896" class="fb-xfbml-parse-ignore">Publicada por <a href="#" role="button">Helio Irie</a> en&nbsp;<a href="https://www.facebook.com/helio.irie/posts/3397644883617896">Domingo, 22 de noviembre de 2020</a></blockquote></div>

### Un mapa del Agropolis

<iframe src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d237.1939507650599!2d2.043860585591994!3d41.28830555566967!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x0%3A0x0!2zNDHCsDE3JzE4LjAiTiAywrAwMiczOC44IkU!5e1!3m2!1sen!2smx!4v1607152965858!5m2!1sen!2smx" width="100%" height="450" frameborder="0" style="border:0;" allowfullscreen="" aria-hidden="false" tabindex="0"></iframe>
 
### Feed RSS de noticias

<!-- start sw-rss-feed code --> 
<script type="text/javascript"> 
<!-- 
rssfeed_url = new Array(); 
rssfeed_url[0]="https://www.eluniversal.com.mx/seccion/1671/rss.xml"; rssfeed_url[1]="https://www.debate.com.mx/rss/feed.xml"; rssfeed_url[2]="https://www.excelsior.com.mx/rss.xml"; rssfeed_url[3]="https://www.reforma.com/rss/portada.xml";  
rssfeed_frame_width="100%"; 
rssfeed_frame_height="430"; 
rssfeed_scroll="on"; 
rssfeed_scroll_step="6"; 
rssfeed_scroll_bar="off"; 
rssfeed_target="_blank"; 
rssfeed_font_size="12"; 
rssfeed_font_face=""; 
rssfeed_border="on"; 
rssfeed_css_url=""; 
rssfeed_title="on"; 
rssfeed_title_name="Noticias México"; 
rssfeed_title_bgcolor="#000"; 
rssfeed_title_color="#fff"; 
rssfeed_title_bgimage=""; 
rssfeed_footer="off"; 
rssfeed_footer_name="rss feed"; 
rssfeed_footer_bgcolor="#fff"; 
rssfeed_footer_color="#333"; 
rssfeed_footer_bgimage=""; 
rssfeed_item_title_length="50"; 
rssfeed_item_title_color="#666"; 
rssfeed_item_bgcolor="#fff"; 
rssfeed_item_bgimage=""; 
rssfeed_item_border_bottom="on"; 
rssfeed_item_source_icon="off"; 
rssfeed_item_date="off"; 
rssfeed_item_description="on"; 
rssfeed_item_description_length="120"; 
rssfeed_item_description_color="#666"; 
rssfeed_item_description_link_color="#333"; 
rssfeed_item_description_tag="off"; 
rssfeed_no_items="0"; 
rssfeed_cache = "e19d6743d060133ccd3575c80069961f"; 
//--> 
</script> 
<script type="text/javascript" src="//feed.surfing-waves.com/js/rss-feed.js"></script> 
<!-- The link below helps keep this service FREE, and helps other people find the SW widget. Please be cool and keep it! Thanks. --> 
<div style="color:#000;font-size:10px; text-align:right; width:540px;">powered by <a href="https://surfing-waves.com" rel="noopener" target="_blank" style="color:#000;">Surfing Waves</a></div> 
<!-- end sw-rss-feed code -->


### iframe

### Formulario de google

<iframe src="https://docs.google.com/forms/d/e/1FAIpQLSefaYY_1_0tdWMdHUIqO0CAdnc_BtGUlsZWK5q0LLJ-UvWzJA/viewform?embedded=true" width="100%" height="380" frameborder="0" marginheight="0" marginwidth="0">Cargando…</iframe>



