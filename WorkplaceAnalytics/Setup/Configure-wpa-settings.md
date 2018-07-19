---
# Metadata Sample
# required metadata

title: Workplace Analytics Setup -- Configure Workplace Analytics settings
description: Describes how to configure the settings for Workplace Analytics.
author: madehmer
ms.author: v-midehm
ms.date: 07/19/2018
ms.topic: get-started-article
localization_priority: normal 
ms.prod: wpa
---

### Time zone

* **Owner** - Workplace Analytics administrator
* **Task** - Default time zone value the system will use in metric calculations if the data is not available for a measured employee or other internal collaborator
* **Outcome** - Default time zone outcome as defined in Workplace Analytics

The default time zone is used to compute after-hours metrics when a time zone has not been configured by the user or provided as part of the organizational data. This is typically the time zone of the corporate headquarters or the time zone in which most employees reside. If a measured employee or other internal collaborator does not have a time zone defined as part of the organizational data, the metric will be computed using the default time zone.

The default time zone for Workplace Analytics is Pacific Standard Time.

For a complete list of valid times zones, see [Time zones in Workplace Analytics](../Use/Timezones-for-workplace-analytics.md)  

### To change the default time zone

1. On the **Settings** page, select **Settings**.
2. Under **System defaults**, select the time zone you want from the **Default time zone** list.
3. Select **Save**.

> [!Important]
> This setting takes effect the next time organizational data is received and processed for the following month. A change in this setting does not affect any historical data.

### Working days and working hours

Users can set their own working days and working hours in their [Outlook settings](https://outlook.office.com/owa/?path=/options/calendarappearance). While there is no option to upload working days or working hours in organizational data, a Workplace Analysis administrator can set default working days and working hours for the organization in the System defaults section on the Settings page:

![System defaults area of Settings page](../images/wpa/setup/settings-system-defaults-a.png)

These admin-configured default settings are used for a particular user only if the user has not already configured their working days and hours.

### Privacy settings

* **Owner** - Workplace Analytics sponsor or Workplace Analytics administrator
* **Task** - Use company-specific legal and privacy guidelines to define settings to use in Workplace Analytics
* **Outcome** - After you define and confirm the privacy settings, you are ready to provision the service using these rules

Being aware of employees’ rights is a key component to ensuring a successful program using Workplace Analytics.  It is important to consider ever-changing laws and regulations regarding employer-employee relationships, privacy, and personal data, as well as company policies, before using Workplace Analytics.

Workplace Analytics does not encode any specific policy, instead it provides controls that administrators can use to configure the product to be consistent with applicable laws, regulations, and company policies. Your organization selects what data to use in Workplace Analytics.

> [!Important]
> Please consult with your legal and human resources teams before enabling Workplace Analytics for your organization.

Once you have examined your privacy needs, you will use the Settings area in Workplace Analytics to define the privacy settings for your data.

### Detail display

* **Minimum Aggregation Size** - Set the minimum group size required to display data in Explore Metrics. By default, the minimum group size is set to five.
* Decide to show or hide subject lines in meeting reports

### User data exclusions

* Exclude emails/meetings to, or from, specific users, or all users from a domain using “;” as the delimiter
* Exclude emails/meetings with specific terms in the subject line using “;” as the delimiter.   Terms can be any combination of letters, numbers and special characters, e.g. client attorney privilege; D&I

> [!Note]
> If you exclude email addresses, do not assign licenses to them.  You should also include all email aliases for  individuals.

### To set your privacy settings

1. On the **Settings** page, select **Settings**.
2. Under **Privacy settings**, configure the settings to meet your company's needs.

   > [!Note]
   > You can select **Save** at any time to save the privacy settings you are working on, but the settings are not final and ready for use until you select the **I confirm that all privacy settings are complete** check box. After you select the check box, the processing of Office 365 data begins.

3. Select **Save**.

   > [!Important]
   > Carefully validate that your privacy settings are correct, before you check the "I confirm that all privacy settings are complete" box, you can change the settings at any time, but the settings changes will not take effect until the data is processed again for the following month.

4. To begin the processing of Office 365 data, select the **I confirm that all privacy settings are complete** check box, and then select **Save**.

### Related topic
[Settings in Workplace Analytics](../Use/Settings.md)
