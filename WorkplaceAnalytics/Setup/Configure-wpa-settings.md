---
# Metadata Sample
# required metadata

title: Configure Workplace Analytics system settings
description: Describes how to configure the system settings for Workplace Analytics
author: paul9955
ms.author: v-midehm
ms.topic: article
localization_priority: normal 
ms.prod: wpa
ms.collection: M365-analytics
manager: scott.ruble
audience: Admin
---

# Workplace Analytics settings

## System settings

Use the Workplace Analytics **System defaults** page in **Admin settings** to set the time zone, working days, and working hours.

   ![System defaults](../images/wpa/use/admin-system-defaults.png)

### Time zone

The following describes who does what for time zone settings:

* **Owner** - Workplace Analytics admin
* **Task** - Default time zone value the system will use in metric calculations if the data is not available for a measured employee or other internal collaborator
* **Outcome** - Default time zone outcome as defined in Workplace Analytics

The default time zone is used to compute after-hours metrics when a time zone has not been configured by the user or provided as part of the organizational data. This is typically the time zone of the corporate headquarters or the time zone in which most employees reside. If a measured employee or other internal collaborator does not have a time zone defined as part of the organizational data, the metric will be computed using the default time zone.

The default time zone for Workplace Analytics is Pacific Standard Time.

For a complete list of valid times zones, see [Time zones in Workplace Analytics](../Use/Timezones-for-workplace-analytics.md)  

### To change the default time zone

1. On the **Admin settings** > **System defaults** page, select the time zone you want from the **Default time zone** list.
2. Select **Save**.

> [!Important]
> This setting change takes effect at the next collaboration data refresh and will not apply to previously calculated data.

### Working days and hours

Users can set their own working days and working hours in their [Outlook settings](https://outlook.office.com/calendar/options/calendar/view/appearance). While there is no option to upload working days or working hours with the organizational data, a Workplace Analytics admin can set default working days and hours for the organization on the System defaults page in Admin settings.

These default settings are only used for users who have not already set up their working days and hours in Outlook.

<!-- PERHAPS NOT NEEDED ANYMORE 
### Related topic
[Settings in Workplace Analytics](../Use/Settings.md)
-->

## Privacy settings

The following describes who does what for privacy settings:

* **Owner** - Workplace Analytics sponsor or Workplace Analytics administrator
* **Task** - Use company-specific legal and privacy guidelines to define settings to use in Workplace Analytics
* **Outcome** - After you define and confirm the privacy settings, you are ready to provision the service to comply with these rules

Being aware of employees’ rights is a key component to ensuring a successful program with Workplace Analytics. It's important to consider ever-changing laws and regulations regarding employer-employee relationships, privacy, and personal data, as well as company policies, before setting up and using Workplace Analytics.

Workplace Analytics does not encode any specific policy, instead it provides controls that administrators can use to configure the product to be consistent with applicable laws, regulations, and company policies. Your organization selects what data to use in Workplace Analytics.

> [!Important]
> Consult with your legal and human resources teams before enabling Workplace Analytics for your organization.

After evaluating your privacy needs, you can use the Privacy settings page in Workplace Analytics to define the privacy settings for your organization's data.

   ![Privacy settings](../images/wpa/use/admin-privacy-settings.png)

### Privacy settings

* Minimum Aggregation Size - Set the minimum group size required to display data in Explore. By default, the minimum group size is set to five. You can change the minimum group size to a level that you consider more relevant for your organization, but you cannot set the group size to lower than five.
* Decide to show or hide subject lines in meeting reports.
* Exclude emails/meetings to, or from, specific users, or all users from a domain using “;” as the delimiter
* Exclude emails/meetings with specific terms in the subject line using “;” as the delimiter. Terms can be any combination of letters, numbers and special characters. However each term must be listed separately, because only exact subject keywords are excluded, for example: client;attorney;privilege;D&I;legal acquisition. For more details, see [Keyword exclusion logic](../Privacy/Privacy-considerations.md#keyword-exclusion-logic).

> [!Note]
> If you exclude email addresses, do not assign licenses to them. Be sure to include all email aliases for a person.

### To set your privacy settings

1. On the **Admin settings** > **Privacy settings** page, configure the settings to meet your company's needs.

   > [!Note]
   > You can select **Save** at any time to save the privacy settings you are working on, but the settings are not final and ready for use until you select the **I confirm that all privacy settings are complete** check box. After you select the check box, the processing of Office 365 data begins.

2. Select **Save**.

   > [!Important]
   > Carefully validate that your privacy settings are correct, before you check the "I confirm that all privacy settings are complete" box, you can change the settings at any time, but the settings changes will not take effect until the data is processed again for the following month.

3. To begin the processing of Office 365 data, select the **I confirm that all privacy settings are complete** check box, and then select **Save**.

### Video: Privacy

<iframe width="640" height="564" src="https://player.vimeo.com/video/282897705" frameborder="0" allowFullScreen mozallowfullscreen webkitAllowFullScreen></iframe>

<!-- PERHAPS NOT NEEDED ANYMORE 
### Related topic
[Settings in Workplace Analytics](../Use/Settings.md)
-->
