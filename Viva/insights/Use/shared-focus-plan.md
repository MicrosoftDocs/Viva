---
ROBOTS: NOINDEX,NOFOLLOW
title: Shared focus plan
description: Learn about the Shared focus plan option in Microsoft Viva Insights in Teams
author: madehmer
ms.author: helayne
ms.topic: article
ms.collection: viva-insights-personal
ms.localizationpriority: medium 
ms.service: viva
ms.subservice: viva-insights
manager: scott.ruble
audience: Admin
---

# Shared focus plan

_**Note**: This is currently only available through a targeted release._

A focus plan helps you automatically block uninterrupted time for top-priority work for up to four hours every day. As an individual, you can schedule a personal focus plan through [Protect time](../personal/teams/viva-insights-protect-time.md) in the Microsoft Viva Insights app in Microsoft Teams.

As an enrolled team lead or manager, you can also start a shared focus plan with your team or co-workers to encourage good productivity habits. With this option, you can invite your team to book daily, uninterrupted time to get their work done. This shared plan also helps your team build a shared productivity habit.

Anyone with a Microsoft Viva Insights license with an applicable [service plan](../personal/overview/plans-environments.md) can start a shared focus plan. However, recipients of the invitation to the shared plan do not need this license.

## Start a shared focus plan

1. In [Teams](https://teams.microsoft.com), open Viva Insights, and then select **Home**.
2. In the **Plans** section, select **Get started** for the **Start a focus plan for your team** option:

   ![Start a shared focus plan](../Images/mya/use/page-showing-plans-row-2.png)

3. When prompted, select **Let’s do this**.
4. In **Customize your shared focus plan**, select the number of hours per day, the general time of day, and whether to silence notifications, and then select **Next**.

   ![Select settings](../Images/mya/use/select-settings.png)

5. In **Who would you like to invite**, select people in your team to receive invitations to the focus plan. Your team members will pre-populate the list of **Recipients**; you can also remove or add people to this list. When you’re done, select **Next**.
6. When prompted, you can either accept or edit the draft note or delete it, and then select **Send invitation**.

After you send the invitation, Viva Insights sends notifications to the recipients. These notifications remain available to your recipients for eight weeks or until you cancel the shared focus plan.

## Respond to a shared focus plan invitation

If you received an invitation for a shared focus plan, use the following steps to join.

1. In [Teams](https://teams.microsoft.com), do one of the following:

   * Select the notification in the upper-right corner of Teams.
   * On the card under **Top actions for today**, select **Open invite**.

2. When you select **Join plan** in the **Shared focus plan** invitation, one of the following occurs. Or if you select **Dismiss**, it cancels the invitation and suppresses any reminders of it.

   * If you were _not_ already enrolled in a focus plan, you'll see the **All done** message and skip the rest of these steps.
   * If you _were_ already enrolled in a focus plan, go to the next step.

3. In **Select focus plan settings**, you can do the following: 

   * To switch from your individual plan to the shared plan, select **Join plan**.
   * To switch and join the shared plan but first change some of the settings, select **Edit settings**. You can then change the number of hours per day, the general time of day, and whether to silence notifications, and then select **Join plan**.
   * To keep your current (individual) focus plan, close this page by selecting the **X**. The invitation will no longer be visible, and your current focus plan will be unaffected.
     ![Select focus plan settings](../Images/mya/use/select-focus-plan-settings.png)

4. On the **All done** page, select **Done**. You have now successfully joined your team’s shared focus plan.

## Check the details of your shared focus plan

To check the details of your new plan, open the **Home** page of Viva Insights. The **Shared focus plan** details will be included in the **Plans** section:

   ![Shared-focus-plan card](../Images/mya/use/shared-focus-plan-card.png)

If you have a Microsoft Viva Insights license with an applicable [service plan](../personal/overview/plans-environments.md), you'll also see the plan details on the **My team** page.

If you are the creator of a shared focus plan, you'll also see details in the **Plans** section of the Viva Insights **Home** page:

   ![Shared-focus-plan card](../Images/mya/use/your-shared-focus-plan.png)

## Leave a shared focus plan

This section describes how to leave a shared focus plan as a [participant in the plan](#as-a-plan-participant) or as the plan's [organizer](#as-the-plan-organizer).

### As a plan participant

As a participant, you can leave a shared focus plan by selecting **Leave plan** in  **Shared focus plan** that's shown in the **Plans** section of Viva Insights.  

After you leave a shared plan, you will still be enrolled in your personal focus plan. To opt out of the personal focus plan or change its settings, as follows:

1. Select the **ellipsis** (…) in the upper right corner of Viva Insights, and then select **Settings**.

   ![Select ellipsis and then Settings](../Images/mya/use/ellipsis-settings.png)

2. In **Settings**, select **Protect time**.
3. In the **Focus plan preferences** section, select **Leave plan**.

### As the plan organizer

After you have organized a shared focus plan, you can leave the plan. To do so, in  **Shared focus plan** in the **Plans** section of Viva Insights, select **Leave plan**, and then select **Confirm**.

Note that your departure from a focus plan does not opt anybody else out of the plan. Plan participants remain enrolled in the focus plan until they opt out.

## Concepts

The following sections provide information that can help you as you create or monitor focus plans.

### Automatic scheduling

After you set automatic booking as your preference, Viva Insights starts looking for time on your Outlook calendar to set aside as focus time. This scheduled time will shown up in a different color in your calendar as "Focus time."

Focus time won't create calendar conflicts by not scheduling over any existing calendar events, such as all-day meetings, booked personal time, or appointments.

Although two hours is the maximum length of an automatically scheduled focus-time block, you can manually extend the scheduled focus time in your calendar.

### Booking schedule

Viva Insights books focus time two weeks in advance. For example, when you open your calendar on a Monday, you should see focus time booked every day of the current week and all the way through the Friday of the following week. Each weekend it looks for time blocks in the next week out and books time accordingly. 

### How time slots are selected

The time it reserves for you depends on the time you have open during the day. Viva Insights starts its search at the beginning of your workday, as it is defined in your Outlook settings.

Viva Insights also respects the **Do not schedule focus time earlier than** setting in the **Plan configuration** options. For example, if you set it to 9:00 AM, Viva Insights will only select focus-time slots that occur after 9:00 AM.  

Viva Insights also prioritizes your preferences for length of focus time slots and part of day (morning or afternoon). For example, if you choose four hours of focus time in the afternoon, Viva Insights first scans your calendar to find four-hour open slots in the afternoon. If it finds no four-hour open slots in the afternoon, it continues to scan your calendar to find four-hour open slots in the morning. If only smaller amounts of time are available, it can book focus blocks as short as 30 minutes.

After it books a block on one day, it then moves on to the next day to find the next suitable block, based on your preferences. (In most cases, it creates only one block of focus time per day.)

#### Lunch time

Viva Insights considers the time from 12:00 PM (noon) to 1:00 PM as time for the midday meal. If you have automatic booking turned on, Viva Insights tries to book any other time of day first. If it finds no other blocks of time available, it will then book focus time during the lunch time period.

### You can mute chats during focus time  

You can choose whether, during focus time, your status changes to "focusing" and chat notifications in Teams are silenced. When the focus time appointment ends, your status reverts back to your previous status. Note that you can set priority contacts in Teams to ensure you don’t miss important messages during focus time.

For more information, see [Manage notifications in Teams](https://support.office.com/article/manage-notifications-in-teams-1cc31834-5fe5-412b-8edb-43fecc78413d).

### Focus plan digest

After you enroll in a focus plan, your digest email will be tailored to your participation in the plan. It might, for example, remind you to book focus time for days on which none is set aside.
