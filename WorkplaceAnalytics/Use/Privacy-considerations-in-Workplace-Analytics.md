---
# Metadata Sample
# required metadata

title: Workplace Analytics Setup Checklist
description: This is a Checklist to introduce what is required to implement Workplace Analytics for your Organization
author: LeisaLaDell
ms.author: v-leash
ms.date: 2/16/2018
ms.topic: get-started-article
ms.prod: wpa
---
# Privacy settings considerations for Workplace Analytics 

[[INTRO CONTENT PLACEHOLDER]]

## Minimum group size
A minimum group size helps maintain employee privacy by ensuring that specific people are not easily identified by the attributes of the group. 

The minimum group size setting determines the minimum group size you can view in the dashboards in [Explore metrics](../Use/Explore-Metrics-Week-in-the-Life.md). The dashboards will not display information about a group that is smaller than the minimum you set. 

The default minimum group size is five. You can increase the minimum to be relevant for your organization. 

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

> [!NOTE]
> Currently, there is only the option to exclude (black list) specific domains, not to include (white list) specific domains.

### Email addresses
You can enter list of email addresses that you want to exclude. _Any and all_ email and meetings in which these email addresses are included (as both sender/recipient and attendee/invitee) will excluded from analysis. Therefore, when adding email addresses to exclude, it's important to consider all the sender/recipient and attendee/invitee implications of the exclusion. 

### Exclude email address example
If you excluded the email address of the CEO (ceo@company.com), all meetings and emails in which the CEO is included would be removed from analysis. Meaning, for all meeting and emails that include the CEO, the metadata for all other recipients and attendees included in those same emails and meetings would be excluded.  

> [!NOTE]
> If a user has multiple aliases, you must enter each email address that you want to exclude.  

### Terms from subject line
You can enter a list of keywords or terms that occur in the subject lines of emails and meetings that you want to exclude. All email and meetings in which contain these keywords will excluded from analysis.

Exclude terms from subject line example
If you wanted to exclude all emails with the terms “confidential,” “ACP,” and “privileged,” you would enter: confidential;ACP;privileged 

#### Keyword exclusion logic
* Case is ignored, so you may use upper or lower-case terms
* Does not match multiple word terms, so you need to list each keyword as a separate term
* Does not match partial words, so you need to list each keyword as a separate term

#### Keyword exclusion logic examples


Column A | Column B | Column C
---------|----------|---------
 A1 | B1 | C1
 A2 | B2 | C2
 A3 | B3 | C3

Term from subject line to exclude	Actual subject line	Excluded
legal;acquisition	Verify this is LEGAL 	Yes - Case is ignored
legal;acquisition	Is this illegal	No – Does not match partial words, and did not exclude illegal
legal;acquisition	Acquisitions are finalized	No - Does not match partial words, and did not exclude acquisitions
 legal;acquisition	 Is this a legal acquisition	 Yes  - Excluded both legal and aquisition

 > [!NOTE]
>When adding the subject line terms to exclude from analysis, Workplace Analytics may not recognize uncommon compound words, especially those in other languages such as Japanese or Chinese. For best results, use single words, separated by a semicolon.

### Related topics 
[[settings]]

[[Privacy]]
