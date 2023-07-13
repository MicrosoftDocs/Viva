---
title: Understand Viva Glint survey access methods
description: Microsoft Viva Glint offers multiple survey access methods that can be used independently or in combination to meet the needs of your employee population. 
ms.author: SarahBerg
author: SarahAnneBerg
manager: pamgreen
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
ms.localizationpriority: high pri
ms.date: 05/22/2023
---

# Understand Viva Glint survey access methods

Microsoft Viva Glint offers multiple survey access methods that can be used independently or in combination to meet the needs of your employee population.

> [!NOTE] 
> Viva Glint recommends that admins enable the requirement for users to authenticate with Azure Active Directory as the most secure method to administer surveys.

## Set up survey access that requires authentication with Azure Active Directory

To enable this survey access method:

1. Work with your Viva Glint Global administrator to [establish access to Viva Glint via Azure AD.](https://go.microsoft.com/fwlink/?linkid=2238425)
2. From the admin dashboard, select the **Configure** symbol, then in **Client Settings**, choose **General Settings**.
3. In the **All Settings** menu, select **Engage Survey Details**.
4. Switch the **Require Azure AD for links in survey emails** setting to **Yes**.
5. Select **Save Changes** in the top right of the **General Settings** page.
6. Select the **Configure** symbol, then in **Employees** , choose **User Roles**.
7. Select **Active Employees** , then choose **Permissions.**
8. In **Survey Programs**, select the **View My Surveys** checkbox,then in the top right of the **Permissions and Access** page, select **Save Changes**.

## Use a personalized survey link

When access with Azure AD isn't enabled, this is the survey access method for users. Survey emails contain a personalized survey link that is tied to each participant and shouldn't be forwarded. When users select this personalized link, they access an active survey with no authentication.

## Set up attribute-based survey access

Viva Glint's attribute-based survey access allows users without a corporate email account to complete surveys by entering two unique pieces of employee information selected by an admin rather than authenticating in Viva Glint. To set up attribute-based survey access or activate optional kiosk mode, follow the guidance in this article: [Set up attribute-based survey access in Viva Glint](https://go.microsoft.com/fwlink/?linkid=2230745).