---

ROBOTS: NOINDEX,NOFOLLOW
title: Configure the Briefing email
description: Learn how to configure the Briefing email for your organization as the admin
author: madehmer
ms.author: madehmer
ms.topic: article
localization_priority: normal 
ms.prod: mya
ms.collection: M365-analytics
manager: scott.ruble
audience: Admin
---

# Configure the Briefing email

As the admin, you can configure Briefing email for your organization. Before configuration, confirm the following.

* **Prerequisite**: Users get access to the Briefing email only if they have licenses that include the Exchange Online service plan.
* **Data privacy**: See the [Privacy guide](be-privacy.md) to understand how privacy is built into Briefing emails and to learn what you can configure to address your organization's specific privacy requirements.

## To configure access at the tenant level

As the admin, use the following steps to change the setting for Briefing email at the tenant level. This setting is enabled by default, so that all users who have an Exchange Online license and their Office language is English (US) will receive the Briefing email.

Users can unsubscribe individually from within any Briefing email they receive. However, if you disable this feature at the tenant level, no users in your organization will receive the Briefing email and individual users cannot override this tenant-level setting.  

1. Sign in to the [Microsoft 365 admin center](https://admin.microsoft.com/Adminportal).
2. Make sure you're using the new admin center. To do this, if the switch in the upper right of the page reads **Try the new admin center**, select it so that it reads **The new admin center**:

    ![New admin center](./images/the-new-admin-center.png)

3. In the left pane, expand **Settings**, and then select **Services & add-ins**.
4. Under **Services & add-ins**, select **Briefing email (Preview)**.
5. Select or deselect the checkbox next to **Let people in your organization receive the Briefing email**, and then select **Save changes**. If you deselect the checkbox, all users in your organization will not receive the Briefing email and individual users cannot override this setting.

   ![Briefing email access](./images/be-admin.png)

> [!Note]
> When the setting is enabled, individual users can select **Unsubscribe** from within any Briefing email to opt out.
<!--As the admin, you can set the Briefing email up at the [tenant level](#tenant-level-configuration) or the [user level](#user-level-configuration).

## Tenant-level configuration

You can enable or disable the Briefing email for all users in your organization at the tenant level. Use the following Exchange Online PowerShell cmdlets to set the tenant default:

  ```powershell
  Set-OrganizationIntelligenceConfig [-BriefingEmailDefault [<"Opt-in" | "Opt-out">]
  ```

   * If you set **BriefingEmailDefault** parameter to **Opt-out**, the Briefing email will be Off by default for your organization. Users can then opt-in at [briefing.microsoft.com](https://briefing.microsoft.com).
   * If you set **BriefingEmailDefault** parameter to **Opt-in**, the Briefing email will be On by default for your organization. Users can then opt-out at [briefing.microsoft.com](https://briefing.microsoft.com). If no action is taken, this setting applies by default.

To get the current state of the Briefing email setting, use:

```powershell
Get-OrganizationIntelligenceConfig
```
-->
<!-- 3/17--Per Mathew, we'll publish this section in place of the exposed steps for the admin center when he say, but maybe keep the admin center steps because they might bring the tenant level instructions back, so keep just in case.
## User-level configuration

You can configure the Briefing email at the user level in your organization. At this level, you can enable or disable it for a user, which turns off or on all Briefing email functionality for that user.

The user can choose to opt out or back in at any time at [briefing.microsoft.com](https://briefing.microsoft.com).

Install the Exchange Online PowerShell V2 module and then use it to set this parameter for one or many users:

* [Set Briefing email access for one user](#set-briefing-email-access-for-one-user)
* [Set Briefing email access for multiple users](#set-briefing-email-access-for-multiple-users)

## Install the Exchange Online PowerShell V2 module

Follow the steps to install the module at [Install and maintain the Exchange Online PowerShell V2 module](https://docs.microsoft.com/powershell/exchange/exchange-online/exchange-online-powershell-v2/exchange-online-powershell-v2?view=exchange-ps#install-and-maintain-the-exchange-online-powershell-v2-module).

> [!Note]
> Before configuring access, confirm you're connected to [Exchange Online](https://docs.microsoft.com/powershell/exchange/exchange-online/exchange-online-powershell-v2/exchange-online-powershell-v2?view=exchange-ps#connect-to-exchange-online-using-the-exo-v2-module).

## Set Briefing email access for one user

To enable or disable the Briefing email for a specific user in your organization, use the Exchange Online PowerShell V2 module and the following cmdlets, where you replace "joe@contoso.com" with your applicable username and organization:

    ```powershell
    Set-UserBriefingConfig -Identity joe@contoso.com [-Enabled [<"$true" | "$false">]
    ```

  - If you set the **Enabled** parameter to **$false**, the Briefing email will be **Off** for that user.
  - If you set the **Enabled** parameter to **$true**, the Briefing email will be **On** for that user. Users can then opt-out from [briefing.microsoft.com](https://briefing.microsoft.com). If no action occurs, this setting applies by default.

  For example, to get the current state of the Briefing email flag for "joe@contoso.com," you'd use:

    ```powershell
    Get-UserBriefingConfig -Identity joe@contoso.com
    ```

## Set Briefing email access for multiple users

You can also set the parameter for multiple users with a PowerShell script that iterates through the users, changing the value one user at a time. Use the following script to:

  - Create a .csv file with all the users that were processed and shows their status.
  - List the user principal name for each user.
  - Set the specified Briefing email Enabled parameter for each user.

  1. Create a comma-separated value (.csv) text file that contains the Identity of the users you want to configure. For example:

    ```powershell
    -Identity
    ClaudeL@contoso.com
    LynneB@contoso.com
    ShawnM@contoso.com
     ```

  2. Specify the location of the input .csv file, the output .csv file, and the value of **Enabled** to **$true** or **$false** for each user:

    ```powershell
    $inFileName="<path and file name of the input .csv file that contains the users, example: C:\admin\Users2Opt-in.csv>"
    $outFileName="<path and file name of the output .csv file that records the results, example: C:\admin\Users2Opt-in-Done.csv>"
    $briefingEmailMode = "$true"

    $users=Import-Csv $inFileName
    ForEach ($user in $users)
    {
    $user.identity
    $upn=$user.identity
    Set-UserBriefingConfig –Identity $upn -Enabled $briefingEmailMode
    Get-UserBriefingConfig –Identity $upn | Export-Csv $outFileName
    }
     ```

  3. Run the resulting commands at the Exchange Online PowerShell V2 module command prompt. For more information about the module, see [Use the Exchange Online PowerShell V2 module](https://docs.microsoft.com/powershell/exchange/exchange-online/exchange-online-powershell-v2/exchange-online-powershell-v2).
-->

## Related topics

[Briefing email overview](be-overview.md)
