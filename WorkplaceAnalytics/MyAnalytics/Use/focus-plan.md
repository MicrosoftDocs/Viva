---
# Metadata Sample
# required metadata

title: Focus plan
description: MyAnalytics focus plan
author: paul9955
ms.author: v-pausch
ms.topic: article
localization_priority: normal
ms.prod: Mya

---

# Focus plan

Meetings, emails, and chats are necessary to get work done, but they often leave us with little time during the work day for uninterrupted individual work. Some people report spending over 80% of their day collaborating with coworkers, and research has shown that it can take over 20 minutes to refocus after checking just one email.

The focus plan in MyAnalytics helps you block regular time for your top-priority work by scheduling up to four hours every day to focus. The plan also lets you configure your focus-plan settings to match your needs: 
* You can silence or allow chats in Teams and in Skype for Business. 
* You can mute or unmute team notifications. 

You can create, configure, or end your focus plan at will. For more information, see [To create your focus plan](#to-create-your-focus-plan) and [To leave or change your focus plan](#to-leave-or-change-your-focus-plan). 

## To create your focus plan

You can create your focus plan in the [MyAnalytics dashboard](#create-focus-plan-in-the-myanalytics-dashboard) or in the [Insights Outlook add-in](#create-focus-plan-in-the-insights-outlook-add-in):

### Create focus plan in the MyAnalytics dashboard

When you enroll in the focus plan, you configure how focus time will be booked on your calendar. MyAnalytics books this time based on the preferences that you set: 
 * The number of focus hours per day &mdash; one, two, or four hours.
 * Your preferred time of day &mdash; morning or afternoon.  
 * Whether to mute or to allow chat notifications in Teams. Muting chat notifications changes your Teams status to "Focusing." 

1. In the header of the **Focus** page of your personal dashboard, select **Get started**. 

   ![Focus plan - Get started](../../Images/mya/use/focus-every-day-83.png)

2. Select the number of hours of focus time you would like MyAnalytics to book for you every day, and then select **Next**.

   ![Focus plan - Choose hours](../../Images/mya/use/focus-plan-choose-hours-83.png)

3. Select the time of day for your focus time, and then select **Next**.
   
   ![Focus plan - Choose AM or PM](../../Images/mya/use/focus-plan-choose-am-pm-101.png)
   
4.	Select whether to have Teams chat notifications muted during focus time, and select **Looks good!** 
   
     ![Focus plan - Choose to mute chat notifications](../../Images/mya/use/focus-plan-choose-mute-105.png)
   
     MyAnalytics now seeks time on your Outlook calendar to set aside as focus time, based on your preferences. The amount and placement of focus time depends on the time your calendar has open. 
   
     For more information, see [Automatic booking of focus time](#automatic-booking-of-focus-time).

#### Change your focus-plan preferences

You can always modify your focus-plan preferences by selecting **Plan Configuration**. 

   ![Focus plan - Choose to mute chat notifications](../../Images/mya/use/focus-plan-open-settings.png)

This opens the **Plan configuration** pane, on which you can change the number of focus hours per day, your preference of morning or afternoon, and whether to mute Teams notifications. See [To leave or change your focus plan](#to-leave-or-change-your-focus-plan). 

### Create focus plan in the Insights Outlook add-in

You can also use the Outlook add-in to enroll in the focus plan. To do so, follow these steps.

1. Select the insight **Want focus time every day?**
   
   ![Create focus plan in add-in](../../Images/mya/use/want-focus-time.png)

2. Select **Book time now**. 

   ![Book time now](../../Images/mya/use/book-time-now.png)

   The Insights pane now notifies you that your focus plan has begun, and your calendar now contains focus-time blocks:

   ![Plan has started](../../Images/mya/use/all-set.png)

Now that your focus plan is underway, you can do the following: 

* [Check the progress of your focus plan](#to-check-the-progress-of-your-focus-plan)
* [Leave or change your focus plan](#to-leave-or-change-your-focus-plan)

## To check the progress of your focus plan

After your plan has started, you can check your progress and make sure that you have focus time booked every day over the upcoming two weeks. If the plan has run for at least few days, it will have numbers to report. 

 * In the MyAnalytics dashboard, select **Focus** in the left navigation pane. A panel opens and shows statistics about your focus time:

    ![Dashboard report](../../Images/mya/use/track-progress.png)
  
An important metric on this page appears under **Last week**. It shows how many days you had focus time last week. 

The **Plan ahead** area helps you to plan focus time for the upcoming days. This area has the following sections: 

### Focus time booked

For the current week and the following week, this area shows how many days and which days have had focus time booked. In the preceding example screenshot, the three days with focus time booked are shown in green. 

### Needs focus time

This section shows upcoming days that have no focus time booked but still have open time available. Select **Book now** to have MyAnalytics select and book this time. 

### Needs review

During the number of days shown (in the screenshot, three days) MyAnalytics has either found no time to book or it has found booked focus time that has a meeting conflict. Select **Review** to open your calendar in Outlook on the web to resolve the issue. 

> [!Note] 
> If you make changes to your Outlook calendar, they will be reflected on your dashboard within five minutes. 

<!-- 
### To add tasks to your focus time
[Need steps here]
-->

## To leave or change your focus plan

You can opt in and opt out of the focus plan as many times as you want. 

* Select **Plan configuration**:

    ![Plan configuration](../../Images/mya/use/plan-config.png)
 
    This opens the **Configurations** page and displays the **Plan configuration** pane, on which you can leave the plan or change your preferences.

    ![Plan configuration card](../../Images/mya/use/plan-config-pane.png)
   
   After you indicate your preferences, select **Save changes**.
   
   To have MyAnalytics stop helping you book focus time, select **Leave plan**. 

## Concepts

The following sections provide information that can help you as you create or monitor focus plans.  

### Automatic booking of focus time

After you set automatic booking as your preference, MyAnalytics starts looking for time on your Outlook calendar to set aside as focus time. The time that it books on your calendar appears in a different color and is labeled "Focus time":  

![Focus prompt in the digest](../../Images/mya/use/focus-time-on-your-calendar.png)

Focus time never creates a calendar conflict; that is, focus time will not be booked over any existing calendar event, such as all-day meetings, booked personal time, or appointments. 

Although two hours is the maximum length of a focus-time block that can be scheduled automatically, you can extend your focus time, by hand, in your Outlook calendar. 

#### Booking schedule

MyAnalytics books focus time two weeks in advance. For example: when you open your calendar on a Monday, you should see focus time booked every day of the current week and all the way through the Friday of the following week. Each weekend it looks for time blocks in the next week out and books time accordingly. 

#### How time slots are selected

The time it reserves for you depends on the time you have open during the day. MyAnalytics starts its search at the beginning of your workday, as it is defined in your Outlook settings. 

MyAnalytics also respects the **Do not schedule focus time earlier than** setting in the **Plan configuration** dialog box. For example, if you set this to 9:00 AM, MyAnalytics will select no focus-time slots that begin earlier than 9:00 AM.  

MyAnalytics also prioritizes your preferences for length of focus time slots and part of day (morning or afternoon). For example, if you choose four hours of focus time and choose afternoon, MyAnalytics first scans your calendar to find four-hour open slots in the afternoon. If it finds no four-hour open slots in the afternoon, it continues to scan your calendar to find four-hour open slots in the morning. If only smaller amounts of time are available, it can book focus blocks as short as 30 minutes. 

After it books a block on one day, it then moves on to the next day to find the next suitable block, based on your preferences. (In most cases, it creates only one block of focus time per day.) 

#### Lunchtime

MyAnalytics considers the time from 12:00 PM (noon) to 1:00 PM as time for the midday meal. If you have automatic booking turned on, MyAnalytics tries to book any other time of day first. If it finds no other blocks of time available, it will then book focus time during the lunchtime period.

### Chats are muted during focus time  

During focus time, your status in Teams and Skype for Business will automatically change to "Focusing" to silence chat notifications and help you stay focused. When the focus time appointment ends, your status will automatically revert back to the status you were previously in. Note that you can set priority contacts in Teams to ensure you don’t miss important messages during focus time.

For more information, see [Manage notifications in Teams](https://support.office.com/article/manage-notifications-in-teams-1cc31834-5fe5-412b-8edb-43fecc78413d).

### Weekly digest and insights add-in

#### Focus plan weekly digest

After you enroll in a focus plan, the content of the weekly digest becomes tailored to your participation in the plan. It might, for example, remind you to book focus time for days on which none is set aside.

#### Insights add-in 

You can open the Outlook add-in to check whether any upcoming days are missing focus time. To do so, use this card:

![Add-in feed card](../../Images/mya/use/add-in-feed-card.png)

Selecting this card shows the following options, with which you can book focus time on individual days or for several days at once:  

![Book focus time inline](../../Images/mya/use/book-focus-time-nudge.png)

<!--
Note that this content is related to this topic: 
\WorkplaceAnalytics\Tutorials\solutionsv2-participants.md
-->