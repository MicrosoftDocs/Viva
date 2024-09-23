---
title: Update attributes in Viva Glint
description: After initial attribute setup in Microsoft Viva Glint, use this guidance to add new attributes, rename attributes, and to manage derived and optional system attributes.
ms.author: aweixelman
author: AliciaWeixelman
manager: melissabarry
audience: admin
f1.keywords: NOCSH
keywords: edit attribute, edit derived attribute, edit optional system attribute, rename attribute
ms.collection: 
 - m365initiative-viva
 - selfserve
search-appverid: MET150
ms.topic: article
ms.service: viva-glint
ms.localizationpriority: high
ms.date: 09/16/2024
---

# Update attributes in Viva Glint

After initial attribute setup in Microsoft Viva Glint, use this guidance to add new attributes, rename attributes, manage derived and optional system attributes, and to update attribute visibility in the platform. New attributes and their values will apply to future survey results only.

> [!CAUTION]
> The Viva Glint Admin that sets up or changes attributes needs to save changes in the **default language for your organization**. Confirm that the default language (often English) is selected in the Language dropdown menu in Glint. Setting up or editing attributes in a different language resets the expected language for Viva Glint data ingestion and causes upload errors.

## Add new attributes to Viva Glint

To add new attributes to your Viva Glint setup from the admin dashboard:

1. Select the **Configuration** symbol and then under the **Employees** section, choose **People**.
2. Select **Actions** and then **Manage User Attributes**.
3. Select **Update dataset** at the top of the page.
4. Upload your dataset with all existing attributes and the new attribute.

     > [!NOTE]
     > Your uploaded file must contain the Attribute Header Row and at least one row of employee data that aligns with the current format.

5. Select **Continue**.
6. If dates are included in your file, select **There are date fields** and then the appropriate date format from the dropdown menu.

     > [!NOTE]
     > This selection should be your existing date format in your employee data.

7. Preview your data and confirm that you see the new attributes.

    :::image type="content" source="../../media/glint/setup/new-attribute.png" alt-text="Screenshot of the preview screen with a newly added attribute highlighted in green.":::

8. Select **Continue**.
9. The Attributes Setup page shows current required, derived, optional system, and hierarchy attributes. If the newly added field is required, derived, or an optional system attribute, make your selection in the appropriate section. Select **Continue**.
  
     > [!NOTE]
     > Derived Manager Hierarchy and Hierarchy Groups can't be edited after initial setup.
  
10. Review newly added attributes and select **Continue**.
11. Choose to **Save attributes and import employee data** or to **Save attributes and discard employee data**.

     > [!TIP]
     > When adding new attributes, choose the **Save attributes and discard employee data** option to save your setup in preparation for future imports.

12. Select **Save** or **Go Back** to make more edits.

## Edit attribute names

Use the following guidance to rename attributes **before** updating your employee data files so that they continue to import seamlessly.

From the admin dashboard:

1. Select the **Configuration** symbol and then in the **Employees** section, choose **People**.
2. Select **Actions** and then select **Manage User Attributes**.
3. Select the corresponding ellipses to the far right of the attribute in the **Active Attributes** row.
4. Select **Rename Attribute**.
5. Enter the new name in the **Attribute Name** field and select **Rename**.

:::image type="content" source="../../media/glint/setup/rename-attribute.png" alt-text="Screenshot of the Rename Attribute window.":::

> [!CAUTION]
> - Use this method if the underlying data remains the same, but the field name changed in your system. Don't repurpose attribute name labels, as this can create issues in reporting. Instead, create a new attribute. 
> - For example, if Department changes to Team and the values in that column change too, add a new Team attribute and don't rename Department to Team.

## Manage Derived Attributes

Viva Glint calculates attributes based on data sent in your employee attribute file. 

To edit derived fields after your initial setup:

1. Select the **Configuration** symbol and then under the **Employees** section, choose **People**.
2. Select **Actions** and then **Manage User Attributes**.
3. In the **Derived Attributes** section, select **Manage Derived Attributes**.
4. Select the checkbox next to the Derived Attribute that you want to edit or add.
   1. To disable a Derived Attribute: Deselect the checkbox next to the desired field.
   1. To enable a Derived Attribute: Select the checkbox next to the desired field and choose a field from your data in the Calculate From dropdown menu.
   1. To update the field used to create a Derived Attribute: Select the checkbox next to the desired field and choose a new field in the Calculate From dropdown menu. 

:::image type="content" source="../../media/glint/setup/new-derived-attribute.png" alt-text="Screenshot of the Derived Attributes section after selecting the Manage Derived Attributes button.":::

> [!NOTE]
> Manager Hierarchy isn't editable after initial setup.

## Manage Optional System Attributes

Choose how and when Viva Glint communicates with employees by mapping language, time zone, and personal emails to Viva Glint fields.

To edit optional system attributes after your initial setup:

1. Select the **Configuration** symbol and then under the **Employees** section, choose **People**.
2. Select **Actions** and then **Manage User Attributes**.
3. In the **Optional System Attributes** section, select **Manage Optional System Attributes**.
   1. To disable an Optional System Attribute: Deselect the checkbox next to the desired field.
   1. To enable an Optional System Attribute: Select the checkbox next to the desired field and choose a field from your data in the Sync From dropdown menu.
   1. To update the field mapped to an Optional System Attribute: Select the checkbox next to the desired field and choose a new field in the Sync From dropdown menu.

   :::image type="content" source="../../media/glint/setup/new-optional-attribute.png" alt-text="Screenshot of the Optional System Attributes section after selecting the Manage Optional System Attributes button.":::

## Update custom attribute visibility

Use the **Visibility** setting to edit whether a custom attribute appears:

- On a user's profile selected from the People page.
- In exports of users in a survey cycle.
- In survey recipient exports downloaded from the Distribution section of survey programs.

> [!NOTE]
> This setting doesn't affect an attribute's visibility in raw survey response exports.

To edit a custom attribute's visibility:

1. Select the **Configuration** symbol and then in the **Employees** section, choose **People**.
2. Select **Actions** and then **Manage User Attributes**.
3. In the **Active Attributes** section, select the ellipses on the desired custom attribute and choose **Edit Attribute.**
   > [!NOTE]
   > The visibility setting isn't editable for Required or Hierarchy attributes.
5. Switch the **Visibility** toggle to **On** or **Off** to show or hide the attribute.
6. Select **Save.**

   :::image type="content" source="../../media/glint/setup/attribute-visibility.png" alt-text="Screenshot of the Edit Attribute dialog with the Visibility toggle switched to On.":::

To give a User Role access to newly visible custom attributes, select the **Configuration** symbol and then in the **Employees** section, choose **User Roles**. Select a role and in **Report Attributes**, make selections for the newly visible attribute. [Learn more about User Role setup](set-up-user-roles.md).

