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

 * **Attendee exclusion**. Use the responses by meeting invitees to optionally exclude them from analysis. For example, invitees who accepted a meeting invitation as "Tentative" would normally be included in analysis by default; now, you can explicitly exclude them. Creating attendee exclusions lets you effectively redefine "meeting attendance." 
 
    If you add no attendee exclusions, meeting attendance means any of the following: that a person accepted the meeting invitation, did not respond to it, or accepted it as "Tentative." But by creating an attendee exclusion, you can change that definition to also include either or both of the invitee actions "Tentative" and "no response." For more information, see [Attendee exclusions](attendee-exclusion-rules.md).  

> [!Note]
> These two exclusion types are not mutually exclusive. As you define a query, you can select exclusions of both types. This lets you exclude data about particular types of meetings (such as long or large meetings) while you, independently, also exclude attendee data for those who responded as "Tentative" or didn't respond to meeting invitations.  