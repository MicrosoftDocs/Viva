---
ms.date: 05/10/2023
title: Export topics created in Viva Engage with PowerShell
ms.author: daisyfeller
author: daisyfell
manager: pamgreen
ms.reviewer: ergradel
audience: admin
ms.topic: article
ms.collection:
  - m365initiative-viva-topics
  - Tier1
ms.service: viva 
ms.subservice: viva-topics 
search.appverid:
    - MET150  
ms.localizationpriority:  medium
description: Learn how to export topics created in Viva Engage (Lite Topics) to a .csv file.
---

# Export topics created in Viva Engage with PowerShell

Using PowerShell, you can export topics created in Viva Engage (also known as Lite Topics) to a .csv file. Topics created before enabling integration with Viva Engage are included.

> [!NOTE]
> This article assumes you have knowledge about how to use PowerShell.

## Requirements

To export the topics, you'll run a PowerShell script. Requirements to run the script are:

- PowerShell 7 or later. To install the latest version of PowerShell, go to [Installing PowerShell on Windows](/powershell/scripting/install/installing-powershell-on-windows?view=powershell-7.3#installing-the-msi-package).
- The user running the script will need to be a Viva Topics admin or Knowledge Manager.

## Run the PowerShell script

1. [Get the script](#export-topics-script).
1. Use the following parameters: <br>
Export-TopicLite -Upn < string > | Export-Csv -Path < string >

Example:

```powershell
Export-TopicLite -Upn "xxxx@xxxx.com" -Path "C:\"
```