---
title: Set up Viva Glint User Roles
description: Admins can customize roles to view and modify members, attributes, and permissions.
ms.author: JudithWeiner
author: JudyWeiner
manager: MelissaBarry
audience: admin
f1.keywords: NOCSH
keywords: permissions, bulk imports, user role imports, custom access 
ms.collection: 
 - m365initiative-viva
 - selfserve
search-appverid: MET150
ms.topic: article
ms.service: viva
ms.subservice: viva-glint
ms.localizationpriority: high
ms.date: 01/26/2024
---

# Set up Viva Glint User Roles

Admins can assign multiple roles with specific permissions - access to different segments of data and filter - within **User Roles** from the admin configuration dashboard. The User Roles and Access Template include prepopulated example roles and detailed instructions for two areas of setup. Use it to help plan your Microsoft Viva Glint programs.

:::image type="content" source="../../media/glint/setup/user-roles-access.png" alt-text="Screenshot that shows how to access User Roles from the Admin Config dashboard.":::

> [!TIP]
> To protect confidentiality, give managers access to only one filterable attribute. Assigning more than one filterable attribute could increase the chance that a manager may be able to deduce the origin of individual responses.

### [Download this template to use as a planning tool to define permissions for User Roles](https://www.microsoft.com/en-us/download/details.aspx?id=105793)

You can use the template as a planning tool to define permissions that your User Roles are allowed to view, according to these three filter distinctions:

- **Report filters**: Attributes this role can view while searching results
- **Report sections**: Which section a user can add to reports
- **Comment filters**: Attributes this role must have to view the Comments report

>[!IMPORTANT]
> Not all User Roles and pre-populated attributes and permissions in a template may apply to your organization. Consult your Employee Attribute File for attributes specific to your organization and make changes, as necessary.

## Default User Roles

The following roles are pre-configured in Viva Glint and can't be edited. Create a new User Role to edit attributes and permissions.

- Company Admin
  - Advanced Configuration Access
- Active Employees
- Inactive Employees
- Managers
- Support Users

## Create User Roles

Program admins can specify the employee population and report filters their leaders can view on their dashboard based on manager, HRBP, and executive roles. Defining roles is important for data cuts, access permissions, and program integrity.

1. Select the **Configure** symbol.
2. In the **Employees** section, select **User Roles**.
3. You'll see predefined User Roles initially, in the Role column. Typically:
   1. Active Employees: Not intended to have data access
   2. Company Admin: Employees who are granted **ALL** permission; can't be edited
   3. Inactive employees: Not intended to have data access
   4. Manager: Commonly used and prepopulated; permissions and attributes can be edited
  
   :::image type="content" source="../../media/glint/setup/user-roles-page.png" alt-text="Screenshot that shows columns and the New Role button on the User Roles page.":::

## Add new User Roles

Select **+ New Role**. The *Role Settings* window opens.
Enter a User Role in the **Untitle Role** name by selecting the **pencil** symbol.

## View and edit Role Settings sections

You can do the following from the Role Settings page:
- Grant permissions
- Configure report attributes

   :::image type="content" source="../../media/glint/setup/user-roles-title.png" alt-text="Screenshot of the Role Settings page.":::

### Permissions and Access setup

Select **Permissions** in the *Role Settings* section. The **Permissions and Access** page opens.

:::image type="content" source="../../media/glint/setup/user-roles-access-permissions.png" alt-text="Screenshot of Access Permissions in Role Settings.":::

**Make choices for the following sections:**

#### Survey Programs

:::image type="content" source="../../media/glint/setup/user-roles-survey-programs.png" alt-text="Screenshot of the Survey Programs Access section in Permissions and Access.":::

#### Focus Areas and Conversations

:::image type="content" source="../../media/glint/setup/user-roles-focus-areas-convos.png" alt-text="Screenshot of the Focus Areas and Conversations section in Permissions and Access.":::

#### Reporting

:::image type="content" source="../../media/glint/setup/user-roles-reporting.png" alt-text="Screenshot of the Reporting section in Permissions and Access.":::

#### Data Management

:::image type="content" source="../../media/glint/setup/user-roles-data-management.png" alt-text="Screenshot of the Data Management section in Permissions and Access.":::

#### Resources

:::image type="content" source="../../media/glint/setup/user-roles-resources.png" alt-text="Screenshot of the Resources section in Permissions and Access.":::

#### Access Permissions

:::image type="content" source="../../media/glint/setup/user-roles-access-permissions-section.png" alt-text="Screenshot of Access Permissions window.":::

Select **Save Changes**.

## Report Attributes setup

:::image type="content" source="../../media/glint/setup/user-roles-report-attributes.png" alt-text="Screenshot of Report access in Role Settings.":::

Select **Report Attributes** in the *Role Settings* section.

Attributes are separated into sections:
- Standard
- Manager Hierarchy
- Location Hierarchy
- Department Hierarchy

Select all attributes and hierarchies that this role should be allowed to view for 
- Report filters
- Report sections
- Comment filters

Select **Save Changes**.

> [!TIP]
> Since filtering through results across too many attributes can make identifying survey respondents within reports easier, it's best to give access to only one attribute per manager role. 

## Add or edit employees in a role

Select the **Add/Edit Employees** button. The *Choose a way to add employees* dialog box opens.

