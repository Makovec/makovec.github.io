---
layout: post
title:  "azure cli account - příklady"
date:   2017-01-30 11:05
comments: false
description: "azure cli account - příklady"
categories: 
    - azure
tags: 
    - cli
---

Pokud pod daným účtem můžete přistupovat do více subskripcí, je dobré se podívat na to, jak se mezi nimi přepínat.
V azure CLI se subskripci říká **account**.

Seznam subskripcí: `azure account list`

Detailní přehled: `azure account show [JmenoNeboIdSubskripce]`

Nastavení kontextu na jinou subskripci: `azure account set JmenoNeboIdSubskripce`

Další příkazy jsou dostupné v [dokumentaci](https://docs.microsoft.com/en-us/azure/virtual-machines/azure-cli-arm-commands#azure-account-manage-your-account-information)