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
* **Data privacy**: See the Privacy Guide to understand how privacy is built into Briefing emails and to learn what you can configure to address your organization’s specific privacy requirements.

### To configure access at the tenant level

As the admin, use the following steps to change the setting for Briefing email at the tenant level. This setting is enabled by default, so that all users who have an Exchange Online license and their Office language is English (US) will receive the Briefing email. Users can unsubscribe individually from within any Briefing email they receive. However, if you disable this feature at the tenant level, no users in your organization will receive the Briefing email and individual users cannot override this tenant-level setting.  

1. Sign in to the [Microsoft 365 admin center](https://admin.microsoft.com/Adminportal).
2. Make sure you're using the new admin center. To do this, if the switch in the upper right of the page reads **Try the new admin center**, select it so that it reads **The new admin center**:

    ![New admin center](./images/the-new-admin-center.png)

3. In the left pane, expand **Settings**, and then select **Services & add-ins**.
4. Under **Services & add-ins**, select **Briefing email (Preview)**.
5. Select or deselect the checkbox next to **Let people in your organization receive the Briefing email**, and then select **Save changes**. If you deselect the checkbox, all users in your organization will not receive the Briefing email and individual users cannot override this setting.

   ![Briefing email access](./images/be-admin.png)

> [!Note]
> Individual users can select **Unsubscribe** from within any of their Briefing emails to opt out of receiving them.
<!--As the admin, you can set the Briefing email up at the [tenant level](#tenant-level-configuration) or the [user level](#user-level-configuration).

## Tenant-level configuration

You can enable or disable the Briefing email for all users in your organization at the tenant level. Use the following Exchange Online PowerShell cmdlets to set the tenant default:

  ```powershell
  Set-OrganizationIntelligenceConfig [-BriefingEmailDefault [<”Opt-in” | “Opt-out”>]
  ```

   * If you set **BriefingEmailDefault** parameter to **Opt-out**, the Briefing email will be Off by default for your organization. Users can then opt-in at [briefing.microsoft.com](https://briefing.microsoft.com).
   * If you set **BriefingEmailDefault** parameter to **Opt-in**, the Briefing email will be On by default for your organization. Users can then opt-out at [briefing.microsoft.com](https://briefing.microsoft.com). If no action is taken, this setting applies by default.

To get the current state of the Briefing email setting, use:

```powershell
Get-OrganizationIntelligenceConfig
```
    
## User-level configuration

You can also configure the Briefing email for individual users in your organization. At this level, you can completely opt-out a user, which turns off all Briefing email functionality for that user. However, the user can choose to opt back in at [briefing.microsoft.com](https://briefing.microsoft.com).

* To enable or disable the Briefing email for a specific user in your organization, use the following Exchange Online PowerShell cmdlets, where you replace “Contoso\Jill” with your applicable organization and username:

    ``` powershell
    Set-UserIntelligenceConfig -Identity Contoso\Jill [-BriefingEmailMode [<”Opt-in” | “Opt-out”>]
     ```

  - If you set the BriefingEmailMode parameter to Opt-out, the Briefing email will be Off by default for that user. Users can then opt-in from [briefing.microsoft.com](https://briefing.microsoft.com).
  - If you set the BriefingEmailMode parameter to Opt-in, the Briefing email will be On by default for that user. Users can then opt-out from [briefing.microsoft.com](https://briefing.microsoft.com). If no action occurs, this setting applies by default.

  For example, to get the current state of the Briefing email flag for “Contoso\Jill,” you'd use:

    ``` powershell
    Get-UserIntelligenceConfig -Identity Contoso\Jill
     ```

* Or you can set the parameter for multiple users with a PowerShell script that iterates through the users, changing the value one user at a time. Use the following script to:

  - List the user principal name for each user.
  - Set the specified Briefing email mode for each user.
  - Create a .csv file with all the users that were processed and shows their status.

  1. Create a comma-separated value (.csv) text file that contains the UserPrincipalName field and the location of the users you want to configure. For example:

    ``` powershell
    UserPrincipalName
    ClaudeL@contoso.onmicrosoft.com
    LynneB@contoso.onmicrosoft.com
    ShawnM@contoso.onmicrosoft.com
     ```

  2. Specify the location of the input .csv file, the output .csv file, and the value of **BriefingEmailMode** of **Opt-in** or **Opt-out** for each user:

    ``` powershell
    $inFileName="<path and file name of the input .csv file that contains the users, example: C:\admin\Users2Opt-out..csv>"
    $outFileName="<path and file name of the output .csv file that records the results, example: C:\admin\Users2Opt-out-Done..csv>"
    $briefingEmailMode = "Opt-in"
    
    $users=Import-Csv $inFileName
    ForEach ($user in $users)
    {
    $user.Userprincipalname
    $upn=$user.UserPrincipalName

    Set-UserInelligenceConfig –Identity $upn -BriefingEmailMode $briefingEmailMode
    Get-UserIntelligenceConfig –Identity $upn | Export-Csv $outFileName
    }
     ```

  3. Run the resulting commands at the PowerShell command prompt. For more information about the Exchange Online PowerShell, see [Connect to Exchange Online PowerShell](https://technet.microsoft.com/library/jj984289(v=exchg.160).aspx).-->


## Related topics

[Briefing email overview](be-overview.md)
