---
# Metadata Sample
# required metadata

title: Email read statistics in Insights
description: See what proportion of recipients opened email from you in Insights
author: paul9955
ms.author: v-midehm
ms.date: 08/13/2019
ms.topic: article
localization_priority: normal 
ms.prod: mya
---

_**Applies to:** MyAnalytics elements are available in varying levels to users of different Microsoft Office 365 and Microsoft 365 plans. See [MyAnalytics plans and environments](../../overview/plans-environments.md) for details._ 

Insights can tell you how many people have opened your emails and the average time they spent reading those emails. In general, it informs you about emails that you sent to five or more Office 365 users who are internal to your organization. (For more information about which email messages are reported about, see [Reporting details](#reporting-details).) 

After you send an email message, it takes up to thirty minutes before Insights can inform you about it. 

Insights shows the open rate for the sent email that is open in Outlook. It also groups open rate information for qualifying sent items into a single summary card that you can select and expand to see a more detailed view.

### Reporting details

Insights does not display read information about every email that you send. Please note the following circumstances.

#### Requirement: qualifying messages

Read statistics are shown only for _qualifying messages_. A qualifying message is an email message that is sent to five or more qualifying recipients. A qualifying recipient is a person who is in the same company as the sender, has a cloud mailbox, and has not opted out of Insights.

#### Exceptions to qualifying messages

Insights does not report about email messages in the following categories:

 * Email that was sent from a shared mailbox
 * Email that was sent to a mailbox that was configured for email forwarding. (Recipients of forwarded email are not included in the count of qualifying recipients.)
 * Email that was sent more than 14 days ago.
 * Email in which the total number of recipients (the sum of all of the recipients in the To:, Cc:, and Bcc: fields) is less than five.

#### Open rate

The Insights add-in reports the open rate of qualifying emails that you have sent, as shown in the following table. Note that for low or high open rates, only imprecise percentages are displayed.  

| Number of recipients | Actual open rate | Open rate that Insights reports | 
| ------- | -------- | ------- |
| 5 - 10  | < 25%    | "< 25%" |
| 5 - 10  | 25 - 75% | _actual open rate_ |
| 5 - 10  | > 75%    | "> 75%" |
| 11 - 20 | < 10%    | "< 10%" |
| 11 - 20 | 10 - 90% | _actual open rate_ |
| 11 - 20 | > 90%    | "> 90%" |
|  > 21   | < 5%     | "< 5%"  |
|  > 21   | 5 - 95%  | _actual open rate_ |
|  > 21   | > 95%    | "> 95%" |

User privacy is the reason that the imprecise values (such as "< 25%" or "> 90%") are reported for the open rate. For more information, see the [Email read rates](../../overview/privacy-guide.md#email-read-rates) section in the [MyAnalytics privacy guide](../../Overview/privacy-guide.md). 

[!INCLUDE [See info about a specific email message](../../Includes/to-see-info-about-email-message.md)]
