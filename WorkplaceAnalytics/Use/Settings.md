---

title: Settings in Workplace Analytics
description: Describes what settings are available in Workplace Analytics to confirm data sources, upload HR data, set system defaults and privacy rules, and other data analysis settings
author: madehmer
ms.author: v-mideh
ms.topic: article
localization_priority: normal 
search.appverid:
- MET150
ms.prod: wpa
ms.collection: M365-analytics
manager: scott.ruble
audience: Admin
---

# Settings

Depending on the role you're assigned in Workplace Analytics, you can use the following to configure settings in Workplace Analytics for your organization:

* [Sources](#sources) – Admins and Analysts use these to verify that Office 365 and organizational data is correctly uploaded into Workplace Analytics.
* [Upload](#upload) – Admins use this to prepare and upload organizational and customer data.
* [Admin settings](#admin-settings) – Admins use these to configure [system defaults](system-defaults.md), [privacy settings](privacy-settings.md), and [manager settings](manager-settings.md).
* [Analysis settings](#analysis-settings) – Analysts use these to customize meeting exclusion rules that help ensure data accuracy.

>[!Note]
> Access to one or more pages in Settings depends on what role you're assigned in Workplace Analytics. The following describes page access based on role assignment.

| Settings | Admin | Analyst | Analyst (Limited Access) |  
|---|---|---|---|
| Sources | Full access| Full access | Full access |
| Upload  | Full access | No access | No access |
| Admin settings | Full access | No access| No access |
| Analysis settings | No access | Full access | Read only |

For more details about roles, see [Assign Workplace Analytics roles](../Setup/Assign-roles-to-wpa-admins.md).

## Sources

**Owners** – Workplace Analytics Admins, Analysts, and limited Analysts have full access to this page

Data sources shows what Office 365 collaboration data and organizational data was most recently uploaded into Workplace Analytics. You can view average weekly meeting and email activity and measured-employee characteristics to ensure sufficient data coverage. You can also see high-level CRM data if it is uploaded and processed in Workplace Analytics. For details, see [Sources](data-sourcesv2.md).

## Upload

**Owner** – Only Workplace Analytics Admins have full access to this page

In **Settings** > **Upload** > **Organizational data**, you can upload an organizational data file to Workplace Analytics. This file must be in .csv format, UTF-8 encoded.

Organizational data is contextual information about employees (such as, job title, level, location) from an HR or other information systems. For details on preparing an organizational data file for upload, see [Prepare organizational data](../setup/prepare-organizational-data.md).

![Upload Organizational data](../images/wpa/use/upload-org-data.png)

## Admin settings

**Owner** – Workplace Analytics Admins have full access to this page

In **Admin settings**, you can configure [system defaults](system-defaults.md), [privacy settings](privacy-settings.md), and [manager settings](manager-settings.md). For details, see [Admin settings](admin-settings.md).

![Admin settings](../images/wpa/use/system-defaults.png)

## Analysis settings

**Owners** – Workplace Analytics Analysts have full access to this page and limited Analysts have read-only access

In **Analysis settings**, you can create and customize meeting exclusion rules to remove meetings that you to exclude from analysis, such as appointments that are unrelated to work.

For details on how to create new exclusion rules, see [Meeting exclusion rules: walkthroughs](../tutorials/meeting-exclusion-rules.md) and [Meeting exclusion rules: Tools and concepts](../tutorials/meeting-exclusion-concept.md).

![Analysis settings](../images/wpa/use/analysis-settings.png)

## Related topics

* [Set up Workplace Analytics](../setup/set-up-workplace-analytics.md)
* [Workplace Analytics plans](../tutorials/solutionsv2-intro.md)
