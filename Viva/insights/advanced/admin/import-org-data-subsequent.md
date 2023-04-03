---
ROBOTS: NOINDEX, NOFOLLOW
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

In this article, we discuss refreshing data your provided when you set up your connection to Viva Insights. First, we’ll describe the two types of imports you can perform. Then, we’ll give you the steps to perform those imports.

>[!Important]
>Only use the following steps if this is not the first time you’re importing organizational data. If this is your first import, refer to [Import organizational data (first import)](import-org-data-first.md) to set up a connection and import data to Viva Insights.

## Types of subsequent imports

When you import data to Viva Insights, you’ll either perform a full or an incremental refresh. If you want to delete fields, you can use a full refresh to do so. We describe both import types in the following sections.

### Full refresh

When you perform a full refresh, you’re replacing all your organization’s data in Viva Insights. During a full refresh, you send every value for every field to Viva Insights, including all previous values—that is, you’re replacing all the data that you've already imported to Viva Insights, except any fields you want to delete. We talk about deleting data in the next section.
 
When you perform a full refresh, make sure to provide data for all licensed and unlicensed employees (meaning those who have a Viva Insights subscription and those who don’t).

#### Fields to include for your full refresh 

If you're performing a full refresh, provide new values for every existing field, for every employee, including all previous historical values for those fields. In other words, your import needs to contain new and previous values for **PersonId**, **ManagerId**, **Organization**, and **EffectiveDate**, and any reserved optional attributes your existing data contains. If you’re adding any reserved optional fields, provide values for those too.

#### Deleting fields with full refreshes

You can use a full refresh to delete fields. To do so, export your data as a .csv that contains all fields except the fields you want to delete. Because a full refresh replaces existing data, you’ll end up with every field except the ones you left out during the import.

##### Fields to include in your full refresh for deletion

If you're deleting fields through a full refresh, include every existing field, for every employee—including all previous values for those fields—except the fields you want to delete. At a minimum, your import needs to contain new and previous values for **PersonId**, **ManagerId**, **Organization**, and **EffectiveDate**, and any reserved optional attributes your existing data contains.
 
### Incremental refresh

Perform an incremental refresh when you only want to add some new information to organizational data you’ve already uploaded to Viva Insights. Here’s what you can do with an incremental refresh:

* Add new employees
* Add new attributes for existing employees
* Add new attributes for new employees
* Edit existing employees’ attributes
 
Let’s use a couple of examples:

Say you want to add five new hires to your organizational data. During the import, you’d only include those five rows that contain new data, plus two required attributes: PersonId and EffectiveDate. After the import finishes, the only change you’d notice is five new rows and their values. 

Or maybe you want to add an optional reserved attribute that wasn’t in your data before—let’s say **HireDate**—for all existing employees. When you go to import your data, you’d only include the **HireDate** column, with values for each employee, in your .csv file. After the import finishes, you’d find the same data that was there before, with the exception of a new column for each employee, **HireDate**. 

#### Fields to include for your incremental refresh 

If you're performing an incremental refresh for *existing* employees’ data, only include the fields you want to add to or edit within your existing data in Viva Insights. If you’re adding data for *new* employees, include **PersonId**, **ManagerId**, **Organization**, and **EffectiveDate**, in addition to your new fields. 

## Data refresh process

For every full and incremental refresh, follow these steps:

1. Export organizational data from your source system as a .csv.
1. Download the [zip folder](https://go.microsoft.com/fwlink/?linkid=2230444) we’ve prepared for you on GitHub.
1.	In the downloaded zip file, open **data.csv**.
1.	Enter your data in **data.csv** and format according to our guidelines in [Prepare organizational data](prepare-org-data.md#structure-the-organizational-data).
1.	Fill out the metadata.json file. For each Viva Insights field, name the corresponding column header in your source data. Mapping fields makes sure Viva Insights uses your data in the right way. 

>[!Note]
>Viva Insights doesn’t support custom fields for data import, so make sure you’re using required and reserved optional fields only. Our [Prepare organizational data](prepare-org-data.md#attribute-reference) article includes an attribute reference. Refer also to the [Automated import template](https://go.microsoft.com/fwlink/?linkid=2230246).