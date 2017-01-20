---
layout: post
title:  "Jak využít Invoke-WebRequest: NFL statistika"
date:   2017-01-20 13:38
comments: false
description: "Jak využít Invoke-WebRequest: NFL statistika"
categories: 
    - PowerShell
    - Web
tags: 
    - PowerShell
    - Invoke-WebRequest
    - NFL
---

Jako pokračování minulé ukázky si můžeme pro porovnání ukázat, jaké jsou nejčastější prohřešky proti pravidlům v NFL.
Na získání dat jsem využil trochu jinou metodu, kterou popíšu později. 

Nyní čistě statistika. Pro připomenutí, jak to vypadalo v roce 2016 v ČLAF:

```
Name               Count
----               -----
false start          112
offside               72
offensive holding     58
```

V NFL máme následující data:

[](/images/posts/2017-01-20-NFLstat.png)

