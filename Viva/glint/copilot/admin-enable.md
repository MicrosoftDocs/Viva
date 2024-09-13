---
title: Administrator enablement for Microsoft 365 Copilot in Viva Glint (preview)
description: Administrators enable Microsoft 365 Copilot in Viva Glint. 
ms.author: JudithWeiner
author: JudyWeiner
manager: MelissaBarry
audience: admin
f1.keywords: NOCSH
keywords: 
ms.collection:  
- m365initiative-viva
- selfserve
- viva-copilot
- magic-ai-copilot 
search.appverid: MET150 
ms.topic: article
ms.service: viva-glint
ms.localizationpriority: high
ms.date: 09/12/2024
---

# Administrator enablement for Microsoft 365 Copilot in Viva Glint (preview)

Prerequisites to enabling Microsoft 365 Copilot in Viva Glint:
- You have at least one Recurring or Ad hoc survey administered or closed on the Viva Glint platform
- Your dashboard default language is set to English

Admins enable Copilot in Viva Glint. Microsoft privacy policies prohibit Copilot in Viva Glint from being enabled by default for any User Roles. 

Assign yourself and others using Copilot in Viva Glint to a new User Role. Create the new User Role with access to the Comments Report enabled. Add that User Role to the survey [**Reporting** page](https://go.microsoft.com/fwlink/?linkid=2285645) in **Program Summary**.

>[!IMPORTANT]
>Users without access to the Comment Report can't access Copilot in Viva Glint.

## Grant Comment Report permission

From your admin dashboard, follow this process:

1.	Select the **configuration (cogwheel)** symbol.
2.	In the **Employees** section, select **User Roles**.
3.	Select the User Role to provide Comment Report access. In this example, Company Admin is chosen.
   
    :::image type="content" source="../../media/glint/setup/copilot-select-user.png" alt-text="Screenshot of how to give a User Role Copilot in Viva Glint permissions." lightbox="../../media/glint/setup/copilot-select-user.png":::

    > [!NOTE]
    > The Manager role has Comment Report permission enabled as a default setting.

4. Select **Permissions**.
  
   :::image type="content" source="../../media/glint/setup/copilot-permissions.png" alt-text="Screenshot of the Permissions access row in **Role Settings**." lightbox="../../media/glint/setup/copilot-permissions.png":::

5.	In the **Reporting** section of the Permissions and Access page, enable **View Comments**.

    :::image type="content" source="../../media/glint/setup/copilot-view-comments-toggle.png" alt-text="Screenshot of the View Comments checkbox.":::

## Grant Comment Reports access

The second step to enabling the Copilot in Viva Glint feature for User Roles happens in the program's **Reporting** section. This step allows users enabled for the Comment Reports to access the report.

From your admin dashboard, follow this process:

1.	Select the **configuration** symbol.
2.	In the **Surveys** section, select **Survey Programs**.
3.	**Select the closed Recurring or Ad hoc program** for which you want to grant access.
4.	In **Program Summary**, select **Reporting**.

     :::image type="content" source="../../media/glint/setup/copilot-reporting.png" alt-text="Screenshot of the Reporting section in Program Summary." lightbox="../../media/glint/setup/copilot-reporting.png":::

5. In **Program Roles**, select the User Role to enable with Copilot in Viva Glint. *In this example, the customized role is 'VI'.*

    :::image type="content" source="../../media/glint/setup/copilot-program-roles.png" alt-text="Screenshot of an example User Role." lightbox="../../media/glint/setup/copilot-program-roles.png":::

6. Toggle **Copilot in Viva Glint** to **On** and then **Save Changes**.

    :::image type="content" source="../../media/glint/setup/copilot-enabled.png" alt-text="Screenshot of the Role Permissions sections within the Reporting section." lightbox="../../media/glint/setup/copilot-enabled.png":::

## Ensure Copilot in Viva Glint is enabled

From your admin dashboard, follow this process:

1.	Select the **Configuration** symbol.
2.	Select **User Roles** in the **Employees** section to see the list of all users assigned to a particular role.
3.	Select any employee in a User Role in which you expect Copilot to be enabled.
4.	Once you are on that user’s profile, select **View As** to validate the user’s reporting experience.

    :::image type="content" source="../../media/glint/setup/copilot-view-as.png" alt-text="Screenshot of the View As button in User Roles.":::

5. Be sure you see the Copilot button on the user's Viva Glint dashboard.

   :::image type="content" source="../../media/glint/setup/copilot-access-button.png" alt-text="Screenshot of the Copilot capability on the manager dashboard." lightbox="../../media/glint/setup/copilot-access-button.png":::

## More Resources

[**Learn how managers can use Copilot in Viva Glint**](https://go.microsoft.com/fwlink/?linkid=2274072)
[**Find answers to technical FAQs**](https://go.microsoft.com/fwlink/?linkid=2274071)
[**Copilot for Microsoft 365**](https://adoption.microsoft.com/copilot/)
