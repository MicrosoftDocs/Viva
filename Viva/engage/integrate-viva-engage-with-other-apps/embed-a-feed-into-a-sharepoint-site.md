---
title: "Include a Viva Engage feed in a SharePoint page"
f1.keywords:
- NOCSH
ms.author: v-bvrana
author: Starshine89
manager: elizapo
ms.date: 01/04/2024
audience: Admin
ms.topic: article
ms.localizationpriority: medium
ms.service: viva
ms.subservice: viva-engage
ms.custom: Adm_Yammer
ms.collection: SPO_Content
search.appverid:
- MET150
- MOE150
- YAE150
ms.assetid: 4817d2fa-50f6-4f25-88a0-a312745768d4
description: "Add a Viva Engage feed to a modern or classic SharePoint site page."
---

# Include a Viva Engage feed in a SharePoint page

To include a Viva Engage feed in a SharePoint page, your organization should have an active Viva Engage network (for example: http&#58;//www&#46;engage&#46;com/contoso&#46;com). 

- For SharePoint Online, you can use the Viva Engage Conversations web part so that page viewers can engage in the conversation without leaving SharePoint.  The Viva Engage Conversations web part has the latest Viva Engage experiences including the ability to start a conversation with any type of post (Questions, Polls, Praise) and mark best answers directly from SharePoint. You can also use the Viva Engage Highlights web part to display recent conversations. However, the Highlights web part doesn't have all the latest Viva Engage experiences. 

- For SharePoint Server 2019 modern pages, you can use the Viva Engage Highlights web part (Classic mode) to add a group, user, article, or Viva Engage home feed.

- For SharePoint Servers 2013 and 2016 and for classic pages in SharePoint Server 2019, use Viva Engage Embed within a script editor web part. This lets you add a group feed, user feed, article feed, Viva Engage home feed, or an open graph object feed. 
  
## Add a Viva Engage feed to a page in SharePoint Online

>[!NOTE]
> The Viva Engage Conversations and Highlights web parts only work when the SharePoint site uses the original domain name, for example contoso.onmicrosoft.com, and are not supported when the SharePoint site uses a vanity domain name.

For instructions for how to use the Viva Engage Conversations or Viva Engage Highlights web part, see [Use a Viva Engage web part in a SharePoint Online](https://support.office.com/article/a53cfa0c-3d09-42c8-a286-1038a81c59da). 

These web parts inherit the page theme, and are usable from mobile devices. 

## Add a Viva Engage feed to a modern page in SharePoint Server 2019

1. Go to Viva Engage in a browser, and go to the Viva Engage page you want to put in SharePoint: a group, person, article, or the Viva Engage home page. Copy the URL. 

2. In SharePoint, go to the page you want to put the Viva Engage feed on, and select **Edit**.

3. Select + to add a new web part. 

4. Select the Viva Engage web part.

5. In the Viva Engage box on the right, paste the URL you copied in step 1 into the **Web address** box.

6. To change the display size, select an option in **Display size**. 

7. To publish your page, select **Publish**.

## Add a Viva Engage feed to a classic page in SharePoint Servers 2013, 2016, and 2019 
<a name="AddFeed"> </a>

There are three basic steps:

1. Add a script editor web part to your SharePoint page.

2. Copy and edit a simple script that identifies the type of feed you want and the Viva Engage network you're using.
    
3. Paste the script into the web part and publish your SharePoint page. 

When a Viva Engage feed is added using this method, the feed can't be viewed when using a mobile browser or if third-party cookies aren't enabled. For more information about browser support when using a Viva Engage feed in a script editor web part, see [Viva Engage Embed requirements](/viva/engage/integrate-viva-engage-with-other-apps/integrate-with-other-applications).
    
### Step 1: Set up the web part 

1. In your SharePoint site, choose **Edit**.
    
2. On the ribbon, choose **Insert** \> **Web Part** and in the **Categories** list, select **Media and Content** \> **Script Editor**. 

3. In **Add part to:**, select where you want to add the web part, and then choose **Add**.   
    
4. Locate your new script editor web part, and choose **Edit Snippet**.
    
5. Paste the script you copied from Viva Engage into the script editor web part.
    
6. Choose **Insert**.
    
7. Save and publish the SharePoint page. You should see the Viva Engage Group conversation on the SharePoint page.

### Step 2: Copy and edit the script to use

The following procedures describe how to add a group feed, my feed, or page feed. For information about other feed types, see [Viva Engage Embed](/viva/engage/integrate-viva-engage-with-other-apps/integrate-with-other-applications). You can also use the Viva Engage Embed configuration tool to create the script to use.e
  
 **Prepare the script for a group feed**
  
1. In Viva Engage, go to the group that you want to embed. Locate the **Access Options** section and select **Embed this group in your site**.
    
    :::image type="content" source="../../media/a0bdb091-2d21-4041-adaf-bb66da668c64.png" alt-text="Screenshot of access options for Viva Engage group.":::
  
2. Copy the script from the window.
   
    **Prepare the script for a my feed**
   
    1. Edit the following script to use your Viva Engage network instead of contoso.com, and then paste it into the script editor web part.
    
       ```javascript
       <div id="embedded-my-feed" style="height:400px;width:500px;"></div> 
           <script type="text/javascript" src="https://c64.assets-yammer.com/assets/platform_embed.js"></script>
           <script 'type="text/javascript"> yam.connect.embedFeed({  
                     container: '#embedded-my-feed',
                     network: 'contoso.com'  });
           </script>
  
       ```

       > [!NOTE]
       > You can also change the height and width parameters to the height and width you prefer. 

    **Prepare the script for a page feed**
  
    1. Go to the page that you want to embed. Copy the URL to the page.
    
    2. Edit the following script, replacing "contoso.com" with your Viva Engage network and the URL with the page you want.
    
       ```javascript
       <div id="embedded-feed" style="height:400px;width:500px;"></div> 
       <script type="text/javascript" src="https://assets.yammer.com/assets/platform_embed.js"></script> 
       <script type="text/javascript"> yam.connect.embedFeed({
                container: "#embedded-feed", 
                network: "contoso.com", 
                feedType: "open-graph", 
                objectProperties: { url: "https://www.contoso.com/sample_page" , type: "page" } }); 
       </script>
  
       ```

      > [!NOTE]
      > You can also change the height and width parameters to the height and width you prefer. 

     This example shows an open graph feed for a web page, but you can create feeds for other open-graph objects. If you're interested in using the Viva Engage Embed widget to add Viva Engage feeds to your SharePoint pages, see [Add the Viva Engage Embed widget to a SharePoint page](/viva/engage/integrate-viva-engage-with-other-apps/viva-engage-and-newsfeed).
    
### Step 3: Paste in the script, and publish the SharePoint page.

- On the SharePoint page, paste in the script, and then select **Publish**.
    
    >[!NOTE]
    >For the Highlights (Classic mode) and the Viva Engage embed script experiences, when you add a Viva Engage My Feed/Home feed to a SharePoint page, you'll see slightly different messages than the ones included in the Home feed available in Viva Engage web, desktop, or mobile. The following feed for users contains messages from people, topics, and files they follow. The My Feed contains messages from All Company and the user's following feed. In Viva Engage web, desktop, and mobile, users can select Discovery, All, or Following feeds, but these aren't available in SharePoint pages. The My Feed/Home feed type is closest to the All feed but doesn't include public posts in public groups the user doesn't belong to.<br><br>

If you want Viva Engage to be the primary social experience for SharePoint, see [SharePoint enterprise social experience](/viva/engage/integrate-viva-engage-with-other-apps/viva-engage-and-newsfeed).