---

title: Introduction to attendee and meeting exclusions in Workplace Analytics 
description: Exclusion rules -- Introduction   
author: paul9955
ms.author: v-pausch
ms.topic: article
localization_priority: normal 
ms.prod: wpa
---

# Attendee and meeting exclusion rules in Workplace Analytics

You can use Workplace Analytics queries to measure work-related calendar collaboration. When you do this, you want to make sure that the data being queried is applicable. That is, you want to include only participation in meetings that reflects actual work-related collaboration. This means that you might need to exclude some events that would otherwise be reflected in the data. 

You exclude events by using two exclusion types: meeting exclusions and attendee exclusions: 

 * **Meeting exclusion**. Exclude from analysis the data from types of meetings (such as all-day training meetings) whose inclusion might skew query results. For more information, see [Meeting exclusions](meeting-exclusions-intro.md). 

 * **Attendee exclusion**. Exclude from analysis data about meeting invitees, by their responses. For example, you can explicitly exclude (or include) invitees who tentatively accepted a meeting invitation. Creating attendee exclusions lets you effectively redefine "meeting attendance." If you add no attendee exclusions, meeting attendance means only one thing: that a person accepted the meeting invitation. But by creating an attendee exclusion, you can change that definition to also include either or both of the invitee actions "tentative" and "no response." For more information, see [Attendee exclusions](attendee-exclusion-rules.md).  

> [!Note]
> These two exclusion types are not mutually exclusive. As you define a query, you can select exclusions of both types. This lets you exclude data about particular types of meetings (such as long or large meetings) while you, independently, also exclude data about attendees who responded as "Tentative" or didn't respond to meeting invitations.  