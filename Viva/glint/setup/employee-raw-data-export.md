---
title: Access Viva Glint raw survey responses
description: Admins can export employee data and raw data from Viva Glint programs.
ms.author: JudithWeiner
author: JudyWeiner
manager: MelissaBarry
audience: admin
f1.keywords: NOCSH
keywords: Microsoft Viva Glint, raw data, extreme circumstance
ms.collection: 
 - m365initiative-viva
 - selfserve
 - essentials-compliance
 - essentials-security
search-appverid: MET150
ms.topic: article
ms.service: viva-glint
ms.localizationpriority: high
ms.date: 05/14/2024
---

# Access Viva Glint raw survey responses

## What are raw survey responses?

In Microsoft Viva Glint, "raw survey responses" refers to unaggregated survey responses that are directly tied to a survey taker. By default, Microsoft 365 Global admins have access to raw survey responses and can export that data using admin controls. 

> [!NOTE]
> "Raw survey responses export" can also be referred to as "Raw data export."

> [!IMPORTANT]
> Customers can use program setup features to respond to users' Data Subject Rights (DSR) requests.
>
> For information on how to support a request to delete data, visit [Delete user data from Viva Glint](https://go.microsoft.com/fwlink/?linkid=2236554).

## Acting on Data Subject Requests (DSRs) from data subjects 

Viva Glint admins, who are assigned by your Microsoft 365 Global admin, are in control of your organization’s data. This role – Data Controller – can act on Data Subject Rights requests from Viva Glint survey takers. [Read more about DSR obligations.](/../../viva/glint/setup/gdpr-special-categories)

>[!NOTE]
> Raw survey response export doesn't need to be enabled to fulfill these requests. Admins can send raw survey responses directly to the survey taker without gaining access and viewing this data.

## Does enabling raw survey response export make survey takers identifiable in reporting?

Export of raw survey responses is only available to your organization through admin controls. Viva Glint admins should consult with their privacy, HR, and legal teams. 

>[!NOTE]
> Reporting is aggregated for surveys with a minimum threshold of three (3) or more respondents.

## Configure raw survey response access
Your organization may not want access to raw survey responses for every survey. This data access decision could be because of the data's sensitivity, employee privacy concerns, regulatory or contractual obligations (such as Works Council agreements), or other reasons. Your role as the Viva Glint admin provides permissions for you to configure them at your discretion.

> [!IMPORTANT]
> When setting up each Viva Glint program, the Viva Glint admin decides whether raw survey response exports are available. Raw survey export does *not* need to be enabled for an employee to request their personal data.

## Admins can opt out of response exports

By default, raw survey responses are available for each new program, but Microsoft 365 Global admins and Viva Glint admins can opt out of response exports. 

### Procedure to opt of our response exports
Opting out of response exports occurs within the *Confidentiality* section of *Program Setup*. Program Summary is accessible from the *Survey Programs* configuration page of the admin dashboard. 

1. Select **Survey Programs** in the *Survey* section.
1. Select the survey and then **Program Setup** on the *Program Summary* page.

>[!NOTE]
> A program can't be in *Approved* status to enable this feature. As necessary, toggle *Approved* to **NO**. The default setting for *Enable Export of Raw Survey Responses* is **YES**. Toggle to NO to opt out of raw survey response export. [Read more about the confidentiality statement](https://go.microsoft.com/fwlink/?linkid=2238614).

To ensure customers meet their Data Subject Rights (DSR) obligations, Viva Glint provides an alternative solution, allowing customers to fulfill DSR requests without accessing the requestors raw survey responses. Read on.

> [!IMPORTANT]
> Even when an admin has opted out of raw survey response exports, the Glint admin can still access data if it meets **extreme circumstance** criteria. It's possible that Glint needs to disclose survey feedback when there is a good faith belief that disclosure is reasonably necessary to protect your safety, the rights and safety of Glint personnel or others, or to investigate, prevent or take action regarding suspected illegal activity, suspected fraud, situations involving potential threats to the physical safety of any person, or if otherwise required by law to do so.
>
> The privacy statement complies with GDPR notice requirements.

## Use the People feature to export responses

As the admin, you can export raw survey responses from an individual's profile in the **People** feature within the *Employee* section of your admin dashboard. Attributes are populated from the data sent to Viva Glint in your Human Resources Information System (HRIS)) file. Admins can export a survey taker's user attributes and raw survey responses and send this data - without viewing it - directly to the survey taker.

### Procedure to export user data:

1. Search for the user in the *Search People* label.
1. On the user page, select **Send User Data** from the *Actions* dropdown menu.
1. In the *Send User Data* slider, all attributes from your HRIS file are preselected.
   1. Select **Clear All** and then select the attributes you want to export, or 
   1. Exclude attributes from the export by deselecting them.
1.	Along with user attributes, in the slider window, there's the option to include raw survey responses. Enable this feature to include the user's responses to current surveys. Data can't be extracted during a live survey.
1.	Select **Send**. The data is sent to the employee email address on file. Check that the email address is correct before selecting Send.
1.	A banner appears, indicating the export has sent successfully.
1.	The employee receives an email with their Viva Glint data attached in a .csv file.

>[!TIP]
> For more information on how to support a request to delete data, visit [Delete user data from Viva Glint.](/../../viva/glint/setup/delete-user-data)

## Disable Raw Data Export access

**Important**: Disabling Raw Data Export (RDE) means that: 
- Admins can't access or export this survey data unless your organization believes extreme circumstance requirements exist. In this case, a Viva Glint admin can enable the export.
- Microsoft won't facilitate direct transfers to third parties, such as alternative survey platforms or data analytics consultants.
- The customer remains the data controller and Microsoft permanently prohibits customer access to non-RDE survey data at the *customers' explicit instruction*.

## Export company-level raw data

For closed surveys where raw survey responses were enabled, admins can export raw survey responses from Viva Glint. 

### Export raw response data for Recurring and Ad-Hoc surveys:

1. Go to **configuration** and select **Survey Programs.**
2. Select your survey program and go to the **Completed** cycles tab.
3. On the row with the appropriate cycle, select the ellipses (three dots) and then **Export Raw Survey Responses.**
4. In the export pane that appears:
   1. Choose whether to include **Comments** and the **Survey Sent Date** in the *Export Options* section.
   2. Select attributes that you want to include in the *Attributes* section.
   3. After making all selections, select **Export**.
5. Your .csv file downloads to your device. Larger files can take more time to generate; you receive an email when your file is ready to download.

### Export raw response data for Lifecycle and Always-On surveys:

1. Go to **configuration** and select **Survey Programs.**
2. Select your survey program and then the **Actions** menu.
3. Choose **Export Raw Survey Responses.**
4. In the export pane:
   1. Select a Start Date and End Date in the *Date Range* section.
   2. Choose whether to include **Comments** and the **Survey Sent Date** in the *Export Options* section.
   3. Select attributes that you want to include in the *Attributes* section.
   4. After you make all selections, select **Export**.
5. The .csv file downloads to your device. Larger files can take more time to generate; you receive an email when your file is ready to download.

### Raw survey response file layout

The fields included in your Viva Glint raw survey response exports vary based on the attributes that your organization sends, the selections that you make for your export, and the items included in your survey. The following columns will always be included, with a field for every survey item:

|Field Label  |Description   |Value Format|
|----------|-----------|------------|
|Survey Cycle Creation Date   |The date and time that surveys were generated for users.       |YYYY-MM-DD hh:mm:ss|
|Survey Cycle Completion Date|The date and time that surveys were completed by each user.    |YYYY-MM-DD hh:mm:ss|
|Survey Cycle Title|The name of the survey cycle.  |\<Month> \<Year> \<Program name> Survey|
|ItemText1  |Full text of survey item. |Numeric response value.|
|ItemText2  |Full text of survey item. |Numeric response value.|
|ItemText3  |Full text of survey item. |Numeric response value.|

>[!NOTE]
> - The export option will only be available to admins.
> -	The export option will only be enabled for a survey cycle if the raw survey response export was enabled for the selected survey program before the survey went live.

>[!CAUTION]
> Once a survey is live, the choice to enable or disable raw survey response export can't be changed for that survey.



