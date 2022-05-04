---
title: Organizational network analysis with Gephi
description: Explains how to install and use Gephi for custom data visualization from Organizational network analysis 
author: lilyolason
ms.author: v-lilyolason
ms.topic: article
ms.localizationpriority: medium 
search.appverid:
- MET150
ms.service: viva 
ms.subservice: viva-insights
ms.collection: 
- M365-analytics
- viva-insights
manager: helayne
audience: Admin
---

# Organizational network analysis with Gephi

Gephi is an open-source network analysis software that enables users to create customized network analysis measures and maps.

## Installation

Install Gephi using the following steps:

1. Download Java and install. Note the folder location in which Java installs.
2. Download Gephi and install. Note the folder location in which Gephi installs.

    You may have to update the Gephi configuration file with the location for Java according to the following steps:

    1. Locate the folder location in which Java is installed. By default, Java installs at  **C:\Program Files (x86)\Java\jre1.8.0_251**
    1. Open the **jre1.8.0_251 folder**, then select address bar and copy the folder path.
    1. Locate the Gephi configuration file (**gephi.conf**) within the folder in which Gephi was installed (**“…Gephi-0.9.2\etc”**). By default, Gephi installs at  **C:\Program Files\Gephi-0.9.2\etc.**
    1. Open the Gephi configuration file with a text editor like Notepad.
    1. Remove the leading **#** from the **#jdkhome** line (towards the end of the Gephi configuration file).
    1. In the **jdkhome** line, paste in the Java folder path that you’ve recently copied to your clipboard so that the Gephi configuration line reads similar to  jdkhome=**"C:/Program Files (x86)/Java/jre1.8.0_251"**.
    1. Save and close the Gephi configuration file, then open Gephi.

## Group-level network map

### Setup

Run a **Group-to-group query** in Workplace Analytics with Viva Insights:

1. In Workplace Analytics with Viva Insights, navigate to the **Group-to-group queries** page (**Analyze > Query designer > Get started > Group-to-group**).
2. Set up a query with monthly data aggregation and a date range.
    
    :::image type="complex" source="../images/ztw-group-network-map.png" alt-text="Screenshot of the Time investors section of the Group-to-group query setup":::
      Screenshot that shows the Group-to-group query setup in Workplace Analytics. It's titled "ZTW Group Network Map." Under the "Group by" heading, "Month" is selected from the dropdown menu. Under the "Time period" heading, "Last 1 month" is selected from the dropdown menu. "Auto-refresh" box is not selected. Under "Meeting exclusions, "Initial Setup Exclusions" appears in the dropdown menu box.
    :::image-end:::

1. Under **Select metrics**, select **Collaboration hours**.
1. Under **Time investors**, group by your preferred attribute.
    
    :::image type="complex" source="../images/g2g-step-4-time-investors.png" alt-text="Screenshot of Group-to-group query setup showing Group by and Time period settings":::
       Screenshot that shows the Time investors section of the Group-to-group query setup in Workplace Analytics. Under "How do you want to group the time investors," "Zone_To_Win" is selected from the dropdown menu. No filters are added underneath "Do you want to limit the analysis to only certain time investors." At the bottom of the image reads, "Measured employees: 9,090" and "Filter group: 8,268.".
    :::image-end:::

1. Under **Their collaborators**:
    1. Optional: You might choose to exclude external collaborators (**IsInternal** = **False**) and focus the analysis on those with a Workplace Analytics license (**WPA_License** = **Y**).
    1. Group by the same attribute selected in step 4.
    
        :::image type="content" source="../images/g2g-step-5-their-collaborators.png" alt-text="Screenshot of Group-to-group query setup's Their collaborators section":::

1. Verify your settings and run your analysis.
1. Once your queries have completed, download the .csv file.
1. Relabel the group names as you would like them to appear on your visual.
1. Use a Pivot Table (Rows = **Source**, Columns = **Target**, Values = **Collaboration_hours**) to:
    1. Filter out groups that you do not wish to show in your analysis (for example, **Other_collaborators**, groups falling below minimum aggregation size, or groups not relevant to your analysis).
    1. Aggregate multiple time periods of data into a single value.
        
        :::image type="content" source="../images/g2g-step-9b-pivot-table-fields.png" alt-text="Screenshot of Excel Pivot Table field list with Target under Columns, Source under Rows, and Sum of Collaboration_hours under Values":::

