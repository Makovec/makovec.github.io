---
layout: post
title:  "Jak využít Invoke-WebRequest: ČLAF"
date:   2017-01-14 13:56
comments: false
description: "Invoke-WebRequest je velmi flexibilní cmdlet pro práci s webem."
categories: 
    - PowerShell
    - Web
tags: 
    - PowerShell
    - Invoke-WebRequest
    - CLAF
---

Mám moc rád `Invoke-WebRequest`. Podle mě je to jeden z nejužitečnějších cmdletů. Rozhodl jsem se ukázat pár příkladů,
kdy tento cmdlet používám.

## Statistiky ČLAF - penalty
Na webu ČAAF ([Česká asociace amerického fotbalu](http://caaf.cz/)) lze v sekci statistiky najít počty a typy jednotlivých
penalt proti jednotlivým týmům. Rozhodl jsem se udělat malou statistiku a k tomu je vhodný právě cmdlet `Invoke-WebRequest`.

**Příklad**

```
(Invoke-WebRequest -Uri $s -UseBasicParsing).Content | 
  Select-string 'PENALTY (...) (.*?)\(' -AllMatches |
  % matches |% Value |
  % { $_ -match 'PENALTY (.*?) (?<foul>.*?) \('|out-null; $matches.foul }
```

V proměnné `$s` je uložen link na webovou stránku. Pomocí parametru `UseBasicParsing` dostáváme obsah bez parsování 
(ukážu někdy příště). Pomocí `.Content` se dostaneme k obsahu webové stránky (stejně jako když v prohlížeči dáme
zobrazení zdroje stránky). Zbytek je již jasný: hledáme určitý text, který potom dále zpracováváme.

Pokud by vás zajímly TOP 3 prohřešky v České lize amerického fotbalu za rok 2016, zde jsou:

```
Name               Count
----               -----
false start          112
offside               72
offensive holding     58
```