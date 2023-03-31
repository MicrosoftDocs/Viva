---
title: Import organizational data (subsequent import)
description: Learn how to refresh your data in the Viva Insights advanced insights app through a connection
author: lilyolason
ms.author: v-lilyolason
ms.topic: article
ms.localizationpriority: medium
ms.collection: viva-insights-advanced
ms.service: viva 
ms.subservice: viva-insights
manager: anirudhbajaj
audience: Admin
---

# Import organizational data (subsequent import)

In this article, we discuss refreshing data that's already been imported to Viva Insights. First, we’ll describe the two types of imports you can perform. Then, we’ll give you the steps to perform those imports.

>[!Important]
>Only use the following steps if this is not the first time you’re importing organizational data. If this is your first import, refer to [Import organizational data (first import)](import-org-data-first.md) to set up a connection and import data to Viva Insights.

## Types of subsequent imports

When you import data to Viva Insights, you’ll either perform a full or an incremental refresh. If you want to delete fields, you can use a full refresh to do so. We describe both import types in the following sections.

### Full refresh

When you perform a full refresh, you’re replacing all your organization’s data in Viva Insights. During a full refresh, you send every value for every field to Viva Insights—that is, you’re removing and replacing all the data that currently lives in Viva Insights, except any fields you want to delete. We talk about deleting data in the next section.
 
When you perform a full refresh, make sure to provide data for all licensed and unlicensed employees (meaning those who have a Viva Insights subscription and those who don’t). 

#### Deleting fields with full refreshes

You can use a full refresh to delete fields. To do so, export your data as a .csv that contains all fields except the fields you want to delete. Because a full refresh replaces existing data, you’ll end up with every field except the ones you left out during the import.
 
### Incremental refresh

Perform an incremental refresh when you only want to add some new information to organizational data you’ve already uploaded to Viva Insights. Here’s what you can do with an incremental refresh:

* Add new employees
* Add new attributes for existing employees
* Add new attributes for new employees
* Edit existing employees’ attributes
 
Let’s use a couple of examples:

Say you want to add five new hires to your organizational data. During the import, you’d only include those five rows that contain new data. After the import finishes, the only change you’d notice is five new rows and their values.

Or maybe you want to add a new attribute, **Building**, for all existing employees. When you go to import your data, you’d only include the **Building** column, with values for each employee, in your .csv file. After the import finishes, you’d find the same data that was there before, with the exception of a new column for each employee, **Building**.

## Data refresh process

For every full and incremental refresh, follow these steps:

1.	Export organizational data from your source system as a .csv.
2.	Download the zip folder we’ve prepared for you here: LINK PENDING
3.	Open **OrganizationalDataFile.xlsx** within the zip folder and save the Template tab as a .csv.
4.	Enter your data in the **Template** tab and format your data according to our guidelines in [Prepare organizational data](prepare-org-data.md). 

    If you’re:

    * Performing a full refresh, provide values for every employee.
    * Performing an incremental refresh, only include the fields you want to add to your existing data in Viva Insights.
    * Deleting fields through a full refresh, include every field except the ones you want to delete.

5.	Fill out the metadata.json file. For each Viva Insights field, name the corresponding column header in your source data. Mapping fields makes sure Viva Insights uses your data in the right way.
