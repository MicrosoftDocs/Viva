---
ms.date: 08/29/2024
title: "Use the Viva Connections Dashboard web part"
ms.reviewer: 
ms.author: evanatkin
author: AtkinE
manager: elizapo
audience: Admin
f1.keywords:
- NOCSH
ms.topic: article
ms.service: viva-connections
ms.localizationpriority: high
ms.collection:
  - Strat_SP_modern
  - M365-collaboration
  - m365initiative-viva-connections
  - Tier1
search.appverid:
- SPO160
- MET150
description: "Learn how to use the Dashboard web part"
---

# The Viva Connections Dashboard web part

[Viva Connections](https://www.microsoft.com/microsoft-viva/connections) is an integrated experience designed to drive user engagement. When [deploying Viva Connections](viva-connections-setup-overview.md), you'll [set up a Dashboard](/viva/connections/create-dashboard) and [use cards](/viva/connections/create-dashboard#available-dashboard-cards) to bring together resources for different audiences to provide a comprehensive view of everything they need to complete common tasks. For example, the Dashboard could include a card that allows users to access cafeteria menus, schedules, reports, shift schedules, HR policies, and more.

Once a Dashboard is published, you can use the Dashboard web part to display it on your SharePoint home site. If you want to add, remove, or reorder cards, the existing Dashboard on your site must be edited. To learn how to create or edit a Dashboard, see [Create a Viva Connections dashboard and add cards](create-dashboard.md).

## Add the Dashboard web part

To add a Dashboard web part, firstly ensure that you are in the **edit** mode. Select **Edit** at the top-right of the SharePoint home site page.

Once in **edit** mode, perform the following steps:

1. Hover your mouse around the section within which you want to place the web part, and select the **circled +**.

2. In the web part search box, enter **Dashboard** to quickly find and select the **Dashboard for Viva Connections** web part.

   :::image type="content" source="../media/connections/dashboard-picker.png" alt-text="Screenshot that shows the screen on which you can search for a web part and select it once displayed.":::

   The web part is added to your page and is populated with the cards from the existing Dashboard on your site. In this example, the Dashboard is placed in a vertical section on the right:

   :::image type="content" source="../media/connections/display-of-web-card.png" alt-text="Screenshot showing the screen that displays the web card.":::

3. Optionally, you can change the title of the Dashboard by selecting it in the web part and typing over it with your own title.

   :::image type="content" source="../media/connections/editing-title-of-dashboard.png" alt-text="The screen that displays the option that allows you to edit the title of a Dashboard.":::

4. To move the web part, select the **Move web part** icon and drag the web part to a different section or column on the page.

5. To set the value for maximum number of cards to display on the web part, select the **Edit web part** pencil icon.

6. Use the slider to indicate the maximum number of cards to display.

   :::image type="content" source="../media/connections/defining-threshold-cards-to-display.png" alt-text="The screen displaying the option by which you can define the count of the cards to be displayed.":::

   > [!NOTE]
   > When there are more cards available than the maximum number set for the web part, users can select **See all** to see the rest of them.

7. Once the card-count threshold is set, select **Publish** or **Republish** to make the page available with your newly placed Dashboard web part.

## Additional information

- **The Dashboard web part is hidden when there are no cards to show**: There might be no cards to show when the Dashboard author has targeted cards for specific audiences, and people outside of those audiences are viewing the page. For example, if all cards are targeted to your development group, only people in the development group will see the Dashboard.

- **We recommend you use the Dashboard web part in a vertical section**: Although a vertical section is recommended, the web part can be used in any section in one, two, or three column layouts. Here’s an example of a Dashboard web part in a horizontal section:

   :::image type="content" source="../media/connections/Dashboard-web-part-horizontal-section.png" alt-text="The screen displaying the web part in a horizontal layout.":::

- **The Dashboard web part can be added to any page on your SharePoint home site**: The Dashboard is most useful on your SharePoint home page, but it's possible to add it to any page on your SharePoint home site. One practical use for adding the Dashboard to your home site is to experiment with your page layout to see where you think the Dashboard fits best. Just create a copy of your SharePoint home page and start experimenting.
- **The Dashboard web part can be used in sections with a colored background**: When editing a section, you can change the background of the section and the cards of the Dashboard will have a different color from that background.

   :::image type="content" source="../media/connections/card-color.png" alt-text="The screen indicating the color of the card.":::

- **“See all” appears on the top-right of the Dashboard web part** when there are more Dashboard cards available than can be displayed in the Dashboard web part. When **See all** is selected, a page that shows the entire Dashboard is displayed.

   :::image type="content" source="../media/connections/full-display-Dashboard.png" alt-text="The screen displaying a full view of the Dashboard.":::

## More resources

[Overview of Viva Connections](viva-connections-overview.md)

[Set up and launch Viva Connections](set-up-admin-center.md)
