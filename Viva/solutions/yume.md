---
title: Yume - Overview
description: Learn about Yume, the solution the employees use to manage their interactions with their managers
author: v-smandalika
ms.author: v-smandalika
ms.topic: article
ms.localizationpriority: medium 
search.appverid:
- MET150
ms.service: viva 
ms.subservice: viva-insights
ms.collection: 
- M365-analytics
- viva-insights
manager: dansimp
audience: Admin
---

# Yume - Overview

Yume is an employee-driven solution to support 1:1 interaction between employees and their managers. It empowers employees to shape 1:1 meetings through topics (cards) that make discussions more meaningful. Employees can build and structure the agenda for an upcoming 1:1 meeting using the cards, which contain content that is simple and easy to access during the meeting. The employees can also refer to cards and key notes from previous 1:1 meetings and prepare cards for the future 1:1 meetings, promoting continuity and evolution of 1:1 meetings. There's also an option for employees to provide their feedback on the 1:1 interaction immediately once the meeting ends.

## Use case

1.	An employee has a challenge (for example, work-life balance and personal situation) that they want to bring up to their manager, but is unsure how to.
2.	An employee wants to explore, discuss and/or focus on their career growth and development.
3.	An employee is a new hire and wants to build a relationship with their new manager.

## Prerequisites for setup of Yume

To set up Yume, perform the following steps:

- [Download the Yume accelerator](#download-the-yume-accelerator)
- [Create an Azure AD Application registration](#create-an-azure-ad-application-registration)
- [Import the PowerApps Custom Connector](#powerapps-custom-connect-import)
- [Create Dataverse tables](#create-dataverse-tables) and [permissions](#create-dataverse-permissions)
- [Import the Yume application](#import-the-yume-application)

### Download the Yume accelerator

Download the Yume accelerator from the samples in the [VivaSolutions GitHub repository](https://github.com/microsoft/VivaSolutions/tree/main/Sample%20Solutions) from the server itself.

Another option is to clone this repository to your local machine and then download the samples in VivaSolutions GitHub repository.

### Create an Azure Active Directory (Azure AD) Application registration

Create an Azure Active Directory (Azure AD) Application registration by performing the following steps:

1. For the attribute **Name**, provide the value **vsol-yume-connector**.
1. Configure the following delegated permissions for the "Microsoft Graph" API:
    - Analytics.Read
    - MailboxSettings.Read
    - User.Read
    - Profile
1. Authenticate using the Web Redirect URL: https://global.consent.azure-apim.net/redirect
1. Create a client secret and make a note of its value.
1. Make a note of the Application ID (also known as the client ID).
   The value of the client secret and the client ID will be used during the PowerApps Custom Connector creation.

### PowerApps Custom Connector import

To import the PowerApps Custom Connector, perform the following steps:
1. Sign in to https://powerapps.microsoft.com.
1. Select **Data** (or **Dataverse**) on the left navigation menu.
1. Select **Custom connectors**.
1. Choose **+ New custom connector**.
1. For the **Connector name** field, enter **vsol-graph-analytics-connector**.
1. Select **Import**.
1. Select the *vsol-yume-connector.swagger.json* file and select **Open**. The **General** page that is displayed.
1. Leave all the values as is and select **Security**. The **Security** page is displayed.
1. On the **Security** page, perform the following substeps:
    1. For the **Client ID** field, enter the client ID (application ID) from the Azure AD application registration process.
    1. For the **Client secret** field, enter the client secret value from the Azure AD application registration process.
    1. For the Resource URL field, enter **https://developer.microsoft.com/graph/**.
    1. For the Scope field, leave the populated value as is.
    1. Select **Create connector** at the top-right of the menu-items bar.
    1. Select **Close** at the top-right of the menu-items bar. The connector should now be listed in the **custom connector** section.
1. Share the connector with the organization (as needed).

### Create Dataverse tables

1. Create the Dataverse tables that are described below. For more information on creating Dataverse tables, see [Create a custom table](/power-apps/maker/data-platform/data-platform-create-entity).

#### Yume Cards


|Column |Description  |
|---------|---------|
|TitleId     |   **Whole number**: Unique ID for the Title and Suggestions      |
|TitleName     |    **Text (850)**: (Primary column, Option Required) Title for the main category (needed only for the title card)     |
|TitleType     |**Text (100)**: Defines what the TitleName will be used for;               **MainTitle**: Identify TitleName as the main card title; **ContentTitle**: Identify the TitleName as the title for the content. |
|TitleContent     |   **Text (2048)**: Content for the card      |
|ContentType     |   **Text (100)**: Defines what the TitleContent will be used for;               **MainTitle**: Identify the TitleContent as the Description content for the main card title; **ContentTitle**: Identify the TitleContent as the content of the main card.      |
|CardType     |     **Text (100)**: Identifies how the display area content for the card will be presented.            **Metrics**: Predefined Viva Personal Insights based on graph data; **Horizontal**: Left/right control for navigating the content for the main card; **Vertical**: Vertical gallery (list) display of the content.  |
|DisplayOrder     |     **Whole Number**: The order to display the content in the horizontal/vertical format.    |

#### Yume Meeting Notes

|Column  |Description  |
|---------|---------|
|MeetingId     |    **Text (512)**: (Primary) Outlook meeting ID     |
|MeetingDateTime     |     Date and time    |
|MeetingName     | **Text (1024)**: Outlook meeting subject line        |
|MeetingTasks     |   **Text (2048)**: Delimited task list      |
|CaIds    |     **Text (1024)**: Delimited card IDs    |
|Emp Feedback     |    **Text(1024)**: Emp meeting feedback     |
|Emp Feeling     |      **Text(100)**: Emp meeting sentiment   |

#### Yume User Options

|Column  |Description  |
|---------|---------|
|SettingName     |    **Text(100)**: (Primary) Setting Name     |
|SettingValue     |   **Text (512)**: Content for the card      |

2. During the Dataverses table creation, make a note of the table prefix name.

   :::image type="content" source="../media/tables-yume-card-data.png" alt-text="Tables containing Yume card data":::

### Create Dataverse permissions

To create Dataverse permissions, perform the following steps:

1. Launch the URL https://admin.powerplatform.microsoft.com/environments. 
1. Select the environment for which you want to create Dataverse permissions.
1. Select **Users and permissions > Security Roles**.
   The following roles are the ones you can create:
    - **Basic User role (for access to User table and Yume tables)**: Updated to include user rights for tables. This role provides read-only access for the card data table and other rights for the other Yume tables.
    
      :::image type="content" source="../media/basic-user-role-permissions.png" alt-text="Basic permissions for a user role":::

    - **YumeContentAdmin (custom role)**: This role is permissive so should only be accounts that need access across all the data (for example, nudges from Power Automate).
        - Yume Cards::: Parent: Child Business Units
        - Yume Meeting Notes ::: Parent: Child Business Units
        - Yume User Options ::: Parent: Child Business Units
    
      :::image type="content" source="../media/yume-content-admin-role.png" alt-text="Yume content admin role":::

### Set working hours and days for users mailbox settings

We recommend the working hours and days to be set for the users who will be using the application for more accurate working hours calculations. For information on how to set working hours and days for user mailbox settings, see [Set-MailboxCalendarConfiguration](/powershell/module/exchange/set-mailboxcalendarconfiguration). If not set, a default value of 45 hours will be used.

## Create the Power Automate flows for nudging

To create the Power Automate flows for nudging, perform the following steps:
1. Download Task and Meeting zip file.
1. Create a service account (as needed).
1. Add the service account as a member of the Yume content administrator security role.
1. Sign in to Power Automate by launching the URL https://powerautomate.microsoft.com.
1. Create connections to **Teams** and **Microsoft Dataverse**, for example, adding connections for Microsoft Dataverse as shown in the following screenshot.

   :::image type="content" source="../media/add-connection-to-dataverse.png" alt-text="Adding a connection to Dataverse":::

1. Import the meeting flows by performing the following substeps:
    1. Select **My flows** on the left navigation pane. The **Flows** page is displayed.
    
       :::image type="content" source="../media/powerautomateimportmeetingsflo1.png" alt-text="The Flows page from which the user can select the Import option":::

    1. Select **Import**. The **Import package** page is displayed.
    
       :::image type="content" source="../media/powerautomateimportmeetingsflo1a.png" alt-text="The Import page":::

    1.  Select **Upload**. The file browser dialog box is displayed.
    
        :::image type="content" source="../media/powerautomateimportmeetingsflo1abrowse.png" alt-text="The dialog box displaying th files from which the user can select the one to upload":::

    1. Select the file you want to upload, and select **Open**.
    
       The selected file is populated in the **Upload** box, and the upload process begins which is indicated by the button changing from **Upload** to **Uploading**.

       :::image type="content" source="../media/uploading-process-commencement.png" alt-text="The page displaying the in-progress upload process":::

       After a few minutes, the package is successfully uploaded, and the same is displayed on the **Import package** page.

       :::image type="content" source="../media/page-containing-uploaded-package.png" alt-text="The page displaying the uploaded package":::
     
    1. Select **Create as new**. The Import setup pane is displayed on the right side of the page, as shown in the following screenshot.
    
       :::image type="content" source="../media/powerautomateimportmeetingsflo1a1.png" alt-text="The page on which you define the package and save it before it is imported":::

    1. Update the name as per discretion from the **Resource name** box, and select **Save**. You return to the **Import package** page, with the updated name displayed under the **Create as new** option.
    1. Select the resource types for **Microsoft Dataverse Connection** and **Microsoft Teams Connection** by performing the following substeps:
        1. Select the option **Select during import** for each of the two connections.
           The **Import setup** pane as shown in the following screenshot is displayed.

           :::image type="content" source="../media/connection-display.png" alt-text="The Import setup pane on which the created connection is displayed":::
        1. Select the connection. On selecting it, the **Save** button is enabled, as shown in the following screenshot.
        
           :::image type="content" source="../media/saving-displayed-connection.png" alt-text="The option to Save the connection that is displayed":::

        1. Select **Save**. You are taken back to the **Import package** page.

           :::image type="content" source="../media/powerautomateimportmeetingsflo1b.png" alt-text="The Import package page with the Import option enabled":::  

    1. Select **Import**. Once the import process is completed successfully, a notification message is displayed as shown in the following screenshot.
   
       :::image type="content" source="../media/powerautomateimportmeetingsflo1c.png" alt-text="The page displaying the notification of the successful import of the package resources":::

       If this import process fails, the page as shown in the following screenshot is displayed.

       :::image type="content" source="../media/saveasnewflow.png" alt-text="The page containing the Save as new flow option":::
           
    1. Select **Save as new flow**. The import process is completed successfully as shown in the following screenshot:
    
       :::image type="content" source="../media/save-as-new-flow-import-completed.png" alt-text="Import completion using Save as new flow option":::
         
    1. Select **Open flow** to edit the flow-related information. The page as shown in the following screenshot is displayed:
    
       :::image type="content" source="../media/page-on-selecting-open-flow.png" alt-text="The page on selecting the Open flow option":::
       
    1. Update the **Initialize variable** page for dataprefix by populating the **Value** field with the value of the Dataverse table created earlier, for example, **cr627** as shown in the following screenshot.
        
           :::image type="content" source="../media/initialize-variable-page.png" alt-text="Initialize variable page":::

    1. Select **Initial variable** to update the **Initialize variable** page for dataprefix.
        1. Populate the **Value** field with the value of the Dataverse table created earlier, for example, **cr627** as shown in the following screenshot.
        
           :::image type="content" source="../media/initialize-variable-page.png" alt-text="The Initialize variable page":::

    1. Select **Initial variable** to update the **Initialize variable** page for Yume URL by populating the **Value** field with the value of the PowerApps Weblink URL for the Yume PowerApp.
    1. Update the frequency as needed (currently set to every 1 week on Sunday).
    1. Save the flow.
1. Repeat the import process for the Tasks flow by performing the following substeps:
    1. Select **Initial variable** to update the **Initialize variable** page for dataprefix:
        1. Populate the **Value** field with the value of the Dataverse table created earlier, for example, **cr627** as shown in the following screenshot.
        
           :::image type="content" source="../media/initialize-variable-page.png" alt-text="Initialize variable page":::

    1. Select **Initial variable** to update the **Initialize variable** page for Yume URL.
        1. Populate the **Value** field with the value of the PowerApps Weblink URL for the Yume PowerApp.
    1. Update the frequency as needed (currently set to every 1 week on Sunday).
    1. Save the flow.
    
## Import data into Dataverse tables

To import data into the Dataverse tables, perform the following steps:
1. Download the Yume Card Data V3 initial content CSV file from the VivaSolutions Github repository if not already downloaded as part of the prerequisites.
1. Sign in to https://powerapps.microsoft.com and select the environment to which you'll be deploying the CSV file.
1. On the left navigation pane, select **Dataverse > Tables**.

   :::image type="content" source="../media/dataverse-tables-options-selection.png" alt-text="The page on which we select Dataverse and Tables options":::

   The page listing the Dataverse tables is displayed.

   :::image type="content" source="../media/importdataverse1a.png" alt-text="The page listing the Dataverse tables":::

1. Find the Yume Cards table using the **search** box as shown in the following screenshot.

   :::image type="content" source="../media/importdataverse1b.png" alt-text="The search box using which the user can find the Yume table":::
 
   The Yume Cards table is displayed.

1. Open the Yume Cards table by selecting the three-dotted option and then selecting **Open**.

   :::image type="content" source="../media/importdataverse1c.png" alt-text="The page from which the user can launch the information of the Yume Cards table":::

   The screen containing information of Yume Cards is displayed.

   :::image type="content" source="../media/import-data-from-excel-option.png" alt-text="The page from which we can select Import > Import data from Excel":::

1. Select **Import > Import data from Excel**. The page as shown in the following screenshot is displayed.

   :::image type="content" source="../media/importdataverse2b.png" alt-text="The Import data pane":::

1. Select **Upload**. A dialog box listing files and folders is displayed.

   :::image type="content" source="../media/importdataverse2c.png" alt-text="The dialog box listing files and folders that the user can select to upload":::

1. Select the *YumeCardDataV3_initialcontent.csv* file. This selected file is displayed in the **File** box as shown in the following screenshot.

   :::image type="content" source="../media/importdataverse2d.png" alt-text="The page on which the file to be uploaded is displayed in the File box":::

1. Select **Map columns** on the far-right side of the page. The column mapping page is displayed, as shown in the following screenshot.

   :::image type="content" source="../media/column-mapping.png" alt-text="Column mapping":::

1. Select **Save changes** on the top right. You return to the Import data pane, as shown in the following screenshot.

   :::image type="content" source="../media/dataimport.png" alt-text="The Import data pane on the right side of the page":::

1. Select **Import** on the top right. A notification message denoting a successful import is displayed, for example, the following screenshot.

   :::image type="content" source="../media/import-completed-successfully.png" alt-text="The notification that the import has been completed successfully":::

## Import the Yume application

To import the Yume application, perform the following steps:
1. Download the Yume PowerApp zip file from the VivaSolutions GitHub repository if not already downloaded as part of the prerequisites.
1. Sign in to https://powerapps.microsoft.com.
1. Select the environment you'll be deploying the CSV file to.
1. Select **Apps**. The **Apps** page is displayed.

   :::image type="content" source="../media/import-canvas-app-option.png" alt-text="The Import canvas app option the user can select":::

1. Select **Import canvas app**. The page with the **Upload** button is displayed.

   :::image type="content" source="../media/importcanvasapp1a.png" alt-text="The page with the Upload option":::
   
1. Upload the zip file that was downloaded earlier. Once the upload process has been successfully completed, the page as shown in the following screenshot is displayed:

   :::image type="content" source="../media/upload-earlier-downloaded-zip-file.png" alt-text="Uploading the zip file downloaded earlier":::

1. Under the **Choose your import options** pane, select **Create as new** that is corresponding to YUME_mobile_MVP. The page shown in the following screenshot is displayed.

   :::image type="content" source="../media/importcanvasapp2a.png" alt-text="The page on which the user can update the name":::

1. Update the name to a unique name for the environment in the **Resource name** box, for example, Yume_mobile.
1. Select **Save**. You return to the Import wizard page.
1. Select the option **Select during import** corresponding to **vsol-yume-connector**. The page with the **Import setup** pane on the right side is displayed.

   :::image type="content" source="../media/importcanvasapp2b2.png" alt-text="The Import setup pane on the right side of the Import wizard page":::

1. Select **Save**. You return to the Import wizard page.
1. Select **Import** at the bottom-right side of the page. 

   :::image type="content" source="../media/selecting-import.png" alt-text="The page on which the user can select the Import option":::

   Once the import process has been completed, there will be a message as shown in the following screenshot.

   :::image type="content" source="../media/notification-to-user.png" alt-text="Notification message that denotes that the import was successful":::

6. Select **Open apps**. The page as shown in the following screenshot is displayed:

   :::image type="content" source="../media/page-containing-application-details.png" alt-text="The page containing details of the application that you want to edit":::

7. Select **Allow** to allow permissions to be applied to the application.
1. Select **Apps** from the left navigation pane.
   > [!NOTE]
   > The application to which access has been allowed will be displayed on the **Apps** section of the page after a few minutes. This time period during which the application is about to be displayed is depicted in the following screenshot:

     :::image type="content" source="../media/editapp1.png" alt-text="The page that indicates the time period leading up to the display of the application":::
   
   The app will appear in the **Apps** section of PowerApps.

   :::image type="content" source="../media/display-of-app-in-apps-section.png" alt-text="The Apps section in which the newly created app is displayed":::

    1. Select **OnStart** from the drop-down list.
    1. Change the value **cr1de** to the table prefix value noted during the Dataverse table creation earlier (in this example, the value is **cr627**)
1. Select **Data** from the left navigation pane. The **Data** page is displayed.

   :::image type="content" source="../media/data-page.png" alt-text="The Data page":::

    1. Remove the following data items:
        1. Yume Cards
        1. Yume User Options
        1. Yume Meeting Notes
        1. Vsol-graph-analytics-connector
    1. Add the following data items:
        1. Yume Cards
        1. Yume User Options
        1. Yume Meeting Notes
        1. Vsol-graph-analytics-connector
1. Share out the power app to the target audience.

### Publish the Yume application to the organization app catalog

The Yume application can be published in the organization app catalog for users to use this application within the Teams client. For more information on how to publish the Yume application to the organization app catalog, see [Embed a canvas app as personal app in Teams](/power-apps/teams/embed-teams-app).

## Edit Dataverse tables or create Yume Cards

This section is classified into the following subsections:

### Edit the Dataverse tables

To edit the Dataverse tables, perform the following steps:
1. Sign in to https://powerapps.microsoft.com, and select the environment in which you've deployed the  Dataverse tables.
1. Select **Dataverse > Tables**.

   :::image type="content" source="../media/dataverse-tables-options-selection.png" alt-text="The Dataverse > Tables path":::

1. Find and open the Yume Cards. The page containing information about the Yume Cards is displayed.

   :::image type="content" source="../media/edit-data-in-new-tab.png" alt-text="The edit data in new tab option":::

1. Select **Edit > Edit in new tab**. The page as shown in the following screenshot is displayed.

   :::image type="content" source="../media/editdataverse1.png" alt-text="The page after the user selects the Edit in new tab option":::

1. Select the drop-down list.

   :::image type="content" source="../media/editdataverse1b.png" alt-text="The page with the drop-down list":::

1. Select and save all the fields defined in the schema for Yume Cards (see [Yume Cards](#yume-cards). The page containing the schema selected from the drop-down list is displayed.

   :::image type="content" source="../media/editdataverse1c.png" alt-text="The page showing the schema that is selected from the drop-down list":::

1. Update the content that you want to, from the cells of the table.

### Create new Yume Cards content

To create new content for the Yume Cards, perform the following steps:
1. Add a new row by selecting **+ New row** on the page containing information of the Yume Cards.

   :::image type="content" source="../media/add-new-row.png" alt-text="The page on which the user can add a new row":::

Examples of the content that can be added are described below:

:::image type="content" source="../media/updating-cards-overall-example.png" alt-text="The top-level example of updating cards":::

Examples of how the cards can be updated are described below:

In the following screenshot:
- Example A describes the process of adding a new TitleName for the main category.
- Example C describes the process of adding a new Title Description for the main category.

  :::image type="content" source="../media/examples-a-and-c.png" alt-text="An example of adding a new name and description for a title":::

- The following screenshot describes Example B, that is, the process of adding the Content Title for the new main card category.

  :::image type="content" source="../media/example-b.png" alt-text="An example that illustrates how to add ContentTitle to the new main card category":::

- The following screenshot describes Example D, that is, the process of adding the Content for the new main card category.

  :::image type="content" source="../media/example-d.png" alt-text="The example that illustrates how to add content for the new main card category":::