Add members to a User Role by choosing one of the following options:

- Attribute Rules - Use rules like location or manager level to populate a User Role. This will dynamically change.
- Import - Use a CSV or XLSX to import employees for this User Role. This will remove attribute rules from this User Role.

### Attribute Rules

:::image type="content" source="../../media/glint/setup/user-roles-attribute-slider.png" alt-text="Screenshot of the **Add Attribute Rules** section in Role Settings.":::

### Import employees in a User Role

:::image type="content" source="../../media/glint/setup/user-roles-import-dialog-box.png" alt-text="Screenshot of the Import Employees to Role dialog box in Role Settings.":::

> [!TIP]
> Switching from Attribute Rules to Import will remove attribute rules. Switching from Import to Attribute Rules will override any employees uploaded.
   
## Remove a user from a User Role category

1. Hover over a user's name.
2. Select the **trash can** symbol.
3. Select **Yes, Remove**.

## Import User Roles in bulk

When you need to assign many individuals to a specific User Role, you can mass assign them by using the bulk import feature.

1. Select the **Configure** symbol.
2. In the **Employees** section, select **User Roles**. Select the User Role you need to update.
3. On the **Role Settings** page, select **Export.** Within the box that displays, make your selections and then again, select **Export**.
4. Open the downloaded .csv file and delete all columns except the column with email addresses.
5. Add or delete email addresses.
     > [!NOTE]
     > This can be a full replacement for the existing file, so you will not need to have an Add or Remove column.
6. Save your file.
7. Return to the **Role Settings** page and select **Import**.
8. Select the checkbox to indicate if you only added users.
9. Drag and drop your file, or browse to select your file, into the area indicated.
10. Select **Import File**.
11. Confirm your import and then select **Confirm Import**.

## View and edit attribute rules for a User Role

This functionality works for roles which already have filters and/or populations applied to them.

1. From the **User Roles** page, select a role to view or edit.
2. On the **Role Settings** page, the number of members of this group will display and the attribute rule applied. (Example: ***Includes: Gender: Female***)
3. To change, select **Edit Attribute Rules**.
4. In the new display window, choose from:
   - I want to include all active employees only, or
   - I want to filter all active employees by the following populations
5. Add new population(s) and filter(s) as desired.
6. Choose whether to include inactive employees or to exclude any employees.
7. Select **Save Changes**.

## Create an attribute rule-based User Role

1. Select  **User Roles**  from the **Configure**  section of your admin dashboard.
2. Choose any role - *excluding preconfigured roles*.
3. Select  **Add/Edit Employees.**
4. In the new display window, choose either:
   - I want to include all active employees only, or
   - I want to filter all active employees by the following populations
5. To add users based on a filtered population, select  **I want to filter all active employees by the following populations**.
6. Select  **+ New Population**.
7. Select  **+ Add Filter**  to select the attribute you want to use to filter your employee list. Your attribute list is unique to your organization based on your Employee Attribute File.
8. Select  **Done**.
9. To exclude someone, search their name and select  **Exclude**.
10. To remove someone from the Excluded list, search their name and select **Remove**.
11. Confirm list for user role and select  **Save Changes**.

## Grant custom access

Custom access is intended for users who need to have the default access overridden or are in a role that is so specific, it needs to be per user rather than at the User Role level. For example, use custom access for HRBPs who serve unique combinations of employee groups in your organization. To grant custom access in bulk to multiple users for survey, Focus Area, and Admin access, see: [Advanced Configuration uploads](advanced-config-uploads.md).

### Set up custom survey access for a user

1. From your Glint dashboard, select **Configuration** and then choose **People**.
2. Go to the User Role with users that need custom access granted.
3. Search for a select a user.
4. On the user's profile, next to the survey name that should have custom data access for this user, select the pencil icon to edit.
     > [!NOTE]
     > The User Role that this person is a member of needs to be granted access to a survey program in the survey's Reporting section for it to appear on their user profile.

     :::image type="content" source="../../media/glint/setup/custom-access-dialog.png" alt-text="Screenshot of dialog that appears to let an admin edit a user's custom access.":::
    
6. Select **+ Population** and then **+ Add Filters**.
7. Select attributes and values that define the segment of employee data that this user should have access to and select **Done**.

     :::image type="content" source="../../media/glint/setup/custom-access-selection.png" alt-text="Screenshot of dialog with custom access attribute values selected.":::
   
9. Select **Save** to apply custom access for this user and survey program.

### Set up custom Admin and Focus Area access for a user

Users can also have their Focus Area and (if they are in a role with admin permissions) their Admin access customized to match their survey access. To grant custom Focus Area and Admin access in bulk for multiple users, see: [Advanced Configuration uploads](advanced-config-uploads.md).

1. From your Glint dashboard, select **Configuration** and then choose **People**.
3. Search for a select a user.
4. On the user's profile, next to **Admin Access** or **Focus Area Access**, select the pencil icon to edit.
5. 7. Select attributes and values that define the segment of employee data that this user should have access to and select **Done**.

     :::image type="content" source="../../media/glint/setup/custom-focus-area-selection.png" alt-text="Screenshot of dialog with custom focus area access attribute values to be selected.":::

9. Select **Save** to apply custom access for this user for **Admin Access** or **Focus Area Access**.
