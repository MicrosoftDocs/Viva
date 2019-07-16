---
# Metadata Sample
# required metadata

title: MyAnalytics configuration for Office 365 administrators
description: Configuration options that Office 365 administrators can make for MyAnalytics users
author: paul9955
ms.author: v-pascha
ms.date: 07/15/2019
ms.topic: article
localization_priority: normal 
ms.prod: mya
---

# Configure MyAnalytics

**Role:** Office 365 admins

The steps in this topic describe how to configure MyAnalytics for the users in your organization. Note the following: 

 * **Prerequisite:** Users have access to MyAnalytics only if they have licenses that include the MyAnalytics service plan, as described in [plans and environments for MyAnalytics](../Overview/plans-environments.md).

 * **Data privacy:** See the [MyAnalytics privacy guide](../Overview/Privacy-Guide.md) to understand how privacy is built into MyAnalytics and to learn what you can configure to address specific privacy requirements.

To configure MyAnalytics, see the following sections:

 * [Assign licenses with the MyAnalytics service plan](#assign-licenses-with-the-myanalytics-service-plan)
 * [Configure MyAnalytics access](#configure-myanalytics-acces)
    * [Configure access at the tenant level](#configure-myanalytics-access-at-the-tenant-level)
    * [Configure access at the user level](#configure-myanalytics-access-at-the-user-level)


## Assign licenses with the MyAnalytics service plan

MyAnalytics is available to users who've been assigned a license that includes a MyAnalytics service plan. For more information about which licenses have MyAnalytics service plans, see [plans and environments for MyAnalytics](../Overview/plans-environments.md).

For information on how to assign a license, see [Assign licenses to users in Office 365 for business](https://support.office.com/en-us/article/assign-licenses-to-users-in-office-365-for-business-997596b5-4173-4627-b915-36abac6786dc). 

<!-- If you don’t want a user to see any statistics from MyAnalytics, you can disable the MyAnalytics service plan for that user. -->

> [!Note]
> Before you assign licenses to users, you can notify them in email that MyAnalytics will be available soon. To help you with this notification, use [this email template](MyAnalytics-announcement-template.docx). You can download it, customize it with your company’s information, and then email it to the new MyAnalytics participants. To learn more about adopting MyAnalytics, see [Adopt MyAnalytics](../Use/MyA-Adoption/adopt-myanalytics.md).  

### MyAnalytics elements

<!-- Updated for Anu and Sourabh Feb 2019: -->

After you assign a user license with the MyAnalytics service plan, the new participant will gain access to the following MyAnalytics elements.  

<!--  
> [!Note]
> The following timeframes pertain to the March 2019 distribution of MyAnalytics features. 
-->

 * **MyAnalytics welcome email:**
  
      * Existing users of Office 365 will receive the welcome email a few days (up to four weeks) after their license is granted.
      * New users will receive the welcome email approximately four weeks after their license is granted.

<!--
    > [!Note]
    > Users will not receive the welcome email outside of their work week. If a user's set work week is Monday to Friday, and the person's welcome email would otherwise arrive on a weekend, its arrival time is delayed to the following Monday. For more details, see [MyAnalytics welcome email](../Use/MyA-Welcome-email.md).
-->

 * **MyAnalytics personal dashboard:** Users can visit their [personal dashboard](../Use/dashboard-2.md) a few days after their license with the service plan is granted.

 * **Insights Outlook add-in:** Users can see the [Insights Outlook add-in](../Use/add-in.md) in a day or so after their license with the MyAnalytics service plan is granted.

 * **Weekly email digest:** Users will begin to receive the MyAnalytics [email digest](../Use/email-digest-2.md) on the Monday of the first week after they receive the welcome email.

 * **Inline suggestions:** Users can see the [inline suggestions](../use/mya-notificatins.md) in a day or so after their license with the MyAnalytics service plan is granted.

## Configure MyAnalytics access 

As the Office 365 admin, you can set a starting point for the MyAnalytics users in your organization. You can do this for all users at once, for just some of them, or for individual users. By default, this starting point is "opted in." This means that, by default, users have access to MyAnalytics. You can change this starting point from "opted in" to "opted out"&mdash;either for all of MyAnalytics or for its individual parts&mdash;by completing the steps in the following sections. 

> [!Note] 
> If you've set the starting point to "opted in," users can still choose to opt themselves out. Similarly, if you've set the starting point to "opted out," users can choose to use MyAnalytics by opting themselves in. The one situation in which a user cannot opt in is if you've removed their license; unlicensed users cannot participate in MyAnalytics. 

### Configure access at the tenant level

You can configure access to MyAnalytics elements for all the users in your organization.  

#### Dashboard and weekly email

1. Sign in to the [Microsoft 365 admin center](https://admin.microsoft.com/Adminportal).
2. Make sure that you are using the new admin center. To do this, if the switch in the upper right of the page reads **Try the new admin center**, select it so that it reads **The new admin center**: 

    ![New admin center](../../images/mya/setup/the-new-admin-center.png)

3. In the left pane, expand **Settings** and select **Services & add-ins**. 
4. In the main pane, under **Services & add-ins**, select **MyAnalytics**. This opens the page for configuring access to the MyAnalytics elements: 

   ![Select visibility](../../images/mya/setup/assign-mya-access-new.png)

5. Select **Insights dashboard** to keep all of the MyAnalytics users in your organization opted _in_ for access to the MyAnalytics personal dashboard. Deselect **Insights dashboard** to opt users _out_ of access to the dashboard. 
6. Select **Weekly insights email** to keep all of the MyAnalytics users in your organization opted _in_ for access to the weekly email. Deselect **Weekly insights email** to opt users _out_ of the weekly email.  

#### Insights Outlook add-in

You can disable the Insights Outlook add-in for your entire organization by using the Exchange admin center.

**To disable the add-in**

> [!Note]
> You must be an Office 365 admin to perform these steps.

1. Open the [Microsoft 365 admin center](https://admin.microsoft.com/Adminportal).

2. Make sure that you are using the new admin center. To do this, if the switch in the upper right of the page reads **Try the new admin center**, select it so that it reads **The new admin center**: 

    ![New admin center](../../images/mya/setup/the-new-admin-center.png)

3. In the left navigation pane, select **Exchange**. This opens the dashboard of the Exchange admin center.          
 
4. In the dashboard, select **add-ins**.
      
5. In the list of add-ins, select **Insights**, and then select **Edit** (the pencil icon). This opens the **Edit add-in settings** dialog box.
 
6. In the dialog box, clear the **Make this add-in available to users in your organization** checkbox to disable the add-in, and then select **Save**.

This disables the add-in for all licensed users in your organization.

### Configure access at the user level

Configure MyAnalytics access for individual users in your organization. 

[!INCLUDE [Configure user settings](../setup/configure-mya-user-settings.md)]  

<!--

## Related topics

[How users can opt out of MyAnalytics](../use/dashboard-2.md#can-i-opt-out-of-myanalytics)

[How users can remove the Insights add-in from Outlook](../use/add-in.md#to-remove-insights-add-in-from-outlook)
-->









