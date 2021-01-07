---

title: Settings in Workplace Analytics
description: Describes what settings are available in Workplace Analytics to confirm data sources,  upload data, set system defaults and privacy rules, and other data analysis settings
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

# Settings in Workplace Analytics

Depending on the role you're assigned, the following settings are available in Workplace Analytics:

* [Sources](#sources) – Admins and Analysts use Sources to verify that Office 365 and organizational data is correctly uploaded into Workplace Analytics.
* [Upload](#upload) – Admins use Upload to prepare and upload organizational and customer data.
* [Analysis settings](#analysis-settings) – Analysts use these to customize meeting exclusion rules that help ensure data accuracy.
* [Admin settings](#admin-settings) – Admins use these to configure [system defaults](admin-settings.md#system-defaults), [privacy settings](admin-settings.md#privacy-settings), and [manager settings](admin-settings.md#manager-settings).

>[!Note]
> Access to one or more pages in Settings depends on what role you're assigned in Workplace Analytics. The following describes page access based on role assignment.

| Settings page | Admin | Analyst | Analyst limited |  
|---|---|---|---|
| Sources | Full access| Full access | Full access |
| Upload  | Full access | No access | No access |
| Analysis settings | No access | Full access | Read only |
| Admin settings | Full access | No access| No access |

For more details about roles, see [Assign Workplace Analytics roles](https://docs.microsoft.com/workplace-analytics/setup/assign-roles-to-wpa-admins).

## Sources

* **Owners** – Workplace Analytics Admins, Analysts, and Analyst limiteds have full access to this page

[Data sources](../Use/data-sourcesv2.md) shows what Office 365 data and organizational data was most recently uploaded into Workplace Analytics. You can view average weekly meeting and email activity and measured-employee characteristics to ensure sufficient data coverage.

## Upload

* **Owner** – Workplace Analytics Admins have full access to this page

In **Settings** > **Upload** > **Organizational data**, you can upload an organizational data file to Workplace Analytics. This file must be in .csv format, UTF-8 encoded.

![Upload Organizational data](../images/wpa/use/upload-org-data.png)

### Organizational data

Organizational data is contextual information about employees (for example, job title, level, location) and can come from HR or other information systems. For detailed information on preparing an organizational data file for upload, see [Prepare organizational data](../setup/prepare-organizational-data.md).

## Analysis settings

* **Owners** – Workplace Analytics Analysts have full access to this page and limited Analysts have read-only access

In **Analysis settings**, you can create and customize meeting exclusion rules to remove meetings (such as appointments that are unrelated to work) that you don't want to include in analysis.

![Analysis settings](../images/wpa/use/analysis-settings.png)

For detailed information on how to create new exclusion rules, see [Meeting exclusion rules: walkthroughs](../tutorials/meeting-exclusion-rules.md) and [Meeting exclusion rules: Tools and concepts](../tutorials/meeting-exclusion-concept.md).

## Admin settings

**Owner** – Workplace Analytics Admins have full access to this page

In **Admin settings**, you can configure [system defaults](admin-settings.md#system-defaults), [privacy settings](admin-settings.md#privacy-settings), and [manager settings](admin-settings.md#manager-settings).

![Admin settings](../images/wpa/use/system-defaults.png)

## Related topics

* [Set up Workplace Analytics](../setup/set-up-workplace-analytics.md)
* [Workplace Analytics plans](../tutorials/solutionsv2-intro.md)
