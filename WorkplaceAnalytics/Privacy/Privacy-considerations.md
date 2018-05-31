---
# Metadata Sample
# required metadata

title: Workplace Analytics Setup Checklist
description: This is a Checklist to introduce what is required to implement Workplace Analytics for your Organization
author: LeisaLaDell
ms.author: v-leash
ms.date: 2/16/2018
ms.topic: get-started-article
localization_priority: normal 
ms.prod: wpa
---
# Privacy settings considerations for Workplace Analytics 

This topic discusses various considerations that Workplace Analytics admins should explore when deciding on privacy settings. 

## Minimum group size

A minimum group size helps maintain employee privacy by ensuring that specific people cannot be easily identified by the attributes of the group. The default minimum group size is five. You can change the minimum group size to a level that you consider more relevant for your organization.

### The rule

The minimum-group-size setting determines what you can view in the dashboards in [Explore metrics](../Use/Explore-Metrics-Week-in-the-Life.md) and in the Solutions area. The dashboards will not display information about a group that is smaller than the minimum size that is in effect. 

The minimum-group-size rule can be stated this way: If a chart area (such as a bar in a bar chart) corresponds to a group whose size less than the minimum group size, that chart area is obfuscated. 

#### Example

In the following illustration (of a column chart), the blue-green columns on the left represent groups whose size exceeds the minimum group size. For this reason, they display real data.

The gray and white columns on the right represent groups below the minimum-group-size threshold. Therefore, they display no data. 

<img src="../Images/WpA/group-size-bars.png" alt="Bar chart with bars above and below group size threshold">

> [!Note] 
> The minimum group size rule applies to charts that display information derived from HR data. In other words, they display information about circumstances that exist in your organization -- such as managers at a specific level or employees in a particular city.  

### Exception to the rule: histogram charts

For histogram charts, the minimum-group-size rule is applied differently, in the following ways:

1. **Filter group too small: histogram is not displayed**

   If the _filter group_ from which the histogram draws its data is below minimum group size, Workplace Analytics does not display the histogram at all.

2. **Bin population too small: bin is still displayed**

   In histograms, the x-axis consists of rectangles (called "bins") that are based on average metric values, and the y-axis is determined by the number of people whose average metric value puts them in that bin. _Neither of these values reflects HR data._ For this reason, the histogram still displays data for a bin even if it contains fewer people than the minimum group value. Histogram charts can safely display this information because it is based on metrics -- on values calculated from observed behavior, _not_ on HR data. 

   Even if a bin in a histogram contained data for only one individual, the histogram still displays that data. You cannot single out this individual because you do not know what HR “group” they belong to. (In some other charts, such as column charts, an individual in a group below the threshold might be identifiable but in a histogram, the HR group to which individuals belong is the larger filter group.) You also cannot determine the precise metric value of an individual because they are in a bin with a minimum 0.5-hour range.

#### Where to find histogram charts

You see histogram charts in the following pages in Workplace Analytics:

 * On the Management and Coaching tab of the Explore page 
 * For goal setting in the Solutions area
 * To track program success on the Track page of the Solutions area

## Hash subject lines 
You can help maintain employee privacy by hiding the subject lines of meetings and emails. There are privacy and data analysis trade-offs for each scenario. The following information can help you determine whether or not you want to hide subject lines in your queries.  

When you select **Yes** for **Hash subject lines**, the subject lines are changed to a hashed value (a number generated from a string of text), which means that the text of the subject lines will not be visible in the queries you generate.   

If you hash subject lines, you can still generate keyword queries based on the subject. However, you would not be able to see a list of meetings showing the subject lines.  

#### Hash subject lines example
With **Hash subject lines** on, you could still run a meeting query with the subject line keyword “All-hands,” and (based on the attributes you include in the query) it could show data about the number of meetings, the length of meetings, the size of meetings, and so on, with that subject line. 

However, you could not get a specific list (one line item for each meeting) of all the meetings with the subject line “All-hands.” 

## Exclude calendar and email terms from analysis 
You can help maintain employee privacy and focus your analysis by excluding certain terms from analysis. Since any items you exclude will not be included in the analysis, it is important to carefully consider and balance your privacy and data analysis goals. It could adversely skew your analysis if you exclude domains, email addresses, or subject terms that frequently appear within the collaboration dataset.

The following information can help you determine what privacy settings best match your company’s policies and objectives. 

### Domains

You can enter a list of domains that you want to exclude. All email and meetings from domains listed here will excluded from analysis. 

> [!Note] 
> There exists only the option to exclude (black list) specific domains, not to include (white list) specific domains.

### Email addresses

You can enter list of email addresses that you want to exclude. _Any and all_ emails and meetings in which these email addresses are included (as both sender/recipient and attendee/invitee) will excluded from analysis. Therefore, when adding email addresses to exclude, it's important to consider all the sender/recipient and attendee/invitee implications of the exclusion. 

#### Example: Exclude email addresses

If you excluded the email address of the CEO (ceo@company.com), all meetings and emails in which the CEO is included would be removed from analysis. This means that for all meetings and emails that include the CEO, the metadata for all other recipients and attendees included in those same emails and meetings would be excluded.  

> [!Note]
> If a user has multiple aliases, you must enter each email address that you want to exclude.  

### Terms in subject line

You can enter a list of keywords or terms that occur in the subject lines of emails and meetings that you want to exclude. All email and meetings that contain these keywords will be excluded from analysis.

#### Example: Exclude terms from subject line

To exclude all emails with the terms “confidential,” “ACP,” and “privileged,” enter: confidential;ACP;privileged 

### Keyword exclusion logic

* Case is ignored, so you may use upper or lower-case terms
* Does not match multiple word terms, so you need to list each keyword as a separate term
* Does not match partial words, so you need to list each keyword as a separate term

#### Examples: Keyword exclusion logic

Term from subject line to exclude | Actual subject line	 | Excluded
---------|----------|---------
 legal;acquisition | Verify this is LEGAL | Yes - Case is ignored
 legal;acquisition | Is this illegal | No – Does not match partial words, and did not exclude illegal
 legal;acquisition | Acquisitions are finalized | No - Does not match partial words, and did not exclude acquisitions
 legal;acquisition |Is this a legal acquisition | Yes  - Excluded both legal and aquisition

 > [!Note]
 > When you add subject-line terms to exclude from analysis, Workplace Analytics might not recognize uncommon compound words, especially those in languages such as Japanese or Chinese. For best results, use single words, separated by a semicolon.

### Related topics

[Configure settings for Workplace Analytics](../Use/Settings.md)

[Workplace Analytics privacy and data access](../Overview/Privacy-And-Data-Access.md)
