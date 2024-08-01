---
ms.date: 06/17/2024
title: Configure check-in reminders, notifications, and templates
ms.reviewer: 
ms.author: rasanders
author: RaSanders-MSFT
manager: Liz.Pierce
audience: Admin
f1.keywords:
- NOCSH
ms.topic: article
ms.service: viva-goals
ms.localizationpriority: medium
ms.collection:  
- Strat_SP_modern
- M365-collaboration
- m365initiative-viva-goals  
search.appverid:
- MET150
description: "Learn how you can set up check-in reminders, notifications, and templates in Viva Goals."
---

# Configure check-in reminders, notifications, and templates

Regular check-ins are a key part of an effective OKR implementation. OKRs are closely aligned, and therefore will reflect inaccuracies if they aren't updated regularly. To avoid such inaccuracies, it’s helpful to send gentle reminders to your team to check in on their OKRs. Setting a cadence to remind teams and users to make check-ins is referred to as the check-in rhythm.

Notifications remind your team to check in regularly. By default, Viva Goals sends a notification to all team members every Monday at 9:00 AM in the user’s time zone, but the notifications can be customized to fit your business needs.

## Set a check-in rhythm

In the **Notifications** tab of the **Admin** dashboard, you can set:

- Frequency (every one, two, or three weeks, or monthly on the first week, second week, third week, fourth week, or last week)

- Days on which notifications are sent

- Time at which notifications are sent

- Disable notifications for OKRs that have had check-ins in the past X days (select number of days)

Team owners can control whether the subteams reporting to their team can set their own check-in rhythm or should follow the parent team's cadence. They can decide if the cadence they're setting should be cascaded down to the reporting teams, or is confined just to their team.

For instance, the Chief of Staff sets a cadence to notify the users belonging to their team every Monday at 9AM PST. They can choose to set the same rhythm across departments such as Marketing, Product, Sales, Engineering, and Customer Success in the organization. Once set, all the users belonging to these teams receive a notification for check-ins every Monday at 9AM PST.

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

- The VP of Sales wants their team to have a weekly check-in cadence and is setting a rhythm to receive notifications every Wednesday at 9AM PST. To ensure everyone is on the same page, they want all the subteams reporting into them to follow the same cadence, rather than each subteam having a cadence of its own. Therefore, they set a cadence, cascade it down to all their reporting teams, and not let them change this rhythm.

   :::image type="content" source="../media/goals/teams-same-cadence.png" alt-text="All the subteams follow the same cadence of the parent team." lightbox="../media/goals/teams-same-cadence.png":::

Team owners can create a custom cadence for reminders for their departments and teams in Admin > Team Settings. These cadences can differ from the organization-level cadence.

If teams have to follow the parent team's check-in rhythm, the team owners won't be able to change the schedule.

:::image type="content" source="../media/goals/subteams-match-parent-cadence.png" alt-text="Subteams won't be able to change the schedule if they're configured to follow the parent team's cadence." lightbox="../media/goals/subteams-match-parent-cadence.png":::

## Check-ins for single and multiple owners

For OKRs having single or multiple owners, you can decide which user in the organization is responsible for making check-ins use the ‘check-in responsibility’ feature. The check-in owner is able to check in the OKR (manual check-ins) and set up a data link on the OKR (for auto check-ins). This user is receiving the check-in reminders. In the case of multiple owners, this prevents all of the owners from receiving reminders. Only the user set as 'check-in responsible owner' will receive the reminders.

### Steps to assign responsibility for check-ins

1. Sign-in to Viva Goals and select the ‘+’ button on the top panel to create a new OKR.

2. Once you enter the objective/ Key Result and want to share it with another individual, choose owners from the ‘Owner’ option. Here you can assign multiple owners for the OKR.

3. Once you assign an owner, select the user who is responsible for making check-ins from the ‘Who is responsible for making check-ins?’ list.

4. Once you make the selection, the user starts receiving the check-in reminders.

> [!NOTE]
> By default, the owner (the first owner in the case of multiple owners) is set as the person responsible for check-in and users need not explicitly choose unless necessary.

## Set a check-in note template for your team

Each check-in includes a check-in note, which is a qualitative description of the progress made on the goal. These notes help leaders understand the context behind a goal's progress and the reason for its current status, such as why it is On Track, Behind, or At Risk.

A common problem with check-in notes is that they all have different formats. This makes it hard for managers to quickly understand the progress the team has made. Creating a check-in note template solves this problem by prescribing a format for all check-ins on the team.

If you're a team owner, you can set a check-in template by performing the following steps:

1. Go to your team and select **...** > **Team settings**.

1. Under the **Check-ins** tab, enable the **Check-in note template** slider.

1. Viva Goals provides a default template, but you can edit it to your prefrences. Select **Save**.

Now, every time a goal is checked in, users will see the recommended template.

If a goal belongs to multiple teams, a user will see a dropdown with all the templates that could apply to the goal, and they can choose from among the templates.

## FAQ

1. **How to set who receives the Nudge for multiple-owned OKRs?**
    1. In the case of an OKR having multiple owners, the Nudge notification is sent out to the Check-in owner only.
        1. For example, Marketing VP and Product VP co-own this OKR while Product VP is set as the Check-in owner.
        
        :::image type="content" source="../media/goals/nudge-button.png" alt-text="Nudge button to nudge the check-in owner." lightbox="../media/goals/nudge-button.png":::
        
        2. Clicking on Nudge will open the modal where the Product Owner will be notified as they're the check-in owner for this OKR.
        
        :::image type="content" source="../media/goals/nudge-modal.png" alt-text="Nudge modal to send the notification." lightbox="../media/goals/nudge-modal.png":::

1. **Notifications for comments**
    1. Viva Goals allows you to add comments on OKRs and check-ins to interact with stakeholders. You can also use @mention to tag certain users. Users receive notifications for comments in the below cases:
        1. When a comment is added on an OKR they own
        1. The user has been mentioned in a comment

1. **I have enabled check-in reminders, but they are not being sent. How can I resolve?**
    1. Check-in reminders will not be sent under the following conditions:
        - **If the OKR approval workflow is enabled and the status of the OKR is in planning.** We don't trigger reminders for draft OKRs. Only when OKRs move from planning to other stages will reminders be triggered.
        - **For OKRs where progress is updated via integration or rolled up from child OKRs**. We trigger reminders only for OKRs where progress is updated manually.
        - **For anyone who is not a check-in owner.** Only check-in owners will receive reminders. This is to avoid creating extra "noise" for other users.
        - **For OKRs where the start date is later than today’s date.**
        - **For OKRs which have the setting 'Do not include OKRs & Projects updated within the last x days' enabled.**
        - **For OKRs where the time period is archived.**
