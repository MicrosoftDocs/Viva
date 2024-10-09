---
ROBOTS: NOINDEX, NOFOLLOW
ms.date: 10/09/2024
title: Viva Insights Outlook add-in reference
description: Learn more about insights in the Viva Insights Outlook add-in
author: zachminers
ms.author: v-zachminers
ms.topic: conceptual
ms.localizationpriority: medium 
ms.service: viva-insights
ms.collection: 
- M365-analytics
- viva-insights-personal
manager: anirudhbajaj

---

# Reporting details in the Viva Insights Outlook add-in


Viva Insights doesn't display read information about every email that you send, such as in the following circumstances.

## Qualifying messages requirement

Read statistics are shown only for _qualifying messages_. A qualifying message is an email message that is sent to five or more qualifying recipients. A qualifying recipient is a person who is in the same company as the sender and has a cloud mailbox. Distribution lists are expanded before counting qualifying recipients.

## Exceptions to qualifying messages

Viva Insights doesn't report about email messages in the following categories:

* Email that was sent from a shared mailbox
* Email that was sent more than 14 days ago.
* Email in which the total number of recipients (the sum of all of the recipients in the To:, Cc:, and Bcc: fields) is less than five.
* Email sent to modern groups. (If users are following the modern group, they're included in the count.)

## Open rate

Viva Insights respects user privacy. For this reason, the Viva Insights add-in doesn't show information about individual recipients, and when necessary to protect privacy, it reports approximated values only.

Within 30 minutes of when you sent qualifying email, the Viva Insights add-in  reports the actual or an approximated open rate, as described here:

* **Below minimum.** For open rates lower than the minimum threshold, the threshold value is reported. For example, when 20% of 10 email recipients open the email, Viva Insights displays the open rate as "_&lt; 25%_."
* **Between thresholds.** If the actual open rate falls between the "Minimum" and "Maximum" values shown in the table, then the actual open rate is reported.
* **Above maximum.** For open rates higher than the maximum threshold, the threshold value is reported. For example, when 96% of the 25 email recipients open the email, Viva Insights displays the open rate as "_&gt; 95%_."

   | Number of recipients | Open rate reported |
   | ------- | ------ |
   | 5 - 10  | Minimum: 25% <br>Maximum: 75% |
   | 11 - 20 | Minimum: 10% <br>Maximum: 90% |
   | &gt; 21 | Minimum: 5%  <br>Maximum: 95% |

 For more information, see "Email read rates and document open rates" in the [Personal insights privacy guide](https://support.microsoft.com/topic/8f2c038c-f80c-4512-bf4c-90a0423377f2). To see who opened an email, use [Outlook's request read receipts](https://support.office.com/article/add-and-request-read-receipts-and-delivery-notifications-a34bf70a-4c2c-4461-b2a1-12e4a7a92141).
