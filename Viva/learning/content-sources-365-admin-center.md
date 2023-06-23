---
title: Manage content sources for Viva Learning 
ms.author: bhaswatic
author: bhaswatic
manager: pamgreen
ms.reviewer: chrisarnoldmsft
ms.date: 10/27/2021
audience: admin
ms.topic: article
ms.service: viva
ms.subservice: viva-learning
search.appverid: MET150
ms.collection:
  - enabler-strategic
  - m365initiative-viva-learning
  - highpri
  - Tier1
ms.localizationpriority: medium
description: Learn how to configure and manage learning content sources for Microsoft Viva Learning in the Microsoft 365 admin center.
---

# Manage content sources for Viva Learning 

The administrators for the Microsoft 365 admin center—either by themselves or by assigning the knowledge admin role to selected individuals in your organization—can manage settings related to Viva Learning and can configure the learning content sources.

The administrator selects which other learning content sources (for example, SharePoint or supported third-party content provider sources) will be available to users of Viva Learning. The admin then configures those sources to make sure the content is available for search and discovery and can be browsed by the employees who use Viva Learning. Content from Microsoft Learn, Microsoft 365 Training, and select content from LinkedIn Learning is available for free and enabled by default. If your organization has a LinkedIn Learning Enterprise subscription, employees can access the entire LinkedIn Learning catalog in Viva Learning without a Viva Suite or Viva Learning license.

>[!NOTE]
>Content accessible through Viva Learning is subject to terms other than the Microsoft Product Terms. Content and any associated services are subject to the content provider's privacy and service terms.

> [!NOTE]
> For non-Microsoft content (except free LinkedIn content), ensure your organization has a subscription for your users to access that content using a work account before connecting it to Viva Learning. Users' personal subscriptions to non-Microsoft learning providers will not be integrated with Viva Learning. Users sign in to non-Microsoft and LinkedIn Learning Pro learnings in a browser or embedded viewer. This configured learning is subject to the separate license, privacy and service terms between your organization and the third party, and not the Viva Learning terms. Before selecting this type of learning, verify you have an agreement in place for your organization and users. If users navigate to content where they do not have an organizational subscription, they may see a provider page where they could sign up for an individual subscription. All non-Microsoft learning is provided under the non-Microsoft provider's terms and not as part of Viva Learning.

## Assign the knowledge admin role (Optional)

You must be a Microsoft 365 global administrator to perform these tasks.

> [!TIP]
> The knowledge admin should be moderately technical and have existing SharePoint admin credentials, preferably someone who is well-versed in the education, learning, training, or employee experience part of the organization.

### Add a knowledge admin

To add a knowledge admin for Viva Learning, follow these steps:

1. In the left navigation of the Microsoft 365 admin center, go to **Roles** and select **Role assignments**.

    ![Image of Role assignments in the left navigation](../media/learning/clcs-orgsettings.png)

2. On the **Role Assignments** page, on the **Azure AD** tab, select **Knowledge Administrator**.

    ![Image of Knowledge Adminstrator selected on the Azure AD tab.](../media/learning/clcs-knowledgeadmin.png)

3. On the **Knowledge Administrator** panel, select **Assigned admins**, and then select **Add**.

    ![Roles page in the Microsoft 365 admin center showing the Knowledge Administrator panel to add a user.](../media/learning/clcs-addadmin.png)

4. On the **Add admins** panel, select the person you choose for the role, and then select **Add**.

### Remove a knowledge admin

To remove a knowledge admin for Viva Learning, follow these steps:

1. In the left navigation of the Microsoft 365 admin center, go to **Roles**, and select **Role assignments**.

    ![Image of Role assignments in the left navigation](../media/learning/clcs-orgsettings.png)

2. On the **Role assignments** page, go to the **Azure AD** tab, and then select **Knowledge Administrator**.

    ![Image of Knowledge Adminstrator selected on the Azure AD tab.](../media/learning/clcs-knowledgeadmin.png)

