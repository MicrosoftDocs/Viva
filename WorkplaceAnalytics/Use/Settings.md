---

title: Configure settings for Workplace Analytics
description: Describes how Workplace Analytics administrators can set and edit settings in Workplace Analytics
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

# Configure Workplace Analytics settings

You use the following Settings pages in Workplace Analytics to customize system defaults and privacy settings and to upload data:

 * [Sources](#sources) – View dashboards to verify that Office 365 and organizational data is loaded.
 * [Upload](#upload) – Prepare and upload organizational and customer data.
 * [Analysis settings](#analysis-settings) – Customize meeting exclusion rules to help ensure data accuracy.
 * [Admin settings](#admin-settings) – Configure [system defaults](#system-defaults), [privacy settings](#privacy-settings), and [manager settings](#manager-settings).

[!INCLUDE [To open the Workplace Analytics Settings page](../includes/to-open-wpa.md)]

>[!Note]
> Access to one or more pages in Settings depends on what role you're assigned in Workplace Analytics. The following describes page access based on role assignment.

| Settings page | Admin | Analyst | Analyst limited |  
|---|---|---|---|
| Sources | Full access| Full access | Full access |
| Upload  | Full access | No access | No access |
| Analysis settings | No access | Full access | Read only |
| Admin settings | Full access | No access| No access |

For more information, see [Assign Workplace Analytics roles](https://docs.microsoft.com/workplace-analytics/setup/assign-roles-to-wpa-admins).

## Sources

 * **Owners** – Workplace Analytics Admins, Analysts, and Analyst limiteds have full access to this page.

The [Data sources](../Use/data-sourcesv2.md) page provides dashboards that describe the Office 365 data and organizational data that has been loaded into Workplace Analytics. You can view average weekly meeting and email activity and measured-employee characteristics to ensure sufficient data coverage.

## Upload

 * **Owner** – Workplace Analytics Admins have full access to this page.

On the **Upload** > **Organizational data** page, you can upload an organizational data file to Workplace Analytics. This file must be in .csv format, UTF-8 encoded.

![Upload page](../images/wpa/use/settings-upload1.png)

### Organizational data

Organizational data is contextual information about employees (for example, job title, level, location) and can come from HR or other information systems. For detailed information on preparing an organizational data file for upload, see [Prepare organizational data](../setup/prepare-organizational-data.md).

## Analysis settings

 * **Owners** – Workplace Analytics Analysts have full access to this page and limited Analysts have read-only access.

On the **Analysis settings** page, you can create and customize meeting exclusion rules to remove meetings (such as appointments that are unrelated to work) that you don't want to include in analysis.

![Meeting exclusion page](../images/wpa/use/settings-analysis-meeting-exclusions.png)

For detailed information on how to create new exclusion rules, see [Meeting exclusion rules: walkthroughs](../tutorials/meeting-exclusion-rules.md) and [Meeting exclusion rules: Tools and concepts](../tutorials/meeting-exclusion-concept.md).

## Admin settings

 * **Owner** – Workplace Analytics Admins have full access to this page

In **Admin settings**, you can configure [system defaults](#system-defaults), [privacy settings](#privacy-settings), and [manager settings](#manager-settings).

![Admin settings](../images/wpa/use/admin-system-defaults.png)

### System defaults

On the **System defaults** page, you can configure the following:

* [Default time zone](#default-time-zone)
* [Working days and hours](#working-days-and-hours)
* [Hourly rate](#hourly-rate)
* [Reclassify external domains](#reclassify-external-domains)

> [!Important]
> Changes made to these system defaults are applied soon after the next data refresh of your organizational (HR) data or Office 365 collaboration data. These changes apply to data retroactively and can affect calculations of historical metrics.

#### Default time zone

Use this setting to configure the default time zone for your organization. Typically, this is the time zone of the corporate headquarters or the time zone in which most employees reside.

Workplace Analytics first attempts to read time zones from each user's mailbox. If time zone has not been set up for the mailbox, Workplace Analytics tries to determine it from the [organizational data](#organizational-data). If time zones have not been uploaded in the organizational data, Workplace Analytics reads the time zone from the setting on this page. If the default time zone was not set on this page, Workplace Analytics uses Pacific Time (US).

Workplace Analytics uses the time zone setting in calculations of collaboration activities, such as emails and meetings. It uses this setting only for Office 365 data that it has yet to process. Changing the time zone setting does not affect data that has already been processed.

##### To set the default time zone

1. For **Default time zone** on the **System defaults** page, select the applicable time zone to use by default for analysis.
2. Select **Save**.

#### Working days and hours

Users can set their own working days and hours in [Outlook settings](https://outlook.office.com/calendar/options/calendar/view/appearance). Workplace Analytics attempts to read these custom settings from each user’s mailbox first. Failing that, it uses the default settings for employees' working days and hours that you set in **System Defaults**.

Workplace Analytics uses the working days and hours settings in calculations of collaboration activities, such as emails and meetings. It uses these settings only for Office 365 data that it has yet to process. Changing the working days and hours settings does not affect data that has already been processed.

##### To set default working days and hours

1. For **Working days**, select the appropriate days of the week.  
2. For **Start time** and **End time** in **Working hours**, select the start and end times to use by default for analysis.
3. Select **Save**.

#### Hourly rate

Workplace Analytics uses hourly rate to calculate the cost of low-quality meetings, where a person's hourly rate for the organization is multiplied by number of low-quality meeting hours. Workplace Analytics first tries to get the Hourly rate value from organizational (HR) data. Failing that, it uses the value of Hourly rate that is set on this page. For more information, see [Meetings overview](../use/explore-metrics-meetings-overview.md#hourly-rate).

##### To set the default hourly rate

1. For **Hourly rate** on the **System defaults** page, enter an average employee hourly rate to use by default for analysis.
2. Select **Save**.

#### Reclassify external domains

With this setting, you can reclassify one or more external domains as internal, which includes them in your organizational data analysis.

After you add a domain and save the change for this setting, it'll change all of the data related to the specified domain as internal to your organization, as follows:

 * The charts and metrics will show the domain as internal *retroactively* for the specified date range. For example, employees in this domain will change from external to internal collaborators for all collaboration metrics shown in **Explore the stats**.
 * Organizational and Office 365 data from this domain will update to be internal after the *next data refresh*.
 * Sources data will include this domain (previously external) in internal-collaborator metrics and applicable coverage data will change based on this new domain classification.
 * The changes can be reverted by removing the domain that was reclassified.
 * [Excluding domains in the privacy settings](#exclude-domains-or-email-addresses) overrides the changes made with this reclassification setting. That is, an excluded domain remains excluded, whether or not it's reclassified as internal.

### Privacy settings

In **Admin settings** > **Privacy settings**, you can decide what data you want to exclude from analysis and what data you want visible in [Queries](../Tutorials/Query-basics.md) and [Explore the stats data](../Use/explore-intro.md). Watch the [Privacy video](#privacy-video) to learn more about how Workplace Analytics keeps personal data private. You can use privacy settings to:

* [Set the minimum group size](#minimum-group-size)
* [Hash subject lines](#hash-subject-lines)
* [Exclude domains or email addresses](#exclude-domains-or-email-addresses)
* [Exclude terms from subject lines](#exclude-terms-from-subject-lines)

![Admin privacy settings](../images/wpa/use/admin-privacy-settings.png)

After you change privacy settings, your changes take effect after data is processed in the following week. This means that these changes do not affect data that has already been extracted. (For example, the privacy settings for excluding email, meetings, and domains do not affect data retroactively.)

#### Privacy video

<iframe width="640" height="564" src="https://player.vimeo.com/video/282897705" frameborder="0" allowFullScreen mozallowfullscreen webkitAllowFullScreen></iframe>

#### Minimum group size

The minimum-group-size rule protects people from being identified in [Explore the stats data](../use/explore-intro.md) and in [Plans data](../tutorials/solutionsv2-intro.md). If you change this setting, your change takes effect immediately.

The default minimum-group setting is *five*, which is the *minimum allowed value*. You can change this setting according to the privacy requirements of your specific organization.

For example, the columns on the left in the following graphic shows chart data for groups that exceed the minimum-group setting. The grayed-out columns on the right represent *unavailable data* for the groups with fewer people than the minimum-group setting.

   ![Bar chart with bars above and below the minimum-group setting](../images/wpa/group-size-bars.png)

> [!Note]
> The minimum-group-size rule applies to charts that are derived from HR data, which is information about your organization, such as managers at a specific level or employees in a particular city.

**Histogram charts are an exception**

For histogram charts, the minimum-group-size rule is applied differently, in the following ways:

1. If the filter group is too small, no histogram appears.

   If the filter group that the histogram uses for its data is below the minimum group size, Workplace Analytics does not display the histogram at all.

2. If the bin population is too small, the bin still appears.

   In histograms, the x-axis consists of bins (rectangles) that are based on average metric values, and the y-axis determines the number of people whose average metric value puts them in that bin. *These values do not reflect organizational (HR) data.* So the histogram can still show data for a bin even if it contains fewer people than the minimum-group setting. Histogram charts can safely show this data because the data is based on calculations from observed behavior, *not from HR data*.

   Even if a histogram bin has data for only one person, it can still show that data. You cannot single out the person because you don't know which HR group they belong to. (In other charts, such as column charts, a person in a group below the threshold might be identifiable, but in a histogram the HR group to which people belong is the larger filter group.) You also cannot determine the precise metric value of specific people because they are in a bin with a minimum 0.5-hour range.
  
   You can see histogram charts in the following areas of Workplace Analytics:

   * In [Management and coaching data](../use/explore-metrics-management-and-coaching.md) 
   * In [Plans](../Tutorials/solutionsv2-intro.md), on the **Identify** and **Track** pages

#### Hash subject lines

Use this setting to control whether to show or hash subject lines in [Meeting query](../tutorials/meeting-queries.md) results, which, by default, are *not* shown.

If you select **Yes** for **Hash subject lines**, they are converted to a hashed value (a system-generated number), so the text in unreadable in any queries. You can still create meeting queries that include subject-line terms, such as for meeting attributes. However, you won't be able to see a list of meetings that show the subject lines. (After you make this setting, it takes effect immediately, affecting data that has already been processed.)

For example, you could run a query with the subject-line keyword "All-hands." Based on the attributes you include in the query, the results could show data with that subject line, including the number of meetings, the length and size of the meetings, and so on. However, you could not get a specific list of all the meetings with the subject line "All-hands" (a row for each all-hands meeting).

> [!Note]
> Workplace Analytics offers a second opportunity to control which HR attributes are included in query output. You can make selections for the "Include in report" and "Hash in report" options in a dropdown menu when you map uploaded HR data. For more information, see the descriptions of **Include in report** and **Hash in report** in the **Field mapping** section of [Upload organizational data](../setup/upload-organizational-data.md#columns-in-the-fields-tables).

#### Exclude domains or email addresses

You can exclude data from specific domains or data that includes specific email addresses:

* In **Exclude domains**, you can enter one or more domains to exclude from analysis. Any email, meetings, calls, or instant messages that involve people included in these domains will be excluded from any queries.

* In **Exclude email addresses**, you can enter one or more email addresses to exclude from analysis. Any email and meetings that have these email addresses (as either sender or recipient, and attendee or invitee) are now excluded from analysis. For this setting, you need to enter every email address for each alias that you want to exclude.

  > [!Important]
  > Be sure to ask your Office 365 admin to not assign licenses to any excluded email addresses.

#### Exclude terms from subject lines

Subject lines are useful for analysts who want to set up meeting exclusion rules or to query meeting data. You can enter a list of specific keywords or terms that occur in the subject lines of emails and meetings that you want to exclude from analysis.

Terms can be any combination of letters, numbers and special characters (such as client attorney privilege or D&I).

#### Exclusion setting considerations

Any domains, email addresses, or terms you exclude will not be included in any of the analysis, so it's important to carefully consider the implications of an exclusion and balance them with your privacy and data-analysis goals. If you exclude a domain or term that frequently appears in the collaboration dataset, it could adversely skew your analysis. Exclusion occurs before metadata is processed within Workplace Analytics. This means that, after you make an exclusion setting, the setting does not affect data that has already been processed.

If you exclude the email address of the CEO (ceo@company.com), all meetings and emails in which the CEO is included are removed from analysis. So for all meetings and emails that include the CEO, the metadata for all other recipients and attendees included in those same emails and meetings is also excluded from analysis.

To exclude all email that contains the keywords "confidential," "ACP," and "privileged," you would type: **confidential;ACP;privileged**

##### Exclusion logic

* You can use upper or lower-case keywords.
* Must match exact string for subject keywords.
* Does not match partial words; you must list all partial words as separate terms.

 When you add subject-line terms to exclude from analysis, Workplace Analytics might not recognize uncommon compound words, especially those in languages such as Japanese or Chinese. For best results, use single words, separated by semicolons.

Term from subject line to exclude | Actual subject line | Excluded
---------|----------|---------
 legal;acquisition | Verify this is LEGAL | Yes - Case is ignored
 legal;acquisition | Is this illegal | No - Does not match partial words, and did not exclude illegal
 legal;acquisition | Acquisitions are finalized | No - Does not match partial words, and did not exclude acquisitions
 legal;acquisition |Is this a legal acquisition | Yes  - Excluded both legal and acquisition

Learn more about [Workplace Analytics privacy and data access](../privacy/privacy-and-data-access.md).

#### To configure privacy settings

1. In **Admin settings** > **Privacy settings**, for **Minimum group size to display in visual dashboards**, set the minimum group size. You cannot use a value lower than 5.

> [!Note]
> The following exclusion settings are optional and only change query results. These settings do not change the way a query functions.

2. In **Hash subject lines**, select **Yes** to hash subject lines in query results.
3. In **Exclude domains**, type one or more domains to exclude.
4. In **Exclude email addresses**, type one or more email addresses to exclude.
5. In **Exclude terms from subject lines**, type one or more terms or keywords to exclude.
6. Carefully confirm all settings, and then select **I confirm that all privacy settings are correct**. Settings can be finalized only when you select this check box.
7. At the top right of the page, select **Save**.

> [!Important]
>* All subsequent changes to privacy settings after the initial setup, take affect on the next data refresh of your organizational (HR) data or Office 365 collaboration data.
>* Changes to **Hash subject lines** take affect immediately in meeting query results.
>* Changes to the **minimum group** and **Hash subject lines** settings apply retroactively to *all data*, including historical data.
>* Changes to the other exclude from analysis settings apply only to *new data* collected during the next data refresh and do not affect historical data.

### Manager settings

On the **Manager settings** page, you can allow all measured people managers or specific managers access to aggregate collaboration insights about their team and the ability to start plans for their team in Workplace Analytics. Only managers whose team meets or exceeds the **Minimum team size** setting can access Workplace Analytics. The size of the team counts the manager and all the employees who directly or indirectly report to that manager within the organization's reporting hierarchy.

The following are based on the latest organizational (HR) data that's been successfully uploaded and processed in Workplace Analytics:

* **Measured managers** - Total number of people managers who are assigned licenses in Workplace Analytics.
* **Managers enabled** - Total number of people managers who meet the minimum team size and have access to their team's insights and plans in Workplace Analytics.

![Manager settings](../images/wpa/use/manager-settings.png)

* **Minimum team size** - You can set the minimum size of a team that a manager is allowed to view insights about and start plans for. The minimum size allowed is 10. This section also shows you how many measured managers currently have teams that are equal to or more than the minimum setting.
* **Insights and plans** - You can select to allow all licensed managers access to aggregated collaboration insights about their teams and to start and manage plans for their teams. Or you can upload a .csv file that lists the email addresses for the managers you want to give access to their team's insights and plans in Workplace Analytics.
  * If you turn **Insights and plans** on, your organizational hierarchy file will also be used to power personal insights for managers in the [Insights add-in](../myanalytics/use/add-in.md), the [MyAnalytics dashboard](../myanalytics/use/dashboard-2.md), and other MyAnalytics surfaces. This file will complement hierarchy information from Azure AD. If a manager in your organization has team members who are listed in both Azure AD and Workplace Analytics, the system will default to using the Workplace Analytics data; otherwise it will use whichever source is available.
   
     Personal insights help managers improve their personal impact on and relationships with direct reports, and are powered exclusively by information from the manager's own Outlook mailbox. Learn more about personal insights for people managers in [Assistance for people managers](../myanalytics/overview/privacy-guide.md#assistance-for-people-managers).

#### To configure manager settings

> [!Important]
> Before managers can access Workplace Analytics, they must be assigned a Workplace Analytics license and have a team that meets or exceeds the **Minimum team size** setting.

1. In **Admin settings** > **Manager settings**, select to change the switch **On** to allow managers with the minimum team size access to their team data in Workplace Analytics.
2. Select one of the following:

   * **All managers** - Allows all measured managers access.
   * **Select managers** (upload .csv) - Enables you to give specific managers access. You then need to:

      a. Create a .csv file that lists the email addresses for the select managers.

      b. Select **Upload .csv** to upload this list.

3. If you're allowing all managers access, continue to **Step 4**. If setting up access for select managers, select **Download currently enabled manual upload manager list .csv** to confirm which managers now have access. If an error occurs, such as an invalid email or an unlicensed manager, the .csv file will show the error for that manager.
4. In **Minimum team size**, you can change the minimum to a number more than 10 (which is the lowest setting allowed), which limits access to only those managers who have teams equal to or more than that number.
5. Select **Save**.

>[!Note]
>Changes to these settings can take up to an hour to apply.

## Related topics

* [Upload organizational data](../setup/upload-organizational-data.md)
* [Workplace Analytics plans](../tutorials/solutionsv2-intro.md)