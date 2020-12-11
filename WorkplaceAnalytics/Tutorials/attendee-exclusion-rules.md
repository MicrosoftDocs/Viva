---

title: Attendee exclusion rules in Workplace Analytics 
description: Attendee exclusion rules -- Introduction and walkthrough   
author: paul9955
ms.author: v-pausch
ms.topic: article
localization_priority: normal 
ms.prod: wpa
---

# Attendee exclusions in Workplace Analytics

Workplace Analytics [queries](query-basics.md) let you measure work-related calendar collaboration. These measurements are most accurate when they include data that reflects genuine collaboration. 

For example, the data should not include meetings that schedule personal time, or count an invitee as "present" at a meeting when they weren't actually there. Workplace Analytics lets you exclude these kinds of events so that they don't skew your data. (For information about _meeting exclusions_, see [Meeting exclusions in Workplace Analytics](meeting-exclusions-intro.md).)

This article describes a different exclusion type, the _attendee exclusion_. You use attendee exclusions to exclude from analysis data about meeting invitees; you base these exclusions on the responses that the invitees made to meeting invitations.

## Responses to meeting invitations

Creating attendee exclusions lets you effectively redefine meeting attendance in Workplace Analytics analyses. By default, "attending a meeting" means that a person did not decline the meeting invitation.

By creating an attendee exclusion, you can change that definition to also include either or both of the invitee actions "tentative" and "no response."

### Tentative

In some countries, it is a cultural practice not to "decline" a meeting; rather, a "Tentative" response means "I won’t be attending but I still want to keep this meeting on my calendar." As an analyst, you can exclude invitees who tentatively accepted a meeting invitation.

Using the "accepted as tentative" exclusion would mean that a meeting invitee who tentatively accepted is not counted as an attendee to that particular meeting.

### No response

Sometimes, meeting invitees do not respond to meeting invitations. Using the "did not respond" exclusion would mean that a meeting invitee who did not respond is not counted as an attendee to that particular meeting.

## Create an attendee exclusion

**Role**: analyst, limited analyst

1. Open [Workplace  Analytics](https://workplaceanalytics.office.com/). If prompted, enter your work credentials.

2.	Select **Settings** > **Analysis settings** to open the **Exclusions** page.

3. Select **Attendee exclusion**.

4. Select **Add exclusion**. 

5. On the **Analysis settings** > **Exclusions** > **New exclusion** page, for **Exclusion type**, select **Attendee exclusion**:

   ![Meeting response options](../images/wpa/tutorials/select-attendee-exclusion.png)

6. Type a name for your exclusion, and, optionally, a description, and then select **Next**. 

7. Choose the types of invitees whose data you want to exclude from analysis: those who did not respond to meeting invitations, those who responded as **Tentative** to meeting invitations, or both types of invitees:

   ![Exclude these invitees](../images/wpa/tutorials/exclude-invitees-who-have-70.png) 

   The **Potential impact of exclusion** area shows the percentage and total number of potential attendees at meetings whose data will be excluded from analysis if you publish and use this exclusion rule.

8. Optionally, select **Apply this exclusion for metrics in Explore the stats**. Selecting this option does not automatically affect any existing queries. It makes this exclusion appear as the default for new queries, and it affects only the data shown in [Explore the stats](../use/explore-intro.md).

9. Select **Publish**. Your new exclusion rule will now be available to analysts who create and run queries.

## Select an attendee exclusion for a query

**Role**: analyst, limited analyst

1. In [Workplace  Analytics](https://workplaceanalytics.office.com/), select **Analyze** > **Queries**.

2. Create a query; for example, a **Meeting** query.

3. Select the **Exclusions** box: 

   ![Exclusions box](../images/wpa/tutorials/meeting-exclusions.png) 

   Which opens the **Exclusions** pane:

   ![Exclusions pane](../images/wpa/tutorials/exclusions-pane.png) 

4. Make a selection for **Attendee exclusions**:

  * Select the name of an attendee exclusion to use that exclusion in this query. In the preceding illustration, an attendee exclusion called "Not-responded" is currently selected. 
  * Select **Clear value** to remove all attendee exclusions from this query. 
