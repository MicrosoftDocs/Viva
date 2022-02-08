---

title: Microsoft Viva Insights Data Lake Solution overview
description: Learn how to set up and use the Viva Insights Data Lake Solution
author: madehmer
ms.author: helayne
ms.topic: article
ms.localizationpriority: medium 
ms.collection: viva-insights-advanced
ms.service: viva 
ms.subservice: viva-insights 
search.appverid: 
- MET150 
manager: scott.ruble
audience: Admin
---

# Viva Insights Data Lake Solution

This walkthrough is an end-to-end data lake solution to extract, transform, and load (ETL) Microsoft Viva Insights data into a database and then report it through Power BI as an end-user platform. The key features of this workload:

- Automated pipeline to avoid manual interaction with the Viva Insights query builder platform.
- Instructions and guidelines on managing and loading Viva Insights historical data.
- Utilizing an open source scripting language (Spark) to enable reusability of the script in other platforms and tools.
- Leveraging Azure Synapse for a seamless, easy-to-manage workspace to implement the solution.

## Example use cases

Several scenarios can benefit from this workload through layering an advanced ETL pipeline on top of Viva Insights:

- Two native out-of-the-box options are available with Viva Insights’ queries:

  - Download the query results file manually.
  - Use the OData links with a secondary tool like Microsoft Power BI to connect through the OData links. To avoid manual downloads and using other unnecessary tools, a program (script) is required to load and ingest the data.

  Many use cases for advanced analytics require automatic processing of data in production environments within existing data warehouses. You can use this solution to combine Viva Insights data with other data sources for a more comprehensive view of the organization.

- Business intelligence (BI) solutions with Power BI or other tools might not scale properly through an OData link with Viva Insights. With this solution, you can use a combination of a SQL Database and Power BI (or any other tool connecting though OData) to scale up.
- The Viva Insights queries are limited by the set time periods in the app. Having an additional work stream to ingest and store the historical data over time might be necessary for some organizations and some scenarios.

## Architecture

