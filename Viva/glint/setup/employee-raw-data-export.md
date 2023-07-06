---
title: Access to Viva Glint raw survey responses
description: Admins can export employee data and raw data from Viva Glint programs.
ms.author: SarahBerg
author: SarahAnneBerg
manager: pamgreen
audience: admin
f1.keywords: NOCSH
keywords: Microsoft Viva Glint, raw data
ms.collection: 
 - m365initiative-viva
 - selfserve
search-appverid: MET150
ms.topic: article
ms.service: viva
localization_priority: high pri
ms.date: 05/22/2023
---

# Access to Viva Glint raw survey responses

## What are raw survey responses?

In Microsoft Viva Glint, "raw survey responses" refers to unaggregated survey responses that are directly tied to the survey taker. By default, customers have access to raw survey responses and can export that data using admin controls. Customers can also use this functionality to respond to users' Data Subject Rights (DSR) requests.

Enabling raw survey response export doesn't mean that survey takers will be identifiable in Viva Glint survey reporting. Reporting will still be aggregated for surveys with a minimum response threshold of three or more. Export of raw survey responses will only be available to your organization through admin controls. Customers should consult with their privacy, HR, and legal teams to determine how to configure raw survey response export in Viva Glint.

Your organization may not want access to raw survey responses for every survey. This could be because of the data's sensitivity, employee privacy concerns, regulatory or contractual obligations (such as works council agreements), or other reasons. To meet this customer need, Viva Glint provides admin controls through which customers can opt out of the raw survey response export functionality on a survey-by-survey basis.

To ensure customers can meet their DSR obligations, Viva Glint provides an alternative solution that allows customers to fulfill DSR requests without accessing the requestors raw survey responses (discussed in more detail below).

Even when a customer has opted out of raw survey response export, the customer can still access this data if they determine certain extreme circumstances exist. [Read more about "extreme circumstances."](https://go.microsoft.com/fwlink/?linkid=2238614)

## Access raw survey responses at the company level

### Enable or disable access to company-level raw survey responses

When setting up each Viva Glint survey, the customer decides whether raw survey response export will be available for the survey.

By default, raw survey responses are available for each new survey program. Admins can choose to opt out of raw survey response export from the **Confidentiality** section of **Program Setup**. **Program Summary** is accessible from the configuration page of the admin dashboard. A program can't be in **Approved** status to enable this feature. As necessary, toggle **Approved** to **NO**.

1. Select **Pulse Programs** in the **Pulses** section.
2. Select the survey and then **Program Setup** on the **Program Summary** page.

The default setting for **Enable Export of Raw Survey Responses** is **YES**. Toggle to **NO** to opt out of raw survey response export. [More information on the confidentiality statement is available here](https://go.microsoft.com/fwlink/?linkid=2238614).

:::image type="content" source="../../media/glint/setup/glint-confidentiality.png" alt-text="Screenshot that displays the confidentiality statement for raw data of Viva Glint." lightbox="../../media/glint/setup/glint-confidentiality.png":::

>[!NOTE]
> Once a survey is live, the availability raw survey response export cannot be changed for that survey.

## Manage Subject requests to access their data

The customer, as the data controller, is responsible for handling certain requests from employees, as data Subjects. Microsoft, the data processor, provides controls in Viva Glint to honor these rights and requests.

Subjects have the right to see what personal information is being processed and Viva Glint provides the export of this raw data, which may contain personal data.

### What if an admin has chosen not to access raw responses?

Viva Glint respects the customer's right as the data controller to maintain the confidentiality of survey responses and prevent the viewing of raw data. However, admins can send this raw data to the requesting employee _without_ personally viewing its contents.

### Export company-level raw data

For surveys, which have a closed cycle where raw survey responses were enabled, customer admins can export raw survey responses from Viva Glint. Company admins can navigate to the Completed cycles tab of the survey program. On the row with the appropriate cycle, select the vertical ellipses (three dots) on the far right. Select **Export raw survey responses**.

For surveys that are always live, such as onboarding surveys, admins can navigate to **Settings** , then **Pulse Programs**. Next choose **Live** status and select a **Lifecycle or Always-On survey program**. In the **Actions** dropdown menu, select **Export raw survey responses**. Select the **Survey Send Date** range desired.

>[!NOTE]
> For both survey types:
>
> - This export option will only be available to admins.
> - This export option will only be enabled for a survey cycle if the raw survey response export was enabled for the selected survey program before the survey went live.

## Supporting requests for raw survey responses from data subjects (DSRs)

The customer, as data controller, is responsible for responding to DSR requests from the organization's Viva Glint users. Read more about DSRs and the role of data controllers in [Advanced privacy guide for data usage and survey item creation](https://go.microsoft.com/fwlink/?linkid=2230859). Microsoft, as data processor, provides controls in Viva Glint that allow customers to respond to meet their DSR obligations.

>[!NOTE]
> Raw survey response export does not need to be enabled to fulfill these requests. Admins can send raw survey responses directly to the user without gaining access and viewing this data.

## Send user data to employees

An admin can export user attributes and raw survey responses from an individual's profile screen in the **People** feature within the **Employee** section on the admin configuration section of the Viva Glint dashboard. Attributes are populated from the data sent to Viva Glint in your HRIS (Human Resources Information System) file. From the Viva Glint admin dashboard, customer admins can export a survey taker's user attributes and raw survey responses and send this data, without viewing it, directly to the survey taker.

:::image type="content" source="../../media/glint/setup/glint-user-data.png" alt-text="Screenshot that displays the user data information.":::

## Export user attributes and raw responses to data Subject

An admin can follow this procedure to export user data:

1. Search for the user in the _Search People_ label.
2. On the user page, select **Send User Data** from the Actions dropdown menu.
3. In the _Send User Data_ slider, all attributes from your HRIS file will be preselected.
   1. Select **Clear All** and then select the attributes you want to export,** or
   2. Individual attributes may be excluded from the export by deselecting them.
4. Along with user attributes, in the slider window, there's the option to **Include raw survey responses**. Enable this feature to include the user's responses to current and closed surveys.

   :::image type="content" source="../../media/glint/setup/glint-raw-data-responses.png" alt-text="Screenshot that displays Viva Glint dashboard.":::

5. Select **Send.** This information will be sent to the employee email address on file. Check that this is correct before selecting **Send**.
6. A banner will appear indicating that your export has been sent successfully.
7. The employee will receive an email with their Glint data attached in a .csv file.

>[!TIP] 
> For information on how to support a DSR request to delete data, visit [https://go.microsoft.com/fwlink/?linkid=2236554](https://go.microsoft.com/fwlink/?linkid=2236554).