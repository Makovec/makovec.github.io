---
layout: post
title:  "az cli - custom image"
date:   2017-04-13 16:48
comments: false
description: "az cli - custom image"
categories: 
    - az
tags: 
    - CLI
    - Azure
---

Při práci s Azure v novém portále zmizela možnost vytvořit VM z již existujícího image. Zkusme to pomocí `az cli` 
[Azure CLI 2.0](https://docs.microsoft.com/en-us/cli/azure/overview).


Nejprve nahrajeme VHD do Azure.

``
az storage blob upload --account-name mysa 
    --account-key key --container-name vhds --type page 
    --file c:\vhds\mydisk.vhd --name myOSDisk.vhd
``

a poté již vytvoříme VM.

``
az vm create --resource-group dmoravec=RG --location westeu 
    --name makovec-VM --storage-account mysa --os-type windows
    --admin-username makovec  --admin-password myPwd123321
    --image https://mysa.blob.core.windows.net/vhds/myOSDisks.vhd 
    --use-unmanaged-disk
``

