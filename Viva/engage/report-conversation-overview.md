---
ms.date: 12/14/2022
title: "Report a Viva Engage conversation"
description: "Configure conversation reporting in Viva Engage to enable people to report conversation starter posts and comments that don't follow guidelines or policies."
ms.reviewer: ethli
ms.author: v-whitfieldd
author: dwhitfield233
manager: dmillerdyson
audience: Admin
f1.keywords:
- NOCSH
ms.topic: article
ms.service: viva
ms.subservice: viva-engage
localization_priority: Priority
ms.collection:  
- M365initiative-viva
- highpri
search.appverid:
- MET150
---

# Report a Viva Engage conversation

Viva Engage tenants have access to a feature that lets users in the network report conversations, comments, and replies in Viva Engage that don't follow guidelines or policies.

Engage admins can enable user reporting from the Engage admin center: Go to the **Setup & Configuration** tab and select **Configure Tenant**. You're redirected to the Yammer admin webpage, where you can access **Report a conversation** under **Content & Security** in the left panel.

:::image type="content" source="../media/yammer-conversations-admin-report-conversations.png" alt-text="Screenshot showing Jammer reporting settings.":::

## Set up the conversation report feature

:::image type="content" source="../media/yammer-conversations-full-admin-panel.png" alt-text="Screenshot showing Hammer reporting admin panel.":::

After you enable conversations, enter information for the following two settings:

- **Report recipient (an organization email address)** - The email address where reports will be sent.
- **Pre-submission details or instructions for user** – This text is shown to users when they select **Report a Conversation**.

There’s also an optional **Post-submission instructions to user** setting. These instructions are shown to users after they submit a report on a conversation or comment.

## Report recipient

You need to provide an organization email address where the reports will be sent.

> [!NOTE]
> Viva Engage doesn't verify that the email address you enter is an organization email address. Make sure you enter a valid organization email address.

## Pre-submission details or instructions for user

The text entered in this field is shown to end users when they start to submit a report so that they understand the process. You can enter a maximum of 1,500 characters.

Some things you may want to include:

- Details you want users to submit when reporting conversations or replies
- Who in your organization the report goes to
- The next steps in the process
- A link to company network usage guidelines

The text you enter is displayed under the **Report Conversation** or **Report Comment** header when a user reports a conversation or comment. 

:::image type="content" source="../media/yammer-conversations-report-comment.png" alt-text="Screenshot showing reporting a conversation.":::

## Post-submission instructions to user

Use this field to explain to your employees what will happen after they submit a report. This text is optional. Your users will see it under a *You’ve successfully reported a conversation* message. You can enter a maximum of 1,500 characters. Some things you may consider want to include:

- When the user can expect a response
- Next steps for the organization 

## End user experience for reporting conversations

When this feature is enabled, users accessing Viva Engage see the **Report Conversation** option on conversation starters and **Report Comment** on comments and replies.

:::image type="content" source="../media/yammer-conversations-report-dropdown.png" alt-text="Screenshot showing user reporting for conversation starter.":::

**Report Conversation option on conversation starter**

:::image type="content" source="../media/yammer-conversations-report-comment-dropdown.png" alt-text="Screenshot showing user reporting for comment.":::

**Report Conversation option on conversation comment**

Users will then see a right-panel pop-out with the custom message from the Engage admin and a required **Reason for Reporting** box.

:::image type="content" source="../media/yammer-conversations-report-comment.png" alt-text="Screenshot showing reason for reporting box.":::

The conversation or comment reported, along with who is reporting and the reason for reporting, is sent to the email address that's specified in the **Report Conversations** settings.

Upon successful submission, the user sees the optional custom message configured by the admin. They also receive a confirmation message with a link to the conversation, comment, or reply reported and the comment included in the report.

:::image type="content" source="../media/yammer-conversations-report-submitted-panel-closeup.png" alt-text="screenshot showing success reporting submission.":::

## Report emails

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

**A:** No, the feature is turned off by default. An Engage admin must turn on the feature for users so they can see the option to report conversations and comments.

**Q:** Can users report conversations from external networks?

**A:** No. The report conversations functionality is only available in the Viva Engage home network. Conversations in external networks can't be reported.

**Q:** Can users report private messages or messages in the Viva Engage Inbox?

**A:** No, The report conversations functionality is only available on conversations within communities and the discovery feed.

**Q:** Can users report messages from private and secret communities?

**A:** Yes, conversations can be reported from all communities in Viva Engage—public, private, and secret. The email report that's sent includes a link to the original conversation starter where the starter or comment was reported. If the person reviewing the reports doesn't have access to the private or secret community, they can either work with the Engage admin to get access to that community to review the message or with the community administrator to get access to the reported message.

**Q:** Can users report messages from Viva Engage integrations with Teams, Outlook, and SharePoint?

**A:** Currently, conversation reporting is only available from the Viva Engage Teams integration.
