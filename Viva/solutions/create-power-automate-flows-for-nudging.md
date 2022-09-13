---
title: (Optional) Step 6-Create the Power Automate flows for nudging
description: Learn how to create the Power Automate flows for nudging
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

# Step 6 - Create the Power Automate flows for nudging

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
    
        :::image type="content" source="../media/powerautomateimportmeetingsflo1abrowse.png" alt-text="The dialog box displaying th files from which the user can select the one to upload" lightbox="../media/powerautomateimportmeetingsflo1abrowse.png":::

    1. Select the file you want to upload, and select **Open**.
    
       The selected file is populated in the **Upload** box, and the upload process begins which is indicated by the button changing from **Upload** to **Uploading**.

       :::image type="content" source="../media/uploading-process-commencement.png" alt-text="The page displaying the in-progress upload process" lightbox="../media/uploading-process-commencement.png":::

       After a few minutes, the package is successfully uploaded, and the same is displayed on the **Import package** page.

       :::image type="content" source="../media/page-containing-uploaded-package.png" alt-text="The page displaying the uploaded package" lightbox="../media/page-containing-uploaded-package.png":::
     
    1. Select **Create as new**. The Import setup pane is displayed on the right side of the page, as shown in the following screenshot.
    
       :::image type="content" source="../media/powerautomateimportmeetingsflo1a1.png" alt-text="The page on which you define the package and save it before it is imported":::

    1. Update the name from the **Resource name** box, and select **Save**. You return to the **Import package** page, with the updated name displayed under the **Create as new** option.
    1. Select the resource types for **Microsoft Dataverse Connection** and **Microsoft Teams Connection** by performing the following substeps:
        1. Select the option **Select during import** for each of the two connections.
           The **Import setup** pane as shown in the following screenshot is displayed.

           :::image type="content" source="../media/connection-display.png" alt-text="The Import setup pane on which the created connection is displayed" lightbox="../media/connection-display.png":::

        1. Select the connection. On selecting it, the **Save** button is enabled, as shown in the following screenshot.
        
           :::image type="content" source="../media/saving-displayed-connection.png" alt-text="The option to Save the connection that is displayed" lightbox="../media/saving-displayed-connection.png":::

        1. Select **Save**. You're taken back to the **Import package** page.

           :::image type="content" source="../media/powerautomateimportmeetingsflo1b.png" alt-text="The Import package page with the Import option enabled":::  

    1. Select **Import**. Once the import process is completed successfully, a notification message is displayed as shown in the following screenshot.
   
       :::image type="content" source="../media/powerautomateimportmeetingsflo1c.png" alt-text="The page displaying the notification of the successful import of the package resources":::

       If this import process fails, the page as shown in the following screenshot is displayed.

       :::image type="content" source="../media/saveasnewflow.png" alt-text="The page containing the Save as new flow option" lightbox="../media/saveasnewflow.png":::
           
    1. Select **Save as new flow**. The import process is completed successfully as shown in the following screenshot:
    
       :::image type="content" source="../media/save-as-new-flow-import-completed.png" alt-text="Import completion using Save as new flow option":::
         
    1. Select **Open flow** to edit the flow-related information. The page as shown in the following screenshot is displayed:
    
       :::image type="content" source="../media/page-on-selecting-open-flow.png" alt-text="The page on selecting the Open flow option" lightbox="../media/page-on-selecting-open-flow.png":::
       
    1. Update the **Initialize variable** page for data prefix by populating the **Value** field with the value of the Dataverse table created earlier, for example, **cr627** as shown in the following screenshot.
      
       :::image type="content" source="../media/initialize-variable-page.png" alt-text="Initialize variable page":::

    1. Select **Initial variable** to update the **Initialize variable** page for data prefix.
        1. Populate the **Value** field with the value of the Dataverse table created earlier, for example, **cr627** as shown in the following screenshot.
        
           :::image type="content" source="../media/initialize-variable-page.png" alt-text="The Initialize variable page":::

    1. Select **Initial variable** to update the **Initialize variable** page for Yume URL by populating the **Value** field with the value of the PowerApps Weblink URL for the Yume PowerApp.
    1. Update the frequency as needed (currently set to every 1 week on Sunday).
    1. Save the flow.
1. Repeat the import process for the Tasks flow by performing the following substeps:
    1. Select **Initial variable** to update the **Initialize variable** page for data prefix:
        1. Populate the **Value** field with the value of the Dataverse table created earlier, for example, **cr627** as shown in the following screenshot.
        
           :::image type="content" source="../media/initialize-variable-page.png" alt-text="Initialize variable page":::

    1. Select **Initial variable** to update the **Initialize variable** page for Yume URL.
        1. Populate the **Value** field with the value of the PowerApps Weblink URL for the Yume PowerApp.
    1. Update the frequency as needed (currently set to every 1 week on Sunday).
    1. Save the flow.