---
layout: post
title:  "Azure VM sizes"
date:   2016-12-13 16:36
comments: false
description: "Azure VM sizes"
categories: 
    - PowerShell
    - Azure
tags: 
    - VM
---

Pro zjištění dostupných velikostí VM v Azure, lze použít PowerShell cmdlet `Get-AzureRmVMSize`

``` powershell
>_ Get-AzureRmVMSize -Location westeurope | Format-Wide -Property Name -AutoSize


Standard_DS1      Standard_DS2      Standard_DS3      Standard_DS4      Standard_DS11    Standard_DS12
Standard_DS13     Standard_DS14     Standard_A0       Standard_A1       Standard_A2      Standard_A3
Standard_A5       Standard_A4       Standard_A6       Standard_A7       Basic_A0         Basic_A1
Basic_A2          Basic_A3          Basic_A4          Standard_D1_v2    Standard_D2_v2   Standard_D3_v2
Standard_D4_v2    Standard_D5_v2    Standard_D11_v2   Standard_D12_v2   Standard_D13_v2  Standard_D14_v2
Standard_D15_v2   Standard_F1       Standard_F2       Standard_F4       Standard_F8      Standard_F16
Standard_A1_v2    Standard_A2m_v2   Standard_A2_v2    Standard_A4m_v2   Standard_A4_v2   Standard_A8m_v2
Standard_A8_v2    Standard_D1       Standard_D2       Standard_D3       Standard_D4      Standard_D11
Standard_D12      Standard_D13      Standard_D14      Standard_DS1_v2   Standard_DS2_v2  Standard_DS3_v2
Standard_DS4_v2   Standard_DS5_v2   Standard_DS11_v2  Standard_DS12_v2  Standard_DS13_v2 Standard_DS14_v2
Standard_DS15_v2  Standard_F1s      Standard_F2s      Standard_F4s      Standard_F8s     Standard_F16s
Standard_H8       Standard_H16      Standard_H8m      Standard_H16m     Standard_H16r    Standard_H16mr
Standard_G1       Standard_G2       Standard_G3       Standard_G4       Standard_G5      Standard_GS1
Standard_GS2      Standard_GS3      Standard_GS4      Standard_GS5      Standard_A8      Standard_A9
Standard_A10      Standard_A11      Standard_NV6      Standard_NV12     Standard_NV24
```