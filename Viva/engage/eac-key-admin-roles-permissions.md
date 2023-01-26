---
title: "Key admin roles and permissions in Viva Engage"
description: "Viva Engage is a new employee experience that connects people across the company—wherever and whenever they work—so that everyone is included and engaged."
ms.reviewer: ethli
ms.author: mamiejohnson
author: mamiepjohnson
manager: dmillerdyson
audience: Admin
f1.keywords:
- NOCSH
ms.topic: article
ms.service: viva
ms.subservice: viva-engage
localization_priority: Priority
ms.collection:  
- M365initiative-viva
- highpri
search.appverid:
- MET150
---

# Key admin roles and permissions in Viva Engage

The following roles will have access to the Engage admin center within the Viva Engage app:  

- Global admin 
- Engage admin  
- Answers admin  
- Corporate communicator 

## Office365 (Global) admin 

This role has unlimited access to your organization’s settings and most of its data. Naturally, the global admin has permissions to perform all configurations for Viva Engage in your organization. Navigate [here](https://learn.microsoft.com/microsoft-365/admin/add-users/about-admin-roles?view=o365-worldwide) to learn more about this role and security guidelines for assigning it.   

## Engage admin  

The Engage admin can set up and configure Engage for your organization and manage data, network related settings, and the various seeded or premium features within the application. The new role of Engage admin will be designated by [adding Yammer administrators in AAD](https://techcommunity.microsoft.com/t5/yammer-blog/the-new-yammer-administrator-role-is-now-available-in-azure/ba-p/3592577). Yammer AAD administrators will automatically become Engage admins and they will have elevated permissions over end users. Tying the Engage admin to the Yammer administrator AAD role was intentional, since Viva Engage as an application is powered by Yammer technology.  

>[!NOTE]
> This admin role can be assigned and modified by a global admin through AAD, PIM, group based role assignments, or Azure portal and PowerShell.  

**Permissions**

The table below shows the range of actions available to Engage admin and Global admin based on their license. Admin permissions will be dependent on the users having the right licensing to configure those features.

> [!div class="mx-tdBreakAll"]
> |**Permissions - Roles in consideration: Engage admin and Global admin**|**M365/O365 customer with Viva Engage seeded**|**Microsoft Viva suite customer**|
> |-------------|----------|---------|---------|
> |**Manage corporate communicators**
- Assign user(s) as a corporate communicator
- Remove user(s) as a corporate communicator|✓|✓|
> |**Manage tenant and user permissions (through Yammer)**|✓|✓|
> |**Manage data and compliance** 
- Manage network and user data 
- **GDPR** delete|✓|✓|
> |**Manage leaders and their audiences** 
- Assign leaders in your organization 
- **Identify audiences for the leaders identified**|✓|✓|
> |**Configure stories and storylines** <br>
- Enable storylines and stories for your organization <br>
- Configure advanced settings like default notifications, specify who can create storyline posts, etc. |✓|✓|
> |**Manage sentiment analysis and other feature specific analytics**<br>
- Configure level of sentiment to be gathered in the organization <br>
- Enable or disable campaign analytics <br>
- Enable or disable answers analytics **| |✓|
> |**Add, view, and manage campaigns**<br>
- Create and manage campaigns <br>
- Access campaign analytics dashboard **| |✓|
> |**Enable and manage badges**| |✓|
> |**Enable Answers**| |O365 (Global) admin only|

## Answers admin  

The Answers admin role can setup and configure Answers within the Viva Engage application. This role can only be assigned or modified by an O365 (Global) admin and will be designated by [adding Knowledge Managers in AAD](https://learn.microsoft.com/azure/active-directory/fundamentals/active-directory-users-assign-role-azure-portal?context=%2Fazure%2Factive-directory%2Froles%2Fcontext%2Fugr-context). All Knowledge Managers will become Answers admins and they will have elevated permissions over end users. Tying the Answers admin to the Knowledge Manager AAD role was intentional, since Answers is best experienced when integrated with Topics.  

**Permissions**

The table below shows the range of actions available to an unlicensed user, Viva Topics licensed user, Answers admin (knowledge manager), Engage (Yammer) admin, and Global admin.

> [!div class="mx-tdBreakAll"]
> |**Answers Permissions - Roles in consideration: Answers admin, Engage admin and Global admin**|**M365/O365 customer with Viva Engage seeded**|**Viva Suite and Viva Topics customer**|
> |-------------|---------|---------|
> |**Ask, answer, upvote, and react**|Interact with questions they are mentioned in|✓|
> |**Suggest topics**| |✓|
> |**Mark Best answer**| |✓|
> |**Delete and close posts**| |✓|
> |**See global insights**| |✓|
> |**Feature topics**| |Answers admin and Global admin only|
> |**Approve suggested topics**| |Answers admin and Global admin only|
> |**Enable and manage badges**| |Answers admin and Global admin only|
> |**Enable Answers**| |Answers admin and Global admin only|

## Corporate communicator 

Corporate communicators have privileges such as creating or managing campaigns, defining leaders in an organization, and more to come as we evolve Viva Engage. This role was created so that it addresses the need to have a role catered towards content management in the organization, beyond being attached to a community (Community admin) but not as powerful as the overall Engage admin. Corporate communicators can be assigned, modified, or deleted from users by the following admin roles: Global admin, Engage admin and fellow corporate communicators. 

**Permissions**

The table below shows the range of actions available to a corporate communicator, Engage (Yammer) admin, and Global (tenant) admin based on their license.  

> [!div class="mx-tdBreakAll"]
> |**Permissions - Roles in consideration: corporate communicator, Engage admin and Global admin**|**M365/O365 customer with Viva Engage seeded**|**Microsoft Viva suite customer**|
> |-------------|----------|---------|---------|
> |**Identify leaders** <br>
- Manage their audience <br>
- Manage their delegates|✓|✓|
> |**Create campaigns**| |✓|
> |**Manage campaigns via:** <br>
- Publishing active campaigns <br>
- Ending active campaigns <br>
- Republishing ended campaigns <br>
- Deleting campaigns| |✓|
> |**View campaign analytics**| |✓|

## See also 

[Access the Engage admin center](/Viva/engage/eac-as-access-eac.md)

[Answers admin scenarios in Viva Engage](/Viva/engage/eac-answers-admin-scenarios.md)
