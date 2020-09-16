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

For example, the data should not include meetings that schedule personal time, or count an invitee as "present" at a meeting when they weren't actually there. Workplace Analytics lets you exclude these kinds of events so that they don't skew your data. 

For information about _meeting exclusions_, see [Meeting exclusions in Workplace Analytics](meeting-exclusions-intro.md). 

This article describes the _attendee exclusion_. Use attendee exclusions to exclude from analysis data about meeting invitees; you base these exclusions on the responses that the invitees made to meeting invitations. 

By default, meeting attendance means one thing: that a person responded to the meeting invitation with **Accept**. But attendees can respond in other ways: 

* Decline the meeting.
* Accept the meeting invitation as **Tentative**.
* Make no response to the meeting invitation.

## Exclude "Tentative" responses

You can explicitly exclude (or include) invitees who tentatively accepted a meeting invitation. Creating attendee exclusions lets you effectively redefine "meeting attendance." If you add no attendee exclusions, meeting attendance means only that a person accepted the meeting invitation. 

By creating an attendee exclusion, you can change that definition to also include either or both of the invitee actions "tentative" and "no response." For example, using an attendee exclusion for the **Tentative** response would mean that a meeting invitee who tentatively accepted is not counted as an attendee to that particular meeting. 

## Exclude cases of no response

Sometimes, meeting invitees do not respond to meeting invitations. There is more than one way to do this. The following actions are all interpreted as "did not respond":

 * The invitee took no action; they actually did not respond to the invitation.
 * The invitee selected **Accept** and also **Do not send a response**.
 * The invitee selected **Tentative** and also **Do not send a response**.
 * The invitee selected **Decline** and also **Do not send a response**.
   
The following screenshot shows the **Do not send a response** option for the **Tentative** meeting response: 
   
   ![Meeting response options](../images/wpa/tutorials/response-options.png)

## Create an attendee exclusion

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

8. Optionally, select **Apply this exclusion for metrics in Explore page**. This option does not automatically affect any queries; it affects only the data that is displayed in the Workplace Analytics [Explore](../use/explore-intro.md) pages. 

9. Select **Publish**. Your new exclusion rule will now be available to analysts who create and run queries. 

## Select an attendee exclusion in a query

**Role**: analyst, limited analyst

1. In [Workplace  Analytics](https://workplaceanalytics.office.com/), open the **Queries** page.

2. Open a query; for example, a **Meeting** query:

   ![Meeting query](../images/wpa/tutorials/meeting-query.png) 

3. Click the **Exclusions** box: 

   ![Exclusions box](../images/wpa/tutorials/exclusions-box.png) 

   This opens the **Exclusions** pane:

   ![Exclusions pane](../images/wpa/tutorials/exclusions-pane.png) 

4. Make a selection for **Attendee exclusions**:

  * Select the name of an attendee exclusion to use that exclusion in this query. In the preceding illustration, an attendee exclusion called "Not-responded" is currently selected. 
  * Select **Clear value** to remove all attendee exclusions from this query. 


 

