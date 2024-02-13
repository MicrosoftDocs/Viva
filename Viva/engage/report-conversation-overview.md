---
ms.date: 11/15/2023
title: "Report a Viva Engage conversation"
description: "Configure conversation reporting in Viva Engage to enable people to report conversation starter posts and comments that don't follow guidelines or policies."
ms.reviewer: ethli
ms.author: mamiejohnson
author: dwhitfield233
manager: dmillerdyson
audience: Admin
f1.keywords:
- NOCSH
ms.topic: article
ms.service: viva
ms.subservice: viva-engage
ms.localizationpriority: medium
ms.collection:  
- M365initiative-viva
- highpri
search.appverid:
- MET150
---

# Report a Viva Engage conversation

Viva Engage admins can empower users across the network to report conversations and comments that don't follow organizational guidelines or policies. An admin can turn on the **Report conversations** option in the Viva Engage admin center to set this up. The options in the admin center change, however, depending on whether you have a license that includes Microsoft Purview Communication Compliance:

- **Licenses that don't include communication compliance**. If you don't have a license that includes communication compliance, when the option is turned on, the Viva Engage admin can specify an email address to receive reported conversations. The admin can also enter pre-submission instructions and post-submission confirmations for the user as described in this article. 

- **Licenses that do include communication compliance**. If you do have a license that includes communication compliance, when the option is turned on, any reported conversations are automatically routed through communication compliance for investigation and remediation. [Learn more about routing reported conversations through Microsoft Purview Communication Compliance](/purview/communication-compliance-policies)
 
## Enable conversation reporting if you don't have a license that includes communication compliance

1. In the Viva Engage admin center, on the **Setup & Configuration** tab, select **Tenant settings**. 

2. On the Tenant settings page, under **Other**, select **Manage other tenant configurations through the Yammer admin center**.

3. Under **Content & Security** on the left panel, select **Report conversations**.

    :::image type="content" source="../media/viva-engage-conversations-admin-report-conversations.png" alt-text="Screenshot that shows reporting settings.":::

4. After you enable conversations, enter information for the following two settings:

    - **Report recipient (an organization email address)** - Provide an organization email address where reports are sent. Viva Engage can't verify that the email address you enter is an organization email address.  

    - **Pre-submission details or instructions for user** – Provide messaging that explains the reporting process to users when they select **Report a Conversation**.  

For example, explain who in your organization their report goes to and next steps in the process. If possible, provide a link to your company network usage guidelines. Limited to 1,500 characters.

5. Optionally, use the **Post-submission instructions to user** setting to explain to your employees what happens after they submit a report. For example, set expectations for when the submitter can expect a response and next steps for the organization. Limited to 1,500 characters.  

    :::image type="content" source="../media/viva-engage-conversations-full-admin-panel.png" alt-text="Screenshot shows the reporting admin panel.":::

### End user experience

When this feature is enabled, users accessing Viva Engage see the **Report Conversation** option on conversation starters and **Report Comment** on comments and replies.

:::image type="content" source="../media/viva-engage-conversations-report-dropdown.png" alt-text="Screenshot showing user reporting for conversation starter.":::

**Report Conversation option on conversation starter**

:::image type="content" source="../media/viva-engage-conversations-report-comment-dropdown.png" alt-text="Screenshot showing user reporting for comment.":::

**Report Conversation option on conversation comment**

Users can find a right-panel pop-out with a custom message from the Engage admin and a required **Reason for Reporting** box.

:::image type="content" source="../media/viva-engage-conversations-report-comment.png" alt-text="Screenshot showing reason for reporting box.":::

The reported conversation or comment, the user who reports the comment, and their reason for reporting, is sent to the email address that's specified in the **Report Conversations** settings.

Upon successful submission, the user sees the optional custom message configured by the admin. They also receive a confirmation message that includes their report and a link to the reported conversation, comment, or reply.

:::image type="content" source="../media/viva-engage-conversations-report-submitted-panel-closeup.png" alt-text="screenshot showing success reporting submission.":::

### Email reports

When a report is submitted, email is sent to the organization email address set for **Report Conversations** in the admin settings. It includes the following information:

- The name of the person who submitted the report.
- Whether a conversation starter or comment is being reported. The title and text of the email indicates whether a conversation starter or comment is being reported.
- The name of the person who started the conversation or wrote the comment being reported.
- The community in which the reported conversation or comment was made.
- The date and time at which the reported conversation or comment was made.
- A link to the specific conversation starter.
- Any comments entered by the reporting user.

> [!NOTE]
> Viva Engage doesn't currently support deep links to comments. In the report emails for both conversation starters and comments, the link that's reported is always the conversation starter link. Reports don't contain deep links to a reported comment. The report reviewer can use the conversation starter link together with the reported comment timestamp to find the actual reported comment in the conversation.

A copy of this email is also sent to the Viva Engage user who submitted the report.

## FAQ

**Q:** I’m an admin. How do I know if my Viva Engage network is eligible for reporting conversations and comments?

**A:** All tenants that have Viva Engage configured for their organization, either seeded or premium, are eligible for the reporting conversations experience.

**Q:** Can I add multiple email addresses for the reports to go to?

**A:** Currently only one email can be used. We suggest you use a group email or distribution list alias if you want the reports to go to multiple people.

**Q:** If my Viva Engage network is eligible for this functionality, is it already on?

**A:** No, the feature is turned off by default. A Viva Engage admin must turn on the feature for users so they can see the option to report conversations and comments.

**Q:** Can users report conversations from external networks?

**A:** No. The report conversations functionality is only available in the Viva Engage home network. Conversations in external networks can't be reported.

**Q:** Can users report private messages or messages in the Viva Engage Inbox?

**A:** No, The report conversations functionality is only available on conversations within communities and the discovery feed.

**Q:** Can users report messages from private and secret communities?

**A:** Yes, conversations can be reported from all communities in Viva Engage—public, private, and secret. The email report that's sent includes a link to the original conversation starter where the starter or comment was reported. If the person reviewing the reports doesn't have access to the private or secret community, they can work with the Engage admin to get access to that community to review the message. Or, they can work with the community administrator to get access to the reported message.

**Q:** Can users report messages from Viva Engage integrations with Teams, Outlook, and SharePoint?

**A:** Currently, conversation reporting is only available from the Viva Engage Teams integration.

**Q:** How do I route reported conversations through Microsoft Purview Communication Compliance instead of using a single email address to report conversations?

**A:** If you have a license that includes communication compliance, [learn how to take advantage of review and remediation capabilities of Microsoft Purview Communication Compliance](/purview/communication-compliance-policies).
