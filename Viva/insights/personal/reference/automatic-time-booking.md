---
ms.date: 03/29/2023
title: How Viva Insights automatically books your time
description: Learn how Viva Insights automatically books time on your calendar
author: lilyolason
ms.author: v-lilyolason
ms.topic: conceptual
ms.localizationpriority: medium 
ms.service: viva 
ms.subservice: viva-insights 
ms.collection: 
- M365-analytics
- viva-insights-personal
manager: anirudhbajaj

---

# How Viva Insights automatically books your time

The following sections provide information that can help you as you create or monitor focus plans.  

### Automatic booking of focus time

After you set automatic booking as your preference, Viva Insights starts looking for time on your Outlook calendar to set aside as focus time. The scheduled focus time shows in your calendar as "Focus time."

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