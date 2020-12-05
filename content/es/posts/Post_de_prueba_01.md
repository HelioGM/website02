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

### JavaScript

``` javascript
document.write('Hello, world!');
```

### CSS

``` css
body {
    background-color: red;
}
```


### Python

``` python
print "Hello, world!"
```

### XML

``` xml
<employees>
    <employee>
        <firstName>John</firstName> <lastName>Doe</lastName>
    </employee>
</employees>
```


### PHP

``` php
 <?php echo '<p>Hello World</p>'; ?> 
```

### SQL 

``` sql
SELECT column_name,column_name
FROM table_name;
```


### Java

```java
import javax.swing.JFrame;  //Importing class JFrame
import javax.swing.JLabel;  //Importing class JLabel
public class HelloWorld {
    public static void main(String[] args) {
        JFrame frame = new JFrame();           //Creating frame
        frame.setTitle("Hi!");                 //Setting title frame
        frame.add(new JLabel("Hello, world!"));//Adding text to frame
        frame.pack();                          //Setting size to smallest
        frame.setLocationRelativeTo(null);     //Centering frame
        frame.setVisible(true);                //Showing frame
    }
}
```

### Latex Equation

```latex
\frac{d}{dx}\left( \int_{0}^{x} f(u)\,du\right)=f(x).
```

```javascript
import {x, y} as p from 'point';
const ANSWER = 42;

class Car extends Vehicle {
  constructor(speed, cost) {
    super(speed);

    var c = Symbol('cost');
    this[c] = cost;

    this.intro = `This is a car runs at
      ${speed}.`;
  }
}

for (let num of [1, 2, 3]) {
  console.log(num + 0b111110111);
}

function $initHighlight(block, flags) {
  try {
    if (block.className.search(/\bno\-highlight\b/) != -1)
      return processBlock(block.function, true, 0x0F) + ' class=""';
  } catch (e) {
    /* handle exception */
    var e4x =
        <div>Example
            <p>1234</p></div>;
  }
  for (var i = 0 / 2; i < classes.length; i++) {
  // "0 / 2" should not be parsed as regexp
    if (checkCondition(classes[i]) === undefined)
      return /\d+[\s/]/g;
  }
  console.log(Array.every(classes, Boolean));
}

export  $initHighlight;
```

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="utf-8">
  <title>Hello world</title>
  <link href='http://fonts.googleapis.com/css?family=Roboto:400,400italic,700,700italic' rel='stylesheet' type='text/css'>
  <link rel="stylesheet" href="index.css" />
</head>
<body>
  <div id="app"></div>
  <script src="//cdnjs.cloudflare.com/ajax/libs/less.js/2.5.1/less.min.js"></script>
  <script src="vendor/prism.js"></script>
  <script src="examples.bundle.js"></script>
</body>
</html>
```

```css
/*********************************************************
* General
*/
pre[class*="language-"],
code {
  color: #5c6e74;
  font-size: 13px;
  text-shadow: none;
  font-family: Consolas, Monaco, 'Andale Mono', 'Ubuntu Mono', monospace;
  direction: ltr;
  text-align: left;
  white-space: pre;
  word-spacing: normal;
  word-break: normal;
  line-height: 1.5;
  tab-size: 4;
  hyphens: none;
}
pre[class*="language-"]::selection,
code::selection {
  text-shadow: none;
  background: #b3d4fc;
}
@media print {
  pre[class*="language-"],
  code {
    text-shadow: none;
  }
}
pre[class*="language-"] {
  padding: 1em;
  margin: .5em 0;
  overflow: auto;
  background: #f8f5ec;
}
:not(pre) > code {
  padding: .1em .3em;
  border-radius: .3em;
  color: #db4c69;
  background: #f9f2f4;
}
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

<iframe src="https://www.facebook.com/plugins/video.php?height=314&href=https%3A%2F%2Fwww.facebook.com%2Fhelio.irie%2Fvideos%2F2469638623085198%2F&show_text=false&width=560" width="560" height="314" style="border:none;overflow:hidden" scrolling="no" frameborder="0" allowfullscreen="true" allow="autoplay; clipboard-write; encrypted-media; picture-in-picture; web-share" allowFullScreen="true"></iframe>

### Video de Facebook con funciones:

<iframe src="https://www.facebook.com/plugins/video.php?height=314&href=https%3A%2F%2Fwww.facebook.com%2Fhelio.irie%2Fvideos%2F2469638623085198%2F&show_text=true&width=560" width="560" height="429" style="border:none;overflow:hidden" scrolling="no" frameborder="0" allowfullscreen="true" allow="autoplay; clipboard-write; encrypted-media; picture-in-picture; web-share" allowFullScreen="true"></iframe>

### Otro video Video de Facebook, porque gracioso:

