---

title: Privacy settings and exclusions for Viva Insights
description: Describes the privacy settings and exclusions in Viva Insights that administrators can set up and edit for your organization
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

# Privacy settings and exclusions

As the Viva Insights admin, you use privacy settings to determine what data your organization wants to exclude from analysis and what data can be visible in [Query designer](../Tutorials/query-designer.md) and [Explore the stats](../Use/explore-intro.md). Watch the [Privacy video](#privacy-video) to learn more about how Viva Insights keeps personal data private.

You can use privacy settings to:

* [Set the minimum group size](#minimum-group-size)
* [Hash subject lines](#hash-subject-lines)
* [Exclude domains](#exclude-domains-or-email-addresses)
* [Exclude email addresses](#exclude-domains-or-email-addresses)
* [Exclude terms from subject lines](#exclude-terms-from-subject-lines)

**Owner** – Viva Insights admins have full access to this page. For details, see [Assign roles to admins and analysts](../setup/assign-roles-to-wpa-admins.md).

Admins configure the privacy settings in **Analyst settings** > **Privacy** when setting up the advanced insights app.

![Privacy settings for advanced insights](../images/wpa/use/privacy-settings.png)

<!-- VERIFY BOTH OF THE FOLLOWING PARAGRAPHS! -->

>[!IMPORTANT]
>You do not need to configure privacy settings while onboarding your organization. You must complete the settings on the **System defaults** page, but you can choose to skip the privacy settings during setup and complete them later. (To indicate that you have completed the **System defaults** settings, select **Next** on that page.)

If you do change privacy settings, your changes take effect after Microsoft 365 data is processed in the following week. This means that these changes do not affect data that has already been extracted and processed. (For example, the privacy settings for excluding email, meetings, and domains do not affect data retroactively.)

## Privacy video

<iframe width="640" height="564" src="https://player.vimeo.com/video/282897705" frameborder="0" allowfullscreen=""></iframe>

## Minimum group size

The minimum-group-size rule protects people from being identified in Viva Insights data, including in [Insights](insights.md), [Explore the stats](../Use/explore-intro.md), and [Plans](../tutorials/solutionsv2-intro.md). If you change this setting, your change takes effect immediately.

The default minimum-group setting is *five*, which is the *minimum allowed value*. You can change this setting according to the privacy requirements of your specific organization.

For example, the columns on the left in the following graphic shows chart data for groups that exceed the minimum-group setting. The gray-striped column represents *unavailable data* for the CEO group that has fewer people than the minimum-group setting.

![1:1 meeting hours protects employee privacy.](../images/wpa/use/1x1-meeting-hours.png)

>[!Note]
>The minimum-group-size rule applies to charts that are derived from HR data, which is information about your organization, such as managers at a specific level or employees in a particular city.

## Hash subject lines

Use this setting to control whether to show or hash subject lines in [Meeting query](../tutorials/meeting-queries.md) results, which, by default, are *not* shown.

If you select **Yes** for **Hash subject lines**, they are converted to a hashed value (a system-generated number), so the text in unreadable in any queries. You can still create meeting queries that include subject-line terms, such as for meeting attributes. However, you won't be able to see a list of meetings that show the subject lines. (After you make this setting, it can take up to ten minutes for your change to take effect. After the change does take effect, it affects data that Viva Insights has already processed.)

For example, you could run a query with the subject-line keyword "All-hands." Based on the attributes you include in the query, the results could show data with that subject line, including the number of meetings, the length and size of the meetings, and so on. However, you could not get a specific list of all the meetings with the subject line "All-hands" (a row for each all-hands meeting).

>[!Note]
>Viva Insights offers a second opportunity to control which HR attributes are included in query output. You can make selections for the "Include in report" and "Hash in report" options in a dropdown menu when you map uploaded HR data. For details, see the descriptions of **Include in report** and **Hash in report** in [Field mapping](../setup/upload-organizational-data2.md#field-mapping).

## Exclude domains or email addresses

You can exclude data from specific domains or data that includes specific email addresses:

* In **Exclude domains**, you can enter one or more domains to exclude from analysis. Any email, meetings, calls, or instant messages that involve people included in these domains will be excluded from any queries.

* In **Exclude email addresses**, you can enter one or more email addresses to exclude from analysis. Any email and meetings that have these email addresses (as either sender or recipient, and attendee or invitee) are now excluded from analysis. For this setting, you need to enter every email address for each alias that you want to exclude.

  >[!Important]
  >Be sure to ask your Microsoft 365 admin to not assign licenses to any excluded email addresses.

## Exclude terms from subject lines

Subject lines are useful for analysts who want to set up meeting exclusion rules or to query meeting data. You can enter a list of specific keywords or terms that occur in the subject lines of emails and meetings that you want to exclude from analysis.

Terms can be any combination of letters, numbers and special characters (such as client attorney privilege or D&I).

![Exclude email addresses, terms from subject lines.](../images/wpa/use/two-exclusions.png)

## Exclusion setting considerations

Any domains, email addresses, or terms you exclude will not be included in any of the analysis, so it's important to carefully consider the implications of an exclusion and balance them with your privacy and data-analysis goals. If you exclude a domain or term that frequently appears in the collaboration dataset, it could adversely skew your analysis. Exclusion occurs before metadata is processed within Viva Insights. This means that, after you make an exclusion setting, the setting does not affect data that has already been processed.

If you exclude the email address of the CEO (ceo@company.com), all meetings and emails in which the CEO is included are removed from analysis. So for all meetings and emails that include the CEO, the metadata for all other recipients and attendees included in those same emails and meetings is also excluded from analysis.

To exclude all email that contains the keywords "confidential," "ACP," and "privileged," you would type: **confidential;ACP;privileged**

## Exclusion logic

* You can use upper or lower-case keywords.
* Must match exact string for subject keywords.
* Does not match partial words; you must list all partial words as separate terms.

 When you add subject-line terms to exclude from analysis, Viva Insights might not recognize uncommon compound words, especially those in languages such as Japanese or Chinese. For best results, use single words, separated by semicolons.

Term from subject line to exclude | Actual subject line | Excluded
---------|----------|---------
 legal;acquisition | Verify this is LEGAL | Yes - Case is ignored
 legal;acquisition | Is this illegal | No - Does not match partial words, and did not exclude illegal
 legal;acquisition | Acquisitions are finalized | No - Does not match partial words, and did not exclude acquisitions
 legal;acquisition |Is this a legal acquisition | Yes  - Excluded both legal and acquisition

Learn more about [Viva Insights privacy and data access](/viva/insights/privacy/privacy-and-data-access?toc=/viva/insights/use/toc.json&bc=/viva/insights/breadcrumb/toc.json).

## To configure privacy settings

1. In **Analyst settings** > **Privacy**, for **Minimum group size to display in visual dashboards**, set the minimum group size. You cannot use a value lower than 5.

   >[!Note]
   >The following exclusion settings are optional and only change query results. These settings do not change the way a query functions.

2. In **Hash subject lines**, select **Yes** to hash subject lines in query results.
3. In **Exclude domains**, type one or more domains to exclude.
4. In **Exclude email addresses**, type one or more email addresses to exclude.
5. In **Exclude terms from subject lines**, type one or more terms or keywords to exclude.
6. Carefully confirm all settings, and then select **I confirm that all privacy settings are correct**. Settings can be finalized only when you select this checkbox.
7. At the top right of the page, select **Save**.

>[!Important]
>
>* All subsequent changes to privacy settings after the initial setup, take effect on the next data refresh of your organizational (HR) data or Microsoft 365 collaboration data.
>* Changes to **Hash subject lines** take effect immediately in meeting query results.
>* Changes to the **minimum group** and **Hash subject lines** settings apply retroactively to *all data*, including historical data.
>* Changes to the other exclude from Analyst settings apply only to *new data* collected during the next data refresh and do not affect historical data.

## Related topics

* [Set up Advanced insights](../setup/set-up-workplace-analytics.md)
* [System defaults](system-defaults.md)