- [Azure Synapse Analytics](https://docs.microsoft.com//azure/architecture/example-scenario/data/small-medium-data-warehouse) is an analytics service that combines data integration, enterprise data warehousing, and big data analytics. This solution includes the following components:

  - An [Azure Synapse workspace](https://docs.microsoft.com/azure/synapse-analytics/quickstart-create-workspace) - Promotes collaboration between data engineers, data scientists, data analysts, and BI professionals.
  - [Azure Synapse pipelines](https://docs.microsoft.com/azure/synapse-analytics/get-started-pipelines) - Orchestrate and ingest data into SQL Database and Data Lake Storage.
  - [Azure Synapse SQL pools](https://docs.microsoft.com/azure/synapse-analytics/get-started-analyze-sql-on-demand) - Run queries and analytics at massive scale once data is stored in relational tables with columnar storage.
  - [Azure Synapse serverless Apache Spark pools](https://docs.microsoft.com/azure/synapse-analytics/get-started-analyze-spark) - For code-first explorations in Data Lake Storage with Spark languages, such as Spark SQL, PySpark, and Scala.

The following shows how these components are used within this solution's architecture.

![Viva Insights Data Lake solution architecture.](./images/vidl-architecture.png)

## Alternatives

- Use [Azure Data Factory](https://azure.microsoft.com/services/data-factory) for data integration instead of Azure Synapse pipelines. The choice depends on several factors:

  - [Azure Synapse pipelines](https://docs.microsoft.com/azure/synapse-analytics/get-started-pipelines) keep the solution design simpler and enable collaboration inside a single Azure Synapse workspace. However, Azure Synapse pipelines do not support rehosting the SSIS packages, which is supported in Azure Data Factory.
  - [Synapse Monitor Hub](https://docs.microsoft.com/azure/synapse-analytics/get-started-monitor) monitors Azure Synapse pipelines, while [Azure Monitor](https://azure.microsoft.com/services/monitor) can monitor Data Factory.

  For more information and a feature comparison between Azure Synapse pipelines and Data Factory, see [Data integration in Azure Synapse Analytics versus Azure Data Factory](https://docs.microsoft.com/eazure/synapse-analytics/data-integration/concepts-data-factory-differences).

- Use SQL Database instead of [Synapse Analytics dedicated SQL pools](https://docs.microsoft.com/azure/synapse-analytics/sql-data-warehouse/sql-data-warehouse-overview-what-is) for storing enterprise data.
- Use Databricks instead of Synapse Spark Pool to transform the data. The link for Databricks notebooks is also available in the [GitHub repository](https://github.com/microsoft/VivaSolutions/tree/main/Sample%20Solutions/Data%20Lake/Viva%20Insights).

## Availability and pricing

SQL Database (standalone or as a Synapse dedicated SQL pool) is a PaaS service that can meet your high availability (HA) and disaster recovery (DR) requirements. For guidance, see [High availability for Azure SQL Database and SQL Managed Instance](https://docs.microsoft.com/azure/azure-sql/database/high-availability-sla).

You can use the [Azure Pricing Calculator](https://azure.microsoft.com/pricing/calculator/) to get an estimate for this workflow. You can use Azure Synapse to scale your compute and storage levels independently. Compute resources are charged by the hour, which you can scale or pause on demand. Because storage resources are billed by the terabyte, your costs will increase as you ingest more data.

- [SQL Database](https://azure.microsoft.com/pricing/details/azure-sql-database/single) pricing depends on the selected Compute and Service tiers, and the number of vCores and Database Transaction Units (DTUs).
- [Data Lake Storage](https://azure.microsoft.com/pricing/details/storage/data-lake/) pricing depends on the amount of data you store and how often you use the data.
- [Azure Synapse pipelines](https://azure.microsoft.com/pricing/details/synapse-analytics/) pricing depends on the number of data pipeline activities, integration runtime hours, data flow cluster size, and execution and operation charges. Pipeline costs increase with additional data sources and amounts of data processed.
- [Azure Synapse Spark pool](https://azure.microsoft.com/pricing/details/synapse-analytics/) pricing depends on node size, number of instances, and uptime.

## Prerequisites

- [Workplace Analytics Analyst](https://docs.microsoft.com/viva/insights/setup/assign-user-roles) – Must be assigned a Viva Insights license and the Analyst role for Workplace Analytics with Viva Insights and know how to use the Query designer.
- [Microsoft Azure subscription](https://azure.microsoft.com/free/) – If you don't have an Azure subscription, create a free account now. You’ll be using Azure Active Directory, OData connector, and Data Factory for this setup.
- [Azure data store](https://docs.microsoft.com/azure/data-share/supported-data-stores) – Your data store must be supported by the [OData connector](https://docs.microsoft.com/azure/data-factory/connector-odata).
- [Azure admin](https://docs.microsoft.com/azure/data-factory/concepts-roles-permissions) – You need Azure admin privileges to create and register the app in Azure. You also need to ask the Azure global admin to grant you permissions in Azure Data Factory to connect your new app to the Azure data store.

## Setup overview

The following steps walk you through how to implement the Viva Insights Synapse pipeline in the architecture. The focus of this workflow will be on transferring and maintain Viva Insights Person and Meetings standard queries in the Azure Synapse Dedicated SQL DB and maintaining the workflow over time.
Use the following steps in conjunction with the Azure documentation to complete this setup.

1. [Update your organizational data](#update-your-organizational-data)
2. [Create a query](#create-a-query)
3. [Prepare the Synapse Workspace](#prepare-the-synapse-workspace)
4. [Set up the Viva Insights Synapse Pipeline]()

## Update your organizational data

The pipeline requires the following data attributes within the organizational (HR) data that’s uploaded and used in Viva Insights:

- **PersonId**, **ManagerId**, and **Organization** - For details, see [Attribute reference](https://docs.microsoft.com/viva/insights/setup/prepare-organizational-data#attribute-reference).
- **LevelDesignation** - Defines the reporting hierarchy and is used in a lot of workplace analysis.
- **EmployeeId** - Secondary unique identifier that’s used a key for joining Viva Insights data with other data sources.

Many advanced use cases can use this workflow to export the Viva Insights query output into a database to join it with other data sources for a comprehensive analysis of organizational collaboration patterns.

>[!Note]
>If you prefer not to use LevelDesignation and EmployeeId, you can change the PySpark script and the database table creation script to remove these attributes.

**Recommendation**: To protect employee privacy, don’t use an existing EmployeeId in your organizational data file. Instead, use a modified, mapped, or hashed version of EmployeeId and only make the reverse mapping available to a limited number of Workplace Analytics or Viva Insights Admins.

After your organizational data is updated based on these instructions, do the following to create a query in Workplace Analytics for Viva Insights.

## Create a query

Within your Viva Insights workspace, follow the instructions in the [Query designer](https://docs.microsoft.com/viva/insights/tutorials/query-designer) to create a standard person query and a standard meeting query with the following configurations.

- Select “Standard Meeting Query” and “standard Person Query” when creating your custom queries.
- In the “select filters” section, select your target group (all employees, active, etc)
- Modify your “organizational data” section to include all attributes. The Pyspark script will only select fields listed below in addition to the secondary EmployeeId to insert into the database. With including all attributes, you have the opportunity to easily modify the workflow to add other attributes in future.

### Person attributes

The following attributes are required when creating the person query for this solution.
&nbsp; | &nbsp; | &nbsp;
-------|--------|------
PersonId | Date | Organization
LevelDesignation | ManagerId | Workweek_span
Meetings_with_skip_level | Meeting_hours_with_skip_level | Generated_workload_email_hours
Generated_workload_email_recipients | Generated_workload_instant_messages_hours | Generated_workload_instant_messages_recipients
Generated_reactions_to_posts | Generated_replies_to_posts | Generated_workload_call_hours
Generated_workload_call_participants | Generated_workload_calls_organized | External_network_size
Internal_network_size | Networking_outside_company | Networking_outside_organization
Multitasking_hours | After_hours_meeting_hours | Open_1_hour_block
Open_2_hour_blocks | Total_focus_hours | Low_quality_meeting_hours
Meetings | Meeting_hours | Conflicting_meeting_hours
Multitasking_meeting_hours | Redundant_meeting_hours__lower_level_ | Redundant_meeting_hours__organizational_
Time_in_self_organized_meetings | Meeting_hours_during_working_hours | Generated_workload_meeting_attendees
Generated_workload_meeting_hours | Generated_workload_meetings_organized | Manager_coaching_hours_1_on_1
Meetings_with_manager | Meeting_hours_with_manager | Meetings_with_manager_1_on_1
Meeting_hours_with_manager_1_on_1 | After_hours_instant_messages | Instant_messages_sent
Instant_Message_hours | Working_hours_instant_messages | Emails_sent
Email_hours | Uninterrupted_focus_hours | After_hours_collaboration_hours
Collaboration_hours_external | Collaboration_hours | Working_hours_collaboration_hours
After_hours_email_hours | Working_hours_email_hours | Channels_with_active_engagement
Teams_with_active_engagement | After_hours_channel_message_hours | Channel_message_hours
Channel_messages_sent | Channel_reactions | Channel_visits
Working_hours_channel_message_hours | After_hours_in_calls | Total_calls
Call_hours | Working_hours_in_calls | IsInternal
IsActive | WorkingStartTimeSetInOutlook | WorkingEndTimeSetInOutlook
WorkingDaysSetInOutlook | |

### Meeting attributes

The following attributes are required when creating the meeting query for this solution.
&nbsp; | &nbsp; | &nbsp;
-------|--------|------
MeetingId | StartTimestampUTC | EndTimestampUTC
Organizer_PersonId | Organizer_Organization | Organizer_LevelDesignation
Organizer_IsInternal | Attendees | Attendees_with_conflicting_meetings
Invitees | Emails_sent_during_meetings | Instant_messages_sent_during_meetings
Attendees_multitasking | Attendee_meeting_hours | Redundant_attendees
Total_meeting_cost | Total_redundant_hours | IsCancelled
DurationHours | IsRecurring | Subject
TotalAccept | TotalNoResponse | TotalDecline
TotalNoEmailsDuringMeeting | TotalNoDoubleBooked | TotalNoAttendees
MeetingResources | BusinessProcesses |

Do the steps in the next section to set the “Time Period, Group by, and Auto-refresh” fields.

### Managing historical data

A production workload requires an initial historical data upload that's set up for weekly or monthly updates. You can use this pipeline for this purpose in one of two ways:

**Option 1**: Create two copies of this pipeline within your Synapse workspace with two sets of queries. For the first set of queries (person and meeting queries), select the following options to load the historical data. Then use the OData links for these queries in your pipeline to copy the data into Blob storage and inserting into database. This pipeline only needs to be triggered one time:

- **Time period** - Select your preferred historical data period (one year).
- **Group by** - Select **Week** for the Person query.
- **Auto-refresh** - Don’t select it.

The second set of queries with the following configuration prepares the weekly or monthly updates. Use the OData links for these queries in your pipeline to copy the data into the Blob Storage and insert into the database on a schedule. Based on your use case requirement, you can do weekly or monthly updates. This pipeline must be triggered on a schedule to load the data updates. With every run, the pipeline reads the data from the OData link, copies it into the Blob Storage, checks the database for the latest available data, and only upserts the latest records based on the existing database records.

- **Time period** - Select the minimum available or your preferred time frame. **Note**: The “Last one month” is the smallest time period available in the product. This works great for the monthly scheduled pipeline (database update). For a weekly scheduled pipeline, the PySpark script will extract “Last week's” data for upserts.
- **Group by** - (for Person Query): Week (for a weekly scheduled pipeline) or “Month” (for the monthly one)
- **Auto-refresh** - Select it.

>[!Note]
>Query results are refreshed when new data is available that can be when your weekly data is being processed and published by Viva Insights or when there is a new organization file upload or update.
Usually, Viva Insights weekly updates are processed on weekends and for some, can take until Monday afternoon to finish. To allow for this possibility, the Synapse pipeline provided in these instructions can be scheduled for Tuesday.

**Option 2**: Use one pipeline and one set of queries. Set up the queries for the historical data load (as described in Option 1) to trigger the pipeline. However, after the triggered pipeline successfully runs, change the configuration to the second set (as described in Option 1), and schedule the pipeline to run based on your preferred settings (weekly or monthly).

## Prepare the Synapse Workspace

- Follow steps in Synapse documentation to create a Synapse workspace and connect it to a new or existing Storage account. When creating the workspace, keep the SQL Server admin credentials.
- Follow the steps in documentation to create a Synapse Dedicated SQL Pool and a Spark Pool.

## Set up the Viva Insights Synapse Pipeline

The following steps walk you through creation of the pipeline in Azure Synapse Analytics. Use the following steps in conjunction with the Azure documentation to complete this setup.

1. Make sure you have followed steps in Viva Insights Query Preparation to setup a Person query and a Meeting query in your Viva Insights platform.
2. In the Azure Synapse resource in portal, select Open Synapse Studio to open the Azure Synapse Workspace.
 Note Keep all your browser windows open because you must switch between them to complete the following steps.
3. In Azure Synapse Studio, select Integrate, and then add a Pipeline.
4. Name your pipeline and in **Parameters**, add the following (use +New) with their initial default values:

   - **StorageAccountName** - This is the name of the storage account linked to Synapse for this workflow. You should create a container with this name manually.
   - **VivaInsightsDataFileSystem** - This is the name of Storage Account Container within StorageAccountName to copy the Viva Insights query results into. (“vivainsights” for this walkthrough)
   - **PersonQueryDatasetFolder** - This is the directory used to write the Person query results within the VivaInsightsDataFileSystem container. (“personQuery” in this walkthrough)
   - **MeetingQueryDatasetFolder** - This is the directory used to write the Meeting query results within the VivaInsightsDataFileSystem container. (“meetingQuery” in this walkthrough)
   - **PersonQueryMetaData** - Metadata of the Person query is “Persons”.
   - **MeetingQueryMetaData** - Metadata of the Meeting query is “Meetings”.

>[!Note]
>For details on finding the metadata value for Viva Insights queries, copy the ODataOData query link from Workplace Analytics > Analyze > Query designer > Results, and open the query link in a new browser window. Then search for metadata to find the entity name, which is shown after $metadata#. For example, the following shows the entity set name as **Persons**

   - **SQLServerEndpoint** - Open Synapse Manage tab from your left vertical menu, in the Analytics Pool -> SQL Pools click on your SQL pool used in this pipeline. In the Properties window Workspace SQL Endpoint is the correct value for the hostname.

     - **DBName** - This is name of the SQL Pool selected to be used in this pipeline
     - **DBUser** - Admin user or any other user with permission to write into DB can be used.
     - **DBPass** - Password for the selected user.
     - **DBPort** - By default port 1433 is used but the value can be changed based on the SQL DB configuration.

5. Follow steps 1 to 5 in “To set up with Azure Synapse Analytics” to register an application and grant permissions. Record the Application (client) ID, Directory (tenant) ID.
6. In the Pipeline activities menu, select Move and Transform, and then drag a Copy data into your pipeline workspace.
7. In General, enter a name (“Person Query Copy” in this walkthrough)
8. In Source, add a new Source dataset. 
9. In New Integration Dataset, enter OData, and then select OData.
10. In Set Properties, enter a name and create a new linked service.
11. In New linked service (OData), enter a name and description for the query data you’re linking to.
12. In Connect via integration runtime, select AutoResolveIntegrationRuntime.
13. In Viva Insights in Workplace Analytics, select Analyze > Query designer > Results, and then copy the OData link for the person query data you want to connect to Azure.
14. In Azure Synapse New linked Service URL, paste the query OData link that you copied in the previous step.
15. In Authentication type, select either AAD service principal with Key or AAD service principal with Cert. Keep New linked service (OData) open in a separate browser window. For details about these options, see Use Azure Key Vault secrets in pipeline activities.
16. In AAD resource, enter https://workplaceanalytics.office.com.
17. If not set by default, paste the tenant id recorded in step 5 in Azure Synapse Studio > New linked service (OData) > Tenant. (if not recorded, In Active Directory, select Overview for the new app, and then copy the Directory (tenant) ID.)
18. Paste the Application (Client) ID recorded in step 5 in Azure Synapse Studio > New linked service (OData) > Service principal ID (if not recorded, In Active Directory, select Overview for the new app, and then copy the Application (client) ID.). For details, see Linked service properties.
19. In Azure Active Directory > your newly registered analytics app, select Certificates & secrets, and then do one of the following.

    - For Key authentication, select New client secret, and then in Add a client secret, enter a description, select when it expires, and then select Add. In Client secrets, select the new secret, and then select the Copy icon to copy it.
    - For Certificate authentication (preferred for higher security), select a certificate and copy it.

20. In Azure Synapse studio, do the following for the applicable authentication type:
    - For Service principal key, paste the new client secret copied in the previous step.
    - For Azure key vault, copy and paste the certificate and the other required information. See Set and retrieve a secret from Azure Key Vault for details.

21. Select Test connection to test the OData linked service.
22. After you see Connection successful, select Create.
23. In Set Properties > Linked service for the new OData linked service, select the new linked service you just created in the previous steps. In Path, ignore the “Failed” status and click OK.
24. In Source, Open the source dataset created. 
25. In the opened OData Resource, in Parameters, add PersonQueryMetaData
26. Go back to the Connection tab, click on the empty box of the Path and use the Add Dynamic Content to set the Path to dynamic value of “@dataset().PersonQueryMetaData”
27. Preview data to make sure you  have the correct setting. (note: if asked, input the PersonQueryMetaData parameter value manually (default is “Persons” for Person query or “Meetings” for meeting query. For other queries refer to the note in step 4 above.)
28. Go back to the Person Query Copy activity -> Source -> Dataset Properties, click on the empty value box of the parameter and use the Add Dynamic Content to set the parameter value.
29. For Person Query Copy activity, select the Sink tab and add a new Sink dataset.
30. Select Azure Data Lake Storage Gen2, continue with DelimitedText as format and Continue
31. In Set properties, select your linked storage account, which will be used as the write destination of the Viva Insights query result, in Linked Service. Leave the File Path as is.

    >[!Note]
    >When creating the Synapse Workspace, it links to a default storage account. To link to a different storage account (new or existing storage), follow the steps in Synapse.

32. In **Sink**, open the created Sync dataset.
33. In **Parameters**, add the **PersonQueryDatasetFolder**, **PipelineID**, and **VivaInsightsDataFileSystem** parameters.
34. In **Connection**, select the **File Path** > **Directory** > **Add Dynamic Content** and create the following path:

    '@concat(dataset().VivaInsightsDataFileSystem,'/',dataset().PipelineID,'/raw/',dataset().PersonQueryDatasetFolder)'

35. Keep the **PersonQuerySink** tab open and go back to the pipeline tab, Person Query Copy activity, under Sink -> Dataset Properties. Use the Add Dynamic Content for each parameter to set the values accordingly.

    >[!Note]
    >PipelineID can be found under system variables Pipeline Run ID.

36. Publish the pipeline to make sure there is no error.
37. Repeat steps 6 to 36, modify the names and parameter names to create another copy data activity for meeting query called Meeting Query Copy in this walkthrough. Changes to parameter names are like PersonQueryDatasetFolder to MeetingQueryDatasetFolder or PersonQueryMetaData to MeetingQueryMetaData.
38. Once step 37 is completed, publish the pipeline to make sure there is no error in the configuration, At this point, your pipeline view should be like the following.
39. Download the two Synapes Notebook ipynb files from this Github repository called vivainsights_person and vivainsights_meeting.
40. From Synapse Develop menu, select the Notebook ellipsis (...) and import the two downloaded ipynb files.
41. Open your Pipeline and from the Pipeline Activities menu, under Synapse, add a Notebook called Viva Insights Person Transformation and connect it to the Person Query Copy.
42. In **Settings** for the Notebook, select the imported vivainsights_person notebook, add the following base parameters and use the Add dynamic content to initialize them with the pre-defined Pipeline parameters.

    - VivaInsightsDataFileSystem
    - StorageAccountName
    - PersonQueryDatasetFolder
    - PipelineId
    - SecondaryEmployeeId
    - SQLServerEndpoint
    - DBName
    - DBUser
    - DBPass
    - DBPort

    The following shows an example of what your pipeline should look like:

       ![Pipeline example.](./images/pipeline-example.png)

43. Repeat steps 41 and 42 to add another notebook called Viva Insights Meeting Transformation and connect it to Meeting Query Copy activity. For this notebook, add the MeetingQueryDatasetFolder instead of PersonQueryDatasetFolder.
44. Your Pipeline now looks like this.
45. Publish the pipeline to make sure there is no error.
46. In the Github repository, download the two SQL scripts to create the viva_insights_meeting and viva_insights_person tables.
47. In **Develop**, select the SQL Script **ellipsis** (...) icon and import the two SQL scripts. Open each, select your SQL server in Connect To and your database in Use Database and run.

## Consume data for analytics

After the Viva Insights query data is included in the SQL Database, you can now add an analytics layer. Almost all platforms, applications, and scripting/programming languages have connectors for SQL Databases. The following is sample script for Python and R.

Follow these steps to connect your Power BI desktop to the SQL Database:

1. Sign in to your Power BI with the same credentials that has access to the Synapse and SQL database.
2. Select **Get Data** > **Database** > **SQL Server Database**, and then select **Connect**.
3. Enter the applicable server and database values, and then select your preferred data connectivity mode.

   >[!Note]
   >Open the **Synapse Manage** tab, and then in **Analytics Pool** > **SQL Pools**, select the SQL pool for this pipeline. In the **Properties** window, confirm **Workspace SQL Endpoint** is the correct value for SQL Database.

4. Select the tables, and then load them.

## Additional external data sources

Many advanced analytics use cases require the joining of multiple data sources for a comprehensive view of workplace interactions and collaboration patterns. The secondary **EmployeeId** for this pipeline is the key that's added to Viva Insight data to enable dataset joins. 

You can use Synapse activities and capabilities to load the additional data source into the SQL database and join via a python script or BI tools like Power BI for analysis.

>[!Note]
>PersonId in Viva Insights data is, by default, a hashed and de-identified employee identifier which cannot be reverse mapped and so cannot be used for the join purpose.
