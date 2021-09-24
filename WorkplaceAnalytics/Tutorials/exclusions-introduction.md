---

title: Introduction to exclusion rules in Workplace Analytics 
description: Learn about meeting and attendee exclusion rules in Workplace Analytics for Microsoft Viva Insights
author: madehmer
ms.author: v-mideh
ms.topic: article
ms.localizationpriority: medium 
ms.prod: wpa
manager: scott.ruble
audience: Admin
---

# Exclusion rules introduction

As an analyst, you use Analyst settings to set up meeting and attendee exclusion rules for data analysis purposes.

You can use Microsoft Viva Insights in Microsoft Teams and in Workplace Analytics to analyze organizational trends, such as work-related calendar collaboration. For this type of analysis, you want to make sure the data is applicable. That is, you want to include only participation in meetings that reflect actual work-related collaboration and exclude unrelated events from the data.

You can exclude events with one of the following exclusion types:

* [Meeting exclusions](meeting-exclusions-intro.md) - Exclude types of meetings from analysis (such as all-day training meetings) where their inclusion might skew query results.

* [Attendee exclusions](attendee-exclusion-rules.md) - Use the responses by meeting invitees to optionally exclude them from analysis. For example, invitees who accepted a meeting invitation as "Tentative" would normally be included in analysis by default. By adding an attendee exclusion, you can explicitly exclude them. In this way, creating attendee exclusions lets you effectively redefine "meeting attendance."

**Owners** – Viva Insights and Workplace Analytics Admins and Analysts have full access and limited Analysts have read-only access to exclusion settings. For details, see [Assign roles](../setup/assign-roles-to-wpa-admins.md).

![Analyst exclusion settings](../images/WpA/Tutorials/analyst-exclusion-settings.png)

## Notes

* **Exclusion types are independent** &ndash; These two exclusion types are not mutually exclusive. As you define a query, you can select exclusions of both types. This lets you exclude data about particular types of meetings (such as long or large meetings) while you, independently, also exclude attendee data for those who responded as "Tentative" or didn't respond to meeting invitations.

* **Rules are applied only in Explore and in Query designer** &ndash; Analysts in your organization might have created meeting or attendee exclusion rules during the set up of Workplace Analytics. After these rules are created, they are applied only in [Explore the stats](../use/explore-intro.md) data and in [queries](query-basics.md). See Q1 in [Application of meeting exclusion rules](meeting-exclusion-concept.md#application-of-meeting-exclusion-rules). Exclusion rules are _not_ applied to the data shown in **Data sources**, including **Office 365 data**.

## Related topics

* [Control settings](../Use/settings.md)
* [Data sources](../Use/data-sourcesv2.md)
