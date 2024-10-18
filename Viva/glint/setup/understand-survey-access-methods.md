---
title: Viva Glint survey access methods
description: Microsoft Viva Glint offers multiple survey access methods that can be used independently or in combination to meet the needs of your employee population. 
ms.author: aweixelman
author: AliciaWeixelman
manager: melissabarry
audience: admin
f1.keywords: NOCSH
keywords: Survey access, survey access method, access methods
ms.collection: 
 - m365initiative-viva
 - selfserve
search-appverid: MET150
ms.topic: article
ms.service: viva-glint
ms.localizationpriority: high
ms.date: 10/18/2024
---

# Viva Glint survey access methods

Microsoft Viva Glint offers multiple survey access methods that can be used independently or in combination to meet the needs of your employee population. Admins can set up these combined access methods:

|First access method   |Second access method   |Supported combined access method?|
|:----------|:-----------|:------------|
|Authentication with Microsoft Entra ID     |Attribute-based access      |Yes       |
|Personalized link |Attribute-based access    |Yes |
|Authentication with Microsoft Entra ID |Personalized link  |No|

> [!TIP] 
> Viva Glint recommends that admins enable the requirement for users to authenticate with Microsoft Entra ID as the most secure method to administer surveys. This access method also allows for participation in integrations across other Viva applications.

> [!NOTE] 
> Personalized links and attribute-based access aren't currently available for [Viva Glint 360 feedback programs](360-overview.md). Participants in 360 feedback (raters, feedback providers, admins) must access 360s with authentication via Microsoft Entra ID. 

## Authentication with Microsoft Entra ID

Use this guidance to enable survey invite links that require authentication with Microsoft Entra ID. Grant all users access to the Viva Glint **My Surveys** tab so that participants can access their surveys. After selecting the **Provide Feedback** button in survey emails, users with one active survey go directly to the survey landing page after authentication. Users with multiple active surveys land on the My Surveys tab to select a survey.

> [!CAUTION] 
> If your organization uses **URL Defense**, a security feature that can rewrite URLs in inbound emails, disable this feature for Glint emails. If left enabled when using survey access that requires authentication with Microsoft Entra, the **Provide Feedback** link in emails directs users to the Glint dashboard instead of their survey or My Surveys tab.

### To enable this survey access method:

1. Work with your Viva Glint Global administrator to [establish access to Viva Glint via Microsoft Entra ID.](https://go.microsoft.com/fwlink/?linkid=2238425)
1. From the admin dashboard, select the **Configuration** symbol, then in **Service Configuration**, choose **General Settings**.
3. In the **All Settings** menu, select **Engage Survey Details**.
4. Switch the **Require Azure AD for links in survey emails** setting to **Yes**.
5. Select **Save Changes** in the top right of the **General Settings** page.
6. Select the **Configuration** symbol, then in **Employees**, choose **User Roles**.
7. Select **Active Employees** and on the **Role Settings** page, choose **Permissions**.
8. To grant access to the **My Surveys** tab for all active users, select the **View My Surveys** permission.
9. Select **Save Changes** at the top of the page.

## Personalized survey link

Survey emails contain a personalized survey link that is tied to each participant and shouldn't be forwarded. When users select this personalized link, they access an active survey with no authentication. To enable this access method:

1. From the admin dashboard, select the **Configuration** symbol, then in **Service Configuration**, choose **General Settings**.
3. In the **All Settings** menu, select **Engage Survey Details**.
4. Switch the **Require Azure AD for links in survey emails** setting to **No**.
5. Select **Save Changes** in the top right of the **General Settings** page.

## Attribute-based survey access

Viva Glint's attribute-based survey access allows users without a work email account to complete surveys in another way. Users enter two unique pieces of employee information rather than authenticating in Viva Glint through an email invite. Admins can convert the survey link into a QR code or shortened link to share with frontline workers. To set up attribute-based survey access, follow the steps in this article: [Set up attribute-based survey access in Viva Glint](https://go.microsoft.com/fwlink/?linkid=2230745).

## Survey participant experiences

Viva Glint survey access methods present different user experiences depending on the method admins select and how many active surveys a user is included in. 

> [!IMPORTANT] 
> Survey access with authentication via Entra and personalized survey links send email invites and reminders with the correct links for survey access. Admins shouldn't copy links from the Viva Glint platform to share with users for these access methods.

> [!NOTE] 
> If admins or managers access the Viva Glint application with a dashboard link during a live survey (not with a link in an invite or reminder email), they'll go to their dashboards. Users can access live surveys by going to the **My Surveys** tab.

|Survey access method   |Survey entry point   |Landing page|
|:----------|:-----------|:------------|
|Authentication with Microsoft Entra ID     |Users select the **Provide Feedback** button in survey invites and reminders.      |If the user is included in **multiple active surveys**, they're taken to the **My Surveys** tab in Viva Glint.<br><br>If the user has **one (1) active survey**, they're taken directly to the survey welcome page.       |
|Personalized link |Users select the **Provide Feedback** button in survey invites and reminders.    |Users go directly to the survey welcome page, regardless of the number of active surveys. The personalized link is specific to each user and each survey. |
|Attribute-based access |Users access the attribute-based access survey link shared by their organization.  |Users go to an access page that prompts them to enter two (2) pieces of information. After users enter correct information, they go to the survey welcome page.|

### Survey session time-outs

Depending on the survey access method that your organization selects, users are prompted to continue their session and have their sessions ended after different periods of inactivity. 

:::image type="content" source="../../media/glint/setup/glint-inactive-session-message.png" alt-text="Screenshot of a message that appears when a user is inactive in their survey session.":::

|Survey access method   |Are you still here? prompt   |Session ends|
|:----------|:-----------|:------------|
|Authentication with Microsoft Entra ID     |After 20 minutes of inactivity       |After another 10 minutes of inactivity        |
|Personalized link |After 20 minutes of inactivity    |After another 10 minutes of inactivity |
|Attribute-based access |After 30 seconds of inactivity   |After another 30 seconds of inactivity|
