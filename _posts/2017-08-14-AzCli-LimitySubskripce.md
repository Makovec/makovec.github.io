---
layout: post
title:  "az cli - limity subskripce"
date:   2017-08-14 14:21
comments: false
description: "az cli - limity subskripce"
categories: 
    - az
tags: 
    - CLI
    - Azure
---

Od doby, kdy se v Azure portále objevila možnost spouštět přímo `az cli`, je to podle mne nejrychlejší možnost,
jak si v příkazové řádce rychle zjistit informace o subskripci.

Jako například limity subskripce:

![Limity subskripce](/images/posts/2017-08-14-az-cli-vm-limits.png)

Seznam lokalit lze zjistit snadno:

`me@Azure:~$ az account list-locations -o table`

|DisplayName | Latitude | Longitude | Name |
|------------|----------|-----------|------|
| East Asia | 22.267 | 114.188 | eastasia |
| Southeast Asia | 1.283 | 103.833 | southeastasia |
| Central US | 41.5908 | -93.6208 | centralus |
| East US | 37.3719 | -79.8164 | eastus |
| East US 2 | 36.6681 | -78.3889 | eastus2 |
| West US | 37.783 | -122.417 | westus |
| North Central US | 41.8819 | -87.6278 | northcentralus |
| South Central US | 29.4167 | -98.5 | southcentralus |
| North Europe | 53.3478 | -6.2597 | northeurope |
| West Europe | 52.3667 | 4.9 | westeurope |
| Japan West | 34.6939 | 135.502 | japanwest |
| Japan East | 35.68 | 139.77 | japaneast |
| Brazil South | -23.55 | -46.633 | brazilsouth |
| Australia East | -33.86 | 151.209 | australiaeast |
| Australia Southeast | -37.8136 | 144.963 | australiasoutheast |
| South India | 12.9822 | 80.1636 | southindia
| Central India | 18.5822 | 73.9197 | centralindia |
| West India | 19.088 | 72.868 | westindia |
| Canada Central | 43.653 | -79.383 | canadacentral |
| Canada East | 46.817 | -71.217 | canadaeast |
| UK South | 50.941 | -0.799 | uksouth |
| UK West | 53.427 | -3.084 | ukwest |
| West Central US | 40.89 | -110.234 | westcentralus |
| West US 2 | 47.233 | -119.852 | westus2 |
| Korea Central | 37.5665 | 126.978 | koreacentral |
| Korea South | 35.1796 | 129.076 | koreasouth |
