---
title: "Box Integration"
ms.reviewer: 
ms.author: vsreenivasan
author: ms-vikashkoushik
manager: <TBD>
audience: Admin
f1.keywords:
- NOCSH
ms.topic: article
ms.service: viva
ms.subservice: viva-goals
ms.localizationpriority: medium
ms.collection:  
- m365initiative-viva-goals
search.appverid:
- MET150

description: "Learn how to integrate your spreadsheets in Box with OKRs in Viva Goals."
---

# Box integration

The Viva Goals Box integration allows you to update your Objectives and Key Results (OKR) progress automatically by syncing your data from your spreadsheets within Box to your OKRs in Viva Goals. 
  
When you link your objectives to the corresponding key performance indicator (KPIs) within spreadsheets in Box, the status of your OKR will be updated based on the data in your spreadsheet. Viva Goals will automatically sync the values for you and chart your progress toward the goal, thus saving time while keeping your OKRs current.

## How to enable the Box integration

Admins can perform the following steps to enable this integration:

1. From the sidebar, go to **Admin** and select the **Integrations** tab.
  
     :::image type="content" source="../media/goals/10/viva-goals-integrations-page.png" alt-text="Integrations page in Viva Goals." lightbox="../media/goals/10/viva-goals-integrations-page.png":::

2. Against **Box**, you can **Enable** the integration. If a connection has been made previously or if the integration has been enabled, you can **Manage** the enabled integration.
  
    :::image type="content" source="../media/goals/10/box-enable-button.png" alt-text="Enabling Box in Viva Goals." lightbox="../media/goals/10/box-enable-button.png":::

3. This integration can also be disabled from the same section. Go to **Change** and select **Disable integration** from the dropdown to disable the integration.
  
    :::image type="content" source="../media/goals/10/box-disable-button.png" alt-text="Disabling Box in Viva Goals." lightbox="../media/goals/10/box-disable-button.png":::

## How to configure the Box integration

1. After you enable the integration, the first step is to configure a Box connection.

2. Select the **Add Objective** button to create an objective.

3. Open the newly created objective and select **Edit** within the **More** option.
  
     :::image type="content" source="../media/goals/10/box-okr-edit-button.png" alt-text="Edit OKR to add new Box connection in Viva Goals." lightbox="../media/goals/10/box-okr-edit-button.png":::

4. Under **Progress**, select **Automatically from a data source** and choose **Box** from the search menu.
  
    :::image type="content" source="../media/goals/10/box-datasource.png" alt-text="Selecting Box from the list of data sources in Viva Goals." lightbox="../media/goals/10/box-datasource.png":::

5. You can add a new connection between Viva Goals and Box by signing in with your Box credentials.

6. This opens up a pop-up window where you can grant access to Box to integrate with Viva Goals. This access allows Viva Goals to read and download files from your Box account.

## How to connect a spreadsheet in Box to an OKR

Once you have configured the connection, the next step is to start linking OKRs to the spreadsheets in Box.

1. Once the connection is established, select the KPIs you would want to reflect within the objective from your spreadsheet in Box. To do this, select **edit integration** which comes up when you select the Box icon.

2. Select the **Edit Integration** link from the drop-down.
  
    :::image type="content" source="../media/goals/10/box-edit-integration-button.png" alt-text="Edit integration to add new Box connection in Viva Goals." lightbox="../media/goals/10/box-edit-integration-button.png":::

3. Next, select the spreadsheet or the excel workbook(.xlsx) by searching for it in the search bar. You can search for any sheet that you own or has been shared with you by other users. For your spreadsheet to be processed, it needs to be unlocked from the sheet.

4. Once the spreadsheet is downloaded, you can select any sheet within it from the **Sheet** drop-down menu.

5. Now can track value by either a **Named Range** or a **Column & Row Number**. This is used to locate your KPI data in the spreadsheet.

6. It takes up to 15 minutes for your newly created Named range to be displayed in the **Select a named range** dropdown.

7. Once you select the named range, you'll see a preview of the selected value from the sheet so you can double-check from the sheet.
  
    :::image type="content" source="../media/goals/10/box-connection-details.png" alt-text="Adding new Box connection to OKRs in Viva goals." lightbox="../media/goals/10/box-connection-details.png":::

8. Select the **Next** button. You'll now see that the objective has been connected to Box.

9. Select **Save** to save the integration.
  
## How to create a named range in Excel and Google Sheets
  
You can create named ranges in Excel(.xlsx) or Google Sheets to keep better track of values in your Box spreadsheets. Instead of using a column and row number to describe a range of cells, you could give the cell a unique range name that can be referred to at any point in time.
  
### The benefits of using named ranges
  
Naming ranges in Box using Excel or Google sheets can help you bring a lot of flexibility into your workbooks.

Named ranges have an explicit name that makes it simpler for you or any user to refer to the contents in a cell. With a unique name, you can mitigate the confusion that comes with using row and column numbers and it becomes much easier for you or for anyone who needs to work with your workbook/sheet.

Also, name ranges are permanent. So, if you make any changes in your sheet by adding or deleting rows and columns, the cell you refer to by a named range will always be permanent. This is not the case when you use row and column numbers.
  
### Create a named range in Excel

1. Select the range for which you want to create a **Named Range** in Excel.

2. Select **Define Name** under **Formulas**.

    :::image type="content" source="../media/goals/9/excel-define-name-button.png" alt-text="Selecting Define Name under Formulas in Excel." lightbox="../media/goals/9/excel-define-name-button.png":::

3. In the **New Name** dialogue box, type the Name you wish to assign to the selected data range. You can specify the scope as the entire workbook or a specific worksheet. If you select a particular sheet, the name would not be available on other sheets.

    :::image type="content" source="../media/goals/9/excel-define-name-dialog.png" alt-text="Define Name dialog box in Excel." lightbox="../media/goals/9/excel-define-name-dialog.png":::

4. Select **OK**.

### Create a named range in Google Sheets

1. Open a spreadsheet in Google Sheets.

2. Select the cells you want to name.

3. Select **Named ranges** under **Data**. A menu will open on the right.

    :::image type="content" source="../media/goals/9/google-named-range-button.png" alt-text="Selecting Named Range under Data in Google Sheets." lightbox="../media/goals/9/google-named-range-button.png":::

4. Type the range name you want.

    :::image type="content" source="../media/goals/9/google-named-range-dialog.png" alt-text="Named Range dialog Box in Google Sheets." lightbox="../media/goals/9/google-named-range-dialog.png":::

5. Select **Done**.
