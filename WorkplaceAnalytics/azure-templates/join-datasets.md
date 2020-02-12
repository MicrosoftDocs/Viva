---
ROBOTS: NOINDEX,NOFOLLOW
title: Join Datasets Azure Template for Workplace Analytics 
description: Learn about the Join Datasets Azure Template for Workplace Analytics and how to use it for advanced data analysis
author: madehmer
ms.author: madehmer
ms.topic: article
localization_priority: normal 
ms.prod: wpa
ms.collection: M365-analytics
manager: scott.ruble
audience: Admin
---
# Join Datasets Azure Template for Workplace Analytics

_These templates are only available as part of a Microsoft service engagement._

Workplace Analytics Azure Templates includes the Join Datasets Template that enables you to securely join, group, and aggregate data imported from Workplace Analytics with other third-party data sources, such as personnel data or HR data that you analysis.

## How it works

 -> some cool graphic explaining the flow of what file has which ID

* [Mapping file](#to-add-a-mapping-file) - The template maintains privacy rules by using a mapping file that is only accessible outside of Workplace Analytics by the HR manager. The HR manager maps an unique identifier, such as a UPN or personnel number, for each employee in the mapping file.
* The HR manager must then add this new unique identifier data column for employee records in the HR data upload file that's uploaded into Workplace Analytics. For more about HR uploads in Workplace Analytics, see [Prepare organizational data](../setup/prepare-organizational-data.md).
* [Workplace Analytics query](#to-add-a-query-file) and [Third party data](#to-add-third-party-data) - The analyst can then select the related Workplace Analytics (WPA) query data to add as a .csv file and the third-party data with the employee IDs that match up to the unique employee identifiers that the HR manager specified in the mapping file and in the organizational (HR) data uploaded into Workplace Analytics.
* The template uses the mapping file to combine (join) the data from the two data sources into a join dataset that connects the data records by using join key logic that links the employee HR ID to the unique employee ID uploaded into Workplace Analytics.
* The join dataset then replaces the join key (that might possibly identify individual employees) with a new Sequence ID (SEQN column) that connects the data records, but keeps the data de-identified for analysis purposes.

After the template creates the join dataset, you can download it as a .csv file for analysis.

## To add a mapping file

1. In Workplace Analytics Azure Templates, select **Join Datasets** > **Mapping Data**.
2. Select **Add New Mapping File** at top right of the table.
3. For **Upload Mapping File**, enter a mapping file name, select the .csv file to upload, and then select **Upload Mapping File**.
4. After the upload succeeds, it'll will be available in the Mapping Data list with the following options:

   * When the **Status** is a green check mark, the data was successfully uploaded. A red X means it failed.
   * Select a table column heading, such as Name or Submitted, to sort by it.
   * Select the **Share** icon next to the file name to select users who you want to share mapping file permissions with.
   * Select the **Update** icon to refresh the data in the mapping file.
   * Select the **Delete** (trashcan) icon to delete the file from the list.

## To upload new HR data to Workplace Analytics

After the HR manager decides on and adds a unique employee ID to the mapping file, that same unique ID column must be added to the HR data that's uploaded into Workplace Analytics. For instructions on how to append new data and re-upload HR data into Workplace Analytics, see [Subsequent uploads](../setup/upload-organizational-data.md#file-upload) and select to **Append** in **Step 9**.

## To add a query file

1. In Workplace Analytics Azure Templates, select **Join Datasets** > **WPA data**.
2. Select **Add New WPA file** at top right of the table.
3. For **Upload WPA File**, select the .csv query file to upload, the time period you want data for, whether you want to allow raw Workplace Analytics metrics in the aggregations, and then select **Upload WPA File**.
4. When prompted to define columns, select which columns in the query data you want to use as a metric for aggregations and as an attribute for groupings, and then select **Submit**.
5. After the upload succeeds, it'll be available in the Workplace Analytics Data list with the following options:

   * When the **Status** is a green check mark, the data was successfully uploaded. A red X means it failed.
   * Select a table column heading, such as Name or Submitted, to sort by it.
   * Select the **Share** icon next to the name to share access to this data with other users.
   * Select the **Delete Analysis** (trashcan) icon to delete the query from the list.

## To add and view joined datasets

1. In Workplace Analytics Azure Templates, select **Join Datasets** > **Joined Datasets**.
2. Select **Add New Join** at top right of the table.
3. For **Data Join Settings**, enter a name for the joined dataset, select the external dataset that matches up with the mapping file, the .csv query file, and the related mapping file.
4. In **Define Join Fields**, select the Workplace Analytics Person ID key and the third-party external data key (such as Personnel ID).
5. In **Time and N Size**, select the time period you want data for and specify the minimum group size for groupings and aggregations, and then select **Submit**. For more information about minimum group sizes, see [Minimum group size](../use/settings.md#minimum-group-size).
6. After the upload succeeds, it'll be available in the **Joined Datasets** list with the following options:

   * When the **Status** is a green check mark, the data was successfully uploaded. A red X means it failed.
   * Select a table column heading, such as Name or Submitted, to sort by it.

## To add and view analysis

1. 

## Related topics

* [Workplace Analytics Azure Templates overview](./overview.md)
* [Deploy and configure Workplace Analytics Azure Templates](./deploy-configure.md)
