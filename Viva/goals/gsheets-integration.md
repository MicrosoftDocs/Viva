---
title: "Google Sheets Integration"
ms.reviewer: 
ms.author: rasanders
author: rasanders
manager: liz.pierce
audience: Admin
f1.keywords:
- NOCSH
ms.topic: article
ms.service: viva
ms.subservice: viva-goals
ms.localizationpriority: medium
ms.collection:  
- m365initiative-viva-goals
search.appverid:
- MET150

description: "Learn how to integrate your Google Sheets with OKRs in Viva Goals."
---

# Google Sheets integration

## About Google Sheets integration

Viva Goals Google Sheets integration allows you to link KRs to Google Sheet cells for real-time updates of your progress. 
  
Say, for example, you have a Google Sheet used to track survey responses. By implementing a Google Sheet integration, you can save yourself the hassle of repeatedly going back and forth between your sheets and Viva Goals to update your progress on KRs: Viva Goals will sync the values for you, thus saving time while keeping your OKRs current.
  
All users and admins can use this feature. Admins can manage the integration from the admin dashboard.

## How to enable Google Sheets integration

Admins can follow these steps to enable this integration:

1. From the sidebar, go to **Admin** and select the **Integrations** tab.
  
    :::image type="content" source="../media/goals/10/viva-goals-integrations-page.png" alt-text="Screenshot of the integrations page in Viva Goals." lightbox="../media/goals/10/viva-goals-integrations-page.png":::

2. For **Google Sheets**, you'll have an option to **Enable** the integration. If you already created a connection, you'll have an option to **Manage** the integration.
  
    :::image type="content" source="../media/goals/10/gitlab-enable-button.png" alt-text="Screenshot highlights the enable option for GitLab in Viva Goals." lightbox="../media/goals/10/gitlab-enable-button.png":::
  
   You can also disable the integration from the same section: Go to **Change** and select **Disable integration** from the dropdown.
    
   :::image type="content" source="../media/goals/10/gitlab-disable-button.png" alt-text="Screenshot shows where you select Disable Integration for GitLab in Viva Goals." lightbox="../media/goals/10/gitlab-disable-button.png"::: 

## For admins: How to connect Google Sheets to your Viva Goals account

1. After you enable the integration as an admin, you need to configure a Google Sheets connection from the **Google Sheets configuration** page.

2. Select **New Connection**, and sign in to your Google account.
  
    :::image type="content" source="../media/goals/10/gitlab-new-connection-button.png" alt-text="Screenshot shows where you choose to add a new GitLab connection in Viva Goals." lightbox="../media/goals/10/gitlab-new-connection-button.png":::

3. Allow Viva Goals to access the below scopes
    a. See and download all Google Drive files
    b. See, edit, create, and delete all you Google Sheets spreadsheets

      :::image type="content" source="../media/goals/10/gitlab-new-connection-button.png" alt-text="Screenshot shows where you choose to add a new GitLab connection in Viva Goals." lightbox="../media/goals/10/gitlab-new-connection-button.png":::

Please be aware that since Google Sheets lacks a granular scope to read the drive files, Viva Goals requires access to expanded scopes as described in step #3. Viva Goals shouldn't be able to manage your Google Drive files other than reading them from your Google drive or Shared drive. 

4. Enter a name for the connection.
  
    :::image type="content" source="../media/goals/10/gitlab-configure-new-connection.png" alt-text="Screenshot shows where you name your new GitLab connection in Viva goals." lightbox="../media/goals/10/gitlab-configure-new-connection.png":::

5. It's optional to share this connection with other users in the organization. Select **Next** to get up and running with this integration. You can edit the saved connection at any time.

6. Viva Goals allows you to connect with multiple Google Sheets. Select **New Connection** to fetch data from another sheet. You differentiate these connections by name. The names will be displayed to other users when they link their OKRs with Google Sheets data.

## How to use Google Sheets integration and connect Google Sheets to an OKR

After you configure the connection, the next step is link OKRs to your Google Sheet.

1. When you create or edit a Key Result, select **Automatically from a data source**. From the drop-down menu, select **Google Sheets**.
  
    :::image type="content" source="../media/goals/10/gitlab-datasource.png" alt-text="Screenshot shows where you select GitLab as the data source." lightbox="../media/goals/10/gitlab-datasource.png":::

2. If you already created a connection, or if your administrator shared a connection with you, that connection will be selected automatically. Viva Goals will prompt you to create a new connection only if there are no connections already created or shared.

3. Select the **spreadsheet** you want to use, followed by the **column** and **row number** of the cell you would like to link to the metric.
  
    :::image type="content" source="../media/goals/10/gitlab-new-connection-details.png" alt-text="Screenshot shows where you add GitLab connection details." lightbox="../media/goals/10/gitlab-new-connection-details.png":::

4. Select an **Next** to save your key result.

## How to disable Google Sheets integration

Admins can disable Google Sheets integration at any time: Go to **Google Sheets** in the **Integrations** section and select **Manage**. On the **Google Sheets Configurations** page, go to the **Change** dropdown, select **Disable**, and confirm.

