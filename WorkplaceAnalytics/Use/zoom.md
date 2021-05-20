---
ROBOTS: NOINDEX,NOFOLLOW
title: Workplace Analytics Zoom integration
description: Learn about and how to use the Workplace Analytics Zoom integration tool to include Zoom data in collaboration analysis
author: madehmer
ms.author: v-mideh
ms.topic: article
localization_priority: normal 
ms.prod: wpa
manager: scott.ruble
audience: Admin
---

# Workplace Analytics Zoom integration

*This experience is only available through private preview at this time.*

The Zoom integration adds meaningful collaboration metrics from Zoom meeting reports that complement existing metrics used in Workplace Analytics. This integration works with R for Windows and when released, will be included in the existing [wpa R package](../tutorials/wpa-r-package.md), which is an open-source repository of more than 100 functions that provide pre-built analyses.

This integration tool enables you to analyze unscheduled collaboration that occurs in Zoom. As an analyst, you can download the Zoom collaboration metrics either as a standalone .csv file or as a Ways of working assessment input file. You can then use the Zoom integration version of the [Ways of working assessment Power BI template](../tutorials/power-bi-collab-assess.md) to analyze a combination of Zoom and Microsoft 365 collaboration data in Power BI.

This analysis helps leaders and analysts get a richer, more complete picture of collaboration patterns within their organization. See [Zoom metrics](#zoom-metrics) for a complete list of the type of metrics used for analysis of Zoom collaboration activity.

![Zoom Power BI dashboard data](../images/wpa/use/zoom-pbi-data.png)

## Demonstrations

This self-serve, open-source toolkit requires a one-time installation of the R package by your Zoom Admin and Workplace Analytics Analyst.

Also, your admins must de-identify the Zoom reports, with a key mapping file, that's uploaded to Workplace Analytics as organizational data.

Subsequent runs will be faster after the initial setup of the mapping key file. The following demonstrations show how quickly you can prepare the Zoom data for integrating and analyzing in Workplace Analytics.  

#### Prepare Zoom files on-demand demo

<img src="../images/wpa/use/zoom-files-demo.gif" height="486" width="800" alt="video" data-linktype="relative-path">

#### Upload Zoom metrics on-demand demo

<img src="../images/wpa/use/zoom-metrics-demo.gif" alt="video" data-linktype="relative-path">

## Prerequisites

The following is required before you can run the Zoom Collaboration analysis in R:

* Workplace Analytics licenses for your analysis population.
* Zoom Business, Education, or API plans and have access to the Zoom Admin portal.
* Zoom Admin and Workplace Analytics Analyst need permission to install R and other associated packages.
* Have the latest version of Power BI Desktop installed. If you have an earlier version of Power BI installed, uninstall it before installing the new version. Then go to [Get Power BI Desktop](https://www.microsoft.com/p/power-bi-desktop/9ntxr16hnw1t?activetab=pivot:overviewtab) to download and install the latest version.

## Setup and configuration

1. **Install R for Windows** - Ask your Zoom Admin and Workplace Analytics Analyst to install [R for Windows](https://cloud.r-project.org/bin/windows/). If necessary, ask IT for permissions to install R for Windows.
2. **Download Zoom analyst integration** - Ask your Microsoft representative for the Zoom integration files. Then ask your Workplace Analytics Analyst to download the Zoom integration analyst package and extract it to a local folder.
3. **Download the Zoom admin integration** - Ask your Zoom Admin to download the Zoom admin integration package and extract it to a local folder. The integration has the following folder structure for both the Admin and the Analyst files.

   ![Zoom Admin integration folder structure](../images/wpa/use/zoom-files.png)

4. **Prepare a mapping file** - The Zoom report data that's downloaded from the Zoom Admin portal will include identifiable data about employees (email IDs). Before the metrics can be computed and shared with a Workplace Analytics Analyst, the information must be de-identified.

   1. The Zoom Admin must replace each **email ID** with a **unique random ID** that's specified by the Workplace Analytics Admin.
   2. Then the Workplace Analytics Admin must create a mapping file that maps a unique random ID (**HashID**) to each email address (**PersonID**) for each of the licensed employees in the company who are included in the analysis. Save this mapping file as a .csv file with the following headers and share it with the Zoom Admin for de-identification.

      ![Zoom mapping file sample data](../images/wpa/use/zoom-mapping-file.png)

   >[!Important]
   >You must save the mapping file as .csv and not as an .xls or .xlsx file.

5. **Append to existing organizational data** - Your Workplace Analytics Admin must upload the .csv mapping file with the **HashIDs** as an additional column named **PersonHashID** that appends the existing organizational data that's already uploaded in Workplace Analytics. For detailed instructions, see [Subsequent organizational data uploads](../setup/upload-organizational-data.md).

   >[!Important]
   >The Zoom meeting data includes identifiable data (email IDs) that must be de-identified before using it to create Workplace Analytics Person query data. Your admins must protect any identifiable data and only use de-identified Zoom data for analysis purposes.

6. **Download Zoom reports** - Your Zoom Admin needs to do the following:

   1. Sign in and go to **Admin** > **Account Management** > **Reports** > **Usage Reports** > **Active Hosts**.
   2. Set the scoped **From** and **To Dates**.
   3. Select **Meetings** > **Generate details report**. If you need more than one month of data, repeat these steps for prior months. Each report takes 1 to 2 hours to download.
   4. Save the downloaded reports in your **Zoom integration**/**Admin**/**input** folder with the mapping file from your Workplace Analytics Admin, and then save it in the same folder.

   ![Zoom admin input example files](../images/wpa/use/zoom-admin-files.png)

7. **Run and download Workplace Analytics data** - Your Workplace Analytics Analyst needs to do the following:

   1. Follow the steps in [Ways of working assessment](../tutorials/power-bi-collab-assess.md) and [Standard meeting query](../tutorials/query-basics.md#predefined-query-templates) to create the applicable query data. When running the queries, use the same date range as the Zoom data that was uploaded in **Step 5** and include the **TimeZone** and **PersonHashID** organizational data attributes.

      ![Required query data](../images/wpa/use/zoom-query-data.png)
      ![HR attributes required for the queries](../images/wpa/use/zoom-hr-attributes.png)

   2. Download the query results (.csv) to the **Zoom integration**/**Analyst**/**input** folder.

8. **Prepare the Zoom file** - Your Zoom admin needs to do the following:

   1. Confirm that the input folder has the relevant **Zoom reports** from **Step 5** and the **mapping file** from **Step 4**.
   2. In the **Zoom integration** folder, double-click **AdminActions.bat** to run it.
   3. When prompted, select **Rscript.exe** for the required script. If prompted to open the Rscript.exe file, close the prompt, and continue  running the file.
   4. Typically, the script file is located in the **C:/Program Files/R/R-4x-x/bin** folder. To find the file:

      * In Windows search, enter **RGUI.exe** to open the R graphical user interface, and then enter **file.path(R.home(), "bin", "Rscript.exe"**
      * Or in a Windows command prompt, enter **PowerShell** to open PowerShell. And then enter **get-childitem -Recurse -Name rscript.exe -path C:\ | select -First 1**

        >[!Note]
        >If R is installed on a custom drive, such as D:\ or E:\, replace C:\ with the applicable drive letter. For subsequent file prep, File Explorer will automatically open the right folder.

    5. Ignore the warnings during processing, and then when prompted, press any key to continue and exit.
    6. During this processing state, the Zoom reports are de-identified by using the hash key from the mapping file, and then joined into one combined file, which is saved in the **Admin**/**output** folder. Give the new Zoom output file to your Workplace Analytics Analyst.

9. **Upload the Zoom output data** - As the Workplace Analytics Analyst, save the Zoom output file to the **Zoom integration**/**Analyst**/**input** folder. Confirm that the Input folder also has the Ways of Working Assessment query, Standard meeting query, and the UTC_offset.rds file.
10. In the **Script** folder, double-click **AnalystActions.bat** to run it. When prompted, point it to **Rscript.exe**, which is usually in **C:/Program Files/R/R-4x-x/bin**.
11. Confirm the Output folder includes a new .csv file for Zoom collaboration metrics and a new .csv Zoom version of the Ways of Working Assessment Person Query that you can use with the new Zoom version of the Ways of Working Assessment dashboard in Power BI.

## Import and analyze in Power BI

Your Workplace Analytics Analyst needs to do the following to import the combined collaboration data into Power BI. After the import, you can analyze a combination of Zoom and Workplace Analytics collaboration metrics in the Ways of working assessment dashboard in Power BI.

1. In the **Analyst/output** folder, double-click **WOW_Zoom_Integration.pbit** to run the template.

   ![Zoom Ways of working assessment Power BI template](../images/wpa/use/zoom-pbi-template.png)

2. When prompted by Power BI, copy and paste the file path for the **Ways of Working Assessment query** .csv file in the **Analyst/output** folder. To copy it, right-click the file, select **Properties** > **Security**, and then select and copy the file path for the **Object's name**.
3. Use the **Standard meeting query** file that you downloaded in [Setup and configuration](#setup-and-configuration). For more information, see the [Ways of working assessment](../tutorials/power-bi-collab-assess.md).

## Zoom metrics

This integration uses the following Zoom metrics for collaboration analysis.

**Core metrics**

* Zoom Unscheduled call hours
* Zoom Scheduled call hours
* Zoom Total call hours
* Zoom Meetings
* Zoom Unscheduled Meetings
* Zoom Scheduled Meetings
* Zoom After hours in unscheduled calls
* Zoom After hours in scheduled calls

**Supplementary metrics**

* Zoom Unscheduled call hours 30 minutes or less
* Zoom Unscheduled call hours 31 to 59 minutes
* Zoom Unscheduled call hours 1 hour
* Zoom Unscheduled call hours 1 to 2 hours
* Zoom Unscheduled call hours more than 2 hours
* Zoom Unscheduled call hours 2 attendees
* Zoom Unscheduled call hours 3 to 8 attendees
* Zoom Unscheduled call hours 9 to 18 attendees
* Zoom Unscheduled call hours 19 or more attendees

## Related topics

* [wpa R package](../tutorials/wpa-r-package.md)
* [Ways of working assessment](../tutorials/power-bi-collab-assess.md)
