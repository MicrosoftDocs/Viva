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

*Applies to: private preview customers*

In this article, we discuss refreshing the data you provided when you set up your connection to Viva Insights. 

>[!Important]
>Only use the following steps if this is not the first time you’re importing organizational data. If this is your first import, refer to [Import organizational data (first import)](import-org-data-first.md) to set up a connection and import data to Viva Insights.
>
>To export and import data at a set frequency, you’ll need to create a *different* app than the **DescriptiveDataUploadApp** console app described in [Import organizational data (first import)](import-org-data-first.md) (for example, a PowerShell script). This app needs to do two things:
>
>1. Export your source data at the frequency you set.
>1. Run the **DescriptiveDataUploadApp** console app described in [Import organizational data (first import)](import-org-data-first.md).
>
>Viva Insights doesn’t supply this source-side, data-export app. However, we describe the steps it needs to take in Data refresh process.

## About subsequent imports

When you import data to Viva Insights, you’ll either perform a full or an incremental refresh. If you want to delete fields, you can use a full refresh to do so. 

### Full refresh

When you perform a full refresh, you’re replacing all your organization’s data in Viva Insights. During a full refresh, you send every value for every field to Viva Insights, including all previous values—that is, you’re replacing all the data you’ve already imported to Viva Insights, except any fields you want to delete. We talk about deleting data in the next section.
 
When you perform a full refresh, make sure to provide data for all licensed and unlicensed employees (meaning those who have a Viva Insights subscription and those who don’t). 

#### Deleting fields with full refreshes

You can use a full refresh to delete fields. To do so, export your data as a .csv that contains all fields except the fields you want to delete. Because a full refresh replaces existing data, you’ll end up with every field except the ones you left out during the import.
 
### Incremental refresh

Perform an incremental refresh when you only want to add some new information to organizational data you’ve already uploaded to Viva Insights. Here’s what you can do with an incremental refresh:

* Add new employees
* Add new attributes for existing employees
* Add new attributes for new employees
* Edit existing employees’ attributes
 
Here are a couple of examples of when you might perform an incremental refresh:

#### Adding new hires

Say you want to add five new hires to your organizational data. During the import, you’d only include those five rows that contain new data, plus two required attributes: PersonId and EffectiveDate. After the import finishes, the only change you’d notice is five new rows and their values.

#### Adding a new attribute

Maybe you want to add an optional reserved attribute that wasn’t in your data before—let’s say Location—for all existing employees. When you go to import your data, you’d only include the Location, PersonId, and EffectiveDate, with current and historical values for each employee, in your .csv file. After the import finishes, you’d find the same data that was there before, with the exception of a new column for each employee, HireDate.

### Fields to include for full and incremental refreshes

Refresh type | Required field | Required value
|------------|-----------------|---------|
|Full |PersonId	|Current and all historical for all employees
||ManagerId |Current and all historical for all employees
|| Organization| Current and all historical for all employees
|| EffectiveDate|Current and all historical for all employees
|| All reserved optional fields (for example, HireDate) that you’ve already imported to Viva Insights | Current and all historical for all employees
|Full (for deleting reserved optional fields) | PersonId | Current and all historical for all employees
|| ManagerId | Current and all historical for all employees
|| Organization | Current and all historical for all employees
|| EffectiveDate | Current and all historical for all employees
|| All reserved optional fields (for example, HireDate) you’ve already imported to Viva Insights, except the reserved optional fields you want to delete| Current and all historical for all employees (except for to-be-deleted fields)
|Incremental (for adding new fields or editing existing fields, but not adding new employees)| PersonId |	Current and last uploaded value
|| Organization | Current and last uploaded value
|| EffectiveDate | Current and last uploaded value
|| Any reserved optional fields (for example, HireDate) you want to add	| Current and last uploaded value
|Incremental refresh (for adding new employees) | PersonId | Current and all historical for new employees only
|| ManagerId | Current and all historical for new employees only
||Organization | Current and all historical for new employees only
|| EffectiveDate | Current and all historical for new employees only
|| All reserved optional fields (for example, HireDate) that you’ve already imported to Viva Insights | Current and all historical for new employees only

## Regular import app

As mentioned earlier, to export data to Viva Insights at a set frequency, you’ll need to create a different app from the one we described in Import organizational data (first import) [add link]. The app can take any form—for example, a PowerShell script—but this is what it needs to do:

1. Export organizational data from your source system as a zip folder based on the zip folder we provide on GitHub. The zip folder needs to contain the following two files:
    1. data.csv, which contains all fields you want to import and is formatted according to our guidelines in Prepare organizational data.
    1. A metadata.json file, which should indicate the following:
        1. DatasetType: HR
        1. IsBootstrap: `True` or `False`. `True` indicates a full refresh and `False` indicates an incremental refresh.
        1. Mapping: include a source-data column name for each Viva Insights field. `“name”` corresponds to the Viva Insights field name. Change the text in the above line if your source system uses a different name for that field.
1. Run the **DescriptiveDataUploadApp** as described in [Import organizational data (first import)](import-org-data-first.md).
