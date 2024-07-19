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

The first time you (as a tenant admin) open Organizational Data in Microsoft 365, you see a message about checking your licensing. Once your license is verified, the feature is provisioned - this can take up to one hour, at which point you can upload custom organization data.

:::image type="content" source="media/orgdata-copilot-1.jpg" lightbox="media/media/orgdata-copilot-1.jpg" alt-text="A screenshot of the Organizational Data landing page the first time you access it.":::

After the experience has been provisioned and loaded, you see the following screen: 

:::image type="content" source="media/orgdata-copilot-2.jpg" lightbox="media/orgdata-copilot-2.jpg" alt-text="A screenshot of the data attributes landing page without any data.":::

By default, because this is your first time using Organizational Data in Microsoft 365 (meaning you haven't already imported your org's data), you see data from Microsoft Entra ID. (But this can take up to seven days post-provisioning.)

Until you import org data, the Copilot Dashboard uses the data from Microsoft Entra ID. A yellow banner on the org data page indicates the source for the Copilot Dashboard data.

:::image type="content" source="media/orgdata-copilot-3.jpg" lightbox="media/orgdata-copilot-3.jpg" alt-text="A screenshot of the data attributes landing page with Microsoft Entra ID data.":::

To make sure you have the highest quality and freshest data to power your Copilot Dashboard reports, upload your organization's data. Go to the **Data imports** tab to import your org data.

:::image type="content" source="media/orgdata-copilot-4.png" lightbox="media/orgdata-copilot-4.png" alt-text="A screenshot of the Data imports page.":::

You must include the **Microsoft_ManagerEmail** and **Microsoft_Organization** attributes for all users for data to be used as a part of Copilot dashboard reports (These attributes are optional for tenants without Copilot.)

On subsequent uploads if you choose to upload *either* **Microsoft_ManagerEmail** or **Microsoft_Organization**, at least 95% of your users must include data for those attributes. If not, the upload fails. If you choose to *omit* those two attributes, the upload succeeds and you see the new data in the Copilot Dashboard. 

For the best experience using the Copilot dashboard, it’s recommended that you upload ManagerID and Organization for all your employees. 

It can take up to seven days to process, validate, and load your data into the Copilot dashboard. Once the data is validated, you can see the uploaded data in the data over section as follows:  

:::image type="content" source="media/orgdata-copilot-5.jpg" lightbox="media/orgdata-copilot-5.jpg" alt-text="A screenshot of the data attributes page with the tenant's org data.":::


If importing your data fails, you see a warning message in the portal. Try the upload again.

## Existing Organizational Data in Microsoft 365 customers who've added a Copilot license
If you’ve previously uploaded organization data and now have access to the Copilot Dashboard, your previous uploads aren't immediately used to power the Copilot Dashboard. The first time you see the Copilot Dashboard, it defaults to using Microsoft Entra ID data (and can take up to seven days to show any data). If you want to use your organizational data instead of the Microsoft Entra ID data in the dashboard, reimport your org data. 

:::image type="content" source="media/orgdata-copilot-6.jpg" lightbox="media/orgdata-copilot-6.jpg" alt-text="A screenshot of the Data imports page with a message to reimport data.":::

## Customers with both Viva Insights or Viva Suite *and* Copilot licenses  

If you have both a Viva Insights or Viva Suite license and a Copilot license, when you upload org data, it's shared with Viva Insights to use in the Copilot dashboard. See [File rules and validation errors](insights/advanced/admin/rules-validation-errors.md) for information about the rules and validation errors for this upload.

## Details about your org data

You can view the following quality information about your org data on the **Data overview** tab. 

|Data quality attribute|Meaning|
|-|-|
|Imported attributes|Names of your imported attributes as they appear in Microsoft 365| 
|Copilot dashboard attributes|These attributes appear in your Copilot dashboard| 
|Quality score|% of rows in an upload that contain data and aren’t blank| 
|Employee with this field|# of employees who have had data uploaded for the field|  
|Unique values|This shows the number of different options within each attribute field| 
|Last updated|Date of last upload of attribute| 

