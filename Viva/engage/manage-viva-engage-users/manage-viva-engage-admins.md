---
title: "Manage Viva Engage admins"
f1.keywords:
- NOCSH
ms.author: v-bvrana
author: Starshine89
manager: pamgreen
ms.date: 7/12/2023
audience: Admin
ms.topic: reference
ms.service: viva
ms.subservice: viva-engage
ms.localizationpriority: medium
ms.custom: Adm_Viva Engage
search.appverid:
- MET150
- MOE150
- YAE150
ms.assetid: 4f6763f4-23e2-43b0-a554-08931295e863

description: "Explains all the admin roles used in Viva Engage, and how to assign and revoke admin roles."
---

# Manage Viva Engage admins

Only users with appropriate roles can perform administrative tasks in Viva Engage. Some roles are managed in Azure Active Directory, and some roles are managed in Viva Engage.

Below are the available roles, their purpose, and the actions that can be performed. Select the role name for a detailed list of tasks available for a role, and for steps to add and remove each role.
  
| Role <br/> | Business purpose <br/> |
|:-----|:-----|
|[Global Admin](manage-viva-engage-admins.md#bmk_global) <br>(Azure Active Directory)<br/> |Manage all aspects of Azure Active Directory  (AD) and Microsoft services that use Azure AD identities, including all tasks a Viva Engage Verified Admin and Office 365 report reader can perform.  <br> Users are assigned this role in Azure Active Directory and reflected in Viva Engage as a Verified Admin.  <br/> |
|[Viva Engage Administrator](manage-viva-engage-admins.md#bmk_yadmin) (Azure Active Directory)<br/> |All the tasks a Viva Engage Verified Admin and Office 365 report reader can perform.  Users are assigned this role in Azure Active Directory and are reflected in Viva Engage as a Verified Admin. <br/> <p>**Note:** This role is currently in preview and not available to all customers. |
|[Viva Engage Verified Admin](manage-viva-engage-admins.md#bmk_verified) <br/> |Configure the Viva Engage network and perform tasks with legal implications for the data stored in Viva Engage, such as configuring security settings, monitoring keywords for appropriate use, managing data retention, and exporting data.  <br/> |
|[Viva Engage Network Admin](manage-viva-engage-admins.md#bmk_network) <br/> |Configure the Viva Engage network.  <br/> |
|[Viva Engage Community Admin](manage-viva-engage-admins.md#bmk_group) <br/> |Manage day-to-day activity within a community to keep the community engaged and productive, including monitoring usage activity.  <br/> |
|[Office 365 Report Reader](manage-viva-engage-admins.md#bmk_reports) <br/> |View reports showing overall Viva Engage usage. This role is helpful for anyone assigned to improve and monitor Viva Engage adoption.  <br/> |
   
You grant and change most admin roles in the Viva Engage admin center. In the following screenshot, Debra Berger is a Verified Admin, Diego Siciliani is a Network Admin, and Megan Bowen is a Global Administrator.
  
:::image type="content" source="../../media/52935d22-dd99-418d-b0e7-9ba70c357042.png" alt-text="Screenshot showing the list of admins.":::
  
<a name="bmk_global"> </a>
## Global Administrator (Azure Active Directory)
The Global Administrator role is assigned in Azure Active Directory. Any user assigned this role has administrative access to all features in Azure Active Directory, services that use Azure Active Directory identities, and the ability to manage subscriptions. Any user assigned this role is synchronized to Viva Engage and reflected as a Viva Engage Verified Admin. 

| Function <br/> | Details <br/> |
|:-----|:-----|
|**Tasks** <br/> |All the tasks a Verified Admin can do, and: <br/><br> Add and remove the Global  Administrator role and the Office 365 reports reader role from other users <br/><br> View reports in the Office 365 Usage Reporting dashboard <br/><br> Manage other Microsoft 365 services<br/><br>  |
|**Who can give this role to others** <br/> | Other users assigned the Global Administrator role.          |
|**How is the Global Administrator role added or removed?** <br/> | **To assign a new Global Administrator, see:**<br> [Assign admin roles for adding the role in Azure Active Directory](/microsoft-365/admin/add-users/assign-admin-roles). <br> <br/> **To remove a  Global Administrator from Viva Engage:** <p> In the Viva Engage admin center, click **admins**. In the row for the admin, select **Change status of Microsoft 365 Admins**. This takes you to the Microsoft 365 page where the role can be changed.|

<a name="bmk_yadmin"> </a>
## Viva Engage Administrator (Azure Active Directory)
The Viva Engage Administrator role is assigned in Azure Active Directory. Any user assigned this role is synchronized to Viva Engage and reflected as a Viva Engage Verified Admin. <p>**Note:** This role is currently in preview and not available to all customers.

| Function <br/> | Details <br/> |
|:-----|:-----|
|**Tasks** <br/> |All the tasks a Viva Engage Verified Admin can perform.  |
|**Who can give this role to others** <br/> | Another user with the role of Global Administrator or Privileged Role Administrator.       |
|**How is the Viva Engage Administrator role added or removed?** <br/> | **To assign a new Viva Engage Administrator, see:** [Assign admin roles for adding the role in Azure Active Directory](/microsoft-365/admin/add-users/assign-admin-roles).  |

<a name="bmk_verified"> </a>
## Viva Engage Verified Admin

| Function <br/> | Details <br/> |
|:-----|:-----|
|**Tasks** <br/> |All the tasks a Network Admin can do, and:    <br/><br>  Assign verified and network admin roles. Manage content policies, including monitor keywords, data retention, security settings, and reading data in private groups.<br/><br>  Export data <br/><br>  Perform integrations with other tools <br/><br> For instructions on typical tasks for  Verified Admins, see [Viva Engage admin help](../overview.md).|
|**Who can give this role to others** <br/> | A Global Administrator, Viva Engage Administrator, or Viva Engage Verified Admin.       |
|**How is the Viva Engage Verified Admin role added or removed without granting the user Global Administrator or Viva Engage Administrator role in Azure Active Directory?** <br/> | **To assign a new Verified Admin:** <br> In the **Appoint Additional Admins** section, search their name, select **Make this user an admin**, and click **Submit**. Find the user in the Current Admins list, and click **Grant Verified Admin**. <br/><br>**To promote an existing Network Admin to Verified Admin:** <br>In the Viva Engage admin center, click **Admins**. If the user is already a network admin, their name will show up in the Current Admins list. Select **Grant Verified Admin**. <br/><br> **To change a Verified Admin  to Network Admin:** <br> In the Viva Engage admin center, click **Admins**. In the **Current Admins** section, in the row for the admin, click **Revoke Verified Admin**. <br/><br> **To remove all admin roles from a Verified Admin:** <br> In the Viva Engage admin center, click **Admins**. In the Current Admins section, in the row for the admin, click **Remove**. <br/> |

<a name="bmk_network"> </a>
## Viva Engage Network Admin

| Function <br/> | Details <br/> |
|:-----|:-----|
|**Tasks** <br/> | Configure network settings, including logo and colors, usage policy, what's included in user profiles. <p>  Manage internal users, outside guests, and unlisted groups<p>  Grant and revoke the Network Admin role <br/> |
|**Who can give this role to others** <br/> | A Global Administrator, Viva Engage administrator, Viva Engage Verified Admin, or Viva Engage Newtwork Admin. |
|**How is the Viva Engage Administrator role added or removed?** <br/> |  **To assign a new Viva Engage Network Admin:** <br> In the Viva Engage Admin Center, click **Admins**. In the **Appoint Additional Admins** section, enter the user's name. Select **Make this user an admin**, and click **Submit**.  <br/><br> **To remove a Network Admin:** <br> In the Viva Engage admin center, click **Admins**. Select the user's name, and click **Remove**. <br/>  |

<a name="bmk_group"> </a>
## Viva Engage Community Admin

| Function <br/> | Details <br/> |
|:-----|:-----|
|**Tasks** <br/> |  Manage the settings for the community, including name, description, image, and header colors. <p>  Manage the conversations and files in the community <p>  Manage members and group admins <p>  Post announcements <p>For instructions for typical tasks to manage a Viva Engage community, see [Manage a group in Viva Engage](https://support.office.com/article/6e05c6d6-5548-4c88-89cd-e6757a514ef2.aspx).  <br/> |
|**Who can give this role to others** <br/> | Any Viva Engage user who creates a community is assigned the Community Admin role automatically, and can add or remove other Community Admins. There is a limit of 100 Community Admins per group. <br/><br> Verified Admins can add or remove Community Admins in any groups.  <br/><br> Network Admins can only add or remove Community Admins for groups they are a member of.  <br/><br> **Note:** Network Admins and Verified Admins can disable the ability for Viva Engage users to create groups. In this case, they must assign the initial Community Admin, who then can do all community admin tasks for the group, including adding more Community Admins. For more information, see [Manage who can create Groups](https://support.office.com/article/4c46c8cb-17d0-44b5-9776-005fced8e618).          |
|**Add or remove a group admin from a group** <br/> | On the group page, click the **Settings** icon, select **Manage Members and Admins**, choose a user, and then select either **Make Admin** or **Revoke Admin**.  <br/> |

<a name="bmk_reports"> </a>
## Office 365 Report Reader

| Function <br/> | Details <br/> |
|:-----|:-----|
|**Tasks** <br/> | View usage reports for Viva Engage in the Office 365 usage reporting dashboard.  <br/><br> For information about accessing and interpreting reports, see: <br>[Office 365 Reports in the Admin Center - Viva Engage activity report](https://support.office.com/article/C7C9F938-5B8E-4D52-B1A2-C7C32CB2312A)<P>[Office 365 Reports in the Admin Center - Viva Engage groups activity report](https://support.office.com/article/94dd92ec-ea73-43c6-b51f-2a11fd78aa31)<P>[Office 365 Reports in the Admin Center - Viva Engage device usage report](https://support.office.com/article/B793FFDD-EFFA-43D0-849A-B1CA2E899F38)  <br/> |
|**Who can give this role to others** <br/> |A Global Administrator <br/> |
|**Add or remove a report reader role** <br/> | In Office 365, go to **Admin** \> **Users** \> **Active Users** and select a user. <br><br>For details, see [Assign admin roles in Office 365 for business](https://support.office.com/article/eac4d046-1afd-4f1a-85fc-8219c79e1504). <br/> |

<a name="Troubleshooting"> </a>
## Troubleshooting admin roles - FAQs

### Q: Can I change my own admin role for Viva Engage?

A: No. Admins can't edit their own roles.
  
### Q: How can I find out who the network and verified admins are for our network?

A: Non‐admin users can see all admins in the **Members** list in the **All Company** group. Admins have a star next to their name. You can also see a list of admins at **https://yammer.com/***your_network***/admin**.
  
Admins can view the list in the Viva Engage admin center by selecting **Admins**. Admins can also export a list of admins to review who has the Network Admin role and who has the Verified Admin role. In the Viva Engage admin center, select **Export Users**. In the exported .ZIP file, open **Admins.csv**. 
  
### Q: I'm an Office 365 Global Admin, so why don't I see any admin tools when I log on to Viva Engage?

A: Check these troubleshooting options to determine why an admin isn't receiving emails from Viva Engage:
  
1. Has the admin created a Viva Engage account?
    
    The Office 365 automated process syncs the Global Admin as a Verified Admin in Viva Engage, but the user must still create an account in Viva Engage to receive a confirmation email.
    
2. Is the admin on the correct domain?
    
    The user must have an email address that is in the same company domain that you used to activate Viva Engage. If you create an admin in customer.uk, but the Viva Engage network you've activated is customer.com, the admin will not be synced as a Viva Engage Verified Admin. For more information on how to edit an admin's domain, see [Set up your Viva Engage network (Viva Engage activation guide)](https://support.office.com/article/e10998fe-f001-42f3-9597-b170d360f475).
    
3. Is the admin using a generic email?
    
    An admin cannot have a generic email address and must be assigned to a real user. To regulate this, there are certain words that are not allowed in the email address of a Global Admin:
    
      - admin, noreply, help, support, workfeed, feedback, yammer, api, abuse, postmaster, hostmaster, root, new, create, index, show, destroy, delete, and update
    
4. Has your company added Viva Engage.com to the Safe Recipients list?
    
    Your email service could be blocking emails from the Viva Engage domain. Please check to make sure Viva Engage.com is on a Safe Recipients list at your company and is not otherwise prevented from delivering emails.
