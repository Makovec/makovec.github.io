---
layout: post
title:  "azure cli RG - příklady"
date:   2016-12-09 20:30
comments: false
description: "azure cli RG - příklady"
categories: 
    - PowerShell
tags: 
    - PowerShell
---

Resource Group (RG) je logická jednotka pro oddělení jednotlivých deploymentů. Pro zobrazení obsahu RG lze použít 
následující přáklady.

**Zobrazení RG a jejích zdrojů**

```
azure group list
```

Zobrazení obsahu konkrétní RG

```
azure resource list dmoravec-RG
```

Místo použití ```group``` použijeme ```resource```.

Podrobnější informace o daném zdroji

```
azure resource show dmoravec-RG WindowsVM Microsoft.Compute/virtualMachines -o "2015-06-15"
```

Te je naprosto nepoužitelné bez doplňování syntaxe. Je potřeba zadat typ zdroje a zároveň verzi použitého API.

*Více informací lze najít v [dokumentaci](https://docs.microsoft.com/en-us/azure/azure-resource-manager/xplat-cli-azure-resource-manager).*