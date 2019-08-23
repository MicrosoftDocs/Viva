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

Insights can tell you how many people have opened your emails and how long they spent reading them. In general, it informs you about emails that you sent to five or more Office 365 users who are internal to your company. (For more information about which email messages are reported about, see [Reporting details](#reporting-details).) 

After you send an email message, it takes up to fifteen minutes before Insights can inform you about it. Insights groups similar information into a single summary card that you can select and expand to see a more detailed view.

### Reporting details

Insights does not display read information about every email that you send. Please note the following circumstances.

#### Requirement: qualifying messages

Read statistics are shown only for _qualifying messages_. A qualifying message is an email message that is sent to five or more qualifying recipients. A qualifying recipient is a person who is in the same company as the sender, has a cloud mailbox, and has not opted out of Insights.

#### Other exceptions

Insights does not report about email messages in the following categories:

 * Email that was sent from a shared mailbox
 * Email that was sent to a mailbox that was configured for email forwarding. (Recipients of forwarded email are not included in the count of qualifying recipients.)
 * Email in which the individual recipient count on each of the To: and Cc: lines is less than 5 AND the Bcc: individual recipient count is also less than 5.
 * Email that was sent more than 14 days ago.

#### Bcc: precision

When you send email that has recipients on the Bcc: line, the precision of the email-read statistics is lowered.

#### Open rate

The Insights add-in reports the open rate of qualifying emails that you have sent. The following table describes how Insights reports the open rate of a particular email:  

<!-- This table, in md, didn't work for some reason
| Number of people who read your email | Reported read activity | 
| ----- | ----- | 
| 0 or 1 readers | "Low" |
| <i>n</i> or <i>n</i>-1 readers, where <i>n</i> is the total number of <p></p>recipients of the email that you sent | "High" |
| all other numbers | the exact read percent |
So resorting to HTML:  -->

<table>
<thead>
<tr>
	<th>Number of people who read your email</th>
	<th>Open rate</th>
</tr>
</thead>
<tbody>
<style>
table, td {
    text-align: left;
}
.percentage {
    width: 60%;
}
.no-border {
    border-bottom: none;
}
}
</style>
        <tr class="no-border">
        	<td class="percentage">0 or 1 readers</p></th>
        	<td>"Low"</td>
        </tr>
        <tr class="no-border">
        	<td class="percentage"><i>n</i> or <i>n</i>-1 readers, where <i>n</i> is the total number of recipients of the email that you sent</p></th>
        	<td>"High"</td>
        </tr>
        <tr class="no-border">  
        	<td class="percentage">all other numbers of readers</p></th>
        	<td >the exact read percent</td>
        </tr>
</tbody>
</table>

User privacy is the reason that the imprecise values ("Low" and "High") are reported for read activity. For more information, see the [Email read rates](../../overview/privacy-guide.md#email-read-rates) section in the [MyAnalytics privacy guide](../../Overview/privacy-guide.md). 

**To see read information about sent emails**

1. On the **Home** ribbon, select the **Insights** icon. If the Insights panel isn't already open, it opens now. 

   > [!Note] 
   > If you see a "Welcome!" message, select **Get started**.

2. On the **Insights** panel, locate the **Track email open rates** card: 

    ![Track email open rates](../../../Images/mya/use/step-1-track-open-rates.png)

3. This card lets you see more information about recent emails that you've sent. To see this information, select the **Track email open rates** card.

4. The panel displays insight cards for each of these recently sent messages These cards state the subject line, a brief summary of the open rate, the open rate (sometimes expressed as a percentage), and the number of forwards.

    ![Email open rates](../../../Images/mya/use/step-2-four-emails.png)

<!--
    Based on the length of the message, Insights estimates how long a person needs to read it. It uses that number to decide whether people glanced, skimmed, or read the email, and informs you of this in a card.
 
    ![Email open rates](../../Images/mya/use/email-open-rates-2.png)

    Depending on how many people opened the email and how long they spent reading it, Insights might suggest that you follow up on your email, or it might show tips to help improve email communication.
-->