10.	Create a new tab and unpivot (manually or automatically through the following steps) your Pivot Table into a new table with the following three columns: **Source** (from Pivot Table Rows), **Target** (from Pivot Table Columns), and **Weight** (from Pivot Table cell values for each row-column combination)
    1. Store data in a table.
    1. Select any cell in the table.
    1. In the command ribbon, select the **Data** tab, then select **From Table/Range**.
        
        :::image type="content" source="../images/g2g-step-10c-from-table-range.png" alt-text="Screenshot of Excel command ribbon, showing Data tab":::

    1. Select the columns you want to unpivot by selecting the first column and holding the Shift key to select the rest.
    1. In the **Transform** tab, select **Unpivot Columns**.
               
        :::image type="content" source="../images/g2g-step-10e-unpivot.png" alt-text="Screenshot of Excel's Query editor with Transform and Unpivot Columns highlighted":::

    1. Select the **Home** tab, then select **Close & Load**.
    1. Manually remove some of the rows as needed.

    Your table should resemble the following image:

    :::image type="content" source="../images/g2g-step-10-example-table.png" alt-text="Screenshot an Excel spreadsheet showing Source, Target, and Weight columns populated with data":::

11.	Save this file to use in the next steps.

### Create

1. Open Gephi and create a **New Project**.
2. Select the **Data Laboratory** button and select **Import Spreadsheet**.
             
    :::image type="content" source="../images/glnm-step 2-import-spreadsheet.png" alt-text="Screenshot of Gephi interface with Data Laboratory button highlighted and Nodes tab highlighted":::

3. Navigate to the folder where you saved your Group-to-group query and select the file you created in previous section. This file will serve as the underlying data for your network map.
4. Select the tab with the cleansed data from the file you prepared and verify that Gephi recognizes this file as an **Edges Table**. If not, select this value from the **Import** as dropdown menu.
            
     :::image type="content" source="../images/glnm-step-4-edges-table.png" alt-text="Screenshot of Gephi interface with Comma selected uner Separator and Edges table selected under Import as":::

> [!NOTE]
> Sometimes, Gephi doesn’t recognize your **Source** and **Target** column due to a problem with the UTF-8 encoding. If you have this problem, try saving the file as a regular .csv.

5. Select **Next** and make sure that Gephi recognizes your **Weight** column as a **Double** data type, then select **Finish**.

    :::image type="content" source="../images/glnm-step-5-weight-double.png" alt-text="Screenshot of Import settings widow with Weight box checked and Double selected in dropdown menu":::

6. You can likely ignore the errors, especially **Edge weight is 0**. Before selecting **OK**, make sure to choose **Append to existing workspace**.
             
    :::image type="content" source="../images/glnm-step-6-append.png" alt-text="Screenshot of Gephi interface with two warnings under Issues tab and Append to existing workspace radio button selected":::

7. To add groupings for coloring, you’ll need to add additional attributes to your nodes. You can add attributes manually (step a.) or by creating a Node file (step b.):
    1. Add manually: Adding attributes through a manual process within Gephi tool is a good option if you have a limited number of rows. When uploading the Edge file, Gephi automatically detects the nodes.
        1. Select the **Nodes** tab and select **Add column** from the bottom of the page.
        
            :::image type="content" source="../images/glnm-step-7ai-add-column.png" alt-text="Screenshot of Gephi interface with Data Laboratory button and Nodes tab selected":::
            
            :::image type="content" source="../images/glnm-step-7ai-add-column2.png" alt-text="Screenshot of Gephi interface with Add column button selected":::

        1. Title your new column and select **Data Type = String**.
        1. A new column will appear in your **Nodes** table. Double-click the first row and add the info that this group falls under. Repeat this action for other attributes you want to add about each group (for example, **GroupSize**). Additionally, you can choose to input custom labels for each node in the Label column.
    1. Prepare a Node file with your desired columns:
        1. An **Id** column is required, and it should correspond to the groups you have as **Source** and **Target** columns in the Edge file.
        1. You can then add additional columns like **Label**, **GroupSize**, and **Organization**. These columns can later be used for coloring and sizing of the nodes in the visualization.
