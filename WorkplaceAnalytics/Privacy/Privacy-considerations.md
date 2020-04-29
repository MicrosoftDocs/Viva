---

title: Workplace Analytics privacy considerations
description: Privacy considerations when using Workplace Analytics to analyze your organizational data
author: madehmer
ms.author: v-midehm
ms.topic: conceptual
localization_priority: normal 
ms.prod: wpa
ms.collection: M365-analytics
manager: scott.ruble
audience: Admin
---

# Privacy considerations for Workplace Analytics

This article introduces various considerations for Workplace Analytics admins to explore while deciding on privacy settings.

## Minimum group size

A minimum group size helps maintain employee privacy by ensuring that specific people cannot be easily identified by the attributes of the group. The default minimum group size is five.

### The rule

The minimum-group setting determines what you can view in the dashboards in [Explore metrics](../Use/Explore-Metrics-Week-in-the-Life.md) and in the [Plans](../Tutorials/solutionsv2-intro.md) area. You can change the minimum group size to a level that you consider more relevant for your organization, but you cannot set the group size to lower than five. The minimum-group-size rule protects people from being individually identified by means of de-identified data presented in a chart.

#### Example

In the following chart, the blue-green columns on the left represent groups whose size exceeds the minimum group size. For this reason, they display real data.

The gray and white columns on the right represent no data because the groups are below the minimum-group-size threshold.

<img src="../Images/WpA/group-size-bars.png" alt="Bar chart with bars above and below group size threshold">

> [!Note]
> The minimum group size rule applies to charts that display information derived from HR data. In other words, they display information about circumstances that exist in your organization -- such as managers at a specific level or employees in a particular city.  

### Histogram charts are an exception to the rule

For histogram charts, the minimum-group-size rule is applied differently, in the following ways:

1. **Filter group too small, then no histogram will appear**

   If the _filter group_ that the histogram uses for its data is below minimum group size, Workplace Analytics does not display the histogram at all.

2. **Bin population too small, the bin will still appear**

   In histograms, the x-axis consists of rectangles (called "bins") that are based on average metric values, and the y-axis determines the number of people whose average metric value puts them in that bin. _Neither of these values reflects HR data._ For this reason, the histogram still displays data for a bin even if it contains fewer people than the minimum-group value. Histogram charts can safely display this information because it is based on metrics -- on values calculated from observed behavior, _not_ on HR data.

   Even if a bin in a histogram contained data for only one individual, the histogram still displays that data. You cannot single out this individual because you do not know what HR “group” they belong to. (In other charts, such as column charts, an individual in a group below the threshold might be identifiable, but in a histogram the HR group to which individuals belong is the larger filter group.) You also cannot determine the precise metric value of an individual because they are in a bin with a minimum 0.5-hour range.

#### Where to find histogram charts

You can see histogram charts in the following pages in Workplace Analytics:

* On the Management and Coaching page in Explore
* For goal setting in Plans
* To track program success on the Track page in Plans

## Hash subject lines

You can help maintain employee privacy by hiding the subject lines of meetings and emails. There are privacy and data analysis trade-offs for each scenario. The following information can help you determine whether or not you want to hide subject lines in your queries.  

When you select **Yes** for **Hash subject lines**, the subject lines are changed to hashed values (a system-generated number), so the text in subject lines will not be readable in any queries.

If you choose to hash subject lines, you can still create queries based keywords in the subject lines. However, you are not able to see a list of meetings that show the subject lines.

#### Example: Hashed subject lines

With **Hash subject lines** turned on, you can run a meeting query with the subject-line keyword “All-hands,” and (based on the attributes you include in the query) it could show data about the number of meetings, the length of meetings, the size of meetings, and so on, with that subject line.

However, you could not get a specific list (one line item for each meeting) of all the meetings with the subject line “All-hands.”

## Exclude calendar and email terms from analysis

You can help maintain employee privacy and focus your analysis by excluding certain terms from analysis. Since any items you exclude will not be included in the analysis, it is important to carefully consider and balance your privacy and data analysis goals. It could adversely skew your analysis if you exclude domains, email addresses, or subject terms that frequently appear within the collaboration data set.

The following information can help you determine what privacy settings best match your company’s policies and objectives.

### Domains

You can enter a list of domains that you want to exclude. All email, meetings, calls, and instant messages from domains listed here are excluded from analysis.

> [!Note]
> There exists only the option to exclude (black list) specific domains, not to include (white list) specific domains.

### Email addresses

You can enter a list of email addresses to exclude. _Any and all_ emails and meetings in which these email addresses are included (as both sender/recipient and attendee/invitee) are excluded from analysis. When adding email addresses to exclude, it's important to consider all the sender/recipient and attendee/invitee implications of an exclusion.

#### Example: Exclude email addresses

If you exclude the email address of the CEO (ceo@company.com), all meetings and emails in which the CEO is included is removed from analysis. This means that all meetings and emails that include the CEO,the metadata for all other recipients and attendees included in those same emails and meetings are also excluded.

> [!Note]
> If a user has multiple aliases, you must enter each email address for each alias that you want to exclude.

### Terms in subject line

You can enter a list of keywords or terms that occur in the subject lines of emails and meetings that you want to exclude. All email and meetings that contain these keywords are excluded from analysis.

#### Example: Exclude terms from subject line

To exclude all emails with the keywords of “confidential,” “ACP,” and “privileged,” enter: **confidential;ACP;privileged**

### Keyword exclusion logic

* Case is ignored, so you can use upper or lower-case keywords
* Matches exact string match for subject keywords
* Does not match partial words, so you need to list each partial word as a separate term

#### Examples: Keyword exclusion logic

Term from subject line to exclude | Actual subject line | Excluded
---------|----------|---------
 legal;acquisition | Verify this is LEGAL | Yes - Case is ignored
 legal;acquisition | Is this illegal | No – Does not match partial words, and did not exclude illegal
 legal;acquisition | Acquisitions are finalized | No - Does not match partial words, and did not exclude acquisitions
 legal acquisition |Is this a legal acquisition | Yes  - Excluded legal acquisition

 > [!Note]
 > When you add subject-line terms to exclude from analysis, Workplace Analytics might not recognize uncommon compound words, especially those in languages such as Japanese or Chinese. For best results, use single words, separated by semicolons.

### Related topics

* [Workplace Analytics settings](../Use/Settings.md)
* [Workplace Analytics privacy and data access](../Privacy/Privacy-And-Data-Access.md)
