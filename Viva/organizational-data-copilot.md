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

To make sure you have the highest quality and freshest data to power your Copilot Dashboard reports, upload your organization's data. Go to the **Data Import** tab to import your org data.

[LP - data import screenshot]

You must include the Microsoft_ManagerEmail and Microsoft_Organization attributes for all users for data to be used as a part of Copilot dashboard reports (These attributes are optional for tenants without Copilot.)

On subsequent uploads if you choose to upload *either* Microsoft_ManagerEmail or Microsoft_Organization, at least 95% of your users must include data for those attributes. If not, the upload fails. If you choose to *omit* those two attributes, the upload succeeds and you'll see the new data in the Copilot Dashboard. For details see: File rules and validation errors | Microsoft Learn 

For the best experience using the Copilot dashboard, it’s recommended that you upload ManagerID and Organization for all your employees. 

It can take up to 7 days to process, validate, and load your data into the Copilot dashboard. Once the data is validated, you can see the uploaded data in the data over section as follows:  

[LP - insert screenshot]

Toggle to **all uploaded attributes** to see the same subset of data,

[LP - insert screenshot]
 
If importing your data fails, you'll see a warning message in the portal. Try the upload again.

## Existing Organizational Data in Microsoft 365 customers who've added a Copilot license
If you’ve previously uploaded organization data and now have access to the Copilot Dashboard, your previous uploads will not be immediately used to power Copilot Dashboard. On your first seeing Copilot Dashboard, it will default to using Entra data and can take up to 7 days to reflect. If you want data uploaded via Organizational Data in M365 to surface in Copilot Dashboard, perform another upload. That upload will then be surfaced in your Copilot Dashboard  

 

 

## Customers with both VI/VS and Co-Pilot licenses  

If you choose to upload data from MODIS, it will be sent to Viva Insights for usage in the Copilot dashboard. The rules and validation errors for this upload are documented at File rules and validation errors | Microsoft Learn. For customers with Viva Insights licenses and Co-pilot licenses please see the following for more details: Import and use Organizational Data in Microsoft 365-5.9.24.docx 

Data Quality 

There are 6 headers for data quality 

Data Quality headers 

Meaning  

Imported attributes 

Names of your imported attributes as they appear in Microsoft 365 

Copilot dashboard attributes 

These attributes will appear in your copilot dashboard 

Quality score  

% of rows in an upload that contain data and aren’t blank.  

Employee with this field 

# of employees who have had data uploaded for the field  

Unique values 

This shows the number of different options within each attribute field 

Last updated  

Date of last upload of attribute 

 

 

Things to add/unsure where to add or if to add 

To learn more about switching back to entra data see page 11: Import and use Organizational Data in Microsoft 365-5.9.24.docx 

 