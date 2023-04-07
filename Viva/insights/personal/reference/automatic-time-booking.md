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

After you set automatic booking as your preference for focus, breaks, message catch-up, learning, or lunch, Viva Insights starts searching for time on your Outlook calendar to set aside. Automatically booked time never creates a calendar conflict—that is, Viva Insights won't book over any existing calendar event, like a meeting, personal time, or appointment.

## Booking schedule

Viva Insights automatically books time two weeks in advance. For example, if you open your calendar on a Monday, you'd notice your automatically booked time appear all the way through the Friday of the following week. Each weekend, Viva Insights finds time blocks in the next week out and books time accordingly.

## How Viva Insights selects time slots

The time Viva Insights reserves for you depends on the time you have open during the day and what kind of time you're booking. However, for all types of booked time, Viva Insights starts its search at the beginning of your workday as defined in your Outlook settings.

|Type | Frequency | Preference|
|-----|-----------|-----------|
|Breaks| Twice per day|5, 10, 15, or 30 minutes
|Learning| Once per week| <ul><li>30 minutes, 1 hour, or 2 hours <li> Morning or afternoon
|Lunch| Once per day|Self-configured|
|Focus| Once per day| <ul><li>1 hour, 2 hours, or 4 hours<li>Morning or afternoon<li>Do not schedule earlier than

>[!Note]
>Although four hours is the maximum length of a focus-time block that can be scheduled automatically, you can extend your focus time, by hand, in your Outlook calendar.

### About preferences

#### Duration and time of day

Viva Insights prioritizes your preferences for length of time slots and part of day (morning or afternoon). For example, if you chose two hours of focus time and afternoon, Viva Insights first scans your calendar to find two-hour open slots in the afternoon. If Viva Insights finds no two-hour open slots in the afternoon, it continues to scan your calendar to find two-hour open slots in the morning. If only smaller amounts of time are available, Viva Insights can book focus blocks as short as 30 minutes.

#### Do not schedule earlier than

Viva Insights also respects the **Do not schedule focus time earlier than** setting for focus time. For example, if you select 9:00 AM here, Viva Insights won't select any focus-time slots that begin earlier than 9:00 AM.  

#### Lunchtime

Viva Insights considers the time from noon to 1:00 PM as time for the midday meal. If you have automatic booking turned on, Viva Insights tries to book any other time of day first. If it finds no other blocks of time available, it will book time during the lunchtime period.