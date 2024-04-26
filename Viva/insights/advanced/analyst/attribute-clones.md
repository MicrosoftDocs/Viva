---
ms.date: 05/01/2024
title: Create and manage attribute clones
description: Educates analysts on how to edit and customize attributes uploaded by admins to create better tailored analyses.
author: zachminers
ms.author: v-zachminers
ms.topic: article
ms.localizationpriority: medium 
ms.collection: viva-insights-advanced 
ms.service: viva-insights
search.appverid: 
- MET150 
manager: helayne
audience: Admin
---

# Create and manage attribute clones

Attribute clones allow analysts to duplicate their admin-uploaded attributes and customize the clone by modifying specific attribute values. This feature lets you update how you define your employee groups, ensuring your attribute data reflects the state of your business and complements your specific analyses.

### Example scenarios

- Rename an attribute value
- Combine multiple attribute values into a singular value
- Update the value of an attribute based on the value of some other attribute

### Create a new attribute clone

You can create a clone of any attribute that your admin has uploaded, except for "ManagerId." Since you’re modifying only the clone, there are never any modifications made to the original admin-uploaded attributes. 

When you create a clone, all the attribute value data is copied from the original column. Only values that you specifically target to change are changed. Everything else remains the same.

There are two locations where you can create a new attribute clone:

* Navigate to the **Data quality** tab in the left-hand navigation panel. Here you can see all the attributes available to you. There's a vertical ellipsis next to your existing attributes. Select the ellipses and then select the option to **Clone attribute**.

* Or, create a new attribute clone when creating a [Person query](./person-query.md) or [Meeting query](./meeting-query.md). In the final stage where you add attributes to your query, open the fly-out panel. There, you'll also see the ellipses. From that location, you can clone an attribute.

Once you have created a clone of an existing attribute, there are a few steps.

1. Enter a new name for this cloned attribute. The name must only contain alphanumeric characters, underscores, no spaces, no special characters, have fewer than 30 characters, and be unique. After you create a clone, the name can’t be changed.

2. In your clone, you can keep the datatype of the original column, or you can change the datatype to a string if it’s nonstring.  Changing the datatype to a string can support scenarios where you want to categorize, for example, grouping a set of HireDates into buckets like "New Hires" and "Tenured Hires."

    * To change from nonstring to string, select the dropdown and select **string**. Now, you can enter string values into your new attribute clone.

3. Define Rules to designate what you want to change. Select current values that exist in the original column and change them to something else by defining a New value. You can define multiple conditions per Rule and define multiple Rules per attribute clone.

4. Select **Save and close**.

### Use Attribute clones

Once you create your clone, you can immediately use it like any other attribute. The next time you create a query, you can add it by opening the attribute fly-out and finding it towards the bottom of the list, after the admin-uploaded attributes. When the query is run, the results show the new attribute value data. The data reflects the clone definition as it’s defined at query execution time.

You can add cloned attributes to your person and meeting queries, but other query types aren’t yet supported. After creation, you can go back and edit the clone definition. Any new query runs will reflect that new definition, including any recurring queries where that clone is used.

Only the creator of the clone can edit the definition of the clone or delete the clone. Other analysts can use the clone in their queries and view the definition of the clone. The clone is only visible and usable in the partition in which it was created. Clones aren't transferrable to other partitions.

### Delete attribute clones

When you're ready to delete the clone, you can delete it from the **Data quality** tab or from the attribute fly-out panel that you can access while creating a Person or Meeting query. Only the creator of the clone can delete it.

Before you delete, ensure the clone isn’t being used in any recurring queries. If you delete a clone that’s used in active recurring queries, that query deactivates. Once you delete, the clone is removed and you can't recover it.