---
title: "Use organizational data in the Microsoft Copilot Dashboard"
ms.reviewer: elizapo
ms.author: elizapo
author: lizap
manager: elizapo
ms.date: 8/14/2024
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
description: "Use organizational data in the Microsoft Copilot Dashboard"
---
# Use organizational data in the Microsoft Copilot Dashboard

If you've configured [Organizational Data in Microsoft 365](organizational-data.md), you can view and use your organizational data in the [Copilot Dashboard](insights/org-team-insights/delegate-access.md) (as long as you've got a Microsoft Copilot license). Use the following information to configure and manage organizational data for the Copilot Dashboard.

> [!NOTE]
> To see data in the Copilot Dashboard, you need either 100 Microsoft Copilot licenses or 10 Viva Insights license.

Your configuration experience with Organizational Data in Microsoft 365 and Microsoft Copilot depends on whether you're configuring organizational data for the first time or if you've previously set it up and are now adding Microsoft Copilot into your infrastructure.

## How data works with the Copilot Dashboard
When you get a Viva Insights or Copilot license, your tenant is considered *new*. To access Copilot reports, you need to meet the prerequisites and upload data  through the Microsoft Admin center or Viva Insights (if you have a Viva Insights license). This initial upload requires that your data has 100% coverage for the **Microsoft_PersonID** column and 95% coverage for the **Microsoft_ManagerEmail** and **Microsoft_Organization** columns. 100% compliance with the **Microsoft_PersonId** attribute helps prevent data import errors. After successful upload, you can access Copilot data quality reports. Until you successfully upload your data and it has been validated, the default data quality report shown uses data from Microsoft Entra ID.  

If you also have a Viva Insights license, it's *strongly recommended* that you complete the upload from Viva Insights. 

>[!NOTE]
> Remember to follow the attribute naming convention of either the Microsoft admin center or Viva Insights, depending on where you're uploading your data.


## New customers with a Microsoft Copilot license (who've never imported organizational data)

The first time you (as a tenant admin) open Organizational Data in Microsoft 365, you see a message about checking your licensing. Once your license is verified, the feature is provisioned - this can take up to one hour, at which point you can upload custom organization data.

:::image type="content" source="media/orgdata-copilot-1.jpg" lightbox="media/orgdata-copilot-1.jpg" alt-text="A screenshot of the Organizational Data landing page the first time you access it.":::

After the experience has been provisioned and loaded, you see the following screen: 

:::image type="content" source="media/orgdata-copilot-2.jpg" lightbox="media/orgdata-copilot-2.jpg" alt-text="A screenshot of the data attributes landing page without any data.":::

By default, because this is your first time using Organizational Data in Microsoft 365 (meaning you haven't already imported your organization's data), you see data from Microsoft Entra ID. (But this can take up to five days post-provisioning.)

Until you import organizational data, the Copilot Dashboard uses the data from Microsoft Entra ID. A yellow banner on the organizational data page indicates the source for the Copilot Dashboard data. See [Prepare and import your organizational data](organizational-data.md#prepare-and-import-your-organizational-data) for the steps to import your data.

:::image type="content" source="media/orgdata-copilot-3.jpg" lightbox="media/orgdata-copilot-3.jpg" alt-text="A screenshot of the data attributes landing page with Microsoft Entra ID data.":::

To make sure you have the highest quality and freshest data to power your Copilot Dashboard reports, upload your organization's data. Go to the **Data imports** tab to import your organizational data.

The first time that you upload organization data, you *must* include the **Microsoft_ManagerEmail** and **Microsoft_Organization** attributes for all users for data to be used as a part of Copilot Dashboard reports (These attributes are optional for tenants without Microsoft Copilot.) 

On subsequent uploads if you choose to upload *either* **Microsoft_ManagerEmail** or **Microsoft_Organization**, at least 95% of your users must have data for those attributes. If not, the upload fails. If you choose to *omit* those two attributes, the upload succeeds, and you see the new data in the Copilot Dashboard. 

For the best experience using the Copilot Dashboard, it’s recommended that you upload ManagerID and Organization for all your employees. 

It can take up to five days to process, validate, and load your data into the Copilot Dashboard. Once the data is validated, you can see the uploaded data in the **Data overview** section as follows:  

:::image type="content" source="media/orgdata-copilot-5.jpg" lightbox="media/orgdata-copilot-5.jpg" alt-text="A screenshot of the data attributes page with the tenant's organizational data.":::


If importing your data fails, you see a warning message in the portal. Try the upload again.

## Existing Organizational Data in Microsoft 365 customers who've added a Microsoft Copilot license
If you’ve previously uploaded organization data and now have access to the Copilot Dashboard, your previous uploads aren't immediately used to power the Copilot Dashboard. The first time you try to view the Copilot Dashboard, it defaults to the Microsoft Entra ID data quality report (and can take up to five days to show any data). If you want to use your organizational data instead of the Microsoft Entra ID data in the dashboard, reimport your organizational data. Existing data isn't computed nor displayed.

Although you can view Entra data quality reports without manager and organization data, you need those two fields to view Copilot reports. To access Copilot data quality report, upload a fresh organizational data .csv file with at least these three attributes:
- **Microsoft_PersonID** (100% coverage)
- **Microsoft_ManagerEmail** (95% coverage)
- **Microsoft_Organization* (95% coverage)

There are other optional attributes used in the Copilot dashboard, such as **Microsoft_JobDiscipline**, that might be helpful to include in your uploads. 


:::image type="content" source="media/orgdata-copilot-6.jpg" lightbox="media/orgdata-copilot-6.jpg" alt-text="A screenshot of the Data imports page with a message to reimport data.":::

## Customers with both Viva Insights or Viva Suite *and* Microsoft Copilot licenses  

If you have both a Viva Insights or Viva Suite license and a Microsoft Copilot license, when you upload organizational data, it's [shared with Viva Insights to use in the Copilot Dashboard](insights/org-team-insights/copilot-dashboard.md). See [File rules and validation errors](insights/advanced/admin/rules-validation-errors.md) for information about the rules and validation errors for this upload.

## Details about your organizational data

You can view the following quality information about your organizational data on the **Data overview** tab. 

|Data quality attribute|Meaning|
|-|-|
|Imported attributes|Names of your imported attributes as they appear in Microsoft 365| 
|Copilot Dashboard attributes|These attributes appear in your Copilot Dashboard| 
|Quality score|% of rows in an upload that contain data and aren’t blank| 
|Employee with this field|# of employees who have had data uploaded for the field|  
|Unique values|This shows the number of different options within each attribute field| 
|Last updated|Date of last upload of attribute| 