1. Navigate back to the **Overview** tab at the top of the page to see an initial view of your group-level network.
1. To color your nodes by an attribute, select the palette icon from the **Nodes** tab, select the **Partition** sub-tab, choose colors, then select **Apply**.

    :::image type="content" source="../images/glnm-step-10-size-nodes.png" alt-text="Screenshot of Gephi interface Appearance tab with Nodes and Ranking tabs selected":::

10.	Size your nodes by selecting the circles icon and selecting an attribute.

    :::image type="content" source="../images/glnm-step-9-color-nodes.png" alt-text="Screenshot of Gephi interface Appearance tab Nodes and Partition tabs selected":::

> [!NOTE]
> You can also color your Edges (Collaboration weights between each node).

11.	Click on the **Overview** tab to begin creating your visual. Run through the following sub-steps to tune your visual in the **Layout** pane on the left-hand side of the screen:
    1. Select **OpenORD** from the dropdown menu and Run after inputting the following settings:
        1. **Liquid** = 50
        1. **Expansion** = 50
        1. Other settings in the **Stages** section = 0
        1. **OpenOrd** settings: Keep defaults
                    
              :::image type="content" source="../images/glnm-step-11aiv-openord.png" alt-text="Screenshot of Gephi interface Layout tab OpenOrd selected from dropdown menu and Stages and OpenOrd lists expanded":::

    1. Next, select **Force Atlas 2** from the dropdown menu and **Run** after inputting the following settings:
        1. **Scaling** = 500
        1. **Gravity** = 0
        1. **Dissuade hubs**: Make sure this is checked
        1. Other parameters: Keep defaults
    1. Stop **Force Atlas 2** after the nodes are sufficiently spread out.
    1. Change the **Scaling** parameter to 1.0 (instead of 500 or 1000) and **Run** again until the node movement is significantly slowed down.
    1. Center on the graph using the magnifying glass icon.
    
        :::image type="content" source="../images/plnm-step-10e-magnifying-glass.png" alt-text="Screenshot of Gephi interface with magnifying glass icon highlighted":::

12.	Once you’ve finished setting up your network visualization, select the **Preview** page to polish your network graph.
                    
     :::image type="content" source="../images/glnm-step-12-preview.png" alt-text="Screenshot of Gephi interface with Preview button highlighted":::

13.	In the **Preview Settings** panel, adjust **Borders**, **Labels**, **Line Thickness**, **Font**, etc., to polish your network. See below for the difference between what we set up in the **Overview** page versus the polishing in the **Preview** page.

    :::image type="content" source="../images/glnm-step-13-preview.png" alt-text="Screenshot of less detailed network map and more network map, separated by an arrow":::

## Person-level network map

### Setup

#### Create a person-to-person interaction table

You have a few options to create a person-level interaction table.

* Network Person-to-person query
* Person-to-person query via Group-to-group query

##### Network person-to-person query

1. In Workplace Analytics with Viva Insights, navigate to the Network person-to-person query page (**Analyze > Query designer > Get started > Network: Person-to-Person**).
 
2. Set up a query with your desired data aggregation level and a date range.
3. Select the “Strong and Diverse tie scores” metric and filters. Filters are not required unless there is a specific group you would like to focus on in the analysis. 
4. Run the query and export the results once the run is complete.
5. Rename these columns as follows:

|Original column name   |New column name  |
|----------|-----------|
 TieOrigin_zId | Source
 TieDestination_zId | Target
StrongTieScore | Weight

6. Copy the **Source**, **Target**, and **Weight** columns over to a new tab. Save this tab as a .csv file named **CleansedInteractions.csv**.

> [!NOTE]
> For **Source** and **Target** columns, you can also use **TieOrigin_PersonId** and **TieDestination_PersonId** columns; however, for consistency with some of the other methods of creating an interaction table, we've selected the **zId** columns.

