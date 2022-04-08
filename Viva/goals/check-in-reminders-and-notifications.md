---
title: Check-in reminders and notifications
ms.reviewer: 
ms.author: vsreenivasan
author: ms-vikashkoushik
manager: 
audience: Admin
f1.keywords:
- NOCSH
ms.topic: article
ms.service: viva
ms.subservice: viva-goals
localization_priority: Priority
ms.collection:  
- m365initiative-viva-goals  
search.appverid:
- MET150
description: "Learn how to customize reminder notifications"
---

# Check-in reminders and notifications

> [!IMPORTANT] 
> Viva Goals is currently available only for private preview customers. The features described here are subject to change. [Learn more about Viva Goals.](https://go.microsoft.com/fwlink/?linkid=2189933) 

## What is a check-in rhythm? 

Regular check-ins are a key part of an effective OKR implementation. OKRs are closely aligned, and therefore will reflect inaccuracies if they aren't updated regularly. That’s why it’s helpful to send gentle reminders to your team to check in on their OKRs. Setting a cadence to remind teams and users to make check-ins be referred to as the check-in rhythm. 

Notifications remind your team to check in regularly. By default, Viva Goals sends a notification to all team members every Monday at 9:00 AM in the user’s time zone, but the notifications can be customized to fit your business needs. 

### Setting a check-in rhythm

In this section you can set:

1. Frequency (every one, two, or three weeks, or monthly)

2. Days on which notifications are sent. 

3. Time at which notifications are sent.

4. Disable notifications for OKRs that have had check-ins in the past X days (select number of days)

5. Admins or managers of a team can control whether the subteams reporting to their team can set their own check-in rhythm or should follow the parent team's cadence. 

    They can decide if the cadence they're setting should be cascaded down to the reporting teams, or is confined just to their team. 

For instance, the Chief of Staff sets a cadence to notify the users belonging to her team every Monday at 9AM PST. She can choose to set the same rhythm across departments in the organization, wherein all the users of Marketing, Product, Sales, Engineering, and Customer Success teams will receive a notification for check-ins every Monday at 9AM PST. 

The Org Admin can control whether the teams reporting to her can set their own check-in rhythm or should follow the parent team's cadence. The aforementioned situation is a classic example of the subteams adhering to the parent team's cadence. 

The two options that determine the cadence and cascading of the cadence are: 

1. Allow teams to change their rhythm anytime.

2. When saving, apply this schedule to teams. 

> [!NOTE]
> These options are check boxes that need to be ticked, as you see fit.

Let's consider the following scenarios to better understand the usage of these configurations to set a check-in rhythm. 

1. The department head, say Chief of Staff, is setting a cadence for the People Operations department to receive notifications every month on the first Friday at 9AM PST.  The Chief of Staff wants the subteams reporting into her to continue having a cadence of their own (preferably, a weekly cadence). Therefore, she won't cascade this cadence down to the reporting teams, and will let each team set their own check-in rhythm. 

    :::image type="content" source="../media/goals/goals-setting-cadence.png" alt-text="Image for setting cadence":::

2. The Head of Marketing is setting a bi-weekly cadence for the Marketing team to receive notifications on every Monday once every two weeks at 9AM PST. The Head of Marketing wants his reporting teams (say, Product Marketing, Demand Generation, and Customer Marketing) to have their own cadence, but highly recommends starting them with the same cadence as the marketing team. In this case, the cadence will cascade down the teams, however, the teams can change this schedule at any given point in time. 

    :::image type="content" source="../media/goals/goals-checkin-bi-weekly cadence.png" alt-text="Image of setting cadence bi-weekly":::

3. The VP of Sales wants her team to have a weekly check-in cadence, and is setting a rhythm to receive notifications every Wednesday at 9AM PST. She wants all the subteams reporting into her to follow the same cadence, and doesn't want them to have a cadence of their own, to ensure everyone is caught upto speed every week, and is on the same page. Therefore, she'll set a cadence, cascade it cadence down to all her reporting teams, and not let them change this rhythm.

    :::image type="content" source="../media/goals/goals-weekly-check-in-cadence.png" alt-text="Images for weekly check-in cadence":::

Team Owners and Team Admins can create a custom cadence for reminders for their departments and teams in **Admin -> Team Settings**. These cadences can differ from the organization-level cadence. 

If teams have to follow the parent team's check-in rhythm, the team owners and/or team admins won't be able to change the schedule.

   :::image type="content" source="../media/goals/goals-checkin-rhythm-team settings.png" alt-text="Image for check-in rhythm":::

Once the updates have been scheduled, you'll receive the notification in one of the following ways:

- If a Slack or MS Teams integration has been enabled, the notifications will be sent through one of those platforms. 

- If the iOS or Android App has been installed, you'll receive a push notification.

- If no integrations have been set up, Viva Goals will send a reminder as an email. 

## Check-ins for single and multiple owners

If there's just one owner or multiple owners assigned to an OKR and you would want a user within the organization to check in and update the progress of the OKR, you can use the ‘check-in responsibility’ feature. The check-in owner will be able to check in on the OKR (manual check-in) and set up a data link on the OKR (to auto-check-in). This user will be receiving the check-in reminders. If there are multiple owners, this will prevent all of the owners from receiving reminders, only the user set as 'check-in responsible owner' will receive the reminders.

Steps to assign responsibility for check-ins:

- Sign in to Viva Goals and select the **+** button on the top panel to create a new OKR.

- Once you enter the objective/ Key Result and want to share it with another individual, choose owners from the ‘Owner’ option. Here you can assign multiple owners for the OKR.

- Once you assign an owner, select the user who will be responsible for making check-ins from the ‘Who is responsible for making check-ins?’ drop-down.

- Once you make the selection, the user will  start receiving the check-in reminders.

> [!NOTE]
> By default, the owner (the first owner in the case of multiple owners) is set as the person responsible for check-in and users need not explicitly choose unless necessary.

:::image type="content" source="../media/goals/goals-check-in.gif" alt-text="Image of assign responsibility for check-ins":::

Learn more about [check-ins and the continuous feedback](https://help.ally.io/en/articles/2107055-check-ins-and-feedback) system.

### FAQs:

### How to set who receives the Nudge for multiple-owned OKRs?

If an OKR has multiple owners, the Nudge notification is sent out to the Check-in owner only.
For example, Customer Success VP and Engineering VP co-own this OKR while Engineering VP is set as the Check-in owner.

:::image type="content" source="../media/goals/goals-nudge-for-multiple-owned-OKRs.png" alt-text="Image of Nudge for multiple-owned OKRs":::

Clicking on Nudge will open the modal where the Engineering VP will be notified as they're the Check-in owner for this OKR.

:::image type="content" source="../media/goals/goals-nudge-engineering-vp.png" alt-text="Image of Nudge for Engineering VP":::


### Notifications for comments

Viva Goals allows you to add comments on OKRs and check-ins to interact with stakeholders. You can also use @mention to tag certain users. Users will receive notifications for comments in the below cases:

1. When a comment is added on an OKR they own.

2. The user has been mentioned in a comment.

The notifications will be received in one of the following ways:

1. Email

2. Slack (if enabled)

3. Discord (if enabled) 