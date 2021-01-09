---

title: Introduction to attendee and meeting exclusions in Workplace Analytics 
description: Exclusion rules -- Introduction   
author: paul9955
ms.author: v-pausch
ms.topic: article
localization_priority: normal 
ms.prod: wpa
---

# Analysis settings

As an analyst in Workplace Analytics, you use Analysis settings to set up meeting exclusion rules for data analysis purposes.

You can use Workplace Analytics queries to measure work-related calendar collaboration. For this type of analysis, you want to make sure the queried data is applicable. That is, you want to include only participation in meetings that reflect actual work-related collaboration and exclude unrelated events from the data.

You can exclude events with one of the following exclusion types:

* [Meeting exclusions](meeting-exclusions-intro.md) - Exclude from analysis the data from types of meetings (such as all-day training meetings) whose inclusion might skew query results.

* [Attendee exclusions](attendee-exclusion-rules.md) - Use the responses by meeting invitees to optionally exclude them from analysis. For example, invitees who accepted a meeting invitation as "Tentative" would normally be included in analysis by default. By adding an attendee exclusion, you can explicitly exclude them. In this way, creating attendee exclusions lets you effectively redefine "meeting attendance."

> [!Note]
> These two exclusion types are not mutually exclusive. As you define a query, you can select exclusions of both types. This lets you exclude data about particular types of meetings (such as long or large meetings) while you, independently, also exclude attendee data for those who responded as "Tentative" or didn't respond to meeting invitations.

**Owners** – Workplace Analytics Analysts have full access to this page and limited Analysts have read-only access. For details, see [Assign roles to Workplace Analytics admins and analysts](../setup/assign-roles-to-wpa-admins.md).

![Analysis settings in Workplace Analytics](../images/WpA/Tutorials/analysis-settings.png)

## Related topics

* [Settings](../Use/settings.md)
* [Sources](../Use/data-sourcesv2.md)
