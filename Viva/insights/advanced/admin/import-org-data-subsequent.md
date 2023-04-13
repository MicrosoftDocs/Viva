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

In this article, we discuss two kind of imports: full and incremental. These imports refresh the data you provided when you set up your connection to Viva Insights. 

>[!Important]
>Only use the following steps if this is not the first time you’re importing organizational data. If this is your first import, refer to [Import organizational data (first import)](import-org-data-first.md) to set up a connection, build an export app, and import data to Viva Insights.

## About subsequent imports

When you import data to Viva Insights, you’ll either perform a full or an incremental refresh. If you want to delete fields, you can use a full refresh to do so. 

The custom export app you created in [Import organizational data (first import)](import-org-data-first.md#prepare-export-and-import-organizational-data), along with the DescriptiveDataUploadApp we created on GitHub, facilitates the refreshes we talk about below. As a quick recap, when DescriptiveDataUploadApp runs, it pulls data from the zipped folder you downloaded from GitHub. This zipped folder contains the following files:

* data.csv, which contains the fields you want to import.
* metadata.json, which maps your source fields to Viva Insights fields. You'll also use metadata.json to tell Viva Insights whether your refresh is full or incremental, as we explain in the next section.

### How to indicate a full or incremental refresh

1. In metadata.json, go to line 3.
1. Update the `“IsBootstrap”:` property to one of the following:
    *  For a full refresh, use `“IsBootstrap” : “true”`.
    * For an incremental refresh, use `“IsBootstrap” : “false”`.

When DescriptiveDataUploadApp runs, Viva Insights will start to process your data either as a full or incremental refresh, depending on what you specified here in metadata.json.

>[!Important]
>Make sure you delete any fields from metadata.json that you're not including in your data.csv file. If you have more fields in your metadata.json file than in your data.csv file—or vice versa—processing for your import will fail.
>
>Refer to [Import organizational data (first import)](import-org-data-first.md#metadatajson) to learn more about metadata.json and how to use it to map fields.

### Refresh types

#### Full

When you perform a full refresh, you’re replacing all your organization’s data in Viva Insights—that is, you overwrite what you’ve already imported. When you perform a full refresh, make sure to provide data for all licensed and unlicensed employees (meaning those who have a Viva Insights subscription and those who don’t). We describe what fields to provide [later](#fields-to-include-in-datacsv-for-full-and-incremental-refreshes) in this article.

You can use a full refresh to delete fields, because fields you leave out won’t show up in your data. We talk about deleting data in the next section.


##### Deleting fields with full refreshes

You can use a full refresh to delete fields. To do so, export your data as a .csv that contains all fields except the fields you want to delete. Because a full refresh replaces existing data, you’ll end up with every field except the ones you left out during the import.

#### Incremental

Perform an incremental refresh when you only want to add some new information to organizational data you’ve already uploaded to Viva Insights. Here’s what you can do with an incremental refresh:

* Add new employees
* Add new attributes for existing employees
* Add new attributes for new employees
* Edit existing employees’ attributes
 
Here are a couple of examples of when you might perform an incremental refresh:

##### Adding new hires

Say you want to add five new hires to your organizational data. During the import, you’d include:

* Five rows that contain new employee data.
* Required attributes: **PersonId**, **ManagerId**, **Organization**, and **EffectiveDate**.
* All reserved optional fields (for example, **HireDate**) that you’ve already imported to Viva Insights.

After the import finishes, the only change you’d notice is five new rows and their values.


##### Adding a new attribute

Maybe you want to add an optional reserved attribute that wasn’t in your data before—let’s say **Location**—for all existing employees. When you go to import your data, you’d only include the **Location**, **PersonId**, and **EffectiveDate**, with current and historical values for each employee, in your .csv file. After the import finishes, you’d find the same data that was there before, with the exception of a new column for each employee, **Location**.

## Fields to include in data.csv for full and incremental refreshes

For the refresh types listed below, include the following fields in your data.csv file. Make sure you:

* Format these fields according to our guidelines in [Prepare organizational data](prepare-org-data.md#structure-the-organizational-data).
* Remove any fields you're not including from your metadata.json file.
* Keep both the data.csv and metadata.json files in the zipped folder you downloaded from GitHub. When you run the DescriptiveDataUploadApp, you'll provide the zipped folder path. Viva Insights will then pull your data from this location.

For this kind of refresh | Include these fields in data.csv| With these values|For these employees
|------------|-----------------|---------|---|
|**Full** |**PersonId**	|<ul> <li>Current <li> All historical (refer to the note below)  |All
||**ManagerId** |<ul> <li>Current <li> All historical |All
|| **Organization**| <ul> <li>Current <li> All historical |All
|| **EffectiveDate**|<ul> <li>Current <li> All historical |All
|| All reserved optional fields (for example, **HireDate**) that you’ve already imported to Viva Insights | <ul> <li>Current <li> All historical |All
|**Full** (for deleting reserved optional fields) | **PersonId** | <ul> <li>Current <li> All historical |All
|| **ManagerId** | <ul> <li>Current <li> All historical |All
|| **Organization** | <ul> <li>Current <li> All historical |All
|| **EffectiveDate** | <ul> <li>Current <li> All historical |All
|| All reserved optional fields (for example, **HireDate**) you’ve already imported to Viva Insights, except the reserved optional fields you want to delete| <ul> <li>Current (except for to-be-deleted fields)<li> All historical (except for to-be-deleted fields)|All
|**Incremental** (for adding new fields or editing existing fields, but *not* adding new employees)| **PersonId** |<ul><li>Current <li> All since the last upload (refer to note below) |All
|| **EffectiveDate** |<ul><li>Current <li> All since the last upload | All
|| Any reserved optional fields (for example, **HireDate**) you want to add	| <ul><li>Current <li> All since the last upload | All
|**Incremental** (for adding *new* employees) | **PersonId** | <ul><li>Current <li> All historical  | New employees only
|| **ManagerId** | <ul><li>Current <li> All historical  | New employees only
||**Organization** | <ul><li>Current <li> All historical  | New employees only
|| **EffectiveDate** | <ul><li>Current <li> All historical  | New employees only
|| All reserved optional fields (for example, **HireDate**) that you’ve already imported to Viva Insights | <ul><li>Current <li> All historical  | New employees only

>[!Note]
>
>* "All historical": Values for previous time periods. For example, if you include monthly data, then you'd include values for every month leading up to this one. When you’re first starting to use Viva Insights, 13 months’ worth of data is recommended. After that, it’s recommended to update data regularly so it builds into 27 months’ worth of data.
>* "All values since the last upload": Values for the period between uploads. For example, if the last upload was in March and now it’s July, include values for April, May, and June.