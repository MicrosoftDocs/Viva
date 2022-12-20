---

title: Focus plan for Viva Insights
description: Viva Insights focus plan
author: lilyolason
ms.author: v-lilyolason
ms.topic: article
ms.localizationpriority: medium
ms.collection: 
- viva-insights-personal
- highpri
ms.service: viva 
ms.subservice: viva-insights 
search.appverid: 
- MET150 
manager: anirudhbajaj
audience: user
---

# Focus plan

Meetings, emails, and chats are necessary to get work done, but they often leave us with little time during the workday for uninterrupted individual work. Some people report spending over 80% of their day collaborating with coworkers, and research has shown that it can take over 20 minutes to refocus after checking just one email.

The focus plan in Microsoft Viva Insights helps you block regular time for your top-priority work by scheduling up to four hours every day to focus. The plan also lets you configure your focus-plan settings to match your needs:

* You can silence or allow chats in Teams.
* You can mute or unmute team notifications.

You can create, configure, or end your focus plan at will. For more information, see [To create your focus plan](#to-create-your-focus-plan) and [To change or leave your focus plan](#to-change-or-leave-your-focus-plan). 

## To create your focus plan

You can create your focus plan in two places:

* [Viva Insights app](#in-the-app)
* [Insights Outlook add-in](#in-the-insights-outlook-add-in)

### In the app

1.	Select the **Protect time** tab.
    
    ![Screenshot that shows the Protect time tab.](../../Images/mya/use/protect-time-tab.png)
1. Locate the **Focus plan** card.
1. Select **Get started**.
   
    ![Screenshot that shows the Focus plan card and the Get started button.](../../Images/mya/use/focus-plan-get-started.png)

2.	If this is:
    * Your first time using a focus plan, you'll be prompted to confirm settings in **Focus plan preferences** after you select **Get started**. These settings are described further in the next section.
    * *Not* your first time using a focus plan, Viva Insights automatically starts booking focus time for you. You can change your settings later in **Focus plan preferences** or by selecting **View settings** on the card.
   
        ![Screenshot that shows the Focus plan card and the View settings link.](../../Images/mya/use/focus-plan-view-settings.png)

### In the Insights Outlook add-in

1. Select the **Want focus time every day?** insight.

   ![Screenshot that shows Want focus time every day? insight](../../Images/mya/use/focus-outlook-insight.png)

2. Select **Book time now**.

   ![Screenshot that shows the Create your focus plan window with Book time now option.](../../Images/mya/use/focus-outlook-insight-enroll.png)

   The Insights pane now notifies you that your focus plan has begun, and your calendar now contains focus-time blocks:

   ![Screenshot that shows the Outlook add-in's focus plan confirmation window.](../../Images/mya/use/focus-outlook-insight-all-set.png)

Now that your focus plan is underway, you can do the following: 

* [Check the progress of your focus plan](#to-check-the-progress-of-your-focus-plan).
* [Change or leave your focus plan](#to-change-or-leave-your-focus-plan).


## To check the progress of your focus plan

After your plan has started, you can check your progress in the Viva Insights app and make sure that you have focus time booked every day over the upcoming week. If the plan has run for at least few days, it will have numbers to report.

**Book focus time** shows you which days already have focus time booked over the next week, and also presents open time slots that you can use to book different focus blocks.

   ![Screenshot that shows the Book focus time section of Protect time in the Viva Insights app.](../../Images/mya/use/focus-plan-time-booked-available.png)

The **Focus plan** card in **Protect your time** shows how many hours of focus time you've kept over the last couple of months, the total hours you have booked for next week, and which days those hours fall on next week.

## To change or leave your focus plan


You can change or opt in and opt out of the focus plan as many times as you want.

### To make changes

From the **Protect time** tab:

1. Locate the **Focus plan** card beneath **Protect your time**.
1. Select **View focus plan preferences**.

     ![Screenshot that shows the Focus plan card with the View plan preferences option](../../Images/mya/use/focus-protect-time-card.png)

3. On the preferences page, you can pick:
   * How many hours you want to spend focusing each day.
   * Whether you want to focus in the morning or afternoon.
   * The earliest you’d want Viva Insights to schedule focus time.
   * Whether you want reminders or to mute Teams notifications during your focus time.

       ![Screenshot that shows Focus plan preferences.](../../Images/mya/use/focus-plan-preferences-app.png)

4. After you're done making edits, select **Save changes**.

#### To leave

Select the **Leave plan** button at top right. 

   ![Screenshot that shows the Leave plan button.](../../Images/mya/use/focus-plan-app-leave-plan.png)

Answer the survey question, then select **Leave plan** again.

## Concepts

The following sections provide information that can help you as you create or monitor focus plans.  

### Automatic booking of focus time

After you set automatic booking as your preference, Viva Insights starts looking for time on your Outlook calendar to set aside as focus time. The scheduled focus time shows in your calendar as a different color and is labeled "Focus time."

Focus time never creates a calendar conflict; that is, focus time will not be booked over any existing calendar event, such as all-day meetings, booked personal time, or appointments.

Although two hours is the maximum length of a focus-time block that can be scheduled automatically, you can extend your focus time, by hand, in your Outlook calendar.

#### Booking schedule

Viva Insights books focus time two weeks in advance. For example: when you open your calendar on a Monday, you should see focus time booked every day of the current week and all the way through the Friday of the following week. Each weekend it looks for time blocks in the next week out and books time accordingly.

#### How time slots are selected

The time it reserves for you depends on the time you have open during the day. Viva Insights starts its search at the beginning of your workday, as it is defined in your Outlook settings. 

Viva Insights also respects the **Do not schedule focus time earlier than** setting in the **Plan configuration** dialog box. For example, if you set this to 9:00 AM, Viva Insights will select no focus-time slots that begin earlier than 9:00 AM.  

Viva Insights also prioritizes your preferences for length of focus time slots and part of day (morning or afternoon). For example, if you choose four hours of focus time and choose afternoon, Viva Insights first scans your calendar to find four-hour open slots in the afternoon. If it finds no four-hour open slots in the afternoon, it continues to scan your calendar to find four-hour open slots in the morning. If only smaller amounts of time are available, it can book focus blocks as short as 30 minutes. 

After it books a block on one day, it then moves on to the next day to find the next suitable block, based on your preferences. (In most cases, it creates only one block of focus time per day.) 

#### Lunchtime

Viva Insights considers the time from noon to 1:00 PM as time for the midday meal. If you have automatic booking turned on, Viva Insights tries to book any other time of day first. If it finds no other blocks of time available, it will then book focus time during the lunchtime period.

### Chats are muted during focus time  

During focus time, your status in Teams and Skype for Business will automatically change to "Focusing" to silence chat notifications and help you stay focused. When the focus time appointment ends, your status will automatically revert back to the status you were previously in. Note that you can set priority contacts in Teams to ensure you don’t miss important messages during focus time.

For more information, see [Manage notifications in Teams](https://support.office.com/article/manage-notifications-in-teams-1cc31834-5fe5-412b-8edb-43fecc78413d).

### Digest emails and Viva Insights Outlook add-in

#### Focus plan digest

After you enroll in a focus plan, the content in your digest email will be tailored based on your participation in the plan. It might, for example, remind you to schedule focus time for days on which none is set aside.

#### Viva Insights add-in

You can open the Outlook add-in to check whether any upcoming days are missing focus time. To do so, use this card:

![Add-in feed card.](../../Images/mya/use/add-in-feed-card.png)

Selecting this card shows the following options, with which you can book focus time on individual days or for several days at once:  

![Book focus time inline.](../../Images/mya/use/book-focus-time-nudge.png)

## Calendar color settings

>[!Note]
>Outlook no longer automatically shows focus time as green, or any other color, on the calendar.

If you want to personalize your focus time to show as a specific color, you can do that by using conditional formatting in the Outlook desktop app on Windows. Follow the steps below to create a new conditional formatting rule.

1. From the calendar view, select the **View** tab **> Current View > View Settings**.

    ![Screenshot that shows navigating the View Settings option.](../../Images/mya/use/focus-plan-view-settings-rule.png)

1. Select the **Conditional formatting** button.

    ![Screenshot that shows the Conditional Formatting button highlighted in the Advanced View Settings dialog box.](../../Images/mya/use/focus-plan-conditional-formatting.png)

1. Select the **Add** button to create a new rule.

    ![Screenshot that shows the Add button highlighted in the Conditional Formatting dialog box.](../../Images/mya/use/focus-plan-add-rule.png)

1. In the **Conditional Formatting** dialog box:
    1. Give your rule a name.
    1. Select the color you want focus time blocks to appear as.
    1. Select the **Condition** button.

    ![Screenshot that shows Name, Color, and Condition highlighted in the Conditional Formatting dialog box.](../../Images/mya/use/focus-plan-assign-name.png)

1. In the **Filter** dialog box, add "Focus time" as your search term. Leave the **In:** field set to "subject field only."

    ![Screenshot that shows the search term field highlighted in the Filter dialog box.](../../Images/mya/use/focus-plan-set-term.png) 

1. Select the **OK** button on each of the three dialog boxes. Your focus time blocks should now appear as the color you set in step 4.
