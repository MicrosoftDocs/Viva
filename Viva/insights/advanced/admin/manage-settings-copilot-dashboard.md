---
ms.date: 08/22/2024
title: Manage settings for the Microsoft Copilot Dashboard
description: This article provides instructions to Viva Insights admins on how to configure several settings for the Microsoft Copilot Dashboard.
author: zachminers
ms.author: v-zachminers
ms.topic: how-to
ms.localizationpriority: medium
ms.collection: 
- viva-insights-advanced
- essentials-manage
- viva-copilot
- magic-ai-copilot
ms.service: viva-insights
manager: anirudhbajaj
audience: Admin
---

# Manage settings for the Microsoft Copilot Dashboard 

>[!Note]
>This feature is rolling out gradually to all customers with more than 50 Copilot assigned licenses.

As an admin, you can configure several features of the Microsoft Copilot Dashboard. These settings, for example, control who can access the dashboard, upload organizational data, manage a list of non-Copilot users, create an exclusion list, upload aggregated survey data, and the minimum group size for generating insights. Let’s review them.

## Manage access for individual users

These steps must be performed by the Microsoft 365 Global Administrator.

>[!Note]
>When you add or remove users to the dashboard, the change will go into effect in 24 hours.

You can also turn access to the dashboard on or off for individual users.

