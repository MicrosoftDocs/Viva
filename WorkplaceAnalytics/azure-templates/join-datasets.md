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

Workplace Analytics Azure Templates includes the Join Datasets Template that enables you to securely join, group, and aggregate data exported from Workplace Analytics with other third-party data sources, such as sensitive, personnel data or HR data that you want to combine and analyze. This template enforces the same data privacy settings that you set in Workplace Analytics, such as minimum group size, data exclusions, and other [privacy settings](../use/settings.md#privacy-settings).

For example, your company wants you to evaluate employee job satisfaction by analyzing poll data from the HR system and employee collaboration and meeting data from Workplace Analytics.

Use this template to analyze a joined dataset as follows.

1. **[Create a mapping file](#create-a-mapping-file), and then [add and share it](#add-a-mapping-file)** - To maintain privacy rules, the owner of your HR system data, such as the HR manager, needs to own and maintain the mapping file, which must only be accessible outside of Workplace Analytics by that owner, who needs to:

   * Create a new .csv mapping file and add an employee ID column that uniquely identifies employees in both the third-party data and the HR data uploaded into Workplace Analytics, such as an email alias or an employee ID.
   * Map a new **Key_ID** to each employee in the mapping file.
   * Add the mapping file in the template and share it with users who need to use it to add and analyze joined datasets and analysis. The users you share with can only use it for joins in the template and cannot read or edit it.
   * The template then adds a sequence (**SEQN**) column to the mapping file that it uses later as a join key to connect the same employee records from the two different data sources into the joined dataset with a de-identified sequence number assigned to each employee record.

    ![Create and add a mapping file](./images/jd-map-file.png)

2. **[Upload the new HR data to Workplace Analytics](#upload-new-hr-data-to-workplace-analytics)** - The HR manager must then add the new **Key_ID** column to the HR data (.csv) upload file and upload it as a subsequent upload with the new appended column and data into Workplace Analytics.

   ![Upload new HR data](./images/jd-wpa-upload.png)

3. **Add a [Workplace Analytics query](#add-a-query-file)** - The owner of the third-party data who has access to Workplace Analytics Queries as an Analyst needs to select the related query (.csv) data that now includes the **Key_ID** data, which was in the most recent HR data upload into Workplace Analytics.

   ![Add Workplace Analytics query data](./images/jd-wpa-query.png)

4. **Add [a new joined dataset](#add-a-new-join)** - While adding a join, you select the third-party data with the employee IDs that match up to the **Key_ID** column in the mapping file.

   ![Add third-party data](./images/jd-3p-data.png)

   * The template uses the mapping file to combine the two data sources into a new joined dataset that connects the data records by using join key look-up logic, and then replaces the Key ID and Employee ID with a system-generated sequence ID in the **SEQN** column for the combined data records, which keeps the data de-identified for analysis purposes.
   * After the template creates the joined dataset, data owners can download it as a .csv file or use it to [create new analysis](#add-and-view-analysis).

    ![New joined dataset](./images/jd-join-data.png)

## Create a mapping file

The owner of HR system data, such as the HR manager, needs to do the following to create and maintain the mapping file, which must only be accessible by that owner outside of Workplace Analytics and the Join Datasets Azure Template.

1. Create a new .csv file that includes employee HR data that uniquely identifies each employee in both the third-party data and the HR data uploaded into Workplace Analytics, such as an email alias and/or an employee number.
2. Then add a new column named **Key_ID** to the file, and then map a new unique key identifier for each employee.
3. Save the mapping file as a .csv file in UTF-8 format.

## Add a mapping file

1. In Workplace Analytics Azure Templates, select **Join Datasets** > **Mapping Data**.
2. Select **Add New Mapping File** at top right of the table.
3. In **Upload Mapping File**, enter a name, select the .csv file that you created in the previous steps, and then select **Upload Mapping File**.
4. After the upload succeeds, it'll be available in the **Mapping Data** list with the following options:

   * When the **Status** is a green check mark, the data was successfully uploaded. A red X means it failed.
   * Select a table column heading, such as **Name** or **Submitted**, to sort by it.
   * Select the **Update** icon to refresh the data in the mapping file. This is useful as your organization's employee data changes over time, such as for new hires.
   * Select the **Share** icon next to the file name, and then you can select which data owners get permission to use this file for joins.
   * Select the **Delete** (trashcan) icon to delete the file from the list.

## Upload new HR data to Workplace Analytics

The same unique Key_ID column created in the mapping file must also be added to the HR data that's uploaded into Workplace Analytics.

Follow the steps in [Subsequent uploads](../setup/upload-organizational-data.md#file-upload) and select to **Append** in **Step 9** to add the new Key_ID data into Workplace Analytics.

## Add a query file

1. In Workplace Analytics (WPA) Azure Templates, select **Join Datasets** > **WPA Data**.
2. Select **Add New WPA file** at top right of the table.
3. In **Upload WPA File**, select the .csv query file to upload, the time group you want data for, and whether you want to allow raw Workplace Analytics metrics in the aggregations.
4. Select **Upload WPA File**.
5. If prompted to define columns, select which columns in the query data you want to use as a metric for aggregations (calculations) and as an attribute for groupings, and then select **Submit**.
6. After the upload succeeds, the query will be available in the **WPA Data** list with the following options:

   * When the **Status** is a green check mark, the data was successfully uploaded. A red X means it failed.
   * Select a table column heading, such as **Name** or **Submitted**, to sort by it.
   * Select the **Share** icon next to the name to share access to this data with other users.
   * Select the **Delete** (trashcan) icon to delete the query from the list.

## Add a new join

1. In Workplace Analytics Azure Templates, select **Join Datasets** > **Joined Datasets**.
2. Select **Add New Join** at top right of the table.
3. In **Data Join Settings**, enter a name for the joined dataset, select the external dataset that matches up with the mapping file, the .csv query file, and the related mapping file.
4. In **Define Join Fields**, select the Workplace Analytics Person ID key and the third-party external data key (such as Employee ID).
5. In **Time and N Size**, select the time group you want data for and specify the minimum group size for groupings and aggregations, and then select **Submit**. For more information about minimum group sizes, see [Minimum group size](../use/settings.md#minimum-group-size).
6. After the dataset is successfully created, it'll be available in the **Joined Datasets** list with the following options:

   * When the **Status** is a green check mark, the dataset was successfully created. A red X means it failed. Check the job details to view an available error message.
   * Select a table column heading, such as **Name** or **Submitted**, to sort by it.
   * Select the **Download** icon to download the joined dataset as a .csv file.
   * Select the **Job Details** (i) icon next to **Status** to view the job details.
   * Select the **Delete Join** (trashcan) icon to delete it from the list.
   * Select the **Share** icon next to the name to share access to this data with other users.

## Add and view analysis

> [!Note]
> Users who are assigned the Analyst role in Admin settings will only see the **Joined Datasets** page. 

1. In Workplace Analytics Azure Templates, select **Join Datasets** > **Joined Datasets**.
2. Select the dataset name from the list.
3. Select **Add New Analysis** at top right of the table.
4. In **New Analysis Settings**, enter a name, select which attribute to group by, and which fields to aggregate (use for calculations), and then select **Submit**.
5. After the analysis is successfully created, it'll be available in the **Joined Datasets** list with the following options:

   * When the **Status** is a green check mark, the analysis was successfully created. A red X means it failed. Check the job details to view an available error message.
   * Select a table column heading, such as **Name** or **Submitted**, to sort by it.
   * Select the **Download** icon to download the analysis as a .csv file.
   * Select the **Dataset Parameters** icon to view parameter details.
   * Select the **Job Details** (i) icon next to **Status** to view the job details.
   * Select the **Delete Analysis** (trashcan) icon to delete it from the list.

## Joined dataset retention setting

Your template admin sets the number of days to retain data created and saved as joined datasets with this template. The current system default is **14 days**. See [Configuration](./deploy-configure.md#configuration) for details.

## Related topics

* [Workplace Analytics Azure Templates overview](./overview.md)
* [Deploy and configure Workplace Analytics Azure Templates](./deploy-configure.md)
