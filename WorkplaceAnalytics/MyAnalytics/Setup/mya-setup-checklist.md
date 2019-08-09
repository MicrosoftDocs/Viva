---
# Metadata Sample
# required metadata

title: MyAnalytics configuration for Office 365 administrators
description: Configuration options that Office 365 administrators can make for MyAnalytics users
author: paul9955
ms.author: v-midehm
ms.date: 08/02/2019
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
 * [Configure MyAnalytics access](#configure-myanalytics-access)
    * [Configure access at the tenant level](#configure-access-at-the-tenant-level)
    * [Configure access at the user level](#configure-access-at-the-user-level)


## Assign licenses with the MyAnalytics service plan

MyAnalytics is available to users who've been assigned a license that includes a MyAnalytics service plan. For more information about which licenses have MyAnalytics service plans, see [plans and environments for MyAnalytics](../Overview/plans-environments.md).

For information on how to assign a license, see [Assign licenses to users in Office 365 for business](https://support.office.com/en-us/article/assign-licenses-to-users-in-office-365-for-business-997596b5-4173-4627-b915-36abac6786dc). 

> [!Note]
> If you choose to notify your organization before you assign licenses for MyAnalytics, you can use [this email template](MyAnalytics-announcement-template.docx). You can download it, customize it with your company's information, and then email it to the new MyAnalytics participants. To learn more about adopting MyAnalytics, see [Adopt MyAnalytics](../Use/MyA-Adoption/adopt-myanalytics.md).  

### MyAnalytics elements become available 

After you assign a user license with the MyAnalytics service plan, the new participant will gain access to the following MyAnalytics elements. 

| Element&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; | Timeframe of user access | 
| ------------------- | ------------------------ |
|  [Welcome email](../use/mya-welcome-email.md?branch=PAS-HA-MA-MyA-settings)  | <ul><li>For E5 plans: Existing users of Office 365 will receive the welcome email a few days (up to four weeks) after their license is granted. New users will receive the welcome email approximately four weeks after their license is granted.</li><li>For E3 plans: _To be rolled out soon to E3 users, at the same time as the email digest_</li></ul> |
|  [Personal dashboard](../use/dashboard-2.md)  | <ul><li>For E5 plans: A few days after the license with the service plan is granted</li><li>For E3 plans: _To be rolled out soon to E3 users_</li></ul> |
|  [Insights Outlook add-in](../use/add-in.md)  | <ul><li>For both E5 and E3 plans: Available about one day after their license with the service plan is granted</li></ul> |
|  [Weekly email digest](../use/email-digest-2.md)  | <ul><li>For E5 plans: On the Monday of the first week after the user receives the welcome email</li><li>For E3 plans: _To be rolled out soon to E3 users_</li></ul> |
|  [Inline suggestions](../use/mya-notifications.md)  | <ul><li>For E5 plans: About one day after the license with the service plan is granted</li><li>For E3 plans: _Not applicable_</li></ul> |


> [!Note]  
> * _Licensed users_ have MyAnalytics automatically enabled for them after a license is assigned to them. 
> * _All users_ in your organization, whether or not they have MyAnalytics licenses issued to them, are opted-in. If you want one or more licensed users to be opted _out_ by default, see [Set MyAnalytics access for one user](#set-myanalytics-access-for-one-user) and [Set MyAnalytics access for multiple users](#set-myanalytics-access-for-multiple-users). 

## Configure MyAnalytics access 

As the Office 365 admin, you have two ways to configure defaults for MyAnalytics.  

 * The first way is to [configure access at the tenant level](#configure-access-at-the-tenant-level). You can use these settings to set organization-wide defaults for MyAnalytics elements 
 * The second way is to [configure access at the user level](#configure-access-at-the-user-level). You can use this to set defaults that affect complete MyAnalytics functionality for particular users. 

> [!Note] 
> When you set the default settings (at either the tenant level or the user level), users can still override your setting. For example, if you keep the dashboard tenant settings as opt in, users can still open the dashboard and then opt themselves out. Similarly, if you opt out users by using user-level settings, those users can choose to opt back in. The one situation in which a user cannot opt in is after you remove their license that contains a MyAnalytics service plan. 

### Configure access at the tenant level

You can configure access to MyAnalytics elements for all the users in your organization.  

#### Dashboard and weekly email

> [!Note] 
> This functionality will become available during August, 2019. 

1. Sign in to the [Microsoft 365 admin center](https://admin.microsoft.com/Adminportal).
2. Make sure that you are using the new admin center. To do this, if the switch in the upper right of the page reads **Try the new admin center**, select it so that it reads **The new admin center**: 

    ![New admin center](../../images/mya/setup/the-new-admin-center.png)

3. In the left pane, expand **Settings** and select **Services & add-ins**. 
4. In the main pane, under **Services & add-ins**, select **MyAnalytics**. This opens the page for configuring access to the MyAnalytics elements: 

   ![Select visibility](../../images/mya/setup/assign-mya-access-new.png)

5. Select **Insights dashboard** to keep all of the MyAnalytics users in your organization opted _in_ for access to the MyAnalytics personal dashboard. Deselect **Insights dashboard** to opt users _out_ of access to the dashboard. 

   > [!Note] 
   > If your organization is a tenant with an E5 plan and your user is using the [old dashboard version](https://msit.delve.office.com/?v=analytics), your deselection of **Insights dashboard** does not remove dashboard access for that user.

6. Select **Weekly insights email** to keep all of the MyAnalytics users in your organization opted _in_ for access to the weekly email. Deselect **Weekly insights email** to opt users _out_ of the weekly email.  

#### Insights Outlook add-in

You can disable the Insights Outlook add-in for your entire organization by using the Exchange admin center.

**To disable the add-in**


1. Open the [Microsoft 365 admin center](https://admin.microsoft.com/Adminportal).

2. In the left navigation pane, select **Exchange**. This opens the dashboard of the Exchange admin center. (If **Exchange** is not visible, first select **Show all** to see more admin centers and then select **Exchange**.)     
 
3. In the dashboard, select **add-ins**.
  
4. In the list of add-ins, select **Insights**, and then select **Edit** (the pencil icon). This opens the **Edit add-in settings** dialog box.
 
5. In the dialog box, clear the **Make this add-in available to users in your organization** checkbox to disable the add-in, and then select **Save**.

This disables the add-in for all licensed users in your organization.

### Configure access at the user level

Configure MyAnalytics access for individual users in your organization. At this level, you can opt-out the user completely, which would turn off all MyAnalytics functionality for that user. The user can choose to opt back in, however. 

You can configure MyAnalytics (change its default behavior) for users in your organization by setting the *PrivacyMode* parameter. For information about the values of PrivacyMode, see [User configuration settings](#user-configuration-settings).

You can set this parameter for one user or for many users: 

 * [Set MyAnalytics access for one user](#set-myanalytics-access-for-one-user) 

 * [Set MyAnalytics access for multiple users](#set-myanalytics-access-for-multiple-users)


### User configuration settings

PrivacyMode parameter  | Licensed user  | Unlicensed user
------------- | -------------  | ---------------
Opt-in (This is the default setting)        | <ul><li>Office 365 data is used for aggregated information shown to licensed users.</li><li>Personal dashboard is available.</li><li>User can opt-out.</li></ul>  | <ul><li>Office 365 data is used for aggregated information shown to licensed users.</li><li>Admins can opt-out unlicensed users through the admin PowerShell. </li></ul>  
Opt-out    | <ul><li>Office 365 data is not used for aggregated information shown to licensed users.</li><li> Personal dashboard is not available.</li><li>User can opt-in through the Feature settings menu.</li></ul>   |  <ul><li> Office 365 data is not used for aggregated information shown to licensed users.</li></ul> |

> [!Important] 
> The Excluded value of PrivacyMode is being retired. Users whose privacy mode was previously set to Excluded will now be set to Opt-out.

### Set MyAnalytics access for one user

Configure MyAnalytics access settings for a user with the following PowerShell cmdlet:

```powershell
Set-UserAnalyticsConfig –Identity <string> [PrivacyMode <string[]>]
```

Parameter   |   Required   |   Description   | Default value
----------  |  ----------  |  -------------- | -------------
Identity   |   Yes   | User ID for the current user as stored in Azure Active Directory (AAD).   |   -
PrivacyMode   |   Yes   | <ul><li>__Opt-out:__ MyAnalytics will not use the current user's data to compute derived statistics for other users. The current user will not see statistics in MyAnalytics, but can change this from the Feature settings menu and choose to opt-in.</li><li>__Opt-in:__ MyAnalytics will use the current user's data to compute derived statistics for other users. The current user will see statistics in MyAnalytics, and can change this from the Feature settings menu to opt out.</li></ul>|  Opt-in

> [!Important] 
> The Excluded value of PrivacyMode is being retired. Users whose privacy mode was previously set to Excluded will now be set to Opt-out.
  
### Determine MyAnalytics access for one user

To determine the MyAnalytics access (the value of PrivacyMode) for one user, use the following cmdlet:

```powershell
Get-UserAnalyticsConfig –Identity <string>
```

Parameter   |   Required   |    Description    |   Default value
----------- | ------------ |  ---------------  | ---------------
Identity    |  Yes         |    User ID for the current user as stored in AAD  | - 


### Set MyAnalytics access for multiple users

You can use PowerShell to change the access to MyAnalytics (the value of PrivacyMode) for multiple users at once. To do this, run a PowerShell script that iterates through the users, changing the value one user at a time. Follow these steps:

1. Create a comma-separated value (.csv) text file that contains the UserPrincipalName field and the addresses of the users you want to configure. For example:

```
UserPrincipalName,UsageLocation
ClaudeL@contoso.onmicrosoft.com,FR
LynneB@contoso.onmicrosoft.com,US
ShawnM@contoso.onmicrosoft.com,US
```

2. Specify the location of the input .csv file, the output .csv file, and the value of PrivacyMode that you want to set for each user:

```powershell
$inFileName="<path and file name of the input .csv file that contains the users, example: C:\admin\Users2License..csv>"
$outFileName="<path and file name of the output .csv file that records the results, example: C:\admin\Users2License-Done..csv>"
$privacyMode = "Opt-in"

$users=Import-Csv $inFileName
ForEach ($user in $users)
{
$user.Userprincipalname
$upn=$user.UserPrincipalName

Set-UserAnalyticsConfig –Identity $upn -PrivacyMode $privacyMode
Get-UserAnalyticsConfig –Identity $upn | Export-Csv $outFileName
}
```
3. Run the resulting commands at the PowerShell command prompt. For more information about the Exchange Online PowerShell, see [Connect to Exchange Online PowerShell](https://technet.microsoft.com/library/jj984289(v=exchg.160).aspx).

This PowerShell command block does the following:

 * Displays the user principal name of each user.
 * Sets the specified privacy mode for each user.
 * Creates a .csv file with all the users that were processed and shows their status.

