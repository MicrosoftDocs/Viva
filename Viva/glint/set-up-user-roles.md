---
title: Set up User Roles in Viva Glint
description: Admins can customize manager roles to provide specific permissions for viewing reports and comments.
ms.author: SarahBerg
author: SarahAnneBerg
manager: pamgreen
audience: admin
f1.keywords: NOCSH
keywords: viva glint, user roles, glint user attribute, glint attributes, glint permissions,
ms.collection: 
 - M365initiative-viva
 - selfserve
search-appverid: MET150
ms.topic: article
ms.service: viva
localization_priority: high pri
ms.date: 04/14/2023
---

# Set up User Roles

You can assign multiple roles with specific permissions - access to different segments of data and filter - within **User Roles** from the admin configuration dashboard. The User Roles and Access Template include prepopulated example roles and detailed instructions for two areas of setup. Use it to help plan your Glint programs.

You can use the template to indicate which attributes User Roles are allowed to view, according to three filter distinctions:

- Report filters: Attributes this role can view while searching results.
- Report sections: Which section a user can add to reports.
- Comment filters: Attributes this role must have to view the Comments report.

> [!TIP]
> To protect confidentiality, give managers access to only one filterable attribute. Assigning more than one filterable attribute could increase the chance that a manager may be able to deduce the origin of individual responses.

>[!NOTE]
> Not all User Roles and pre-populated attributes and permissions in the template may apply to your organization. Consult your Employee Attribute File for attributes specific to your organization and make changes, as necessary.

[Download the template to use as a planning tool to define permissions for your User Roles.](https://acrobat.adobe.com/link/review?uri=urn:aaid:scds:US:1e304311-018e-330d-ab5a-79bbe2c4631c)

## Create User Roles

Program admins can specify the employee population and report filters their leaders can view on their dashboard based on manager, HRBP, and executive roles. Defining roles is important for data cuts, access permissions, and program integrity.

### Procedure to create User Roles

1. Select the **Configure** symbol.
2. In the **Employees** section, select **User Roles**.
3. You'll see predefined user roles initially:
   1. Active Employees: Not intended to have data access
   2. Company Admin: Employees who are granted **ALL** permission; can't be edited
   3. Inactive employees: Not intended to have data access
   4. Manager: Commonly used and prepopulated; permissions and attributes can be edited
4. To add roles, select **+ New Role**.
5. Enter a User Role name by selecting the pencil symbol next to the title box.

## Set up the Role Settings page

You can do the following from the Role Settings page:

- [Permissions](#permissions-setup)
- [Report Attributes](#report-attributes)
- [Add or remove users](#add-user-to-a-role)

### Permissions setup

1. Select **Permissions** in the **Role Settings** section.
2. Choose all appropriate permissions and access capabilities you want for the new User Role.
3. Select **Save Changes**.

### Report Attributes

1. Select **Report Attributes** in the **Role Settings** section.
2. Select all attributes and hierarchies that this role should be allowed to view for report filters, report sections, and comment filters.
3. Select **Save Changes**.

> [!TIP]
> Since filtering through results across too many attributes can make identifying survey respondents within reports easier, we recommend giving access to only one attribute per manager role. For example, *Managers with Country Access* or *Managers with Comments*.

### Add user to a role

1. Select **+ Search for an employee to add**.
2. Select their name.
3. The new user will now appear in the **All Members** section.

### Remove a user from a User Role category

1. Hover over a user's name.
2. Select the **trash can** symbol.
3. Select **Yes, Remove**.

## Import User Roles in bulk

When you need to assign many individuals to a specific User Role, you can mass assign them by using the bulk import feature.

### Procedure to import User Roles in bulk

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

This functionality works for roles, which already have filters and/or populations applied to them.

1. From the **User Roles** page, select a role to view or edit.
2. On the **Role Settings** page, the number of members of this group will display and the attribute rule applied. (Example:***Includes: Gender: Female***)
3. To change, select **Edit Attribute Rules**.
4. In the new display window, choose from:
   - I want to include all active employees only
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

## Grant Custom access

Custom access is intended for users who need to have the default access overridden or are in a role that is so specific, it needs to be per user.

### Create Custom Team Access for Programs

1. From your Glint dashboard, select **Configure** and then **People** and then **Select User.**
2. Review User Roles for accuracy.
3. Next to the survey name, select **Edit**.
4. Customize the survey access from the dialog box that opens and select **Save**. Customized data access for that program now displays on the user profile.