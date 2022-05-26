---
title: Incorporate learning into your organization
description: Learn how to use Viva Learning to integrate learning and skilling opportunities into your operations.
author: daisyfell
ms.author: daisyfeller
ms.topic: article
ms.localizationpriority: medium 
search.appverid:
- MET150
ms.service: viva 
ms.subservice: viva-learning
ms.collection: 
- M365-analytics
- viva-learning
manager: pamgreen
audience: Admin
---

# Integrate Slack data with Viva Insights

You can join Viva Insights query data with collaboration data from a third-party tool. In this article, we use Slack as an example of an end-to-end pipeline for Viva Insights data and a third-party data set. For additional instructions on how to use Viva Insights, refer to the [Viva Insights training resources](/learn/browse/?products=m365%2Cviva-insights&expanded=viva).
  
## High-level architecture flow

Here is a high-level flow of the pipeline.

:::image type="content" source="./images/high-level-overview1.png" alt-text="Architecture flow beginning with Enterprise Grid Slack Web API and ending with Power BI":::

## Prerequisites

To complete the steps in this setup, confirm or do the following:

* Download the Slack synapse pipeline sample files from the [VivaSolutions GitHub repository](https://github.com/microsoft/VivaSolutions), or clone the repository to your local machine

* Have PowerShell (minimum version 5.1) and the latest [Az PowerShell Module](/powershell/azure/new-azureps-module-az)

* Have access to the Slack enterprise grid

* Complete the Slack app registration and get an oAuth token (see [Slack app registration](#slack-app-registration) to learn how to get the oAuth token)

### Slack app registration

To get the OAuth token this pipeline needs:

1. Create a [Slack application registration](https://api.slack.com/authentication/basics#creating) with the following settings:

   * Redirect URL:

        ```json
        https://app.slack.com

        https://slack.com/

        https://flow.microsoft.com/
        ```

    * User scopes:

        ```json
        admin.analytics:read
        ```

    As shown in the following App Manifest example, you can update the redirect URLs and user scope.

    ```json

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

2. Install the application (`vsappanalyticc`) to the enterprise and enable it in the workspace, as shown in the following example.
 
    :::image type="content" source="./images/install-and-enable-app.png" alt-text="vsappanalyticc install and enable":::

4. Find the User oAuth Token (`xoxp xxxxxx`) needed for authentication to the workspace under the Install App & OAuth & Permissions sidebar. You’ll input this token in the `parameters.json` file.

## Deploy Azure infrastructure

1. Update the `parameters.json` file with the configuration values that are described within the file.
2. Launch a PowerShell command prompt.
3. Navigate to where you saved the files from the GitHub download.
4. Run the following Powershell:

     `synapseworkspace_arm_deployment.ps1`.

Once the PowerShell command in step 4 is successfully executed, follow the steps in [the next section](#deploy-synapse-pipeline) to deploy the pipeline.

## Deploy Synapse pipeline

1. To maintain consistency, use the same `parameters.json` file you did in the [previous section](#deploy-azure-infrastructure).
2. Run the following PowerShell:  
`synapseworkspace_pipeline.ps1`.

1. Update the **Notebook** activities in the **SlackAnalyticsPipeline**:

    1. In the [Azure portal](https://portal.azure.com/#home), open the deployed **Synapse workspace**.

    2. Under **Getting started**, select **Open Synapse Studio**.

        :::image type="content" source="./images/open-synapse-studio.png" alt-text="'Open Synapse Studio' link beneath the 'Getting started' header":::

    3. Expand the left menu and then select **Integrate**.

        1. Expand the **Pipelines** header.

            :::image type="content" source="./images/expand-pipelines.png" alt-text="Pipelines header expanded in the Integrate window":::

        1. Select **SlackAnalyticsPipeline** to see the **Activities** pane.

            :::image type="content" source="./images/select-slackanalyticspipeline.png" alt-text="SlackAnalyticsPipeline selected and Activities pane expanded":::

    4. On the **Activities** pane, select each   **Notebook** activity and then select its available **Spark pool**.
  
       :::image type="content" source="./images/update-sparkpool1.png" alt-text="Notebook activities selected":::

       :::image type="content" source="./images/update-sparkpool2.png" alt-text="Spark pool within a Notebook selected":::

    5. In the **Until** activity, select the pencil icon.

       :::image type="content" source="./images/until-activity-pencil.png" alt-text="Selected pencil icon on the 'Until' activity":::

    6. Update the **Notebook** activities by selecting the available **Spark pool**.

       :::image type="content" source="./images/update-sparkpool3.png" alt-text="Selected Spark pool within Notebook":::

    7. Select **Publish all** > **Publish**.

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

Before performing the steps below, you’ll need the following two reference files, which you downloaded or cloned from the Viva Solutions GitHub repository. The first one—`Activity Time Config.csv`—is pre-populated with default values. You’ll need to add values to the second one, `personmapping.csv`.

### Activity Time Config.csv

The `Activity Time Config.csv` file is pre-populated with time allocations for Slack activities. The time allocations will be used by the transformation in the pipeline of activity counts to activity time.

Schema:

|Activity|Time_in_seconds|
|----|----|
|Slack_messages_posted|22|
|Slack_reactions_added| 8|
|Slack_channel_messages_posted| 300|
|Slack_files_added| 22|
|Slack_searches| 22|

### personmapping.csv

The `personmapping.csv` file is a comma-delimited mapping of an email address (used in Viva Insights organization data) to a Hash ID (person identifier). `personmapping.csv` allows these two datasets—email and Hash ID—to be surfaced in a report, such as the Viva Insights Ways of Working Power BI report.

To create `personmapping.csv`, you’ll need to add in the Hash ID and email addresses. Make sure the person identifier is the same in `personmapping.csv` as it is in the organization data loaded into Viva Insights. The email address is the same as what’s used in Slack.

Schema:

|Column| Description|
|------|------------|
|hashid| Person identifier that is the same as used in Viva Insights organization data|
|emailaddress| Slack email address that represents the same user in the Viva Insights organization data|

The following image shows how the Hash ID allows the two datasets to be combined.

   :::image type="content" source="./images/combined-datasets-with-hashid1.png" alt-text="Flow diagram beginning with 'Admin/Hash ID to person ID mapping' and ending with 'Analyst/Joined data sets'":::

## Upload reference files

Upload the `personmapping.csv` to the **reference** container in the blob storage account created during the [infrastructure deployment](#deploy-azure-infrastructure). If you made any changes to the `Activity Time Config.csv` file, also upload it to the **reference** container.

1. Launch the Azure Portal.

1. As specified in the `parameters.json` file, navigate to the **resource group** hosting the infrastructure and then select the **blob storage account**.

3. Select **Blob containers**, then select **reference**. The **Upload blob** window appears.

1. Upload the file by dragging and dropping into the **Drag and drop files here** box. You can also select **Browse for files** and select the file.

   :::image type="content" source="./images/blob-containers-reference.png" alt-text="Right: 'Storage browser' with 'Blob containers' expanded and 'reference' container selected. Left: 'Upload blob window'":::

## Execute the pipeline

You can execute the pipeline in two ways, depending on what you want to achieve. They both share the first step, which is to:

1. Open the Synapse Studio created during the [infrastructure deployment](#deploy-azure-infrastructure):
    1. Launch the Azure Portal.
    2. Navigate to the resource group hosting the infrastructure.
    3. Select the Synapse workspace in the resource group.
    4. Under **Getting started**, select **Synapse Studio**.
    5. Expand the left menu and select **Integrate**, expand **Pipelines**, and select **SlackAnalyticsPipeline**.

2. Next, follow the steps in either option a or option b.
    1. Daily execution:

        Execute the pipeline by selecting **Debug**.

       :::image type="content" source="./images/select-debug.png" alt-text="Ribbon containing 'Validate,' 'Debug,' and 'Add trigger.' 'Debug' command selected":::

        If you select this option, you don’t need to make any changes before executing the pipeline. Option a executes the pipeline for a single day; it obtains the data from Slack for the present day minus 2. The Slack API may require a couple of days to produce the summary report.

        For reference, option a's setting works by having `Set startdate variable` as `empty` and `Set enddate variable` as `@formatDateTime(addDays(convertTimeZone(utcNow(),'UTC','Pacific Standard Time'),-2),'yyyy-MM-dd')`.

        The following images show using this setting.

       :::image type="content" source="./images/set-startdate-variable-to-empty.png" alt-text="Top: 'Set startdate variable' box selected. Bottom: 'General,' 'Variables,' and 'User properties' tabs. 'Variables' tab selected. Name field contains 'startdate'; value field contains 'empty'":::

       :::image type="content" source="./images/set-enddate-variable.png" alt-text="Top: 'Set enddate variable' box selected. Bottom: 'General,' 'Variables,' and 'User properties' tabs. 'Variables' tab selected. Name field contains 'enddate'; value field contains '@formatDateTime...'":::

    2. Execution for historical data:

        You would typically run this execution a single time to get daily data from the Slack API up to the API's historical date limits (visit [admin.analytics.getFile on Slack](https://api.slack.com/methods/admin.analytics.getFile) for more information).
        1. In the pipeline details value for the Set startdate variable, change empty to a date in the YYYY-MM-DD format (2022-02-25).
        2. Execute the pipeline by selecting **Debug**.

    > [!NOTE]
    > This execution gathers Slack data from the date entered (2021-11-15) to the present date minus 2. Because you only need to execute the historical date once to get the data, we don’t recommend publishing this change. To revert the change, set the value back to `empty`.

## Schedule pipeline execution

You can schedule when the pipeline executes by creating a trigger.

To create a trigger, select **Integrate**, expand **Pipelines**, select **SlackAnalyticsPipeline**, then select **Trigger**.

:::image type="content" source="./images/select-trigger.png" alt-text="'Activities' pane open. 'Trigger' selected on ribbon.":::

We don't recommend setting triggers more frequently than daily. You can also set the trigger to weekly or monthly.

## Applying the output

Once you’ve joined Viva Insights data and a third-party data set—like Slack’s—you can populate reports and visualizations to see this information in new ways. One example might be modifying the [Viva Insights Ways of working template](/Viva/insights/tutorials/power-bi-collab-assess) with a new visual, as pictured below.

:::image type="content" source="./images/ways-of-working-vis.png" alt-text="Power BI report with graphs titled 'Ways of Working Assessment with Slack (inc. new view for Slack activity)'.":::
