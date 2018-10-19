---
# Metadata Sample
# required metadata

title: Email read statistics in MyAnalytics
description: See what proportion of recipients opened email from you in MyAnalytics.
author: paul9955
ms.author: v-pascha
ms.date: 07/19/2018
ms.topic: get-started-article
localization_priority: normal 
ms.prod: mya
---

## Email read statistics 

MyAnalytics can tell you how many people have opened your emails and how long they spent reading them. In general, it informs you about emails that you sent to five or more Office 365 users who are internal to your company. (For more information about which email messages are reported on, see [Reporting details](#reporting-details).) 

<!-- REMOVED PER NOELLE 24 AUGUST 2018: 
It displays this information in "cards," such as this one:

<img src="../../../Images/mya/use/Still-updating.png" alt="Still updating">
-->

After you send an email message, it takes up to fifteen minutes before MyAnalytics can inform you about it. MyAnalytics groups similar information into a single summary card that you can select and expand to see a more detailed view.

### Reporting details 
MyAnalytics does not display read information about every email that you send. Please note the following circumstances: 

#### Requirement: qualifying messages 
Read statistics are shown only for _qualifying messages_. A qualifying message is an email message that is sent to five or more qualifying recipients. A qualifying recipient is a person who is in the same company as the sender and has not opted out of MyAnalytics.

#### Other exceptions 
MyAnalytics does not report about email messages in the following categories: 
 * email that was sent from a shared mailbox
 * email that was sent to a mailbox that was configured for email forwarding. (Recipients of forwarded email are not included in the count of qualifying recipients.)
 * email in which the individual recipient count on each of the To: and Cc: lines is less than 5 AND the Bcc: individual recipient count is also less than 5.

#### Bcc: precision
When you send email that has recipients on the Bcc: line, the precision of the email-read statistics is lowered. 

#### Read percentage

The MyAnalytics add-in reports the "read activity" of a qualifying email that you have sent. The following table describes how MyAnalytics calculates its reported display of read activity for a particular email:  
<!-- This table, in md, didn't work for some reason
| Number of people who read your email | Reported read activity | 
| ----- | ----- | 
| 0 or 1 readers | "Low" |
| <i>n</i> or <i>n</i>-1 readers, where <i>n</i> is the total number of <p></p>recipients of the email that you sent | "High" |
| all other numbers | the exact read percent |
So resorting to HTML:  -->

<table align="left">
<thead>
<tr>
	<th>Number of people who read your email</th>
	<th>Reported read activity</th>
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

[!INCLUDE [See info about a specific email message](../../Includes/to-see-info-about-email-message.md)]
