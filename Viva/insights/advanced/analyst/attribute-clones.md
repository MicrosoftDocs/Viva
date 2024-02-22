---
ROBOTS: NOINDEX,NOFOLLOW
ms.date: 02/22/2024
title: Introducing attribute clones
description: Learn how to create and manage attribute clones
author: kateylundquist
ms.author: v-klundquist
ms.topic: article
ms.localizationpriority: medium 
ms.collection: viva-insights-advanced 
ms.service: viva 
ms.subservice: viva-insights 
search.appverid: 
- MET150 
manager: helayne
audience: Admin
---

# Create and manage attribute clones

>[!IMPORTANT]
> This feature is for private preview customers only. Features in preview might not be complete and could undergo changes before becoming available in the broader public release.

Attribute clones allow you to create copies of your admin-uploaded attributes and modify them via rules that conditionally update the attribute value data. This feature enables you to dynamically create new ways of grouping employees, resulting in new ways to analyze your data insights. 

### Example scenarios
- Rename an attribute value.
- Combine multiple attribute values into a singular value.
- Update the value of an attribute based on the value of some other attribute.
- And more.

### Create a new attribute clone
Here are some ways to create a new attribute clone:

- Create a new attribute clone by navigating to the Organizational Data tab in the left-hand navigation panel and then selecting Data Quality. Here you can see all the attributes that you have available to you. You now notice that there is a vertical ellipsis next to your existing attributes. Select the ellipses and then select the option to Clone Attribute.

    >[!Note]
    >The Organizational Data tab is not available if you have access to a partition and not the Global partition. In this case, you must access the entry point via the query interface, explained in the next step.

- Create a new Attribute Clone when creating a Person or Meeting query. In the final stage where you add attributes to your query, you can open up the fly-out panel. There, you'll also see the ellipses. From that location, you can clone an attribute.
- Create a clone of any attribute that your admin uploaded. Since the clone is what is modified, there are never any modifications made to the admin-uploaded attributes. Those attributes continue to remain unchangeable by the analyst.
- You're not able to create a clone of a clone. 
- Define a new name for this cloned attribute. The name must contain only ASCII alphanumeric characters. It can't contain any spaces or other special characters. It must be less than 30 characters. It also must be unique. After you create a clone, the name can't be changed.
- When you create a clone, all of the attribute value data is copied over from the original column. Only values that you specifically target to change will change. Everything else remains as default.
- In your clone, you can keep the datatype of the original column, or you can change the datatype to a string.
    - Keeping the same datatype is simple if it is a string or integer. You just input a string or integer, respectively, into the New Value. Maintaining a Date field can be a bit challenging since the format you need to enter isn’t clear yet. Use the date format: ‘MM-DD-YYYY’
    - Being able to change the datatype to a string can support scenarios where you want to group a set of HireDates into buckets like “New Hires” and “Tenured Hires,” for example. When you enter a New Value, if you don’t input the datatype of the original column, you'll see a warning saying: if you continue the datatype changes to string. You can choose to ignore this warning and save the column with a string datatype.
    - You're not able to change the datatype to anything other than string today.

### Use attribute clones
Once your clone is created, you can immediately use it like any other attribute. When you add it to a query and run it, the results show the new attribute value data. When a query is run, it reflects the clone definition as it is defined at query execution time.

Currently, you can add cloned attributes to both your person and meeting queries. Other query types like Cross-Collaboration and External Collaboration queries are not supported yet.

After creation, you're welcome to go back and edit the clone definition. Any new query runs reflect that new definition, including any recurring queries where that clone is being used.

You can view the Data Quality of the Clone within the Organizational Data tab. If the Clone only takes input from a single column, it inherits the original column’s data quality information. If it takes input from multiple columns, the data quality information won't be available.

Only the creator of the clone can edit the definition of the clone or delete the clone. Other analysts can use the clone in their queries and view the definition of the clone. The clone is only visible and usable in the partition in which it was created. Clones are not transferrable to other partitions today.

### Delete attribute clones
When you're ready to delete the clone, you can delete it from the Data Quality section under the Organizational Data tab. Only the creator of the clone can delete.

>[!Note]
>If you use the workbench via a partition, the Organizational Data tab may not be available to you yet, and you won’t be able to delete. This tab should become available to you within the next few weeks.

Before you delete, ensure that the clone isn’t being used in any recurring queries. If you delete a clone that is being used in active recurring queries, that query deactivates. Once you delete, the clone is removed and there's no opportunity to recover.

### Known bugs
There are no known bugs today.
