---
title: Export and import Viva Glint User Role members
description: Admins can export lists of members associated with specific roles from the People page on their admin dashboard and import users in User Roles.
ms.author: JudithWeiner
author: JudyWeiner
manager: MelissaBarry
audience: admin
f1.keywords: NOCSH
keywords: export default roles, People page export function, role import
ms.collection: 
 - m365initiative-viva
 - selfserve
search-appverid: MET150
ms.topic: article
ms.service: viva-glint
ms.localizationpriority: high
ms.date: 10/09/2024
---

# Export and import Viva Glint User Role members

Viva Glint Administrators can export lists of members associated with specific roles from the People page and import users in User Roles.

## View User Roles on the People page

:::image type="content" source="../../media/glint/setup/user-roles-column-people-page.png" alt-text="Screenshot that shows how to view User Roles in the People feature.":::

The left-most column shows all User Roles set up for your organization. 

## Export an individual role

All exports generate a .csv download. Downloads may take a few minutes, depending on the number of members.

1. Select a User Role and then select **Export**.

   :::image type="content" source="../../media/glint/setup/user-role-export.png" alt-text="Screenshot that shows how to Export roles in the People feature.":::
   
4. A new Export dialog opens.
   
   :::image type="content" source="../../media/glint/setup/export-manager-role.png" alt-text="Screenshot of the Export role dialog for the Manager role.":::

5. The .csv report includes first and last names, email address, and employee status. Choose whether to include all user attributes and User Roles.
6. Select  **Export**.
7. After following these steps, you'll receive a "Report Downloaded" message in a new browser tab.

   :::image type="content" source="../../media/glint/setup/report-downloaded.png" alt-text="Screenshot of the Report Downloaded dialog box.":::

## Import users to a User Role

> [!IMPORTANT]
> Importing a list of users to a User Role removes attribute rules that automatically add users based on their attribute values.

1. As a Viva Glint Admin, go to **Configuration** and select **User Roles** in the **Employees** section.
2. Select a User Role to update.
3. On the role's detail page, select **Add/Edit Employees**.
4. In the dialog that appears, select the **Import** option.
  
   :::image type="content" source="../../media/glint/setup/add-employees-role-modal.png" alt-text="Screenshot of the dialog that appears when a user adds members to a User Role.":::

5. In the **Import Employees to role** dialog that appears, select **Download CSV** to download a list of users that are in the User Role.

   :::image type="content" source="../../media/glint/setup/import-to-role-modal.png" alt-text="Screenshot of the dialog that appears when a user selects the Import option to add users to a role.":::

6. A .csv file downloads to your device with an **email** column. Add or remove email addresses for users that should leave or join this role. Save the edited file as .csv or .xlsx.
   1. Users in this file must already have a record in Viva Glint and the email address added to the User Role file must match their email in Viva Glint.
7. In the User Role **Import Employees to role** dialog, drag and drop to upload or browse to choose your list of users for this role.
   - Select **Preserve the employees already in this role** to keep existing users
   - Deselect **Preserve the employees already in this role** to replace all existing users with the users in the uploaded file.
8. Select **Import File.**
9. In the **Confirm your import** dialog that appears, review the summary of changes and select **Confirm Import** or **Cancel**.
    
    :::image type="content" source="../../media/glint/setup/confirm-role-import-modal.png" alt-text="Screenshot of the dialog that appears for a user to confirm their user role import.":::

10. Return to the User Role details page and check that the number of members decreased or increased as expected.
