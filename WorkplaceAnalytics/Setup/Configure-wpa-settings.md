---
# Metadata Sample
# required metadata

title: Configure Workplace Analytics system settings
description: Describes how to configure the system settings for Workplace Analytics.
author: paul9955
ms.author: v-midehm
ms.date: 10/29/2018
ms.topic: get-started-article
localization_priority: normal 
ms.prod: wpa
---

# Workplace Analytics settings

## System settings

Use the Workplace Analytics **Settings** page to set the time zone, week days, weekend days, and working hours.
      
   ![Make system settings](../images/wpa/setup/02a-settings-sys.png)

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
> This setting change takes effect at the next collaboration data refresh and will not apply to previously calculated data.

### Working days and hours

Users can set their own working days and working hours in their [Outlook settings](https://outlook.office.com/owa/?path=/options/calendarappearance). While there is no option to upload working days or working hours with the organizational data, a Workplace Analytics administrator can set default weekend or non-working days and hours for the organization in the System defaults section on the Settings page.

![System settings default](../images/Wpa/setup/settings-system-defaults-a.png)

These default settings are only used for users who have not already set up their working days and hours in Outlook.

<!-- PERHAPS NOT NEEDED ANYMORE 
### Related topic
[Settings in Workplace Analytics](../Use/Settings.md)
-->

## Privacy settings

* **Owner** - Workplace Analytics sponsor or Workplace Analytics administrator
* **Task** - Use company-specific legal and privacy guidelines to define settings to use in Workplace Analytics
* **Outcome** - After you define and confirm the privacy settings, you are ready to provision the service to comply with these rules

Being aware of employees’ rights is a key component to ensuring a successful program with Workplace Analytics. It's important to consider ever-changing laws and regulations regarding employer-employee relationships, privacy, and personal data, as well as company policies, before setting up and using Workplace Analytics.

Workplace Analytics does not encode any specific policy, instead it provides controls that administrators can use to configure the product to be consistent with applicable laws, regulations, and company policies. Your organization selects what data to use in Workplace Analytics.

> [!Important]
> Consult with your legal and human resources teams before enabling Workplace Analytics for your organization.

After evaluating your privacy needs, you can use the Settings page in Workplace Analytics to define the privacy settings for your organization's data.

   ![Make system and privacy settings](../images/wpa/setup/02b-settings-priv.png)

### Detail display

* Minimum Aggregation Size - Set the minimum group size required to display data in Explore. By default, the minimum group size is set to five. You can change the minimum group size to a level that you consider more relevant for your organization, but you cannot set the group size to lower than five.
* Decide to show or hide subject lines in meeting reports.

### User data exclusions

* Exclude emails/meetings to, or from, specific users, or all users from a domain using “;” as the delimiter
* Exclude emails/meetings with specific terms in the subject line using “;” as the delimiter. Terms can be any combination of letters, numbers and special characters, e.g. client attorney privilege; D&I

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

### Video: Privacy

<iframe width="640" height="564" src="https://player.vimeo.com/video/282897705" frameborder="0" allowFullScreen mozallowfullscreen webkitAllowFullScreen></iframe>

<!-- PERHAPS NOT NEEDED ANYMORE 
### Related topic
[Settings in Workplace Analytics](../Use/Settings.md)
-->