7. Follow the steps in [Person query to create a node file](#person-query-to-create-a-node-file) to create a node file to go with the interaction table you just created.

#### Person-to-person query through a Group-to-group query

Workplace Analytics doesn't have a **Person-to-person query** as an out-of-the-box query template. However, you can turn a **Group-to-group query** into a **Person-to-person query** by following this guidance.

**PersonId**, the main person identifier in the Workplace Analytics Organizational data, will be hashed (de-identified) in your reports and not available to be selected as your group **Collaborator** in the **Group-to-group query**. However, if you add an additional person identifier to your HR org file when uploading (that is, you generate a column that has anonymized **PersonId** for each person), you can use that metric in **Time investors** and **Their collaborators** sections of the **Group-to-group query** to change the group collaboration to a person-level collaboration. In the following image, **zId** is that additional person identifier.

> [!IMPORTANT]
> Make sure the additional person identifier (**zId**) is not an employee ID or any identifiable number that would allow the analyst to identify and analyze the interactions at the person level. For privacy reasons, Workplace Analytics de-identifies the **PersonId** by default when the HR org file is uploaded.

:::image type="complex" source="../images/ona-zid(1).png" alt-text="Screenshot of Workplace Analytics Query designer step 2":::
   Screenshot that shows the Workplace Analytics Query designer's interface. Under step 2, Time Investors, zID is selected from the dropdown menu beneath the prompt, "How do you want to group the time investors".
:::image-end:::

To create the interaction matrix (or Edge list) for the ONA analysis:

1. Navigate to the **Group-to-group query** page in Workplace Analytics (**Analyze> Query designer > Group-to-group**).
1. Set up a query with your desired data aggregation level and time period.
1. Select the metrics like **Collaboration hours**, **Email hours**, **Meeting hours**. Set filters as needed.
1. Select the zId under **Time investors** and **Their collaborators** .
1. Run the query and export the results once the run is complete.
1. In the exported file, select the following columns and rename using your preferred naming structure.

|Original column name   |New column name  |
|----------|-----------|
 TimeInvestors_zId (zId) | Source
 Collaborators_zId | Target
Collaboration_hours (or any other metric that you prefer to be used) | Weight

7. Copy the **Source**, **Target**, and **Weight** columns over to a new tab and save this tab as a .csv file named **CleansedInteractions.csv**.
1. Follow the steps in [Person query to create a node file](#person-query-to-create-a-node-file) to create a node file to go with the interaction table you just created.

> [!NOTE]
> If you want to see the metrics available in the Person-to-group query (like email counts) as part of the interaction table, you can transform the **Person-to-group query** to a **Person-to-person query** using the same process as steps 1-8 above (in step 4, Select the **zId** in the **Their Collaborators** and **Organizational data** sections of the query).
> In this case, the selection and renaming of the columns should match the following table:

|Original name|New name|
|-------------|---------|
TimeInvestors_zId (zId)|Source
Collaborators_zId |Target
Collaboration_hours (or any other metric that you prefer to be used) |Weight

#### Person query to create a node file

1. Navigate to the Person query page in Workplace Analytics: **Analyze > Query designer > Get started > Person**.

    :::image type="content" source="../images/plnm-step-1-query.png" alt-text="Screenshot of Workplace Analytics Query designer with Get started button highlighted":::

    :::image type="content" source="../images/plnm-step-1-query(2).png" alt-text="Screenshot of Workplace Analytics Choose a query type menu with Person button selected":::

2. Set up a query with the following settings:

    |Setting |Selection|
    |-------------|---------|
    Group by |Month
    Time Period |Last 1 month
    Collaboration_hours (or any other metric that you prefer to be used) |Weight
    Select metrics| Minimum one metric; the specific metric isn’t important for our purposes here
    Select filters| All employees or Active employees
    Organizational data | zId in addition to any organizational data that you plan to use for grouping, sorting, coloring, and sizing of the nodes

3. Run the query and export the results once the run is complete.
4. Rename the column **zId** as **ID**.
5. Filter and aggregate the data so that you get a single value for each employee (ID aka zId).
6. Select the **ID** column and the **Organizational data** columns you selected in step 2, copy into a new tab, and then save the tab as its own .csv file named CleansedNodeMetrics.csv. Close the .csv file.

> [!NOTE]
> You can also filter the node file to only include the nodes/employees/ IDs that are either a Source or Target in the CleansedInteractions.csv file you just created.

### Create 

1. Create a new workspace in Gephi by navigating to **Workspace > New**, then selecting the **Data Laboratory** button.

    :::image type="content" source="../images/plnm-step-1-new-datalab.png" alt-text="Screenshot of Gephi interface with Workspace tab hovered over and New highlighted on the dropdown list":::

2. Select **Import Spreadsheet**, then select the **CleansedInteractions.csv** file that you created via one of the approaches above (Person-to-person query via Group-to-group query or Person query to create a node file). This .csv file is the underlying data for your network map.
3. Make sure that Gephi recognizes the file as an **Edges** table under **Import as**, then select **Next**.
:::image type="content" source="../images/plnm-step-2-edges.png" alt-text="Screenshot of Gephi interface General CSV options window with Comma selected under Separator and Edges table selected under Import as":::
4. Make sure the **Weight** column is identified as a **Double** data type, then select **Finish**.
5. Ignore the warnings, then select Append to existing workspace.

    :::image type="content" source="../images/plnm-step-5-append.png" alt-text="Screenshot of Gephi interface that shows warning and Append to existing workspace radio button selected":::

1. Select Import Spreadsheet again, then select your CleansedNodeMetrics.csv file. This additional data enables grouping, coloring, and node sizing based on your Org Data.

> [!NOTE]
> If you receive a Gephi memory error, follow the instructions [here](https://gephi.org/users/install/#memory) to increase the memory allotment.

7. This time, make sure that Gephi recognizes the .csv file as a **Nodes** table under **Import as**. If it doesn’t, change the type using the dropdown menu, then select **Next**.
8. Make sure that Gephi detects the right datatypes for each column, then select **Finish**.
9. Select **Append** to existing workspace, then select **OK**.
10. Select the **Overview** tab to begin creating your visual. Then, run through the following sub-steps to tune your visual in the **Layout** pane on the left-hand side of the screen:
    1. Select OpenORD and run after inputting the following settings:
        1. **Liquid** = 50
        1. **Expansion** = 50
        1. Other settings in the **Stages** section = 0
        1. **OpenOrd** settings: Keep defaults
        
            :::image type="content" source="../images/plnm-step-10aiv-openord.png" alt-text="Screenshot of Gephi interface Layout tab with OpenOrd selected from the dropdown menu and Stages and OpenOrd lists expanded":::

    1. Next select **Force Atlas 2** and **Run** after inputting the following settings:
        1. **Scaling** = 500
        1. **Gravity** = 0 
        1. **Dissuade hubs**: Make sure this is checked
        1. Other parameters: Keep defaults
    1. Stop **Force Atlas 2** after the nodes are sufficiently spread out.
    1. Change the **Scaling** parameter to 1.0 (instead of 500 or 1000) and run again until the node movement is significantly slowed down.
    1. Center on the graph using the magnifying glass icon.
    
        :::image type="content" source="../images/plnm-step-10e-magnifying-glass.png" alt-text="Screenshot of Gephi interface with magnifying glass icon highlighted":::

> [!NOTE]
> You can also create organic community groupings by selecting the Statistics tab on the right panel and running the Modularity algorithm with default settings.
 
11.	Color your network map by modularity grouping:
    1. Select the **Nodes** tab in the **Appearance** panel.
    1. Select the **Partition** sub-tab.
    1. In the dropdown menu, choose the **Modularity Class** grouping as your color designation.
    1. Select **Apply**.

        :::image type="content" source="../images/glnm-step-9-color-nodes.png" alt-text="Screenshot of Gephi interface Appearance tab with Nodes and Partition tabs selected":::

> [!NOTE]
> You can increase the number of groups that are colored by selecting the **Palette** button at the bottom right of the **Appearance** panel and choosing to generate a new palette with a higher color limit. You can also customize the colors within your palette.

  :::image type="content" source="../images/plnm-step-11-note.png" alt-text="Screenshot of Gephi interface's Generate Palette popup window with Limit number of colors box checked and 8 in the value field":::

12.	Optional: Adjust the bubble sizes using any of the node-level metrics.