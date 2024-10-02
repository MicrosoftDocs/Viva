---
title: "Manage admin roles in Viva Engage"
description: "Learn about admin roles and permissions in Viva Engage and how to assign them."
ms.reviewer: ethli
ai-usage: ai-assisted
ms.author: v-bvrana
author: Starshine89
manager: elizapo
ms.date: 05/20/2024
audience: Admin
f1.keywords:
- NOCSH
ms.topic: how-to
ms.service: viva-engage
ms.localizationpriority: high
ms.collection:  
- M365initiative-viva
- highpri
- essentials-manage
search.appverid:
- MET150
---

# Manage administrator roles in Viva Engage

To perform administrative tasks and facilitate many of the premium features in Viva Engage, users need to be assigned specific roles. The table below describes each of the admin roles in Viva Engage and the business functions they enable.

>[!NOTE]
>A Viva Engage license isn't required for an admin to configure Viva Engage (core or premium).
Unlike Viva Engage users, Microsoft 365 Global administrators and Engage administrators are exempt from needing a Viva Engage Core or premium license to access the [Engage website](https://engage.cloud.microsoft), the Engage Admin center, or legacy network admin center.
Other Viva Engage admin roles can also administer premium features without being assigned a premium license.

*Select a role in the table to learn more about it.*

|Admin role|Business function|
|------------|----------------|
|[Microsoft 365 Global Administrator](#microsoft-365-global-administrator)| Manages all aspects of Microsoft 365 Entra and services that use Microsoft 365 Entra identities. This role controls admin role assignment and configuration in Viva Engage. As such, global admins have unlimited access to settings and most of its data, including subscription management.|
|[Engage Administrator](#engage-administrator)| Configures and manages all aspects of Viva Engage including tenant settings, core and premium features, and compliance. This role is also referred to as *Yammer administrator* in Microsoft Entra ID.  |
|[Verified Administrator](#verified-administrator)| Configures the Viva Engage network. Performs tasks that have legal implications, such as managing security settings, monitoring keywords for appropriate use, managing data retention, and exporting data. |
|[Network Administrator](#network-administrator)| Configures the Viva Engage network|
|[Answers Administrator](#answers-administrator)| Configures Answers in Viva Engage, manages topics, and enables badges |
|[Corporate Communicator](#corporate-communicator)| Creates and manages official campaigns, defines leaders, and manages content across the organization |
|[Community Administrator](#community-administrator)| Manages day-to-day activity (including usage) within a community to keep it engaged and productive|

## Who assigns roles and where?

Some admins have more permissions than others and can assign Viva Engage roles to users. The following table lists admins in order of their permissions, with those having the most permissions at the top.

|Admin role | Can assign these roles |Assigned in|
|------------|-------|--------|
|Microsoft 365 Global Administrator|Other global admins, Engage admins, Answers admins (Knowledge manager)|Microsoft Entra ID|
|Engage Administrator|Verified admins, Network admins, Corporate communicators|Microsoft Entra ID|
|Verified Administrator|Verified admins, Network admins, Corporate communicators|Yammer admin center / Viva Engage admin center|
|Network Administrator|Other network admins, Corporate Communicators|Yammer admin center / Viva Engage admin center|
|Community Administrator|Other community admins|Viva Engage community|

## Role hierarchy

:::image type="content" source="../media/engage/admin/engage-admin-hierarchy.png" alt-text="Diagram that shows the hierarchy of administrator roles in Viva Engage, with roles having the most power at the top.":::

## Microsoft 365 Global Administrator

|Function |Details |
|------------|-----------------|
|**Permissions** |<ul><li>Assign or remove the [Microsoft 365 Global administrator role](/microsoft-365/admin/add-users/about-admin-roles#commonly-used-microsoft-365-admin-center-roles)</li><li>Manage other Microsoft 365 services</li><li>View reports in [Microsoft 365 usage analytics](/microsoft-365/admin/usage-analytics/usage-analytics)</li><li>[Set up and manage Viva Engage](/viva/engage/setup)</li><li>[Manage feature access with usage policies in Microsoft 365](/viva/engage/configure-copilot-for-engage#control-access-to-copilot-and-ai-summarization-services)</li><li>[Configure Answers](/viva/engage/eac-answers-overview-set-up)</li></ul>|
|**Who can assign**|A Microsoft 365 Global administrator|
|**How to assign**| See [Assign admin roles in the Microsoft 365 admin center](/microsoft-365/admin/add-users/assign-admin-roles)|

## Engage Administrator

|Function |Details |
|------------|-----------------|
|**Permissions** |<ul><li>[Configure Viva Engage](/viva/engage/setup) and its features for the organization, including data management and compliance, network settings</li><li>For Viva Engage core, assign the [Corporate Communicator](#corporate-communicator)</li><li>For Viva Engage premium, assign additional permissions and features:<ul><li>[Identify leaders and their audiences](/viva/engage/leadership-identification)</li><li>[Set up storylines](/viva/engage/eac-storyline)</li><li>[Access analytics features](/viva/engage/analytics) and data collected for metrics</li><li>[Create and manage official campaigns](/viva/engage/campaigns)</li><li>[Manage Answers](/viva/engage/eac-answers-admin-scenarios)</li><li>[Manage feature access with usage policies in Microsoft 365](/viva/engage/configure-copilot-for-engage#control-access-to-copilot-and-ai-summarization-services)</li></ul>|
|**Who can assign**|A Microsoft 365 Global administrator|
|**How to assign**| Assign the Engage admin role in [Microsoft Entra ID](/microsoft-365/admin/add-users/assign-admin-roles) or [Privileged Identity Management (PIM)](/entra/id-governance/privileged-identity-management/pim-how-to-add-role-to-user)|

## Verified Administrator

|Function |Details |
|------------|-----------------|
|**Permissions** |<ul><li>Manage content policies, monitors keywords, data retention, security settings, and reading data in private communities</li><li>Assign verified and network admin roles</li><li>[Identify leaders and their audiences](/viva/engage/leadership-identification)</li><li>[Export data](/viva/engage/eac-as-manage-data) and perform integrations with other tools</li></ul>|
|**Who can assign**|Engage admin or verified admin|
|**How to assign**|In the [Yammer admin center](https://www.yammer.com/yammertest10.onmicrosoft.com/), select **Admins**.  Find and select the user's name and select **Make this user an admin**. If the user is already an admin, find their name from the Current Admins list and select **Grant Verified Admin**.</li></ul>|

## Network Administrator

|Function |Details |
|------------|-----------------|
|**Permissions** |<ul><li>Configure network settings, usage policy, and user profiles</li><li>Manage internal users, [outside guests](/viva/engage/get-started-with-viva-engage/azure-ad-b2b-guests-viva-engage), and unlisted groups</li><li>[Close and reopen conversations](https://support.microsoft.com/en-gb/topic/close-pin-or-report-a-conversation-in-viva-engage-1d2489a7-925f-40f7-9f0a-b32e6a6d4f27) in communities and storylines on behalf of any user<li>[Identify leaders and their audiences](/viva/engage/leadership-identification)</li><li>View reports in the Microsoft 365 Usage Reporting dashboard</li></ul>|
|**Who can assign**|Engage admin or network admin|
|**How to assign**|In the [Yammer admin center](https://www.yammer.com/yammertest10.onmicrosoft.com/), select **Admins**.  Find and select the user's name and select **Make this user an admin**. If the user is already an admin, find their name from the Current Admins list and select **Grant Network Admin**.</li></ul>|

## Answers Administrator  

|Function |Details |
|------------|-----------------|
|**Permissions** |<ul><li>Manage Answers in Viva Engage. (For details, see [list of permissions.](/viva/engage/eac-answers-admin-scenarios#permissions))</li><li>[Manage topics](/microsoft-365/topics/topic-experiences-viva-engage) in Answers</li><li>Manage badges</li><li>View global insights</li></ul>|
|**Who can assign**|A Microsoft 365 Global administrator|
|**How to assign**|Assign a [Knowledge Manager role in Microsoft Entra ID](/entra/identity/role-based-access-control/permissions-reference)</li></ul>|

## Corporate Communicator

|Function |Details |
|------------|-----------------|
|**Permissions** |<ul><li>Send announcements</li><li>[Identify leaders and their audiences](/viva/engage/leadership-identification)</li><li>[Feature conversations](https://support.microsoft.com/en-us/office/feature-a-conversation-in-viva-engage-92469ece-8a63-424f-9ad6-802ad90fc5c4)</li><li>Create and manage official campaigns:<ul><li>Publish draft campaigns to Active and viewable to the network</li><li>Set Active campaigns to Ended</li><li>Republish recurring campaigns from **Ended** to **Active**</li><li>Delete campaigns created by mistake</li><li>Update campaign assets (such as goal tracker, cover photo, hashtag theme colors, pinned posts, pinned resources and links</li><li>View campaign analytics</li></ul>|
|**Who can assign**|Engage admin|
|**How to assign**|In the Viva Engage admin center, on the **Setup and configuration** tab, select **Manage corporate communicators**. Select **Add user** to search for a user by name or email ID. Assignees appear in the list of active corporate communicators in your organization.|

## Community Administrator

|Function |Details |
|--------|-----------------|
|**Permissions** |Community admins only have permissions in their communities:<ul><li>[Add and remove members](/viva/engage/manage-viva-engage-users/add-block-or-remove-users) and community admins.</li><li>Manage conversations, including marking best answers, removing posts, and closing posts to replies.</li><li>Manage settings, such as [customizing the community appearance](https://support.microsoft.com/en-us/office/customize-a-viva-engage-community-d74a23a1-c3aa-4b5f-abf7-61b912138609) and changing the default post type.</li><li>[Send announcements](https://support.microsoft.com/en-us/topic/storyline-announcements-in-viva-engage-8db19630-ecd0-4d1e-b735-437aea62e248).</li></ul>
 |**Who can assign**|Engage admins can assign community admins. Additionally, any Engage user who creates a community is automatically assigned the community admin role. Community admins can assign up to 100 other community admins.<br>**Note:** Network admins and verified admins can prevent Engage users from creating communities. In this case, they must assign the initial community admin who performs all community admin tasks. |
|**How to assign**|On the community page, select **Settings** icon > **Manage Members and Admins**. Choose a user and select either **Make Admin** or **Revoke Admin**.|
