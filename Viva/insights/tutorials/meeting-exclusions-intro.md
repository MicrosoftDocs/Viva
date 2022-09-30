---
ROBOTS: NOINDEX,NOFOLLOW
title: Meeting exclusion rules introduction
description: Introduction to meeting exclusion rules in Microsoft Viva Insights  
author: madehmer
ms.author: helayne
ms.topic: conceptual
ms.localizationpriority: medium 
ms.collection: viva-insights-advanced 
ms.service: viva 
ms.subservice: viva-insights 
search.appverid: 
- MET150 
manager: scott.ruble
audience: Admin
---

# Meeting exclusions in Viva Insights

Microsoft Viva Insights uses email and calendar activities that are stored in a person's Microsoft 365 account to reveal internal and external collaboration trends. However, a person's calendar and email can contain a diverse set of activities (such as personal meetings, work-related social activities, all-day training meetings, and so forth) that are not relevant to work-related collaboration, and, if included in the metrics, would skew query results.

You use meeting exclusion rules to exclude particular types of collaboration data from analysis. This data can be about meetings that were scheduled or about attendee responses to those meetings. See [Select exclusion type](/viva/insights/tutorials/meeting-exclusion-concept?toc=/viva/insights/use/toc.json&bc=/viva/insights/breadcrumb/toc.json#select-exclusion-type).

>[!Note]
>There is a problem with meetings that have more than 250 participants. For more information, see [Meeting exclusion rules: Large-meeting limitation](/viva/insights/tutorials/meeting-exclusion-250?toc=/viva/insights/use/toc.json&bc=/viva/insights/breadcrumb/toc.json).

Meeting exclusion rules are used in Viva Insights to help ensure that query results accurately represent relevant meeting norms within the organization. <!-- Organizations can also use these rules to promote privacy by excluding from analysis meetings that are of a sensitive nature.  -->

### Video: Learn about meeting exclusion rules

<!-- FOR THIS VIDEO LINK, VERIFY THE EMBED/SCREEN SETTINGS. 
WE USE THE FOLLOWING ONES IN OTHER PLACES: 

<iframe allowfullscreen="" mozallowfullscreen="" webkitallowfullscreen=""></iframe>
-->

<iframe src="https://player.vimeo.com/video/434889700" width="580" height="512" frameborder="0" allow="autoplay; fullscreen" allowfullscreen></iframe>

Viva Insights provides a default meeting exclusion rule that excludes a set of meetings that would commonly fall outside of relevant collaboration for analysis. Analysts can also use the meeting exclusion feature to create custom meeting exclusion rules.

To learn how to create and use meeting exclusion rules, see the following:  

* [Meeting exclusion rule walkthroughs](/viva/insights/tutorials/meeting-exclusion-rules?toc=/viva/insights/use/toc.json&bc=/viva/insights/breadcrumb/toc.json) describe how to [View meeting exclusion rules](/viva/insights/tutorials/meeting-exclusion-rules?toc=/viva/insights/use/toc.json&bc=/viva/insights/breadcrumb/toc.json#to-view-meeting-exclusion-rules), [Create a meeting exclusion rule](/viva/insights/tutorials/meeting-exclusion-rules?toc=/viva/insights/use/toc.json&bc=/viva/insights/breadcrumb/toc.json#create-a-meeting-exclusion-rule), [Edit a draft rule](/viva/insights/tutorials/meeting-exclusion-rules?toc=/viva/insights/use/toc.json&bc=/viva/insights/breadcrumb/toc.json#edit-a-draft-rule), [Select which rule to use](/viva/insights/tutorials/meeting-exclusion-rules?toc=/viva/insights/use/toc.json&bc=/viva/insights/breadcrumb/toc.json#select-which-rule-to-use), [Duplicate a rule](/viva/insights/tutorials/meeting-exclusion-rules?toc=/viva/insights/use/toc.json&bc=/viva/insights/breadcrumb/toc.json#duplicate-a-rule), and [Archive a rule](/viva/insights/tutorials/meeting-exclusion-rules?toc=/viva/insights/use/toc.json&bc=/viva/insights/breadcrumb/toc.json#archive-a-rule).

* [Meeting exclusion rule concepts and tools](/viva/insights/tutorials/meeting-exclusion-concept?toc=/viva/insights/use/toc.json&bc=/viva/insights/breadcrumb/toc.json): Describes screen elements and concepts whose understanding can help you create and use meeting exclusion rules.

## Related topics

[Meeting exclusion rule limitation for large meetings](/viva/insights/tutorials/meeting-exclusion-250?toc=/viva/insights/use/toc.json&bc=/viva/insights/breadcrumb/toc.json)
