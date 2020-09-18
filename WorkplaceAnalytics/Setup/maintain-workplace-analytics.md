---

title: Workplace Analytics Maintenance
description: Admin tasks for keeping Workplace Analytics and the data it uses up-to-date
author: madehmer
ms.author: v-mideh
ms.topic: article
localization_priority: normal 
ms.prod: wpa
ms.collection: M365-analytics
manager: scott.ruble
audience: Admin
---

# Maintain Workplace Analytics

After you have installed Workplace Analytics and your organization is using it, it will require maintenance by an admin. Some maintenance tasks are needed infrequently, while others must be performed regularly.  

## Update system defaults

 * **Task** - Set the default time zone and the default settings for working days and hours.  
 * **Frequency** - As needed to update these settings.

[System defaults in Admin settings](../use/settings.md#system-defaults)

## Update privacy settings

 * **Task** - Configure the following privacy settings:

   * Set the minimum group size for data shown in charts and dashboards.
   * Decide to show or hash subject lines from analysis.
   * Update settings to exclude emails or meetings for specific email addresses, from specific domains, or key terms in subject lines for emails or meetings.

 * **Frequency** - As needed. Perform this task after your organization has decided that the current settings are insufficient or inaccurate.

[Privacy settings](../use/settings.md#privacy-settings)

## Update organizational data

 * **Task** - Prepare a .csv file that contains organizational data and upload it to Workplace Analytics.  
 * **Frequency** - Regularly. You can update organizational data as frequently as you like, but it will be refreshed upon the latest Office 365 collaboration data. Since email, calendar, and Teams data is updated once a week, it makes sense to provide updates for this data on a similar cadence.

[Prepare organizational data](prepare-organizational-data.md)

[Upload organizational data (subsequent uploads)](upload-organizational-data.md)

## Assign licenses  

 * **Task** - Assign Workplace Analytics licenses to individuals.  
 * **Frequency** - As needed. Perform this task primarily as one step to add a new employee.

[Assign licenses](assign-licenses-to-population.md)

## Assign roles

 * **Task** - Assign Workplace Analytics roles to individuals.  
 * **Frequency** - As needed. Perform this step when a new employee requires one of the Workplace Analytics roles, or an existing employee changes roles.

[Assign roles](assign-roles-to-wpa-admins.md)

## Validate and verify data

 * **Task** - Use **Data sources** to verify that the Office 365 and other organizational data is loaded and ready for use.
 * **Frequency** - As needed, particularly after uploading organizational data.

[Validate and verify data](validate-verify-data.md)

## Set up meeting exclusions

 * **Task** - Create custom meeting exclusion rules to remove meetings from analysis.  
 * **Frequency** - As needed, create these rules to exclude meetings that might skew your data.

[Meeting exclusion rules in Workplace Analytics](../tutorials/meeting-exclusions-intro.md)

## Audit Workplace Analytics activity

 * **Task** - As an Exchange admin, you can monitor the Office 365 audit logs and track Workplace Analytics activity for all user actions.
 * **Frequency** - As needed to ensure compliance with your organization's privacy and security policies.

[Workplace Analytics audit logs](../setup/audit-logs.md)

## Related topics

[Workplace Analytics settings](../use/settings.md)