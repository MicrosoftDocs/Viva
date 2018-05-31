---
# Metadata Sample
# required metadata

title: Workplace Analytics Setup -- Configure Workplace Analytics settings
description: Eighth setup step -- Configure Workplace Analytics settings
author: paul9955
ms.author: v-leash
ms.date: 04/19/2018
ms.topic: get-started-article
localization_priority: normal 
ms.prod: wpa
---

### Time zone

* **Owner** - Workplace Analytics administrator
* **Task** - Provide default time zone values the system will use in metric calculations if the data is not available for a measured employee or other internal collaborator
* **Outcome** - Default time zone values are defined in Workplace Analytics

The default time zone is used to compute after-hours metrics when a time zone has not been configured by the user or provided as part of the organizational data. This is typically the time zone of the corporate headquarters or the time zone in which most employees reside. If a measured employee or other internal collaborator does not have a time zone defined as part of the organizational data, the metric will be computed using the default time zone. 

The default time zone for Workplace Analytics is Pacific Standard Time. 

For a complete list of valid times zones, see [Time zones in Workplace Analytics](../Use/Timezones-for-workplace-analytics.md)  

### To change the default time zone 

1. On the **Settings** page, click **Settings**.
2. Under **System defaults**, select the time zone you want from the **Default time zone** list.
3. Click **Save**.

> [!Important]
> This setting takes effect the next time organizational data is received and processed for the following month. A change in this setting does not affect any historical data.

### Working days and working hours

Users can set their own working days and working hours in their [Outlook settings](https://outlook.office.com/owa/?path=/options/calendarappearance). While there is no option to upload working days or working hours in organizational data, a Workplace Analysis administrator can set default working days and working hours for the organization on the System defaults area of the Settings page:

![System defaults area of Settings page](../images/wpa/setup/settings-system-defaults.png)

These admin-configured default settings are used for a particular user only if the user has not already configured their working days and hours. 

### Privacy settings
* **Owner** - Workplace Analytics sponsor, Workplace Analytics administrator
* **Task** - Use company-specific legal and privacy guidelines to define settings to use in Workplace Analytics
* **Outcome** - Privacy settings are defined in Workplace Analytics and you have confirmed that you are ready to provision the service using these rules

Being aware of employees’ rights is a key component to ensuring a successful program using Workplace Analytics.  It is important to consider ever-changing laws and regulations regarding employer-employee relationships, privacy, and personal data, as well as company policies, before using Workplace Analytics.

Workplace Analytics does not encode any specific policy, instead it provides controls that administrators can use to configure the product to be consistent with applicable laws, regulations, and company policies. Your organization chooses what data to use in Workplace Analytics.

> [!Important]
> Please consult with your legal and human resources teams before enabling Workplace Analytics for your organization.

Once you have examined your privacy needs, you will use the Settings area in Workplace Analytics to define the privacy settings for your data.

### Detail display:
- **Minimum Aggregation Size**: Set the minimum group size required to display data in Explore Metrics. By default, the minimum group size is set to five. 
- Decide to show or hide subject lines in meeting reports

### User data exclusion:
- Exclude emails/meetings to, or from, specific users, or all users from a domain using “;” as the delimiter
- Exclude emails/meetings with specific terms in the subject line using “;” as the delimiter.   Terms can be any combination of letters, numbers and special characters, e.g. client attorney privilege; D&I

> [!Note] 
> If you exclude email addresses, you should not assign licenses to them.  You also should consider all aliases for an individual.

### To set your privacy settings 
1. On the **Settings** page, click **Settings**.
2. Under **Privacy settings**, configure the settings to meet your company's needs.

   > [!Note]
   > You may click **Save** at any time to save the privacy settings you are working on, but the settings are not final and ready for use until you click the **I confirm that all privacy settings are complete** checkbox. When you click the checkbox, it begins the processing of Office 365 data.

3. Click **Save**.

   > [!Important]
   > Carefully validate that your privacy settings are correct, before you click the I confirm that all privacy settings are complete checkbox, You can change the settings at any time, but the settings changes will not take effect until the data is processed again for the following month.

4. To begin the processing of Office 365 data, click **I confirm that all privacy settings are complete**, and then click **Save**.

### Related topic
[Settings in Workplace Analytics](../Use/Settings.md) 
