---
# Metadata Sample
# required metadata

title: Chats and calls in MyAnalytics
description: The display of chats and calls in MyAnalytics. 
author: paul9955
ms.author: v-pascha
ms.date: 01/14/2018
ms.topic: get-started-article
localization_priority: normal 
ms.prod: mya
---

## Chats and calls

MyAnalytics counts audio calls, video calls, and chats that people make in Teams and in Skype for Business as collaboration activities. It calculates the duration of these activities this way: 

### Chats in Teams and in Skype for Business

 * Every chat message that you send counts as 30 seconds.
 * Every chat message that you receive counts as 0 seconds. This is because it has been empirically determined that the sent-messages time is a good predictor of the total duration of the Teams session or Skype for Business session.

### Calls in Teams and in Skype for Business

 * For every ad hoc call, MyAnalytics uses the actual duration of the call. An "ad hoc" call is a call that does not appear in the Outlook calendar. 
 * For any call that is also a meeting on the Outlook calendar, the time counts as 0. This is because the time is already being counted as a meeting on the calendar.

  >[!Note]
  > Skype for Business data is usually prompt. However, in rare instances, users can experience delays of two to four days. For more information see [MyAnalytics FAQ](../../Overview/MyA-faq.md)