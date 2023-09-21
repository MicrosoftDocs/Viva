---
ROBOTS: NOINDEX, NOFOLLOW
ms.date: 03/29/2023
title: Meeting and communications in Viva Insights reference
description: Learn how Viva Insights calculates some meeting- and communications-related insights
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

# Meeting and communications insight reference

## In Teams

## Productivity

### Meeting habits and meeting exclusions

Here's how we calculate the insights shown in **Productivity > Meeting habits** and **Meeting exclusions**:

#### Meeting habits

* **<= 1 hour** – Meetings you organized that were one hour or shorter
* **Advanced notice** – Meeting invitations you sent with more than 24 hours' notice before the scheduled start time
* **Added a Teams link** – Meetings you organized that included a Teams link for remote attendees
* **During working hours** – Meetings you organized or accepted during your working hours
* **Ended on time** – Online meetings (on Microsoft Teams) that you ended within one minute of the scheduled end time
* **High attendance** – Meetings you organized or accepted that had a response rate over 50%
* **Joined on time** – Online meetings (on Microsoft Teams) you joined within five minutes of the scheduled start time
* **No overlap with other meetings** – Meetings that didn't overlap with other meetings on your calendar
* **RSVP'd to invite** – Meetings you were invited to and either accepted or declined (that is, you didn't leave your status as **Tentative**)
* **You didn't multitask** – Meetings where you didn't read or send emails or chats

#### Meeting exclusions

These types of meetings are excluded from meeting metrics—that is, they don't factor into the habits you see in this section.

* Meetings that are 24 hours or longer, which include meetings marked as **All day** 
* Meetings marked as **Private**
* Meetings where you're the only participant, like when you block focus time in your calendar or set reminders
* Meetings with a **Show As** status set to one of these:
    * Free
    * Working Elsewhere
    * Tentative
    * Out of Office

>[!Note]
>Viva Insights counts double-booked meetings only one time for metric calculations. For example, if you have two meetings scheduled for 10:00 AM to 11:00 AM on the same day, Viva Insights counts this as only one hour of meeting time.

## Teamwork

### Network

#### Communication habits

Let's discuss how Viva Insights arrives at the numbers you see in **Communication habits**.

##### Email  

**Emails sent** and **Emails read** estimate how much time you've spent sending and reading emails across all devices, like laptops and mobile phones. 

To figure out which emails to include in its **Emails read** calculations, Viva Insights uses an email's **To** and **Cc** lines. If you, or a group you're a member of, are on an email's **To** or **Cc** line, Viva Insights uses that email to calculate **Emails read**. Viva Insights *doesn't* use emails you delete without opening in its calculations.

###### Sending and reading time

For each email you *send*, Viva Insights assigns five minutes of sending time. For each email you *open*, Viva Insights assigns two and a half minutes of reading time.

However, in the following situations, Viva Insights assigns shorter times:  

* You send one email and then open or send another one within five minutes. In this case, Viva Insights assigns the time between the two actions to the *first* email (that is, the sent email).
* You open one email and then open or send another one within two and a half minutes. In this case, Viva Insights also assigns the time between the two actions to the first email (that is, the opened email).  

>[!Note]
>The time you spend sending or reading email outside your Outlook-defined working hours affects some insights you get on the **Wellbeing** tab.  

##### Chats and calls  

Your audio calls, video calls, and chats in Teams also count as collaboration activities. Here's how Viva Insights calculates those activities:

###### Chats

For each chat you *send*, Viva Insights assigns 30 seconds of sending time. Viva Insights doesn't assign any time for chats received, because the time you spend sending chats is a good indicator of how much time you spent in a chat conversation.

Viva Insights counts all chats you send within a 15-minute window as one chat.

>[!Note]
>Viva Insights doesn't use chats from Teams channels in its calculations.

###### Calls

For each call that isn't scheduled as a meeting on your calendar, Viva Insights uses the actual duration of the call. Viva Insights doesn't assign any time for calls scheduled as meetings in your calendar, because it's already counting those calls as meeting time. 

##### Insight calculation reference

|Insight | Time assigned|
|----|----|
|Emails sent| 5 minutes
|Emails read| 2.5 minutes
|Chats sent| 30 seconds
|Chats read| 0 seconds
|Unscheduled calls| Call duration
|Scheduled calls| 0 seconds


