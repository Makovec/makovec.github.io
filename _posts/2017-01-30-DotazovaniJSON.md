---
layout: post
title:  "Dotazování JSON"
date:   2017-01-30 18:08
comments: false
description: "Dotazování JSON"
categories: 
    - PowerShell
tags: 
    - JSON
    - Azure
---

Dnes jsem se podíval trochu podrobněji na nový [Azure CLI 2.0](https://docs.microsoft.com/en-us/cli/azure/overview), který
je prozatím v Preview.  Syntaxe mi přijde hodně podobé "starému" (aktuálnímu) Azure xplat cli. Co mne však zaujalo je použití parametru
`query`, který používá pro dotazování do JSON odpovědí jazyka [JMESPath](http://jmespath.org/).

V PowerShellu lze pro práci s formátem JSON použít s úspěchem cmdlet `ConvertFrom-Json`, nicméně práce s JMESPath mi přijde o něco
elegantnější - obzvlášť ve spojení s azure cli.

Ukažme si pár příkladů přímo v Azure CLI 2.0:

* `az vm list --query "[*].name"` Vylistuje jména všech VMs
* `az vm list --query "[*].[name,resourceGroup]"` U všech VM vypíše i Resource group
* `az vm list --query "[*].{VM:name, RG:resourceGroup}"` Výpis jako předchozí, navíc pojmenuje výstupní data
* `az vm list --query "[0].{VM:name, OS:storageProfile.imageReference.offer}"` Pomocí tečkové notace můžeme přistupovat ke vnořeným položkám
* `az vm list --query "[?resourceGroup=='DMORAVEC-RG'].name"` V rámci query můžeme rovnou i filtrovat, zde pouze na danou Resource group

Musím říci, že tento objev mě docela nakopnul. Rozhodně podrobím výstupy z `azure` CLI dalšímu zkoumání.


