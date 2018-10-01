---
# Metadata Sample
# required metadata

title: Chats and calls in MyAnalytics
description: The display of chats and calls in MyAnalytics. 
author: buntus
ms.author: v-pascha
ms.date: 07/25/2018
ms.topic: get-started-article
localization_priority: normal 
ms.prod: mya
---

## Chats and calls

MyAnalytics counts audio calls, video calls, and chats that people make in Skype for Business Online as collaboration activities. It calculates the duration of these activities this way: 

### Chats in Skype for Business Online

 * Every Skype for Business Online chat message that you send counts as 30 seconds.
 * Every Skype for Business Online chat message that you receive counts as 0 seconds. This is because it has been empirically determined that the sent-messages time is a good predictor of the total duration of the Skype session.

### Calls in Skype for Business Online

 * For every ad hoc call in Skype for Business Online, MyAnalytics uses the actual duration of the call. An "ad hoc" call is a call that does not appear in the Outlook calendar. 
 * For any Skype for Business Online call that is also a meeting on the Outlook calendar, the time counts as 0. This is because the time is already being counted as a meeting on the calendar.


  >[!Note]
  > Skype-for-Business data is usually prompt. However, in rare instances, users can experience delays of from two to four days. For more information see [MyAnalytics FAQ](../../Overview/MyA-faq.md)