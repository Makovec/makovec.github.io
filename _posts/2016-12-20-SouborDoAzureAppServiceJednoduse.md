---
layout: post
title:  "Soubor do Azure App Service jednoduše"
date:   2016-12-20 16:42
comments: false
description: "Soubor do Azure App Service jednoduše"
categories: 
    - Azure
    - App Service
tags: 
    - web
    - AppService    
---

Potřeboval jsem nahrát jednoduchý `index.html` soubor do čistého webu v App Service. Po chvíli trápení mne napadlo využít *Kudu*.

## Postup

1. Vytvořit stránku v Portálu
2. Jít na adresu Kudu, tj. `http://{JmenoSite}.scm.azurewebsites.net/DebugConsole`
3. Navigovat do site/wwwroot
4. Pomocí Drag&Drop tam soubor nahrát

A to je vše - jednoduché a rychlé :)
