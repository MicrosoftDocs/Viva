---
title: Step 5-Import the Yume application
description: Learn how to import the Yume application
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

# Step 5 - Import the Yume application

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

## Publish the Yume application to the organization app catalog

The Yume application can be published in the organization app catalog for users to use this application within the Teams client. For more information on how to publish the Yume application to the organization app catalog, see [Embed a canvas app as personal app in Teams](/power-apps/teams/embed-teams-app).