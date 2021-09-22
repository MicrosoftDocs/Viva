---

title: Settings for Workplace Analytics
description: Describes what settings are available in Workplace Analytics for Microsoft Viva Insights to confirm data sources, upload HR data, set system defaults and privacy rules, and other analysis settings
author: madehmer
ms.author: v-mideh
ms.topic: article
ms.localizationpriority: medium 
search.appverid:
- MET150
ms.prod: wpa
ms.collection: M365-analytics
manager: scott.ruble
audience: Admin
---

# Analyst settings

Depending on the role you're assigned in Microsoft Viva Insights in Workplace Analytics, you can use the following to configure settings in Workplace Analytics for your organization:

* [Data sources](#data-sources) – Admins and Analysts use these to verify that Microsoft 365 and organizational data is correctly uploaded into Workplace Analytics.
* [Upload](#upload) – Admins use this to prepare and upload organizational and customer data.
* Admins use these to configure [system defaults](system-defaults.md), [privacy settings](privacy-settings.md), and [manager settings](manager-settings.md). Analysts use these to customize meeting exclusion rules that help ensure data accuracy.

>[!Note]
> Access to one or more pages in Settings depends on what role you're assigned in Workplace Analytics. The following describes page access based on role assignment.

| Settings | Admin | Analyst | Analyst (Limited Access) |  
|---|---|---|---|
| Data sources | Full access| Full access | Limited access |
| Upload  | Full access | No access | No access |
| Analyst settings | Full access | Limited access | Read only |

For more details about roles, see [Assign roles](../Setup/Assign-roles-to-wpa-admins.md).

## Data sources

**Owners** – Viva Insights or Workplace Analytics Admins, Analysts, and limited Analysts have full access to Sources

In **Data sources**, you can see what Microsoft 365 collaboration data and organizational data was most recently uploaded into Workplace Analytics. You can view average weekly meeting and email activity and measured-employee characteristics to ensure sufficient data coverage. You can also see high-level CRM data if it is uploaded and processed in Workplace Analytics. For details, see [Data sources](data-sourcesv2.md).

## Upload

**Owner** – Only Viva Insights and Workplace Analytics Admins have full access to Upload

In **Upload**, admins can upload the following types of data files in .csv format, UTF-8 encoded:

* **Organizational data** - Contextual information about employees (such as, job title, level, location) from an HR or other information systems that admins upload as a data file into Workplace Analytics. For details on preparing this upload file, see [Prepare organizational data](../setup/prepare-organizational-data.md).

* **CRM data** - Customer relationship management data from Microsoft Dynamics or Salesforce, which typically includes customer account information, sales records, purchasing history, service history, customer requests, and product inquiries. For details, see [CRM data in Workplace Analytics](../setup/crm-data-upload.md).

## Admin settings

**Owner** – Workplace Analytics Admins have full access to these settings

In **Admin settings**, you can configure [system defaults](system-defaults.md), [privacy settings](privacy-settings.md), and [manager settings](manager-settings.md). For details, see [Admin settings](admin-settings.md).

## Analyst settings

**Owners** – Workplace Analytics Analysts have full access and limited Analysts have read-only access to these settings

In **Analyst settings**, you can create and customize meeting exclusion rules to remove meetings that you to exclude from analysis, such as appointments that are unrelated to work.

For details on how to create new exclusion rules, see [Meeting exclusion rules: walkthroughs](../tutorials/meeting-exclusion-rules.md) and [Meeting exclusion rules: Tools and concepts](../tutorials/meeting-exclusion-concept.md).

## Related topics

* [Set up Workplace Analytics](../setup/set-up-workplace-analytics.md)
* [Workplace Analytics plans](../tutorials/solutionsv2-intro.md)
