---
layout: post
title:  "Nastavení Jekyll na lokálním PC"
date:   2016-12-21 13:48
comments: false
description: "Nastavení Jekyll na lokálním PC"
categories: 
    - Web
tags: 
    - Jekyll
---

Tyto stránky běží na enginu [Jekyll](https://jekyllrb.com/), který mám napojen na [GitHub Pages](https://pages.github.com/).
Po nějaké době mi začalo vadit upravování v remote Git a tak jsem se rozhodl nainstalovat Jekyll na svůj notebook.

## Postup instalace Jekyll na lokalnim PC

1. Pomocí [Chocolatey](https://chocolatey.org/) jsem si nainstaloval Ruby: `choco install ruby`
2. Instalace Jekyllu v Ruby: `gem install jekyll`
3. Instalace pluginu pro GitHub Pages: `gem install github-pages`

Tím jsou nainstalovány základní nástroje, nyní jak na web jako takový. 

1. Nový blog na test: `jekyll new blog`, poté přejít do nově vytvořeného adresáře *blog*.
2. Build blogu: `jekyll build`
3. Pro zobrazení webu lokálně: `jekyll serve`, blog je poté dostupný na `http://127.0.0.1:4000/`. Konzole zůstane locknutá pro web.
4. Po **CTRL+C** lze web zničit pomocí: `jekyll clean` a smazání adresáře blog

Při testování jsem našel hezkou sbírku šablon, kterou jsem postupně testoval. Dostupné jsou na adrese [Jekyll Tips](http://jekyll.tips/templates/).

**Pozn.:** Samozřejmě, že pro ostrý web už nedělám krok 4 z předchozího seznamu :)

