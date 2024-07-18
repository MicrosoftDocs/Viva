---
title: "Organizational Data in Microsoft 365 and Copilot"
ms.reviewer: elizapo
ms.author: elizapo
author: lizap
manager: elizapo
ms.date: 7/18/2024
audience: Admin
f1.keywords:
- NOCSH
ms.topic: article
ms.service: viva-suite
ms.localizationpriority: medium
ms.custom:
ms.collection:  
- M365initiative-viva
- m365solution-overview
- highpri
- tier1
search.appverid:
- MET150
description: "Use Organizational Data in Microsoft Copilot and Microsoft 365"
---
# Use Organizational Data in Microsoft Copilot and Microsoft 365

If you've configured [Organizational Data in Microsoft 365](organizational-data.md), you can view and use your organizational data in Copilot (as long as you've got the correct license). Use the following information to configure and manage organizational data in Copilot.

## Licensing
To access your organizational data in Copilot, you need one of the following license:
- Microsoft 365 Copilot
- Viva Insights or Viva Suite

Your configuration experience with Organizational Data in Microsoft 365 and Microsoft Copilot depends on whether you're configuring organizational data for the first time or if you've previously set it up and are now adding Copilot into your infrastructure.

## New customers with a Copilot license (who've never imported organizational data)

The first time you (as a tenant admin) open Organizational Data in Microsoft 365, you'll see a message about checking your licensing. Once your license is verified, the feature is provisioned - this can take up to one hour, at which point you can upload custom organization data.

After the experience has been provisioned and loaded, you see the following screen: 

[lp - insert graphic]

By default, because this is your first time using Organizationl Data in Microsoft 365 (meaning you haven't already imported your org's data), you'll see data from Microsoft Entra ID. (But be aware that this can take up to 7 days post-provisioning.)

[lp - insert graphic]
 
Until you import org data, the Copilot Dashboard uses the data from Entra ID. A yellow banner on the org data page indicates the source for the Copilot Dashboard data.

To make sure you have the highest quality and freshest data to power your Copilot Dashboard reports, upload your organization's data. To do this:


When it’s an admins first time entering and using Copilot Dashboard, the data source will default to Entra. It is recommended that an Admin performs a new data upload to provide higher quality and fresher data to power Copilot Dashboard reports. To perform an upload navigate to the Data imports tab, where if you have not performed an upload before you will see the following screen: 

A screenshot of a computer

Description automatically generated 

Here admins can upload Organizational data to support M365, Copilot Dashboard, and Viva experiences. For non-copilot tenants Microsoft_ManagerEmail and Microsoft_Organization are not needed as a part of the upload to start using data in M#65 and Viva apps. However for Copilot an upload must have Microsoft_ManagerEmail and Microsoft_Organization attributes for the copilot report to show.  

For an admins first upload, the Microsoft_ManagerEmail and Microsoft_Organization attributes must be populated for all users for data to be used as a part of Copilot dashboard reports 

On subsequent uploads if you choose to upload either Microsoft_ManagerEmail or Microsoft_Organization, those fields must have data for 95% of users or greater. If not the upload will fail. If you choose to omit those two attributes the upload will succeed and be reflected in the Copilot Dashboard. For details see: File rules and validation errors | Microsoft Learn 

For the best experience using Copilot dashboard, it’s recommended that you upload ManagerID and Organization for all your employees. 

After an admin uploads data, it can take up to 7 days for the data to process, be validated, and then be loaded in the copilot dashboard. Once the data is validated admins will be able to see their uploaded data in the data over section as follows:  

They will also be able to toggle to “all uploaded attributes” and see the same subset of dataA screenshot of a computer

Description automatically generated 

 

If an Ingestion fails Admins may see a warning as below, in which case you should reattempt upload.A screenshot of a computer

Description automatically generated 

## Existing Organizational Data in Microsoft 365 customers who've added a Copilot license