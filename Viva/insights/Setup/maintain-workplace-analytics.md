---

title: Viva Insights maintenance
description: Admin tasks for maintaining Microsoft Viva Insights data
author: madehmer
ms.author: helayne
ms.topic: article
ms.localizationpriority: medium 
ms.collection: viva-insights-advanced 
ms.service: viva 
ms.subservice: viva-insights 
search.appverid: 
- MET150 
manager: scott.ruble
audience: Admin
---

# Maintenance tasks

After you have installed and set up Microsoft Viva Insights, it will require maintenance by an admin. Some maintenance tasks are infrequently required, while others must be done regularly.  

## Update system defaults

* **Task** - Set the default time zone and the default settings for working days and hours.  
* **Frequency** - As needed to update settings.

[System defaults](../use/system-defaults.md)

## Update privacy settings

* **Task** - Configure the following privacy settings:

  * Set the minimum-group size for data shown in analysis.
  * Show or hide subject lines from analysis.
  * Update settings to exclude emails or meetings for specific email addresses, from specific domains, or key terms in subject lines for emails or meetings.

* **Frequency** - As needed to keep the settings up-to-date.

[Privacy settings](../use/privacy-settings.md)

## Update organizational data

* **Task** - Prepare a .csv file that contains organizational data and upload it to the advanced insights app.
* **Frequency** - Update organizational data as frequently as you like; however, it will be refreshed upon the latest Microsoft 365 collaboration data. Because email, calendar, and Microsoft Teams data is updated weekly, it makes sense to update this data on a similar cadence in Viva Insights.

[Prepare organizational data](prepare-organizational-data.md)

[Upload organizational data (subsequent uploads)](upload-organizational-data2.md)

## Assign licenses  

* **Task** - Assign licenses to individuals.  
* **Frequency** - As needed, such as to add a new employee.

[Assign licenses](assign-licenses-to-population.md)

## Assign roles

* **Task** - Assign roles to individuals or groups.  
* **Frequency** - As needed, such as to assign a new employee a role, or when an existing employee changes roles.

[Assign roles](assign-roles-to-wpa-admins.md)

## Validate and verify data

* **Task** - Use **Data sources** to verify that the Microsoft 365 and other organizational data is loaded and ready for use.
* **Frequency** - As needed, particularly after uploading organizational data.

[Validate and verify data](validate-verify-data.md)

## Set up meeting exclusions

* **Task** - Create custom meeting exclusion rules to remove meetings from analysis.  
* **Frequency** - As needed, create these rules to exclude meetings that might skew your data.

[Meeting exclusion rules.](../tutorials/meeting-exclusions-intro.md)

## Audit activity

* **Task** - As an Exchange admin, you can monitor the Microsoft 365 audit logs and track Viva Insights activity.
* **Frequency** - As needed to ensure compliance with your organization's privacy and security policies.

[Audit logs](../setup/audit-logs.md)

## Related topics

[Settings](../use/settings.md)
