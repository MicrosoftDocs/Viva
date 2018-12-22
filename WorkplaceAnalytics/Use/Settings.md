---
# Metadata Sample
# required metadata

title: Configure settings for Workplace Analytics
description: Describes how Workplace Analytics administrators can set and edit settings in Workplace Analytics. 
author: buntus
ms.author: v-johtob
ms.date: 12/06/2018
ms.topic: get-started-article
localization_priority: normal 
ms.prod: wpa
---

# Configure Workplace Analytics settings

The Settings pages of Workplace Analytics are used to customize system defaults and privacy settings and to upload data. These are the four Settings pages: 

 * [Sources](#sources). View dashboards to verify that Office 365 and organizational data is loaded.
 * [Upload](#upload). Prepare and upload organizational and customer data.
 * [Analysis settings](#analysis-settings). Customize meeting exclusion rules to help ensure data accuracy.
 * [Admin settings](#admin-settings). Configure system defaults and privacy settings.

[!INCLUDE [To open the Workplace Analytics Settings page](../includes/to-open-wpa.md)] 

>[!Note] 
> The access you have to the Settings pages depends on the role (admin, analyst, or analyst limited) that you’ve been assigned:

| Settings page | Admin | Analyst | Analyst limited |  
|---|---|---|---|
| Sources | Full access| Full access | Full access | 
| Upload  | Full access | No access | No access |
| Analysis settings | No access | Full access | Read only | 
| Admin settings | Full access | No access| No access | 

For more information, see [Assign Workplace Analytics roles](https://docs.microsoft.com/workplace-analytics/setup/assign-roles-to-wpa-admins).

## Sources

 * **Owner** – Workplace Analytics admin, Workplace Analytics analyst, Workplace Analytics Analyst limited. 

The [Sources](../Use/data-sources.md) page provides dashboards that describe the Office 365 data and organizational data that has been loaded into Workplace Analytics. You can view average weekly meeting and email activity and measured-employee characteristics to ensure sufficient data coverage.

## Upload

 * Owner – Workplace Analytics admin.

On the **Upload** page under the **Organizational data** tab, you can upload an organizational data file to Workplace Analytics. This file must be in .csv format, UTF-8 encoded.

![Upload page](../images/wpa/use/settings-upload1.png)

### Organizational data

Organizational data is contextual information about employees (for example, job title, level, location) and can come from HR or other information systems. For detailed information on preparing an organizational data file for upload, see [Preparing organizational data](../setup/prepare-organizational-data.md).

## Analysis settings

On the **Analysis settings** page, you can create and customize meeting exclusion rules to remove meetings (such as appointments that are unrelated to work) that you don't want to include in analysis.

![Meeting exclusion page](../images/wpa/use/settings-analysis-meeting-exclusions.png)

For detailed information on how to create new exclusion rules, see [Meeting exclusion rules: walkthroughs](../tutorials/meeting-exclusion-rules.md) and [Meeting exclusion rules: Tools and concepts](../tutorials/meeting-exclusion-concept.md). 

## Admin settings

 * Owner – Workplace Analytics admin. 

On the **Admin settings** page, you can configure system defaults and privacy settings.

![Admin settings](../images/wpa/use/settings-system-defaults.png)

## System defaults

On the **System and privacy** tab, in the **System defaults** section, you can configure the following employee options:

- Default time zone
- Working days and hours
- Hourly rate

### Default time zone

Use this setting to configure the default time zone for your organization. Typically, this is the time zone of the corporate headquarters or the time zone in which most employees reside.

Workplace Analytics first attempts to read time zones from each user's mailbox. If time zone has not been set up for the mailbox, Workplace Analytics tries to determine it from the [organizational data](#organizational-data). If time zones have not been uploaded in the organizational data, Workplace Analytics reads the time zone from the setting on this page. If the default time zone was not set on this page, Workplace Analytics uses Pacific Time (US). 

#### To set the default time zone

 * In the **Default time zone** list box, under **System defaults**, select the appropriate time zone.

   ![Default time zone](../images/wpa/use/settings-default-time-zone-b.png)

### Working days and hours

Users can set their own working days and hours in [Outlook settings](https://outlook.office.com/owa/?path=/options/calendarappearance). Workplace Analytics attempts to read these custom settings from each user’s mailbox. Failing that, it uses the values for employees' working and non-working days and hours that you have set in the **System Defaults** section. 

#### To configure working days and hours

1. For **Working days**, select the appropriate check boxes for the days of the week.
2. For the **Working day starts** and **Working day ends** list boxes, select the appropriate start and end times.

   ![Working days and hours](../images/wpa/use/settings-system-defaults-b.png)

### Hourly rate

A value for Hourly rate is used to calculate the cost of low-quality meetings: a person's hourly rate for the organization multiplied by number of low-quality meeting hours. Workplace Analytics first attempts to obtain the Hourly rate value from organizational data. Failing that, it uses the value of Hourly rate that is set on this page. For more information, see [Meetings overview](../use/explore-metrics-meetings-overview.md#hourly-rate).

#### To set the hourly rate

 * In the **Hourly rate** field, under **System defaults**, enter the appropriate employee hourly rate. 

## Privacy settings

In the **Privacy settings** section, you can decide what data you want to exclude from analysis and what data you want to be visible in queries and dashboards. You can use privacy settings to:

* Specify the minimum group size
* Specify whether to hide subject lines in meeting query results
* Exclude words from subject lines
   
### Specify the minimum group size

The minimum group size setting determines what you can view in the [Explore metrics](../Use/Explore-Metrics-Week-in-the-Life.md) dashboards and in the [Solutions](../tutorials/solutions-task.md) area.

This setting helps to maintain employee privacy by ensuring that individuals cannot be easily identified by the attributes of groups that they are in. The default minimum group size is set to five, but you can adjust it to suit the needs of your organization. (The minimum allowed value is five.) 

The minimum-group-size rule protects people from being identified by causing charts to display data differently.

**Example**

In the following chart, the blue-green columns on the left represent groups whose size exceeds the minimum group size. For this reason, they display real data. The gray and white columns on the right represent no data because the groups are below the minimum-group-size threshold.

   ![Bar chart with bars above and below group size threshold](../images/wpa/group-size-bars.png)

> [!Note]
> The minimum-group-size rule applies to charts that display information derived from HR data. In other words, the charts display information about circumstances that exist in your organization -- such as managers at a specific level or employees in a particular city.  

**Histogram charts: an exception to the rule**

For histogram charts, the minimum-group-size rule is applied differently, in the following ways:

1. If the filter group is too small, no histogram appears.

   If the filter group that the histogram uses for its data is below the minimum group size, Workplace Analytics does not display the histogram at all.

2. If the bin population is too small, the bin still appears.

   In histograms, the x-axis consists of rectangles, called "bins", that are based on average metric values, and the y-axis determines the number of people whose average metric value puts them in that bin. _Neither of these values reflects organizational data._ For this reason, the histogram still displays data for a bin even if it contains fewer people than the minimum-group-size value. Histogram charts can safely display this information because the information is based on metrics -- on values calculated from observed behavior, _not_ on HR data.

   Even if a bin in a histogram contained data for only one individual, the histogram still displays that data. You cannot single out this individual because you do not know what HR group they belong to. (In other charts, such as column charts, an individual in a group below the threshold might be identifiable, but in a histogram the HR group to which individuals belong is the larger filter group.) You also cannot determine the precise metric value of individuals because they are in a bin with a minimum 0.5-hour range.
  
   You can see histogram charts on the following pages in Workplace Analytics:

   * In **Explore** on the [Management and coaching](../use/explore-metrics-management-and-coaching.md) tab  
   * In [Solutions:](../Tutorials/solutions-intro.md)
  
       * To set goals 
       * To track program success on the Track page 

### Specify whether to hide subject lines in meeting query results

Use this setting to control whether to include or hide subject lines in [Meeting query](../tutorials/meeting-queries.md) results, which, by default, are _not_ shown.

![Privacy settings](../images/wpa/use/settings-privacy-settings-1a.png)

If you select **Yes** for **Hide subject lines from meeting query results**, the subject lines are converted to a hashed value (a system-generated number), so that the text in subject lines is not readable in any queries. You can still create meeting queries that include subject line keywords as meeting attributes. However, you won't be able to see a list of meetings that show the subject lines. 

**Example**   
If you select **Yes**, you could run a meeting query with the subject-line keyword "All-hands." Based on the attributes you include in the query, the results could show data about the number of meetings, the length of meetings, the size of meetings, and so on, with that subject line. However, you could not get a specific list – one line item for each meeting – of all the meetings with the subject line "All-hands."
    
### Exclude words from subject lines

Subject lines are useful for analysts who want to set up meeting exclusion rules or to query meeting data. You can enter a list of specific keywords or terms that occur in the subject lines of emails and meetings that you want to exclude from analysis. You can decide to:

 * Exclude instances of collaboration between: 
    * Specific email addresses
    * Specific users in specific domains

That is, you can exclude from analysis any emails and meeting invitations to, or from, specific users, or exclude all users from specified domains. Any and all emails and meetings in which these email addresses are included (as both sender or recipient, and attendee or invitee) are now excluded. Regarding domains, you only have the option to exclude (blacklist), not include (whitelist), specific domains.

Terms can be any combination of letters, numbers and special characters (e.g., client attorney privilege, D&I, etc.). Any items you exclude will not be included in the analysis, so it is important to carefully consider and balance your privacy and data-analysis goals. If you exclude domains, email addresses, or subject terms that frequently appear in the collaboration data set, it could adversely skew your analysis. Exclusion occurs before metadata is processed within Workplace Analytics. 
 
Learn more about [Workplace Analytics privacy and data access](../privacy/privacy-and-data-access.md).

> [!Note]
> Office 365 admins should not assign licenses to any excluded email addresses.

![Privacy settings](../images/wpa/use/settings-privacy-settings-b.png)
  
As an example, if you exclude the email address of the CEO, (ceo@company.com) all meetings and emails in which the CEO is included are removed from analysis. This means that for all meetings and emails that include the CEO, the metadata for all other recipients and attendees included in those same emails and meetings is also excluded. 

If a user has multiple aliases, you must enter every email address for each alias that you want to exclude. When adding email addresses to exclude, it's important to consider all the implications of an exclusion.

**Example: Exclude terms from subject line**

To exclude all emails that contain the keywords "confidential," "ACP," and "privileged," you would type: **confidential;ACP;privileged**

#### Keyword exclusion logic

* You can use upper or lower-case keywords.
* Matches exact string for subject keywords.
* Does not match partial words; you must list all partial words as separate terms.

#### Examples: Keyword exclusion logic

Term from subject line to exclude | Actual subject line | Excluded
---------|----------|---------
 legal;acquisition | Verify this is LEGAL | Yes - Case is ignored
 legal;acquisition | Is this illegal | No - Does not match partial words, and did not exclude illegal
 legal;acquisition | Acquisitions are finalized | No - Does not match partial words, and did not exclude acquisitions
 legal;acquisition |Is this a legal acquisition | Yes  - Excluded both legal and acquisition

 When you add subject-line terms to exclude from analysis, Workplace Analytics might not recognize uncommon compound words, especially those in languages such as Japanese or Chinese. For best results, use single words, separated by semicolons.

### To configure privacy settings

1.	Under **Privacy settings**, for **Minimum group size to display in visual dashboards**, type the minimum group size. You cannot use a value lower than 5. 
2.	(Optional) Select **Hide meeting subject lines from meeting query results** to hide subject lines. This does not change the way a query functions; it changes only the display of the results.
3.	(Optional) Exclude from analysis any sensitive domains, email addresses, or keywords in subject lines.
4.	Carefully verify that your privacy settings are correct and then select **I confirm that all privacy settings are complete and that data will not be made available until user licenses have been applied**. Settings can be finalized only if you've selected this check box.
5.	At the top right of the page, select **Save**. 

> [!Note] 
> All subsequent changes to privacy settings after they run for the first time do not take effect until the next time that Workplace Analytics refreshes collaboration data. Any changes made to system defaults affect existing data.

### Video: Privacy

<iframe width="640" height="564" src="https://player.vimeo.com/video/282897705" frameborder="0" allowFullScreen mozallowfullscreen webkitAllowFullScreen></iframe>
