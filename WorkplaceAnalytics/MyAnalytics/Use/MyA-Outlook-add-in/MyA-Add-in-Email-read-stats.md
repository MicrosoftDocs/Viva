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

The Insights add-in reports the open rate of qualifying emails that you have sent, as shown in the following table. Note the following:

* For open rates lower than the minimum threshold, the threshold value itself is reported. Example: If an email with 10 recipients has an actual open rate of 20%, Insights displays the open rate as _&lt; 25%_. 
* If the actual open rate falls between the "Minimum" and "Maximum" value, then the actual open rate is reported. 
* For open rates higher than the maximum threshold, the threshold value itself is reported. Example: If 100% of the recipients of an email open it, only the value shown in the table for "Maximum" is displayed; for example: _&gt; 95%_. 

   | Number of recipients | Open rate reported |
   | ------- | ------ |
   | 5 - 10  | Minimum: 25% <br>Maximum: 75% |
   | 11 - 20 | Minimum: 10% <br>Maximum: 90% |
   | &gt; 21 | Minimum: 5%  <br>Maximum: 95% |

MyAnalytics respects user privacy; this is why imprecise values are reported for particular email open rates. For more information, see the [Email read rates](../../overview/privacy-guide.md#email-read-rates) section in the [MyAnalytics privacy guide](../../Overview/privacy-guide.md). 



<!-- HERE'S A CLEARER TABLE BUT THEY WANTED A SHORTER TABLE
<table>
  <tr>
    <th>Number of recipients</th>
    <th>Actual open rate</th>
    <th>Open rate that Insights reports</th>
  </tr>
  <tr>
    <td rowspan = 3 >5 - 10</td>
    <td>&lt; 25%</td>
    <td>"&lt; 25%"<td>
  </tr>
  <tr>
    <td>25 - 75%</td>
    <td><i>actual open rate</i></td>
  </tr>    
  <tr>
    <td>&gt; 75%</td>
    <td>"&gt; 75%"</td>
  </tr>  
  <tr>
    <td rowspan = 3 >11 - 20</td>
    <td>&lt; 10%</td>
    <td>"&lt; 10%"<td>
  </tr>
  <tr>
    <td>10 - 90%</td>
    <td><i>actual open rate</i></td>
  </tr>    
  <tr>
    <td>&gt; 90%</td>
    <td>"&gt; 90%"</td>
  </tr>
  <tr>
    <td rowspan = 3>> 21</td>
    <td>&lt; 5%</td>
    <td>"&lt; 5%"<td>
  </tr>
  <tr>
    <td>5 - 95%</td>
    <td><i>actual open rate</i></td>
  </tr>    
  <tr>
    <td>&gt; 95%</td>
    <td>"&gt; 95%"</td>
  </tr>     
</table>
-->

[!INCLUDE [See info about a specific email message](../../Includes/to-see-info-about-email-message.md)]
