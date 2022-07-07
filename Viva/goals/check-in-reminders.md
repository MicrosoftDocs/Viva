---
title: Configure check-in reminders and notifications
ms.reviewer: 
ms.author: ranjaliroy
author: ranjali-MS
manager: 
audience: Admin
f1.keywords:
- NOCSH
ms.topic: article
ms.service: viva
ms.subservice: viva-goals
ms.localizationpriority: medium
ms.collection:  
- Strat_SP_modern
- M365-collaboration
- m365initiative-viva-goals  
search.appverid:
- MET150
description: "Learn how you can set up check-in reminders and notifications in Viva Goals"
---

# What is a check-in rhythm? 

> [!IMPORTANT]
> Viva Goals is currently available only for private preview customers, and only in English. The features described here are subject to change. Viva Goals is only being released to WW tenants. It isn't being released to GCC, GCC High, or DoD environments. [Learn more about Viva Goals.](https://go.microsoft.com/fwlink/?linkid=2189933)

Regular check-ins are a key part of an effective OKR implementation. OKRs are closely aligned, and therefore will reflect inaccuracies if they aren't updated regularly. To avoid such inaccuracies, it’s helpful to send gentle reminders to your team to check in on their OKRs. Setting a cadence to remind teams and users to make check-ins is referred to as the check-in rhythm.

Notifications remind your team to check in regularly. By default, Viva Goals sends a notification to all team members every Monday at 9:00 AM in the user’s time zone, but the notifications can be customized to fit your business needs. 

## Setting a check-in rhythm

In this section you can set:

- Frequency (every one, two, or three weeks, or monthly)

- Days on which notifications are sent 

- Time at which notifications are sent

- Disable notifications for OKRs that have had check-ins in the past X days (select number of days)

Admins or managers of a team can control whether the subteams reporting to their team can set their own check-in rhythm or should follow the parent team's cadence. They can decide if the cadence they're setting should be cascaded down to the reporting teams, or is confined just to their team. 

For instance, the Chief of Staff sets a cadence to notify the users belonging to their team every Monday at 9AM PST. They can choose to set the same rhythm across departments such as Marketing, Product, Sales, Engineering, and Customer Success in the organization. Once set, all the users belonging to these teams will receive a notification for check-ins every Monday at 9AM PST. 

The Org Admin can control whether the teams reporting to them can set their own check-in rhythm or should follow the parent team's cadence. The aforementioned situation is a classic example of the subteams adhering to the parent team's cadence. 

The two options that determine the cadence and cascading of the cadence are: 

- Allow teams to change their rhythm anytime 

- When saving, apply this schedule to teams 

> [!NOTE]
> These options are check boxes that need to be ticked, as you see fit. 

Let's consider the following scenarios to better understand the usage of these configurations to set a check-in rhythm. 

- The department head, say Chief of Staff, is setting a cadence for the People Operations department to receive notifications every month on the first Friday at 9AM PST. The Chief of Staff wants the subteams reporting into them to continue having a cadence of their own (preferably, a weekly cadence). Therefore, they won't cascade this cadence down to the reporting teams and will let each team set their own check-in rhythm. 

   :::image type="content" source="../media/goals/teams-own-cadence.png" alt-text="Subteams follow their own cadence." lightbox="../media/goals/teams-own-cadence.png":::

- The Head of Marketing is setting a bi-weekly cadence for the Marketing team to receive notifications on every Monday once every two weeks at 9AM PST. The Head of Marketing wants his reporting teams (say, Product Marketing, Demand Generation, and Customer Marketing) to have their own cadence, but highly recommends starting them with the same cadence as the marketing team. In this case, the cadence will cascade down the teams; however, the teams can change this schedule at any time. 

   :::image type="content" source="../media/goals/teams-partial-own-cadence.png" alt-text="Subteams partially follow their own cadence." lightbox="../media/goals/teams-partial-own-cadence.png":::

- The VP of Sales wants their team to have a weekly check-in cadence and is setting a rhythm to receive notifications every Wednesday at 9AM PST. To ensure everyone is on the same page, they want all the subteams reporting into them to follow the same cadence, rather than each subteam having a cadence of its own. Therefore, they'll set a cadence, cascade it down to all their reporting teams, and not let them change this rhythm.

   :::image type="content" source="../media/goals/teams-same-cadence.png" alt-text="All the subteams follow the same cadence of the parent team." lightbox="../media/goals/teams-same-cadence.png":::

Team Owners and Team Admins can create a custom cadence for reminders for their departments and teams in Admin > Team Settings. These cadences can differ from the organization-level cadence. 

If teams have to follow the parent team's check-in rhythm, the team owners, and/or team admins won't be able to change the schedule. 

:::image type="content" source="../media/goals/subteams-match-parent-cadence.png" alt-text="Subteams won't be able to change the schedule if they are configured to follow the parent team's cadence." lightbox="../media/goals/subteams-match-parent-cadence.png":::

Once the updates have been scheduled, you'll receive the notification in one of the following ways:

- If a Slack or MS Teams integration has been enabled, the notifications will be sent through one of those platforms. 

- If the iOS or Android App has been installed, you'll receive a push notification.

- If no integrations have been set up, Viva Goals will send a reminder as an email. 

## Check-ins for single and multiple owners

For OKRs having single or multiple owners, you can decide which user in the organization is responsible for making check-ins use the ‘check-in responsibility’ feature. The check-in owner will be able to check in the OKR (manual check-ins) and set up a data link on the OKR (for auto check-ins). This user will be receiving the check-in reminders. In the case of multiple owners, this will prevent all of the owners from receiving reminders. Only the user set as 'check-in responsible owner' will receive the reminders.

### Steps to assign responsibility for check-ins:

1. Log in to Viva Goals and select the ‘+’ button on the top panel to create a new OKR.

2. Once you enter the objective/ Key Result and want to share it with another individual, choose owners from the ‘Owner’ option. Here you can assign multiple owners for the OKR.

3. Once you assign an owner, select the user who will be responsible for making check-ins from the ‘Who is responsible for making check-ins?’ list.

4. Once you make the selection, the user will start receiving the check-in reminders.

> [!NOTE]
> By default, the owner (the first owner in the case of multiple owners) is set as the person responsible for check-in and users need not explicitly choose unless necessary.

## FAQs: 

**Q:** How to set who receives the Nudge for multiple-owned OKRs?

**A:** In the case of an OKR having multiple owners, the Nudge notification is sent out to the Check-in owner only.

   For example, Marketing VP and Product VP co-own this OKR while Product VP is set as the Check-in owner.

   :::image type="content" source="../media/goals/nudge-button.png" alt-text="Nudge button to nudge the check-in owner." lightbox="../media/goals/nudge-button.png":::

   Clicking on Nudge will open the modal where the Product Owner will be notified as they are the check-in owner for this OKR.

   :::image type="content" source="../media/goals/nudge-modal.png" alt-text="Nudge modal to send the notification." lightbox="../media/goals/nudge-modal.png":::

**Q:** Notifications for comments

**A:** Viva Goals allows you to add comments on OKRs and check-ins to interact with stakeholders. You can also use @mention to tag certain users. Users will receive notifications for comments in the below cases:

   - When a comment is added on an OKR they own

   - The user has been mentioned in a comment

The notifications will be received in one of the following ways:

- Email

- Slack (if enabled)

- Discord (if enabled) 