3. On the **Knowledge Administrator** panel, on the **Assigned Admins** tab, select **Remove**, and then select the person you want to remove from the role. To confirm, select **Remove**.

    ![Roles page in the Microsoft 365 admin center showing the Assigned admins panel to remove a user.](../media/learning/clcs-removeadmin.png)

## Configure settings for the learning content sources

You must be a Microsoft 365 global administrator or knowledge admin to perform these tasks.

To configure settings for learning content sources in Viva Learning:

1. Go to the **Admin** tab in Viva Learning and select **Manage Providers** on the left menu.

2. Select **Add Provider**  

 ![Settings page in the Microsoft 365 admin center showing the Learning app listed.](../media/learning/clcs-services.png)

3. Select the provider you want to configure from the Provider list and select **Next**.

![Learning panel in the Microsoft 365 admin center showing content sources options.](../media/learning/manage-providers-select-providers.png)

4. Enter the configuration details and click **Save**. Note that these details vary depending on the provider.

5. Once the configuration is saved, the provider displays on the **Manage Providers** dashboard of the tenant.

5.	The start of the sync indicates a successful configuration. You can refer to the sync status for more details.
6.	To edit or delete the already configured provider, select **Edit** or **Delete** from the provider menu.

![Manage providers page with a successful configuration status of the chosen provider](../media/learning/manage-providers-configured.png)


> [!NOTE]
> You'll need a Viva Learning or Viva Suite license to connect external content sources, with the exception of LinkedIn Learning. You'll need a LinkedIn Learning Enterprise subscription to access LinkedIn Learning content other than the select free courses. [Learn more about licensing](https://www.microsoft.com/microsoft-viva/learning).


Some learning content sources will be enabled by default. These learning sources include:

- LinkedIn Learning select free content
- Microsoft Learn
- Microsoft 365 Training
- Bring your own content

The Bring your own content feature allows users in your organization to bring their own content from SharePoint into Viva Learning and share it with others. However, content brought in by end users isn't searchable.

> [!NOTE]
> For data that you copy to Viva Learning from a non-Microsoft service (learning provider or learning management system), you are not able to directly extract, correct, or delete that data in Viva Learning. We refresh the data you import from non-Microsoft providers promptly to reflect changes and deletions in the non-Microsoft source data.
You need to work with the supplier of the non-Microsoft service to access, correct, delete or extract data under the license, service, or privacy terms of the non-Microsoft service. The changes made there will be reflected in the data processed for your use in Viva Learning upon completion of the data update cycles of the non-Microsoft service and Viva Learning. If you turn off the connection between Viva Learning and a non-Microsoft service, all data you had previously imported from that service will be deleted.

## Additional app settings

You can control the Viva Learning availability in your org from Teams Admin center. 

To control the ability to bring your own content or privacy related settings go to the Viva Learning settings page on the Microsoft 365 Admin center.
You can also search for Viva learning landing page on M365 Admin center to get a comprehensive list of all the Viva Learning settings.

![Microsoft 365 Admin page that displays a list of Viva Learning settings](../media/learning/manage-providers-additional-settings1.png)

## Enable tracking of recommended content

Users can recommend content to each other in Viva Learning. Enable tracking to allow a recommender to set due dates and track the progress of content they recommended. Tracking is enabled by default.

1. In the left navigation of the Microsoft 365 admin center, go to **Settings** > **Org settings**.

2. On the **Org settings** page, on the **Services** tab, select **Viva Learning**.

3. Check the box to enable tracking, or uncheck the box to disable tracking.

    ![Image of the enable tracking checkbox in the admin center.](../media/learning/manage-providers-admin-center.png)

## Change your existing LMS instance

To change your existing learning management system instance: 

1.**Delete** the existing provider from **Manage providers**. 
Once deleted, the data is removed immediately from app UX for end users. Underlying metadata (content, user metadata, LRS) is deleted in 3 days. 
2. Enable the new provider by going to **Add providers** and configuring a new provider.


## Next step


[Add SharePoint as a content source for Microsoft Viva Learning](configure-sharepoint-content-source.md)