In the [Microsoft 365 admin center](https://admin.microsoft.com/adminportal/home?#/viva/insights):  

1. Go to the Settings tab and select **Microsoft Viva**, then **Viva Insights**. You need to enter your credentials if you're not already signed in.  

2. Under **Viva Insights in Microsoft 365**, select **Manage settings for viewing the Copilot dashboard**.  

3. To see how many employees have automatic access, at the top, select **General**.

   :::image type="content" source="../../org-team-insights/images/copilot-dashboard-02b.png" alt-text="Screenshot that shows how to view the number of employees with access." lightbox="../../org-team-insights/images/copilot-dashboard-02b.png":::

**To enable access for new report users:**

1. Search for the people you'd like to add, and select them from the list.
1. At the bottom, select **Add**.

   :::image type="content" source="../../org-team-insights/images/copilot-dashboard-03.png" alt-text="Screenshot that shows how to add new users.":::

**To disable access for existing report users:**

1. At the top, select **Assigned**.
1. Select the users from the list for whom you'd like to remove access.
1. Select **Remove user**.

   :::image type="content" source="../../org-team-insights/images/copilot-dashboard-04.png" alt-text="Screenshot that shows how to remove users.":::

**Delegate access to the dashboard:**

If you have access to the dashboard, you can also delegate access to the dashboard to other people in your company. [Learn how](../../org-team-insights/delegate-access.md).

>[!Note]
>Employees can view the dashboard in the Viva Insights Teams or web app. To install the Teams app, please use [these instructions](../../advanced/setup-maint/setup-overview.md) (it is on by default).

## Remove access to the dashboard for the entire tenant with Powershell

These steps must be performed by the Microsoft 365 global admin.

You can set a policy to disable the dashboard for the tenant using Powershell cmdlets. This is a tenant-level policy, not a user, or group-level policy. No users are able to access the dashboard until you remove or update the policy, even if they were added in the Microsoft 365 admin center using the process above. Before you can use the cmdlet, you need to install a module and sign in to be authenticated. [Learn more about how to set these policies](/viva/feature-access-management).

1. [Connect to Exchange Online](/Viva/insights/advanced/setup-maint/configure-personal-insights#connect-to-exchange-online) and, when prompted, sign in with your admin credentials.
1. After you’ve signed in, you can manage access for your tenant using the Add-VivaModuleFeaturePolicy cmdlet: [Add-VivaModuleFeaturePolicy](/powershell/module/exchange/add-vivamodulefeaturepolicy).

**Example: Turn off the dashboard for all users in your tenant**

```powershell
 ModuleId : VivaInsights
 FeatureId : CopilotDashboard
 Name : DisableFeatureForAll
 IsFeatureEnabled : false
 Everyone
```
## Turn off dashboard auto-enablement with Powershell 

These steps must be performed by the Microsoft 365 global admin.

This feature access control allows Global admins to enable or disable the auto-enablement feature for the Copilot Dashboard in their tenant. This control supports tenant-level policies only, not user or group-level policies. You can set tenant polices using PowerShell cmdlets. Learn more about how to set these policies.  [Learn more about how to set these policies](/viva/feature-access-management).

* **Default state**: Enabled, meaning that eligible users will be auto-enabled for access to the dashboard based on the identification criteria.

* **Disable or enable**: Admins can disable the dashboard auto-enablement control for their entire tenant using PowerShell cmdlets. Disabling the control prevents any user from getting auto-enabled for access to the dashboard.

    >[!Note]
    >User- and group-level policies are not supported for this feature and will not take effect if used.

1. [Connect to Exchange Online](/Viva/insights/advanced/setup-maint/configure-personal-insights#connect-to-exchange-online) and, when prompted, sign in with your admin credentials.

1. After you’ve signed in, you can manage access for your tenant using the Add-VivaModuleFeaturePolicy cmdlet: [Add-VivaModuleFeaturePolicy](/powershell/module/exchange/add-vivamodulefeaturepolicy).

**Example: Turn off dashboard auto-enablement for your tenant**

```powershell
 ModuleId : VivaInsights
 FeatureId : AutoCxoIdentification
 Name : DisableFeatureForAll
 IsFeatureEnabled : false
 Everyone
```

## Upload organizational data 

### For Viva Insights customers 

These steps apply to Viva Insights admins.

>[!Note]
>This data upload process will go into effect within seven days.

If your company has Viva Insights licenses, your Insights admin can continue to upload organizational data through the advanced Insights app as explained [here](../admin/org-data-overview.md). Your global admin may choose to upload more organizational attributes through the Microsoft 365 admin center using [these steps](/viva/organizational-data).

There are two ways you can upload Organizational data:

1. Your Viva Insights admin can upload data through the advanced insights app using [these steps](../admin/org-data-overview.md). This is the recommended way to upload data if you have Viva Insights.  

    * [Learn more about data quality in the advanced insights app](../admin/org-data-overview.md#organizational-data-in-the-advanced-insights-app).
    * To avoid more delays on data showing in the dashboard, the Insights admin should include **EffectiveDate** fields and set the date earlier than the upload date. [Learn more](../admin/prepare-org-data.md).

2. Your Microsoft 365 Global admin can upload data through the admin center using [these steps](/viva/organizational-data).

If the Viva Insights admin and Global admin *both* upload data, the dashboard displays insights based on the merge of the uploads and show data based on the more recent upload. The uploaded .csv file should include the required attributes shown below, otherwise the data won't show in the dashboard.

Below are the attributes that are used in the Copilot dashboard. Your admin should use the exact same attribute names as below when uploading correspondingly.

| Attribute names for organizational data in Viva Insights | Attribute names for organizational data in Microsoft 365 | Required or optional for Copilot dashboard |
|----|----|----|
| PersonId | Microsoft_PersonEmail | Required |
| ManagerId | Microsoft_ManagerEmail | Required |
| Organization | Microsoft_Organization | Required |
| FunctionType | Microsoft_JobDiscipline | Optional. The “Job function” filter in the dashboard will be available if this attribute is uploaded. |

### For Copilot customers

This process applies to the Microsoft 365 global admin.

>[!Note]
>This data upload process will go into effect within seven days.

If your company has Copilot licenses but not Viva Insights licenses, you can upload organizational data through the Microsoft 365 admin center using [these steps](/viva/organizational-data).

Below are the attributes used in the dashboard. The admin should use the exact same attribute names as below when uploading the data.

| Attribute names for organizational Data in Microsoft 365  | Required or optional for Copilot dashboard |
|---|---|
| Microsoft_PersonEmail | Required |
| Microsoft_ManagerEmail | Required |
| Microsoft_Organization | Required |
| Microsoft_JobDiscipline | Optional. The “Job function” filter in the dashboard will be available if this attribute is uploaded.  |

## Upload aggregated survey results

This process applies to the Microsoft 365 global admin.

You can also upload aggregated survey responses to enable a summary view of Copilot sentiment for the entire company. [Learn how using these steps](/microsoft-365/admin/adoption/ai-assistance). If you use this upload method, filters and heat maps are *not* supported. Filters and heat maps are only available to customers with a Viva Insights license.

>[!Note]
>If you upload survey data both as a .csv file *and* as aggregated results through the Microsoft 365 admin center, only the .csv survey results are shown in the dashboard. If you subsequently delete the .csv data, then the aggregated results are shown in the dashboard.

## Set minimum group size 

These steps apply both to Microsoft 365 global admins and Viva Insights admins.

>[!Note]
>This change will go into effect in 24 hours. This will be used for the metric comparison between groups in the Copilot dashboard.

The dashboard’s adoption and impact pages provide group-level metrics for groups that meet or exceed the minimum group size you set, which by default is 10 employees.

If your tenant does *not* have a Viva Insights license and you're a global admin, use these steps to set the minimum group size:

1. In the [Microsoft 365 Admin Center](https://admin.microsoft.com), go to the **Settings** tab and select **Microsoft Viva**, then **Microsoft Viva Insights**. 

2. Under **Copilot dashboard in Microsoft 365**, select **Manage minimum group size**. 

3. Enter your preferred minimum group size, which must be at least five, then select **Save**. 

    :::image type="content" source="../images/min-group-size-admin.png" alt-text="Screenshot that shows admins how to set the minimum group size.":::

Or, if your tenant has a Viva Insights license and you're a Viva Insights admin, [use these steps to change the minimum group size](../../advanced/setup-maint/privacy-settings.md).  

## Manage and upload non-Copilot users 

These steps apply to Microsoft 365 global admins.

>[!Note]
>When you upload a list of non-Copilot users for cohort analysis, the process could take up to five days. This will be used for the metric comparison between groups in the Copilot dashboard.

This feature lets you upload a list of non-Copilot users for cohort analysis in the dashboard. Cohort analysis enables leaders to compare the various metrics of two groups of users: Copilot users and non-Copilot users.

The maximum number of users you can add for cohort upload is equal to the number of your available Copilot licenses. Any additional users you add are not processed in the cohort list.

You can upload a list of users for cohort analysis in the [Microsoft 365 Admin Center](https://admin.microsoft.com). To do so, follow these steps: 

1. Go to the **Settings** tab and select **Microsoft Viva**, then **Microsoft Viva Insights**.  

2. Under **Microsoft Copilot Dashboard**, select **Manage non-Copilot users**.

    :::image type="content" source="../images/cohort-upload-03.png" alt-text="Screenshot that shows where to access the cohort upload feature.":::

3. Select **Import users**. Then choose the upload mode: **Add to existing users** or **Replace all existing with new users**. **Add to existing users** adds the new users to the existing list, while **Replace all existing with new users** overwrites the existing list with the new users.

    :::image type="content" source="../images/cohort-upload-01.png" alt-text="Screenshot that shows how import new Copilot users.":::

    >[!Note]
    >You’ll be able to upload non-Copilot users with Entra ID in the coming weeks. 

4. To upload a list of users, upload a .csv file that contains the “PersonId” of the users you want to include in the cohort analysis. The “PersonId” is a unique identifier for the employee record. It can be an employee's primary SMTP address or email alias. For example, person.name@xyz.com. For guidance, you can download a template for the .csv file from the admin center.

    :::image type="content" source="../images/cohort-upload-02.png" alt-text="Screenshot that shows how to import new users from a csv file.":::

5. Validate the list of users: Before you upload the list, you can validate the data to ensure that it’s accurate and compliant with the formatting rules. The validation checks for errors such as missing or invalid attributes, duplicate or conflicting records, or unsupported characters. The validation results show the number of errors, warnings, and successful records, and the results allow you to download a detailed report or fix the errors in the file. 

6. Confirm the list of users: After you upload the list, you can confirm the data and view a summary of the upload status, such as the number of users added, removed, or updated, the upload mode, and the upload date and time. The confirmation also shows a sample of the uploaded data and allows you to download the full list or undo the upload.

### Cohort upload scenarios based on Viva Insights licenses

Due to recent updates to the Copilot Dashboard, there are several scenarios to be aware of related to the number of Viva Insights licenses in the tenant during certain time periods. 

**Scenario 1: Tenant has Viva Insights licenses on June 30, 2024, and continues to have licenses going forward**

All the non-Copilot users who have Viva Insights licenses appear as non-Copilot users in the cohort. If you upload additional users for cohort analysis, they’re appended to the list of non-Copilot users. If you upload a list of cohort users with **Replace** mode, they’re included as non-Copilot users.

**Scenario 2: Tenant has Viva Insights licenses on June 30, 2024, but does not have them going forward**

Starting July 1, 2024, the non-Copilot user cohort is 0. Use cohort upload to generate the user list for cohort analysis. No history is saved for non-Copilot users who previously had Viva Insights licenses. 

**Scenario 3: Tenant doesn’t have any Viva Insights licenses on June 30, 2024, and doesn’t have any going forward**

You can only upload non-Copilot users in the Microsoft 365 admin center. The list of non-Copilot users is the same list of cohort users uploaded. 

**Scenario 4: Tenant doesn’t have any Viva Insights licenses on June 30, 2024, but purchases licenses at any time in the future**

When the tenant purchases Viva Insights licenses that are allocated to non-Copilot users, that group is part of the cohort analysis, together with additional uploaded non-Copilot users in Microsoft 365 Admin Center.

## Create an exclusion list (hide users from aggregates)

This process applies to Microsoft 365 global admins.

>[!Important]
>If you don’t create an exclusion list, *all* employees who either have a Copilot license, a Viva Insights license, or are uploaded manually using the Cohort upload feature in the admin center, are included in the Copilot dashboard’s insights. Any previous exclusions made in the analyst workbench do *not* apply to this feature. Any user exclusions you make with this feature do not apply elsewhere in Viva Insights or the analyst workbench.

>[!Note]
>When you upload an exclusion list, the process could take up to five days to run and complete. This means that users won’t be immediately excluded after the list is uploaded.

Your organization might want to exclude certain users from being included in the aggregated insights in the Microsoft Copilot Dashboard for various reasons, such as legal, compliance, or ethical concerns.

The user exclusion list allows Global admins to specify which employees' data should not be shown in the dashboard.

You can access this feature in the [Microsoft 365 Admin Center](https://admin.microsoft.com) using these steps: 


1. Go to the **Settings** tab and select **Microsoft Viva**, then **Microsoft Viva Insights**. 

2. Select **Exclusion list for the Copilot in Microsoft 365 Dashboard**. 

3. Select **Import users**. Then choose the upload mode: **Add to existing users** or **Replace all existing with new users**. **Add to existing users** adds the new users to the existing list, while **Replace all existing with new users** overwrites the existing list with the new users.

    :::image type="content" source="../images/exclusion-list-01.png" alt-text="Screenshot that shows how to import users with the exclusion list feature.":::

4. To upload a list of users, upload a .csv file that contains the “PersonId” of the users you want to include in the cohort analysis. The “PersonId” is a unique identifier for the employee record. It can be an employee's primary SMTP address or email alias. For example, person.name@xyz.com. For guidance, you can download a template for the .csv file from the admin center.

    :::image type="content" source="../images/exclusion-list-02.png" alt-text="Screenshot that shows how to upload a csv file for the exclusion list.":::

5. Validate the list of users: Before you upload the list, you can validate the data to ensure that it’s accurate and compliant with the formatting rules. The validation checks for errors such as missing or invalid attributes, duplicate or conflicting records, or unsupported characters. The validation results show the number of errors, warnings, and successful records, and the results allow you to download a detailed report or fix the errors in the file. 

6. Confirm the list of users: After you upload the list, you can confirm the data and view a summary of the upload status, such as the number of users added, removed, or updated, the upload mode, and the upload date and time. The confirmation also shows a sample of the uploaded data and allows you to download the full list or undo the upload. 


### Related topic

[Connect to the Microsoft Copilot Dashboard for Microsoft 365 customers](../../org-team-insights/copilot-dashboard.md)