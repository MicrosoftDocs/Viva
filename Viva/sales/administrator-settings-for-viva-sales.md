---
title: Administrator settings for Viva Sales
description: Learn how to configure administrator settings for Viva Sales.
ms.date: 01/23/2023
ms.topic: article
ms.service: viva
ms.collection: highpri
author: sbmjais
ms.author: shjais
manager: shujoshi
ms.localizationpriority: medium
ms.subservice: viva-sales
---

# Administrator settings for Viva Sales

As a CRM administrator, you can customize Viva Sales as per your business requirements. For example, customizing the CRM information displayed in Viva Sales across Outlook and Teams.

You can access administrator settings from the Viva Sales app for Teams. The customization applies to the CRM environment you log in to Viva Sales from Outlook. If you want to customize Viva Sales in another environment, you must switch environments in Outlook.

When you open administrator settings, following tabs are available:

- **Home**: Serves as the landing page for the Viva Sales app.

- **Settings**: Contains all the settings for an administrator.

- **About**: Displays details of the Viva Sales app.

> [!NOTE]
> Administrator settings are visible only when you log in with your administrator credentials.

**To access administrator settings**

1.  Sign in to Microsoft Teams with your administrator credentials.

2.  In the app bar on the left, select **Viva Sales**.

    If **Viva Sales** is not visible, select **More added apps** (**…**), and then select **Viva Sales**.
    
    ![Screenshot showing to select the Viva Sales app](media/viva-sales-app-select.png "Screenshot showing to select the Viva Sales app.")
    
    The **Viva Sales** app is opened with the **Home** tab selected.
    
    ![Screenshot showing Viva Sales Home tab](media/viva-sales-home.png "Screenshot showing Viva Sales Home tab.")

3.  On the **Settings** tab, select the required option, and update the settings.

    - **Forms**: Allows you to specify what information should be displayed in Viva Sales across Outlook and Teams. More information: [Configure forms and fields](configure-forms-and-fields.md)

    ![Screenshot showing Viva Sales Settings tab](media/viva-sales-admin-settings.png "Screenshot showing Viva Sales Settings tab.")

## Who can access administrator settings?

### Dynamics 365

|Requirement type  |You must have  |
|---------|---------|
|Security role     |  System Administrator, System Customizer, or Viva Sales Administrator<br>More information: [Predefined security roles for Sales](/dynamics365/sales/security-roles-for-sales)  |

### Salesforce

|Requirement type  |You must have  |
|---------|---------|
|Permission    |  User profile needs to have Modify All Data or Manage Data Integrations permission  |

> [!NOTE]
> Changes in user permissions or security roles in  CRM can take up to 15 minutes to reflect in Viva Sales app for Teams.

## FAQ

### Can I access administrator settings if my organization does not have Microsoft Teams?

No. Administrator settings are currently accessible only through the Viva Sales app for Teams. 

### Which CRM environment do administrator settings apply to?

The settings apply to the environment signed in to from Viva Sales in Outlook. If you want to customize Viva Sales in another environment, you must switch environments in Outlook. Come back to Viva Sales in Teams and refresh the **Settings** tab.

### Why do I see the message "Sign in to Viva Sales in Outlook first"?

You need to be signed in to a CRM environment from Viva Sales in Outlook.

[Launch Viva Sales from Outlook](https://support.microsoft.com/topic/use-viva-sales-in-outlook-ec3605f9-fdb0-4593-9c5b-b43a76c07081). On the **Welcome to Viva Sales!** screen, select **Sign in to get started**, and then select your CRM and environment to use. 

Come back to the Viva Sales app in Teams and refresh the **Settings** tab. 

### Why do I see the message "Settings are coming soon"?

Personal settings for Viva Sales will also be accessible through the **Settings** tab, and will be launching soon. If you are a CRM administrator, you should already see administrator settings in the **Settings** tab, and you should not see this message – check that you have the right permissions or security roles. More information: [Who can access administrator settings?](#who-can-access-administrator-settings)

