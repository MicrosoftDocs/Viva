---
# Metadata Sample
# required metadata

title: Focus plan
description: MyAnalytics focus plan
author: paul9955
ms.author: paul9955
ms.topic: article
localization_priority: normal
ms.prod: mya

---

# Focus plan

_**Applies to:** Focus plan is currently available for MyAnalytics users who have an E5 license. Focus plan will become available to all MyAnalytics users in the coming months. MyAnalytics elements are available in varying levels to users of different Microsoft Office 365 and Microsoft 365 plans. See [MyAnalytics plans and environments](../overview/plans-environments.md) for details. To determine your plan and service plan, see [How do I find my plan?](../overview/mya-faq.md#q4-how-can-i-find-out-what-my-plan-is)._

Meetings, emails, and chats are necessary to get work done, but they often leave us with little time during the work day for uninterrupted individual work. Some people report spending over 80% of their day collaborating with coworkers, and research has shown that it can take over 20 minutes to refocus after checking just one email.

The focus plan in MyAnalytics helps you block time every day for your top-priority work. MyAnalytics will help you schedule one to two hours every day to focus (with the option to automatically book that time), and silence chats in Teams and Skype for Business during that booked time. 

You can create or end your focus plan at will. For more information, see [To create your focus plan](#to-create-your-focus-plan) and [To leave or change your focus plan](#to-leave-or-change-your-focus-plan). 

## To create your focus plan

You can create your focus plan in the MyAnalytics dashboard or in the Outlook add-in:

### Personal dashboard

1. In the header of the **Focus** page of your personal dashboard, select **Get started**. 

   ![Focus plan card in digest](../../Images/mya/use/focusplan-intro.png)

   This displays a page where you can indicate your preferences:

   ![Personalize your experience](../../Images/mya/use/focusplan-preferences.png)
 
2. On this page, select either **Automatically book time** or **Reminders only**. (Learn more about [Automatic booking of focus time](#automatic-booking-of-focus-time).) If you select the former, MyAnalytics will automatically add one to two hours of focus time per day on your Outlook calendar, depending on what times your calendar has open. If you select **Reminders only**, MyAnalytics will send you a [weekly digest](#focus-plan-weekly-digest) and [inline suggestions](#inline-suggestions-and-other-alerts) in Outlook that remind you to schedule your own focus time. 

2.	Select **Book focus time now**. This enrolls you in your focus plan. MyAnalytics now carries out the option that you chose&mdash;to book focus time or to remind you to book focus time.

### Outlook add-in

You can also use the Outlook add-in to enroll in the focus plan. To do so, select the **Create your focus plan**. 

![Create your focus plan](../../Images/mya/use/card-in-add-in-2.png)

The steps that follow match the steps in [Personal dashboard](#personal-dashboard): Select either **Automatically book time** or **Reminders only** and then select **Get started**. 
 
## To check the progress of your focus plan

After your plan has started, you can check your progress and make sure that you have focus time booked every day over the upcoming two weeks. If the plan has run for at least few days, it will have numbers to report. 

 * In the MyAnalytics dashboard, select **Focus** in the left navigation pane. A panel opens up to display statistics about your focus time:

    ![Dashboard report](../../Images/mya/use/focusplan-planahead.png)
  
An important metric on this page is displayed under **Last week**. It shows how many days you had focus time last week. 

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

    ![Plan configuration](../../Images/mya/use/plan-config-80.png)
 
    This opens the **Configurations** page and displays the **Plan configuration** card, on which you can leave the plan or change your preferences.

<!-- REMOVED PER PETER. TOO MUCH DETAIL. 
2.	Your status determines what you see on the **Plan configuration** card: 

    * <u>Already in a plan:</u> If you are already in a focus plan, the card gives you two options: 
       * To change your plan preference, select the option to switch between auto-booking and reminders, and then select **Save changes**. 

         ![Personalize your experience](../../Images/mya/use/plan-config-card.png)

       * To end your participation in the focus plan, select **Leave plan** and then respond **Yes** or **No** in the **Leave focus plan** confirmation message. 

    * <u>Not in a plan:</u> If you are not already in a focus plan, the **Plan configuration** card gives you the option to join. To do this, select **Try it now**. This displays the **Personalize your experience** card. 

       On this card, select either **Book time for me** or **Just remind me to book time**, and then select **Get started**.
 
      ![Personalize your experience](../../Images/mya/use/preferences.png)
-->
 
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

The time it reserves for you depends on what you have open during the day. MyAnalytics starts its search at the beginning of your workday, as it is defined in your Outlook settings. If your day starts at 8:00 AM and you have two hours open right then, MyAnalytics schedules two hours of focus time, from 8:00 to 10:00 AM. If it finds no open time at the beginning of your day, it continues to scan your calendar to find open blocks later in the day. If only smaller amounts of time are available, it can book a focus block as short as one hour. 

After it books a block on one day, it then moves on to the next day to find the next suitable block. (In most cases, it creates only one block of focus time per day.)

#### Lunchtime

MyAnalytics considers the time from 12:00 AM to 1:00 PM as time for the midday meal. If you have automatic booking turned on, MyAnalytics tries to book any other time of day first. If it finds no other blocks of time available, it will then book focus time during the lunchtime period.

### Chats are muted during focus time  

During focus time, your status in Teams and Skype for Business will automatically change to "Focusing" to silence chat notifications and help you stay focused. When the focus time appointment ends, your status will automatically revert back to the status you were previously in. Note that you can set priority contacts in Teams to ensure you don’t miss important messages during focus time.

For more information, see [Manage notifications in Teams](https://support.office.com/article/manage-notifications-in-teams-1cc31834-5fe5-412b-8edb-43fecc78413d).

<!-- DELETED 27 JUNE, PER PETERB

## Focus plan in MyAnalytics surfaces

### Before you create the plan

As a MyAnalytics user, you might become aware of the focus plan when you see focus-related prompts and messages in the weekly digest, the dashboard, and insights. Examples: 

#### Focus plan prompt in the digest

![Focus prompt in the digest](../../Images/mya/use/focus-prompt-in-email-digest-75-90.png)

#### Focus plan prompt in the dashboard
  
![Focus prompt in the dashboard](../../Images/mya/use/focus-prompt-in-dashboard.png)

For more information about the weekly digests, which for focus plan participants becomes tailored to the plan, see [MyAnalytics weekly digest](#myanalytics-weekly-digest-email). 

-->

### Weekly digest and inline suggestions

#### Focus plan weekly digest

After you enroll in a focus plan, the content of the weekly digest becomes tailored to your participation in the plan. It might, for example, remind you to book focus time for days on which none is set aside.

#### Inline suggestions and other alerts

If you choose not to have MyAnalytics automatically book focus time for you, MyAnalytics delivers [inline suggestions](mya-notifications.md) in Outlook that remind you to reserve time to focus every day.

You can also open the Outlook add-in to check whether any upcoming days are missing focus time. To do so, use this card:

![Add-in feed card](../../Images/mya/use/add-in-feed-card.png)

Selecting this card shows the following options, with which you can book focus time on individual days or for several days at once:  

![Book focus time inline](../../Images/mya/use/book-focus-time-nudge.png)

<!--
Note that this content is related to this topic: 
\WorkplaceAnalytics\Tutorials\solutionsv2-participants.md
-->


<!--  DELETED PER PETERB 27 JUNE

If you've chosen not to turn on auto-booking and if other circumstances arise that will limit your focus time (even if you choose to delete a focus block), MyAnalytics alerts you of the focus time that you are missing over the upcoming days.

For example, the add-in might display this card: 
 
![Add-in feed card](../../Images/mya/use/add-in-feed-card.png)

### After you create the plan
 
#### MyAnalytics weekly digest

As described under [To check the progress of your focus plan](#to-check-the-progress-of-your-focus-plan), you use the MyAnalytics dashboard to see how well your focus plan is working. 

You can also find similar information in the MyAnalytics weekly digest. After you enroll in a focus plan, the content of the digest becomes tailored to your participation in the plan. 

It reports on your recent progress in the plan, it gives opportunities to plan for the near future, and it presents food-for-thought items that can help you succeed in the plan. Finally, it contains an _Explore more_ section that lets you dig deeper into various performance indicators for recent days. It looks something like this: 

![Focus prompt in the digest](../../Images/mya/use/new-digest-email-2.png)

-->