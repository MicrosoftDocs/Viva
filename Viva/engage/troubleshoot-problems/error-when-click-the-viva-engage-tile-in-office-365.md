---
title: Sign-in error when selecting the Viva Engage tile in Microsoft 365
description: Describes an issue in which you receive "Sorry, but we're having trouble signing you in" error when you select the Viva Engage tile in Microsoft 365.
author: Starshine89
manager: pamgreen
audience: ITPro
ms.service: sharepoint-online
ms.topic: article
f1.keywords:
- NOCSH
ms.author: pamgreen
ms.date: 06/25/2019
---

# Sign-in error when you select the Viva Engage tile in Microsoft 365

## Problem

You recently activated Viva Engage Enterprise by using the Microsoft 365 admin center. The Viva Engage tile appears in the app launcher, but when you select it, you receive the following error message:

**Sorry, but we're having trouble signing you in. We received a bad request.**

## Solution

To resolve this issue, the Viva Engage Service Principal must be enabled.

Before you follow these steps, make sure that the following prerequisites are met:

- Install the Azure Active Directory module for Windows PowerShell. For more information, go to [Connect PowerShell to Microsoft 365 services](/microsoft-365/enterprise/connect-to-microsoft-365-powershell).

- You must be a Microsoft 365 Global administrator to perform these steps.

Follow these steps:

1. Verify the Viva Engage Service Principal is currently disabled. To do this, open Azure Active Directory module for Windows PowerShell, and then run the following cmdlets:

   > [!NOTE]
   > Press Enter after you type each cmdlet. The response to the last cmdlet should be **False**.

   ```
   Connect-MsolService
   SMSP = Get-MsolServicePrincipal -AppPrincipalId "00000005-0000-0ff1-ce00-000000000000"
   SMSP.AccountEnabled
   ```

2. Change the **Account** setting for this service principal to **True**. To do this, run the following cmdlet:

   ```
   Set-MsolServicePrincipal -AppPrincipalId $MSP.AppPrincipalId -AccountEnabled $true
   ```

3. Sign in to Microsoft 365. Select the Viva Engage tile again to verify that you can sign in.

## More information

Still need help? Go to [Microsoft Community](https://answers.microsoft.com).
