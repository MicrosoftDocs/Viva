---
ms.date: 04/18/2022
title: "Box Integration"
ms.reviewer: 
ms.author: rasanders
author: RaSanders-MSFT
manager:
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

Viva Goals Box integration lets you update your objective and key result (OKR) progress automatically by syncing your data from your spreadsheets in Box to your OKRs in Viva Goals.
  
When you link your objectives to the corresponding key performance indicator (KPIs) within spreadsheets in Box, the status of your OKR will be updated based on the data in your spreadsheets. Viva Goals automatically syncs the values for you and charts your progress toward the goal, saving time while keeping your OKRs current.

## How to enable Box integration

Admins can follow these steps to enable the integration:

1. From the sidebar, go to **Admin** and select the **Integrations** tab.
  
     :::image type="content" source="../media/goals/10/viva-goals-integrations-page.png" alt-text="Screenshot shows the integrations page in Viva Goals." lightbox="../media/goals/10/viva-goals-integrations-page.png":::

2. For **Box**, choose to **Enable** the integration. If a connection was made previously or if the integration was already enabled, you can choose to **Manage** the enabled integration.
  
    :::image type="content" source="../media/goals/10/box-enable-button.png" alt-text="Screenshot shows where you enable Box in Viva Goals." lightbox="../media/goals/10/box-enable-button.png":::

3. This integration can also be disabled from the same section: Go to **Change** and select **Disable integration** from the dropdown.
  
    :::image type="content" source="../media/goals/10/box-disable-button.png" alt-text="Screenshot shows how you disable Box integration in Viva Goals." lightbox="../media/goals/10/box-disable-button.png":::

## How to configure Box integration

1. After you enable the integration, the next step is to configure a Box connection.

2. Select the **Add Objective** button to create an objective.

3. Open the newly created objective and select **Edit** within the **More** option.
  
     :::image type="content" source="../media/goals/10/box-okr-edit-button.png" alt-text="Screenshot shows where you choose to edit an OKR to add a new Box connection." lightbox="../media/goals/10/box-okr-edit-button.png":::

4. Under **Progress**, select **Automatically from a data source** and choose **Box** from the search menu.
  
    :::image type="content" source="../media/goals/10/box-datasource.png" alt-text="Screenshot shows where you select Box from the list of data sources in Viva Goals." lightbox="../media/goals/10/box-datasource.png":::

5. To add a new connection between Viva Goals and Box, sign in with your Box credentials.

6. A dialog opens where you grant access to Box to integrate with Viva Goals. This access allows Viva Goals to read and download files from your Box account.

## How to connect a spreadsheet in Box to an OKR

After you configure the connection, the next step is to link OKRs to the spreadsheets in Box.

1. Select the KPIs you want to reflect within the objective from your spreadsheet in Box. To do this, select **edit integration**, which appears when you select the Box icon.

2. Select the **Edit Integration** link from the dropdown.
  
    :::image type="content" source="../media/goals/10/box-edit-integration-button.png" alt-text="Screenshot shows the option to edit the integration to add a new Box connection in Viva Goals." lightbox="../media/goals/10/box-edit-integration-button.png":::

3. Next, select the spreadsheet or the Excel workbook (.xlsx) by searching for it from the search bar. You can search for any sheet that you own or that was shared with you by other users. For your spreadsheet to be processed, it needs to be unlocked from the sheet.

4. After the spreadsheet is downloaded, you can select any sheet within it from the **Sheet** drop-down menu.

5. Now can track value by either a **Named Range** or a **Column & Row Number**. This value is used to locate your KPI data in the spreadsheet.

   It takes up to 15 minutes for your newly created named range to be displayed in the **Select a named range** dropdown.

7. After you select the range, you'll see a preview of the selected value from the sheet so you can double-check from the sheet.
  
    :::image type="content" source="../media/goals/10/box-connection-details.png" alt-text="Screenshot shows a preview from your selected worksheet in Box." lightbox="../media/goals/10/box-connection-details.png":::

8. Select the **Next** button. You'll see that the objective has been connected to Box.

9. Select **Save** to save the integration.
  
## How to create a named range in Excel and Google Sheets
  
You can create named ranges in Excel (.xlsx) or Google Sheets to keep better track of values in your Box spreadsheets. Instead of using a column and row number to describe a range of cells, you could give the cell a unique range name that can be referred to.
  
### The benefits of using named ranges
  
Naming ranges in Box using Excel or Google sheets bring flexibility into your workbooks.

Named ranges have an explicit name that makes it simpler for you or other users to refer to the contents in a cell. With a unique name, you can mitigate the confusion that comes with using row and column numbers, and it's much easier for anyone who needs to work with that workbook/sheet.

Also, name ranges are permanent. So, if you make any changes in your sheet such as adding or deleting rows and columns, the cell you refer to by a named range will always be permanent. This isn't the case when you use row and column numbers.
  
### Create a named range in Excel

1. Select the range for which you want to create a **Named Range** in Excel.

2. Select **Define Name** under **Formulas**.

    :::image type="content" source="../media/goals/9/excel-define-name-button.png" alt-text="Screenshot shows where you select Define Name in Excel." lightbox="../media/goals/9/excel-define-name-button.png":::

3. In the **New Name** dialogue, type the name you want to assign to the selected data range. You can specify the scope as the entire workbook or a specific worksheet. If you select a particular sheet, the name wouldn't be available on other sheets.

    :::image type="content" source="../media/goals/9/excel-define-name-dialog.png" alt-text="Screenshot shows the Define Name dialog box in Excel." lightbox="../media/goals/9/excel-define-name-dialog.png":::

4. Select **OK**.

### Create a named range in Google Sheets

1. Open a spreadsheet in Google Sheets.

2. Select the cells you want to name.

3. Select **Named ranges** under **Data**. A menu will open on the right.

    :::image type="content" source="../media/goals/9/google-named-range-button.png" alt-text="Screenshot shows where you select a Named Range under Data in Google Sheets." lightbox="../media/goals/9/google-named-range-button.png":::

4. Type the range name you want.

    :::image type="content" source="../media/goals/9/google-named-range-dialog.png" alt-text="Screenshot shows the Named Ranges option highlighted on the Data menu." lightbox="../media/goals/9/google-named-range-dialog.png":::

5. Select **Done**.

