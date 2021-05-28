---

title: System defaults for Workplace Analytics
description: Describes the system default settings in Workplace Analytics that administrators configure and edit for your organization
author: paul9955
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

# System defaults

In **System defaults**, you can configure the following:

* [Default time zone](#default-time-zone)
* [Working days](#working-days)
* [Working hours](#working-hours)
* [Hourly rate](#hourly-rate)
* [Minimum group size for analysis](#minimum-group-size)

If you are setting up Workplace Analytics, follow these steps:

1. Examine the default values of these **System defaults** settings. Either accept these default values or change one or more of them. 
2. Expand the **Exclusions** section and look at its settings. (For more information about these settings, see [Privacy settings / Exclusions](privacy-settings.md).)
3. Optionally, specify data to exclude in one or the **Exclusion** options and, optionally, select to hash subject lines.
4. Select **Next**. Workplace Analytics now begins to process your organization's collaboration (Microsoft 365) data.

If you are not setting up Workplace Analytics, feel free to change these settings whenever it's necessary.

<!-- REMOVING THIS PER NEW REARRANGEMENT BY NISHANT MAY 2021:
* [Reclassify external domains](#reclassify-external-domains) -->

> [!Important]
> Changes made to these system defaults are applied soon after the next data refresh of your organizational (HR) data or Microsoft 365 collaboration data. These changes apply to data retroactively and can affect calculations of historical metrics.

**Owner** – Only Workplace Analytics Admins have full access to this page. For details, see [Assign roles to Workplace Analytics admins and analysts](../setup/assign-roles-to-wpa-admins.md).

![Admin settings](../images/wpa/use/wpa-setup-start.png)

## Default time zone

Use this setting to configure the default time zone for your organization. Typically, this is the time zone of the corporate headquarters or the time zone in which most employees reside.

Workplace Analytics first attempts to read time zones from each user's mailbox. If time zone has not been set up for the mailbox, Workplace Analytics tries to determine it from the [organizational data](organizational-data.md). If time zones have not been uploaded in the organizational data, Workplace Analytics reads the time zone from the setting on this page. If the default time zone was not set on this page, Workplace Analytics uses Pacific Time (US).

Workplace Analytics uses the time zone setting in calculations of collaboration activities, such as emails and meetings. It uses this setting only for Microsoft 365 data that it has yet to process. Changing the time zone setting does not affect data that has already been processed.

### To set the default time zone

1. For **Default time zone** on the **System defaults** page, select the applicable time zone to use by default for analysis.
2. Select **Save**.

## Working days and working hours

Users can set their own working days in [Outlook settings](https://outlook.office.com/calendar/options/calendar/view/appearance). Workplace Analytics attempts to read these custom settings from each user’s mailbox first. Failing that, it uses the default settings for employees' working days and hours that you set in **System Defaults**.

Workplace Analytics uses the working days and hours settings in calculations of collaboration activities, such as emails and meetings. It uses these settings only for Microsoft 365 data that it has yet to process. Changing the working days and hours settings does not affect data that has already been processed.

### To set default working days

* For **Working days**, select the appropriate days of the week.  

### To set default working hours

* For **Working hours**, select the start and end times to use by default for analysis.

## Hourly rate

Workplace Analytics uses hourly rate to calculate the cost of low-quality meetings, where a person's hourly rate for the organization is multiplied by number of low-quality meeting hours. Workplace Analytics first tries to get the Hourly rate value from organizational (HR) data. Failing that, it uses the value of Hourly rate that is set on this page. For more information, see [Meetings overview](../use/explore-metrics-meetings-overview.md#hourly-rate).

### To set the default hourly rate

1. For **Hourly rate**, enter an average employee hourly rate to use by default for analysis.
2. Select **Save**.

## Minimum group size for analysis

The minimum-group-size rule protects people from being identified in Workplace Analytics data, including in [Insights](insights.md), [Explore the stats](../Use/explore-intro.md), and [Plans](../tutorials/solutionsv2-intro.md). If you change this setting, your change takes effect immediately.

The default minimum-group setting is *five*, which is the *minimum allowed value*. You can change this setting according to the privacy requirements of your specific organization.

For example, the columns on the left in the following graphic shows chart data for groups that exceed the minimum-group setting. The gray-striped column represents *unavailable data* for the CEO group that has fewer people than the minimum-group setting.

![1:1 meeting hours protects employee privacy](../images/wpa/use/1x1-meeting-hours.png)

>[!Note]
>The minimum-group-size rule applies to charts that are derived from HR data, which is information about your organization, such as managers at a specific level or employees in a particular city.

### Histogram charts are an exception

For histogram charts, the minimum-group-size rule is applied differently, in the following ways:

1. If the filter group is too small, no histogram appears.

   If the filter group that the histogram uses for its data is below the minimum group size, Workplace Analytics does not display the histogram at all.

2. If the bin population is too small, the bin still appears.

   In histograms, the x-axis consists of bins (rectangles) that are based on average metric values, and the y-axis determines the number of people whose average metric value puts them in that bin. *These values do not reflect organizational (HR) data.* So the histogram can still show data for a bin even if it contains fewer people than the minimum-group setting. Histogram charts can safely show this data because the data is based on calculations from observed behavior, *not from HR data*.

   Even if a histogram bin has data for only one person, it can still show that data. You cannot single out the person because you don't know which HR group they belong to. (In other charts, such as column charts, a person in a group below the threshold might be identifiable, but in a histogram the HR group to which people belong is the larger filter group.) You also cannot determine the precise metric value of specific people because they are in a bin with a minimum 0.5-hour range.
  
   You can see histogram charts in the following areas of Workplace Analytics:

   * In [Management and coaching](../use/explore-metrics-management-and-coaching.md)
   * In [Plans](../Tutorials/solutionsv2-intro.md), on the **Identify** and **Track** pages

<!-- REMOVING THIS SECTION FOR NOW. IT'S GONE FROM BOTH THE SPEC AND FROM FIGMA (MAY 2021)

## Reclassify external domains

You can use this setting to reclassify one or more external domains as internal, which includes them in your organizational data analysis.

After you add a domain and save the change for this setting, it'll change all of the data related to the specified domain as internal to your organization, as follows:

* Explore the stats charts and metrics will show the domain as internal *retroactively* for the specified date range. For example, employees in this domain will change from external to internal collaborators for all collaboration data shown in **Explore the stats**.
* Organizational and Microsoft 365 data from this domain will update to be internal after the *next data refresh*.
* Sources data will include this domain (previously external) in internal-collaborator metrics and applicable coverage data will change based on this new domain classification.
* The changes can be reverted by removing the domain that was reclassified.
* [Excluding domains in the privacy settings](privacy-settings.md#exclude-domains-or-email-addresses) overrides the changes made with this reclassification setting. That is, an excluded domain remains excluded, whether or not it's reclassified as internal.

### To reclassify an external domain

1. For **Reclassify external domain**, enter an external domain in the search field, and then select it to reclassify it as internal to your organization.
2. Select **Save** (top right of page).

-->

## Related topics

* [Set up Workplace Analytics](../setup/set-up-workplace-analytics.md)

* [Privacy settings / Exclusions](privacy-settings.md)
