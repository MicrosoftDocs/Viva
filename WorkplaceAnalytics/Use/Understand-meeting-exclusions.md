---

title: Understand meeting exclusions in Workplace Analytics
description: How to use meeting exclusions in Workplace Analytics 
author: madehmer
ms.author: v-pausch
ms.topic: article
localization_priority: normal 
ms.prod: wpa
---

# Meeting exclusions in Workplace Analytics

Workplace Analytics uses activities stored in a person’s Office 365 email and calendar to reveal internal and external collaboration trends. However, a person’s calendar and email can contain a diverse set of activities (such as personal meetings, work-related social activities, all-day training meetings, and so forth) that are not relevant to work-related collaboration, and if included in the metrics, can skew query results.

Analysts can use the **Meeting exclusions** feature to create custom meeting exclusions that help ensure query results accurately represent relevant meeting norms within their company. Or, analysts may choose to use the default meeting exclusions that exclude a set of meetings that would commonly fall outside relevant collaboration for analysis.

The following topics offer a framework to use when determining which meeting exclusions are relevant for your company, how to validate the accuracy of meeting query results, and how to create and validate custom meeting exclusions.

## Default meeting exclusions

By default, Workplace Analytics excludes the following types of meetings from query results, as they are not likely to represent relevant workplace meetings:

* Meetings with only one attendee
* Meetings equal to or longer than eight hours
* Meetings with 250 or more attendees
* Cancelled Meetings

> [!Note]
> To respect user privacy, meetings marked as private and/or confidential are always excluded from meeting query calculations.

## Before in-depth analysis, validate default meeting exclusions

Before performing in-depth collaboration analysis, we recommend that analysts validate whether the default meeting exclusions accurately reflect your company’s meeting culture.

If not, by using the **Meeting exclusions** feature, you can define and customize what kind of meetings you want to exclude from query calculations.

In this phase, you will run two meeting queries: an "all meetings" query that lists all the meetings not excluded using the default settings, and a "default meetings excluded" query, which lists the meetings excluded by the default settings. Then, you will review the query results for relevance and meeting trends.

### Step one: Run meeting queries

In this step, generate a list of both included and excluded meetings that you will use to determine if the default exclusions are representative of your company’s meeting culture. It is not necessary or advisable to attempt 100% accuracy in your review. In this case, identifying general relevance is the goal.

**Related topics**

[To create and run an “All meetings default” query using default exclusions](Create-custom-meeting-exclusions-rules.md#create-and-run-an-all-meetings-default-query-using-default-meeting-exclusions) 

[To create and run a “Meetings excluded default” query](Create-custom-meeting-exclusions-rules.md#create-and-run-a-meetings-excluded-default-query) 

### Step two: Review query results for trends and relevance

In this step, review the included and excluded meeting results for relevance and company collaboration trends. Reviewing for trends can be a subjective exercise, more art than science. Here again, it’s best to focus on relevance in general trends, rather than strive for 100% accuracy.

**Tips for reviewing meeting query results**

* **Prioritize review based on potential impact** – Depending on the size of your organization and data set, there will likely be too many meetings to review them all, so prioritize to focus your review on meetings that have a large impact. For example: meetings with the longest duration, and meetings with the greatest number of attendees.

* **Account for company culture** – Examine the default excluded meetings in light of your company’s meeting culture. For example, if your company has weekly “all hands” meetings of 50 attendees or more, or has regular meetings of 8 hours or longer, then using the default exclusions would give non-representative results, and so you would likely decide to use a custom meeting exclusions.

  **Some questions to consider**
  Should you always include or exclude certain meeting types: 
  * based on meeting subject keywords?
  * based on number of attendees or duration of meeting?
  * based on group or locale?
  
* **Document your observations** – As you review the meetings, document your insights and observations about trends in the data.

## Business scenario - Review meeting query results for relevance

### Review excluded meetings

An analyst at Company A is reviewing results of the **Default meetings excluded** query and notices the following:

Meeting ID | Subject | Attendees | Duration
---------|---------- |---------|---------
 1000 | Quarterly Client Budget Review | 251 attendees |6 hours
 2000 | Bob’s Workout at Gym | 1 attendee | 1.5 hours

**Default meetings excluded**

* Meeting 1000 was excluded based on the default settings for number of attendees. However, based on the meeting subject and the potential for high person-hours impact, the analyst may conclude that this meeting is work-relevant and should be included. Also, if there are other, similar meetings, the analyst could decide to create custom meeting exclusion rules with a higher attendee threshold.
* Meeting 2000 was excluded by default due to only having 1 attendee, and based on the meeting subject and should continue to be excluded.

**Related topic** 

[Create and run a “Meetings excluded default” query](Create-custom-meeting-exclusions-rules.md#create-and-run-a-meetings-excluded-default-query) 

### Review included meetings

Our analyst is now reviewing the results of the **All meetings default settings** query, and notices the following:

**All meetings default settings**

Meeting ID | Subject | Attendees | Duration
---------|----------|--------- |---------
 3000 | Bob’s Surprise Party | 249 attendees | 7.5 hours
 4000 | FY17 Sales Strategy Meeting | 8 attendees | 2 hours


* Meeting 3000 was included by default based on the default settings for number of attendees. However, based on the meeting subject, the analyst may conclude that this meeting is not work-relevant and should be excluded. This meeting could be excluded using relevant keywords in the subject line such as "Party".
* Meeting 4000 was included, and based on the meeting subject should continue to be included.

## Choose default or custom meeting exclusions

Once you’ve reviewed the meeting query results for relevance and identified your company’s collaboration trends, you can use those insights to determine if you will use the default meeting exclusions, or create custom exclusions.
If you decide to use the default settings, no further action is required and you are ready to create queries and analyze collaboration trends.
If you decide to create custom meeting exclusion rules, continue to the **Create and validate custom exclusions** phase.

## Create and validate custom exclusions

In this phase, you will create the custom meeting exclusions that you want, and then review and validate their relevance using the same steps that you used to validate the default meeting exclusions.

### Step one: Create custom meeting exclusions

Based on your review, create a set of custom meeting exclusion rules that are relevant for your company.

### Step two: Create a custom meeting excluded query

Using the same process that you used to create the “default meetings excluded” query, create a query that gives you a list of the meetings excluded by your custom meeting exclusion rules.

### Step three: Run and review queries

Run and review meeting queries using your custom meeting exclusion rules, and then, as you did for the default exclusions, review the results for trends and relevancy.

**Related topic**

[Create custom meeting exclusions](../Use/Create-custom-meeting-exclusions-rules.md)
