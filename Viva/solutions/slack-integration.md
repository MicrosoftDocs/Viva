---
ROBOTS: NOINDEX, NOFOLLOW
title: Slack Integration
description: Learn how to join Viva Insights query data with collaboration data from a third-party tool
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

# Slack Integration

You can join Viva Insights query data with collaboration data from a third-party tool. In this article, we use Slack as an example of an end-to-end pipeline for Viva Insights data and a third-party data set. For additional instructions on how to use Viva Insights, refer to the [Viva Insights training resources](https://docs.microsoft.com/learn/browse/?products=m365%2Cviva-insights&expanded=viva).
  
## High-level architecture flow

Here is a high-level flow of the pipeline.

:::image type="content" source="./images/high-level-overview.png" alt-text="Architecture flow beginning with Enterprise Grid Slack Web API and ending with Power BI":::

## Prerequisites

To complete the steps in this article, you’ll need:

1. To download the Slack synapse pipeline sample files from the [VivaSolutions GitHub repository](https://github.com/microsoft/VivaSolutions), or clone the repository to your local machine
2. PowerShell (minimum version 5.1) and the latest [Az PowerShell Module](https://docs.microsoft.com/powershell/azure/new-azureps-module-az)
3. Access to the Slack enterprise grid
4. To have completed the Slack app registration and gotten an oAuth token (see [Slack app registration](#slack-app-registration) to learn how to get the oAuth token)

### Slack app registration

To get the oAuth token this pipeline needs:

1. Create a [Slack application registration](https://api.slack.com/authentication/basics#creating).

    You’ll need the following settings:

   * Redirect URL:

        ```
        https://app.slack.com

        https://slack.com/

        https://flow.microsoft.com/
        ```

    * User scopes:

        ```
        admin.analytics:read
        ```

    Refer to the following App Manifest example. The redirect URLs and user scope have updates.

    ```
    display_information:
        name: vsappanalytics
        features:
          bot_user:
            display_name: vsappanalytics
            always_online: true
        oauth_config:
            redirect_urls:
                - https://app.slack.com/
                - https://slack.com/
                - https://flow.microsoft.com/
            scopes:
                user:
                    - admin.analytics:read
                bot:
                    - commands
                    - incoming-webhook
        settings:
            org_deploy_enabled: true
            socket_mode_enabled: false
            token_rotation_enabled: false
    ```
2. Install the application (e.g., `vsappanalyticc`) to the enterprise and enable it in the workspace.

    Here’s an example:
:::image type="content" source="./images/install-and-enable-app.png" alt-text="vsappanalyticc install and enable":::

4. Find the User oAuth Token (`xoxp xxxxxx`) needed for authentication to the workspace under the Install App & OAuth & Permissions sidebar. You’ll input this token in the `parameters.json` file.

## Deploy Azure infrastructure

1. Update the `parameters.json` file. The needed configuration values are described within the file.
2. Launch a PowerShell command window.
3. Navigate to where you saved the files from the GitHub download.
4. Execute the `synapseworkspace_arm_deployment.ps1` PowerShell.

Once the PowerShell command in step 4 is successfully executed, follow the steps in [Deploy synapse pipeline](#deploy-synapse-pipeline).

## Deploy Synapse pipeline

1. To maintain consistency, use the same `parameters.json` file you did in [Deploy Azure infrastructure](#deploy-azure-infrastructure).
2. Execute the `synapseworkspace_pipeline.ps1` PowerShell.
3. Update the **Notebook** activities in the **SlackAnalyticsPipeline**:

    1. In the [Azure portal](https://portal.azure.com/#home), open the deployed **Synapse workspace**.

    :::image type="content" source="./images/deployed-synapse-workspace.png" alt-text="Deployed synapse workspace":::

    2. Under **Getting started**, select **Open Synapse Studio**.

    :::image type="content" source="./images/open-synapse-studio.png" alt-text="'Open Synapse Studio' link beneath the 'Getting started' header":::

    3. Expand the left menu by selecting the **>>** symbol.
  
        Then:

        1. Select **Integrate**.

        :::image type="content" source="./images/select-integrate.png" alt-text="'Integrate' selected on the left-hand sidebar":::

        1. Expand the **Pipelines** header.

        :::image type="content" source="./images/expand-pipelines.png" alt-text="Pipelines header expanded in the Integrate window":::

        1. Select **SlackAnalyticsPipeline**. The **Activities** pane appears.

        :::image type="content" source="./images/select-slackanalyticspipeline.png" alt-text="SlackAnalyticsPipeline selected and Activities pane expanded":::

    4. On the **Activities** pane, select each   **Notebook** activity, then select its available **Spark pool**.
  
   :::image type="content" source="./images/update-sparkpool1.png" alt-text="Notebook activities selected":::

   :::image type="content" source="./images/update-sparkpool2.png" alt-text="Spark pool within a Notebook selected":::

    5. In the **Until** activity, select the pencil icon.

   :::image type="content" source="./images/until-activity-pencil.png" alt-text="Selected pencil icon on the 'Until' activity":::

    6. Update the **Notebook** activities by selecting the available **Spark pool**.

   :::image type="content" source="./images/update-sparkpool3.png" alt-text="Selected Spark pool within Notebook":::

    7. Select **Publish all**. When the **Publish all** window appears, select **Publish**.

   :::image type="content" source="./images/publish-all.png" alt-text="'Publish all' icon on ribbon above 'Validate,' 'Debug,' and 'Add trigger'":::

   :::image type="content" source="./images/publish.png" alt-text="'Publish' button at the bottom of the 'Publish all' window":::

## Add reference files

Refer to the following Azure Blob storage container descriptions.

|Container|Description|
|----------|------------|
|output    |Where the Synapse workspace Notebook writes the output files from the processing run. Visualizations, like the Power BI file in [Apply the output](#add-reference-files), use the output files.|
|pbixdatasets| Placeholder container. This can be deleted if it’s not used.|
reference|Contains the reference activity configuration, Slack API extraction error dates, and person-mapping data|
synworkingtmp| Hosts the Slack data output from the web API calls|

## Get and update .csv files

Before performing the steps below, you’ll need the following two reference files, which you downloaded or cloned from the VivaSolutions GitHub repository. The first one—`Activity Time Config.csv`—is pre-populated with default values. You’ll need to add values to the second one, `personmapping.csv`.

### Activity Time Config.csv

The `Activity Time Config.csv` file is pre-populated with time allocations for Slack activities. The time allocations will be used by the transformation in the pipeline of activity counts to activity time.

Schema:

|Activity| Time_in_seconds|
|--------|----------------|
|Slack_messages_posted| 22|
|Slack_reactions_added| 8|
|Slack_channel_messages_posted| 300|
|Slack_files_added| 22|
|Slack_searches| 22|

### personmapping.csv

The `personmapping.csv` file is a comma-delimited mapping of an email address (used in Viva Insights organization data) to a Hash id (person identifier). `personmapping.csv` allows these two datasets—email and Hash id—to be surfaced in a report, such as the Viva Insights Ways of Working Power BI report.

To create `personmapping.csv`, you’ll need to add in the Hash id and email addresses. Make sure the person identifier is the same in `personmapping.csv` as it is in the organization data loaded into Viva Insights. The email address is the same as what’s used in Slack.

Schema:

|Column| Description|
|------|------------|
|hashid| Person identifier that is the same as used in Viva Insights organization data|
|emailaddress| Slack email address that represents the same user in the Viva Insights organization data|

The following image shows how the Hash id allows the two datasets to be combined.

   :::image type="content" source="./images/combined-datasets-with-hashid.png" alt-text="Flow diagram beginning with 'Admin/Hash id to person id mapping' and ending with 'Analyst/Joined data sets'":::

## Upload reference files

Upload `personmapping.csv` to the **reference** container in the blob storage account created during the [infrastructure deployment](#deploy-azure-infrastructure). If you made any changes to the `Activity Time Config.csv` file, also upload it to the **reference** container.

1. Launch the Azure Portal.
2. Navigate to the **resource group*** hosting the infrastructure.
3. Select the **blob storage account***.
4. Select **Blob containers**, then select **reference**. The **Upload blob** window appears.
5. Upload the file by dragging and dropping into the **Drag and drop files here** box. You can also select **Browse for files** and select the file.

    \* specified in `parameters.json`

   :::image type="content" source="./images/blob-containers-reference.png" alt-text="Right: 'Storage browser' with 'Blob containers' expanded and 'reference' container selected. Left: 'Upload blob window'":::

## Execute the pipeline

There are two methods to execute the pipeline, depending on what you’d like to achieve. They both share the first step, which is to:

1. Open the Synapse Studio created during the [infrastructure deployment](#deploy-azure-infrastructure):
    1. Launch the Azure Portal.
    2. Navigate to the resource group hosting the infrastructure.
    3. Select the Synapse workspace in the resource group.
    4. Under **Getting started**, select **Synapse Studio**.
    5. Expand the left menu by selecting the **>>** symbol.
    6. Select **Integrate**, expand **Pipelines**, and select **SlackAnalyticsPipeline**.

2. Next, follow the steps in either option a or option b.
    1. Daily execution:

        Execute the pipeline by selecting **Debug**.
       :::image type="content" source="./images/select-debug.png" alt-text="Ribbon containing 'Validate,' 'Debug,' and 'Add trigger.' 'Debug' command selected":::

        If you select this option, you don’t need to make any changes before executing the pipeline. Option a executes the pipeline for a single day; it obtains the data from Slack for the present day minus 2. The Slack API may require a couple of days to produce the summary report.

        For reference, this setting works by having `Set startdate variable` as `empty` and `Set enddate variable` as `@formatDateTime(addDays(convertTimeZone(utcNow(),'UTC','Pacific Standard Time'),-2),'yyyy-MM-dd')`.

        The following images display this setting.

       :::image type="content" source="./images/set-startdate-variable-to-empty.png" alt-text="Top: 'Set startdate variable' box selected. Bottom: 'General,' 'Variables,' and 'User properties' tabs. 'Variables' tab selected. Name field contains 'startdate'; value field contains 'empty'":::

       :::image type="content" source="./images/set-enddate-variable.png" alt-text="Top: 'Set enddate variable' box selected. Bottom: 'General,' 'Variables,' and 'User properties' tabs. 'Variables' tab selected. Name field contains 'enddate'; value field contains '@formatDateTime...'":::

    2. Execution for historical data:

        You would typically run this execution once to get daily data from the Slack API up to the API's historical date limits (visit [admin.analytics.getFile on Slack](https://api.slack.com/methods/admin.analytics.getFile) for more information).
        1. In the pipeline details value for the Set startdate variable, change empty to a date in the YYYY-MM-DD format (e.g., 2021-11-15).
        2. Execute the pipeline by selecting **Debug**.

    > [!NOTE]
    > This execution gathers Slack data from the date entered (e.g., 2021-11-15) to the present date minus 2. Because you only need to execute the historical date once to get the data, we don’t recommend publishing this change. To revert the change, set the value back to `empty`.

## Schedule pipeline execution

You can schedule when the pipeline executes by creating a trigger.

To create a trigger, select **Integrate**, expand **Pipelines**, select **SlackAnalyticsPipeline**, then select **Trigger**.

:::image type="content" source="./images/select-trigger.png" alt-text="'Activities' pane open. 'Trigger' selected on ribbon.":::

We don't recommend setting triggers more frequently than daily. You can also set the trigger to weekly or monthly.

## Applying the output

Once you’ve joined Viva Insights data and a third-party data set—like Slack’s—you can populate reports and visualizations to see this information in new ways. One example might be modifying the [Viva Insights Ways of working template](../insights/tutorials/power-bi-collab-assess) with a new visual, as pictured below.

:::image type="content" source="./images/ways-of-working-vis.png" alt-text="Power BI report with graphs titled 'Ways of Working Assessment with Slack (inc. new view for Slack activity)'.":::
