---
title: Support participants during a live Viva Glint survey
description: "During a live Viva Glint survey, participants can use online support content to answer many of their questions. Take additional steps listed here to set up users for success to submit their valuable feedback."
ms.author: aweixelman
author: AliciaWeixelman
manager: skaradzic
audience: admin
f1.keywords: NOCSH
keywords: survey taker, survey participant, live survey, support
ms.collection:  
- m365initiative-viva
- selfserve 
search.appverid: MET150 
ms.topic: article
ms.service: viva
ms.subservice: viva-glint
ms.localizationpriority: high
ms.date: 02/13/2024
---

# Support survey participants during a live Viva Glint survey

Introduce Viva Glint surveys and [communicate proactively](https://go.microsoft.com/fwlink/?linkid=2241178) with your organization about upcoming surveys. During a live Viva Glint survey, participants can use [online support content](https://go.microsoft.com/fwlink/?linkid=2239301) to answer many of their questions. Take steps listed here to set up users for success to submit their valuable feedback.

## Create an FAQ document

Use the [Viva Glint FAQ template](survey-taker-faq.md) to create your own internal document to address commonly asked questions in your organization. Include how users are eligible to participate, what to do if users run into login issues, the survey start and end dates, the sending email address for survey emails, and the [resend survey link](#use-the-viva-glint-survey-invite-link) filled in with your company ID.

## Allow survey resubmission

Use the Allow Survey Resubmission feature during survey [program setup](https://go.microsoft.com/fwlink/?linkid=2238328) so that participants can resubmit their responses by selecting a link on the survey Thank You page.

:::image type="content" source="../../media/glint/setup/vg-survey-resubmit.png" alt-text="Screenshot of the Thank You page with survey resubmission enabled.":::

## Manage authentication issues

Your organization may require that you authenticate with Microsoft Entra to access surveys in Viva Glint. If users encounter any issues when logging in, the following articles help with common troubleshooting topics related to multi-factor authentication. Route Microsoft Entra login issues to your IT help desk.

- [Common problems with two-step verification for a work or school account](https://go.microsoft.com/fwlink/?linkid=2260397)
- [Troubleshoot problems using Microsoft Authenticator](https://go.microsoft.com/fwlink/?linkid=2260398)

## Confirm eligibility

If a user reaches out because they weren't included in a survey, use Viva Glint to confirm whether they should receive a survey invite. In the configuration section, select **Survey Programs** and then choose your live survey. In the **Distribution section**, confirm which lists are included and excluded. To confirm their eligibility, review Distribution Lists and the requesting user’s profile.

:::image type="content" source="../../media/glint/setup/vg-distribution.png" alt-text="Screenshot of a survey distribution setup with included and excluded employee groups.":::

## Validate credentials for attribute-based survey access

Your organization may use [attribute-based access](https://go.microsoft.com/fwlink/?linkid=2230745), which is often set up for access with a QR code or shortened link. If a user sees a "could not validate credentials" message, they'll reach out to confirm their details. To confirm a user’s credentials, go to Viva Glint Advanced Configuration. Export their information as it was when the survey launched with the [Export Users from a Survey Cycle Data App](https://go.microsoft.com/fwlink/?linkid=2245700).

## Resend survey invites

### Use the Resend Survey option in Viva Glint

If a user should have been eligible for a survey but wasn’t included at the time of launch, use the Viva Glint [Send Survey](https://go.microsoft.com/fwlink/?linkid=2230865) option to send an invite during a live survey. In the configuration section, select People and search for a user. After selecting their profile, select Actions and choose Send Survey, which will send in invite email.

### Use the Viva Glint survey invite link

Any user in your organization can use the resend survey link to resend invites for all a user’s active surveys. Replace the **‘companyID’ with your own in the URL** (as an admin, go to General Settings and confirm the Client UUID value as your company ID). Enter a user’s email address and select **Email Survey Invite** to resend emails.

- US server: https://app.us1.glint.cloud.microsoft/companyID/q2/resend-pulse
- EU server: https://app.eu1.glint.cloud.microsoft/companyID/q2/resend-pulse 

:::image type="content" source="../../media/glint/setup/vg-resend-url-page.png" alt-text="Screenshot of the Viva Glint resend survey landing page.":::

## Be mindful of scheduled monthly maintenance

To strive for consistent improvement, Viva Glint undergoes [monthly maintenance](https://go.microsoft.com/fwlink/?linkid=2250774) to release new features, enhancements, and fixes. If when attempting to access a survey, users are presented with a maintenance message, ask them to revisit the survey the following day.


