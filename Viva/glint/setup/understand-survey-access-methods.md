---
title: Understand Viva Glint survey access methods
description: Microsoft Viva Glint offers multiple survey access methods that can be used independently or in combination to meet the needs of your employee population. 
ms.author: SarahBerg
author: SarahAnneBerg
manager: elizapo
audience: admin
f1.keywords: NOCSH
keywords: Survey access, survey access method, access methods
ms.collection: 
 - m365initiative-viva
 - selfserve
search-appverid: MET150
ms.topic: article
ms.service: viva
ms.subservice: viva-glint
ms.localizationpriority: high
ms.date: 02/22/2024
---

# Understand Viva Glint survey access methods

Microsoft Viva Glint offers multiple survey access methods that can be used independently or in combination to meet the needs of your employee population.

> [!NOTE] 
> Viva Glint recommends that admins enable the requirement for users to authenticate with Microsoft Entra ID as the most secure method to administer surveys. This access method also allows for participation in integrations accross other Viva applications.

> [!IMPORTANT] 
> Survey access with authentication via Entra and personalized survey links send email invites and reminders with the correct links for survey access. Admins can't copy links from the Viva Glint platform to share with users as a survey access method.

<a name='set-up-survey-access-that-requires-authentication-with-azure-active-directory'></a>

## Set up survey access that requires authentication with Microsoft Entra ID
Use this guidance to enable survey invite links that require authentication with Microsoft Entra ID and to grant all users access to the Viva Glint My Surveys tab so that participants can access their surveys. After selecting the Provide Feedback button in survey emails, users with one active survey go directly to the survey landing page after authentication. Users with multiple active surveys land on the My Surveys tab to select a survey.

### To enable this survey access method:

1. Work with your Viva Glint Global administrator to [establish access to Viva Glint via Microsoft Entra ID.](https://go.microsoft.com/fwlink/?linkid=2238425)
1. From the admin dashboard, select the **Configure** symbol, then in **Client Settings**, choose **General Settings**.
3. In the **All Settings** menu, select **Engage Survey Details**.
4. Switch the **Require Azure AD for links in survey emails** setting to **Yes**.
5. Select **Save Changes** in the top right of the **General Settings** page.

### To grant all users access to the My Surveys tab in Viva Glint:

1. Select the **Configure** symbol, then in **Employees** , choose **User Roles**.
2. Select **+ New Role** and give your new User Role name in the top left. For example: Entra Survey Access Users.
3. In **Permissions**, select the **View My Surveys** checkbox, then in the top right of the **Permissions and Access** page, select **Save Changes**.
4. In the **All Members** section of the role, select **Add/Edit Employees** and then choose **Attribute Rules.**
5. In the setup pane, select the **I want to include all active employees only** option and select **Save Changes.**
   1. To enable the **Save Changes** selection, make a small edit and undo. For example, select the **Include Inactive Employees** checkbox and then unselect.

## Use a personalized survey link

When the **Require Azure AD for links in survey emails** setting in **General Settings** is set to **No**, this is the survey access method for users. Survey emails contain a personalized survey link that is tied to each participant and shouldn't be forwarded. When users select this personalized link, they access an active survey with no authentication.

## Set up attribute-based survey access

Viva Glint's attribute-based survey access allows users without a corporate email account to complete surveys by entering two unique pieces of employee information selected by an admin rather than authenticating in Viva Glint. Admins can convert the survey link into a QR code or shortened link to share with frontline workers. To set up attribute-based survey access, follow the guidance in this article: [Set up attribute-based survey access in Viva Glint](https://go.microsoft.com/fwlink/?linkid=2230745).

## Survey session timeouts

Depending on the survey access method that your organization selects, users are prompted to continue their session and have their sessions ended after different periods of inactivity. 

:::image type="content" source="../../media/glint/setup/glint-inactive-session-message.png" alt-text="Screenshot of a message that appears when a user is inactive in their survey session.":::

|Survey access method   |Are you still here? prompt   |Session ends|
|:----------|:-----------|:------------|
|Authentication with Microsoft Entra ID     |After 20 minutes of inactivity       |After an additional 10 minutes of inactivity        |
|Personalized link |After 20 minutes of inactivity    |After an additional 10 minutes of inactivity |
|Attribute-based access |After 30 seconds of inactivity   |After an additional 30 seconds of inactivity|
