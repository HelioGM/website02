---
title: "Twitch Video"
date: 2021-01-07T22:44:33-08:00
description: Otra entrada de prueba
author: Helio
authorEmoji: 📡
draft: true
hideToc: false
enableToc: false
enableTocContent: false
tocPosition: inner
tocLevels: ["h2", "h3", "h4"]
tags:
- Test
series:
-
categories:
- Herramientas
image: /images/nuevas/Logo.png
---


### Transmisión de twitch


<script src= "https://player.twitch.tv/js/embed/v1.js"></script>
<div id="SamplePlayerDivID"></div>
<script type="text/javascript">
  var options = {
    width: 854,
    height: 480,
    video: "857864723",
    // only needed if your site is also embedded on embed.example.com and othersite.example.com
    parent: ["embed.example.com", "othersite.example.com"]
  };
  var player = new Twitch.Player("SamplePlayerDivID", options);
  player.setVolume(0.5);
</script>