<iframe src="https://www.facebook.com/plugins/video.php?height=365&href=https%3A%2F%2Fwww.facebook.com%2Fhelio.irie%2Fvideos%2F3144207428961644%2F&show_text=true&width=560" width="560" height="480" style="border:none;overflow:hidden" scrolling="no" frameborder="0" allowfullscreen="true" allow="autoplay; clipboard-write; encrypted-media; picture-in-picture; web-share" allowFullScreen="true"></iframe>

### Video de YouTube

<iframe width="560" height="315" src="https://www.youtube.com/embed/n-KudQDVpR0" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

### Tweet

<blockquote class="twitter-tweet"><p lang="en" dir="ltr">WTF! White fragility! <a href="https://t.co/QgRY3mv1Ez">https://t.co/QgRY3mv1Ez</a></p>&mdash; Gad Saad (@GadSaad) <a href="https://twitter.com/GadSaad/status/1306566054869700611?ref_src=twsrc%5Etfw">September 17, 2020</a></blockquote> <script async src="https://platform.twitter.com/widgets.js" charset="utf-8"></script> 

### Post de Tumblr

 <div class="tumblr-post" data-href="https://embed.tumblr.com/embed/post/lNvfxVmZY1u_QqdqNGCjbg/636618977925382144" data-did="c3cc989fd1f53548b98d713e9a22492b6cb4c57f"><a href="https://neurosciencestuff.tumblr.com/post/636618977925382144/how-waves-of-clutches-in-the-motor-cortex-help">https://neurosciencestuff.tumblr.com/post/636618977925382144/how-waves-of-clutches-in-the-motor-cortex-help</a></div>  <script async src="https://assets.tumblr.com/post.js"></script>

### Otro post de Tumblr (Meme)

 <div class="tumblr-post" data-href="https://embed.tumblr.com/embed/post/wKJaCnMR-HSRGld6lqnMcA/636611572742209536" data-did="da39a3ee5e6b4b0d3255bfef95601890afd80709"><a href="https://en.futubandera.cl/post/636611572742209536">https://en.futubandera.cl/post/636611572742209536</a></div>  <script async src="https://assets.tumblr.com/post.js"></script>

### Feed de Tweeter

<a class="twitter-timeline" data-height="480" data-theme="dark" href="https://twitter.com/Helio0401?ref_src=twsrc%5Etfw">Tweets by Helio0401</a> <script async src="https://platform.twitter.com/widgets.js" charset="utf-8"></script> 
 
 
### Una publicación de Facebook

<div class="fb-post" data-href="https://www.facebook.com/helio.irie/posts/3397644883617896" data-show-text="true" data-width=""><blockquote cite="https://www.facebook.com/helio.irie/posts/3397644883617896" class="fb-xfbml-parse-ignore">Publicada por <a href="#" role="button">Helio Irie</a> en&nbsp;<a href="https://www.facebook.com/helio.irie/posts/3397644883617896">Domingo, 22 de noviembre de 2020</a></blockquote></div>

### Un mapa del Agropolis

<iframe src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d237.1939507650599!2d2.043860585591994!3d41.28830555566967!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x0%3A0x0!2zNDHCsDE3JzE4LjAiTiAywrAwMiczOC44IkU!5e1!3m2!1sen!2smx!4v1607152965858!5m2!1sen!2smx" width="600" height="450" frameborder="0" style="border:0;" allowfullscreen="" aria-hidden="false" tabindex="0"></iframe>
 
### Feed RSS de noticias

<!-- start sw-rss-feed code --> 
<script type="text/javascript"> 
<!-- 
rssfeed_url = new Array(); 
rssfeed_url[0]="https://www.eluniversal.com.mx/seccion/1671/rss.xml"; rssfeed_url[1]="https://www.debate.com.mx/rss/feed.xml"; rssfeed_url[2]="https://www.excelsior.com.mx/rss.xml"; rssfeed_url[3]="https://www.reforma.com/rss/portada.xml";  
rssfeed_frame_width="540"; 
rssfeed_frame_height="240"; 
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

### Chat de Disqus
 
 <div id="disqus_thread"></div>
<script>
    /**
    *  RECOMMENDED CONFIGURATION VARIABLES: EDIT AND UNCOMMENT THE SECTION BELOW TO INSERT DYNAMIC VALUES FROM YOUR PLATFORM OR CMS.
    *  LEARN WHY DEFINING THESE VARIABLES IS IMPORTANT: https://disqus.com/admin/universalcode/#configuration-variables    */
    /*
    var disqus_config = function () {
    this.page.url = PAGE_URL;  // Replace PAGE_URL with your page's canonical URL variable
    this.page.identifier = PAGE_IDENTIFIER; // Replace PAGE_IDENTIFIER with your page's unique identifier variable
    };
    */
    (function() { // DON'T EDIT BELOW THIS LINE
    var d = document, s = d.createElement('script');
    s.src = 'https://helio5.disqus.com/embed.js';
    s.setAttribute('data-timestamp', +new Date());
    (d.head || d.body).appendChild(s);
    })();
</script>
<noscript>Please enable JavaScript to view the <a href="https://disqus.com/?ref_noscript">comments powered by Disqus.</a></noscript>


