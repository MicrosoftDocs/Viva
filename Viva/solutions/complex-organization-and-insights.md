---

title: Complex organization and insights
description: Learn about a complex organization and its associated Viva insights
author: v-smandalika
ms.author: v-smandalika
ms.topic: article
search.appverid:
- MET150
ms.prod: wpa
ms.collection: M365-analytics
manager: dansimp
audience: Admin
---

# What is a complex organization?

Complex organizations are Microsoft Azure Active Directory (AAD) customers who use multiple Office365 tenants. There are primarily two reasons for this type of configuration:

- [Mergers and acquisitions](#mergers-and-acquisitions)
- [Conglomerates](#conglomerates)

## Mergers and acquisitions

A business merger between two companies resulting in an organization made up with multiple Office365 tenants and separate AADs. The tenants either choose to remain separate and collaborate together or merge into a single tenant (For example, M&A: Bayer & Monsanto).

## Conglomerates

A conglomerate is a corporation made up of several independent subsidiaries. The subsidiaries are tenants that have separate AAD and will collaborate together and remain separate (For example, The Walt Disney Company, Honeywell).

## What is the purpose of this article?

Complex organizations represent challenges for deriving insights. Often, the task falls to analyzing each of the tenants that make up the complex organization independently and comparing them manually. The process can be highly manual in nature. This article provides a growing number of examples that explain how to overcome manual processes. These examples also include those that lead to output visualizations.

## Complex organizations and Viva insights

Microsoft Viva insights provide information and research-based behavioral insights into:

- the tasks an organization has to execute to get work done. For example:
    - how to enhance organizational agility
    - how to boost employee engagement
    - how to improve agility
    - how to foster innovation

Advanced analytics for organizations comprised of multiple Viva Insights tenants can be enabled by:

- combining the data in a central location, and
- combining that data with additional data sources.

A few starter use cases that would be enabled by this data combination strategy are:

- Identify collaboration patterns between two distinct business groups (tenants)
- Distinguish collaboration patterns between cross business groups (tenants) VS true external interactions.
- Data combined from Viva Insights with external sources to address headcount planning, employee well-being, permanent remote work, inclusion and diversity, and so on.

There are different methods and data storage locations possible as storage accounts, sql databases and synapse to name a few. An example leveraging Azure Data Factory, Viva Insights organizational data, and azure blob storage will be described below using the [Business Continuity](../insights/Tutorials/power-bi-bc.md) use case.

## Requirements

The following requirements to be fulfilled, prior to continuing with its analytical process using Microsoft Viva Insights:

### Organizational data

Organizational data is a key requirement for Viva Insights and further advanced analysis. It can be used to enable joins with additional data sources (as sales data), and more granular person attribute analysis, to name a couple.

General required organizational data is further described in [Viva Insights prepare organizational data](../insights/Use/organizational-data.md). For an insight into advanced analysis, the following example can be uploaded into Viva Insights.


|Attribute Name  |Attribute Description  |
|---------|---------|
|EffectiveDate     |      Date for which the given attribute value applies for the employee. The attribute applies until another record for the same attribute with a different effective date is specified.   |
|PersonId    | Unique identifier for the employee record. This identifier can be the employee's primary SMTP address or email alias. It must be in a simplified format that contains no spaces. For example,  the format **person.name@xyz.com** is allowed; however, the format **<Name, Person> (person.name@xyz.com)** is not allowed.     |
|ManagerId    |  Unique identifier for the employee’s manager, which is needed to correctly calculate metrics for time spent with managers and their direct reports.
This identifier can be the manager's primary SMTP address or email alias. It must be in a simplified format that contains no spaces. For example,  the format **person.name@xyz.com** is allowed; however, the format **<Name, Person> (person.name@xyz.com)** is not allowed.      |
|Organization    |    The internal organization that the employee belongs to. An employee’s organization will be specific to the individual needs and could be identified by the leader of the organization, or by another naming convention. This data is needed to correctly calculate metrics for redundancy and insularity.     |
|FunctionType  |    The job function that the employee performs. This job function is specific to the organization. This data is used to filter and group reports, and for grouping of data in [Explore the stats](../insights/Use/explore-intro.md) features.     |
|LevelDesignation    |      The employee’s level, which is represented as a string. This level is specific to the organization and can represent an employee’s experience or management level, or seniority within the organization. This data is needed to correctly calculate metrics for redundancy and insularity.   |
|Layer     |      The place where the employee is within the organizational hierarchy. Layer is represented as an integer and expressed as the distance the employee is from the top leader of the organization. For example, the CEO is at layer 0. This data is used to filter and group reports, and for grouping of data in [Explore the stats](../insights/Use/explore-intro.md) features.   |
|SupervisorIndicator     |    The attribute used to view the habits of people managers or influencers in the organization in Power BI visualizations. This attribute powers the Overview table, the Generated Workload charts that are generated when you use a template that requires it.
This attribute indicates the manager status of each employee as IC (individual contributor), Mngr (manager), or Mngr+ (manager of managers); however, if a different nomenclature is used in the file, you must update the Power BI chart filters accordingly. If you include SupervisorIndicator, you must also include the values **IC**, **Mngr**, or **Mngr+** in the organizational data. |
|TimeZone     |    Time zone in which the employee works. This attribute must be one of the time zones in [Time zones for Workplace Analytics](../insights/Use/Timezones-for-workplace-analytics.md). If no time zone is mapped to for an employee, the system will use the default time zone, which is Pacific Standard Time.     |
|TenantInd     |    Unique name for the Tenant. For example, TenantA, TenantB, TenantC, and so on.     |
|Location   |     Geographic region or other location detail.    |
|HashId    |      Unique Hashed identifier for the employee. This attribute enables further advanced analysis on the Viva insights query results.   |

**Example:  Sample of an organizational data file**


### Viva Insights Business Continuity dashboard

Set up the [Business Continuity](../insights/Tutorials/power-bi-bc.md) dashboard for your tenant with the following modification:

-	In the **Organizational data** section of the **Business Continuity and Hourly Collaboration** report, add **HashId** and **TenantInd** columns to the list. Additional columns can be added for this report if needed, for analysis.

### Azure

For Adhoc with oData and Automated Data Pipeline, you will need:

- An application registration
- Registered application's secret for each tenant from which you are planning to pull Viva Insights query results.

You will also need an azure subscription to host the data from the two tenants.

1. To register an application, accomplish Steps 1 to 5 in the [Automate Exports](automate-exports.md) for each tenant.
    1. To obtain a secret for the registered application, select **Certificates & secrets** from your newly registered application in Azure Active Directory.
        1. For Key authentication, select **New client** secret and in **Add a client** secret, enter a description, select when it expires, and then click **Add**. In **Client** secrets, select the new secret value, and then click the **Copy** icon to copy the value.
    2. Make a note of the Application ID and secret that are created for each tenant.
2. In the case of Microsoft Azure subscription, perform the following steps:
    1. Deploy custom deployment from arm template.
    1. Configure the deployed resources.

The template creates the following resources: 
- Resource group
- Key vault
- Storage Account
- Azure data factory using managed identity

(The example of a privilege that allows for creation of the above resources is Azure Administrator.)

## Solution option samples

Using the case for the need to pull query data from Viva insights from multiple tenants, there are a few sample solutions as described below:

### Adhoc manual approach

Viva Insights queries can be executed and the output can be downloaded and further analyzed offline. 
This sample will be using the **Business Continuity** report listed in the **Requirements** section. 
There are no other pipeline setup requirements. To visualize it in the sample Business Continuity PowerBi, click here.

### Adhoc using oData approach

Viva Insights queries can be scheduled to auto refresh and accessed via oData links to provide further analysis or to be visualized in PowerBi reports. 
This sample will be using the **Business Continuity** report listed in the **Requirements** section.
There are no other pipeline setup requirements. To visualize it in the sample Business Continuity PowerBi, click here.

### Automated data pipeline

Viva Insights queries can be scheduled to auto refresh and downloaded to a central data store location for further analysis or visualizations. The solution sample uses Azure blob storage. 
This sample will be using the **Business Continuity** report listed in the **Requirements** section.
The setup details are available here.

## Solution Sample Pipeline Setup

### Automated data pipeline

1. Deploy the arm template for Data Factory creation for MultiTenant by performing the following steps:

    1. Launch the azure portal for the subscription that you will use.
    1. Search for and open **Deploy from a custom template**.
    1. Click **Build your own template** in the editor.
    1. Click **Load file** , and select the **DataFactory_oData_arm_template.json** file (a download location needed for this>.
    1. Click **Save**.
    1. Fill and select the highlighted items. 
    1. Click the **Review + create** tab, and click **Create**.

1. Grant access to the Data Factory Managed Service Identity to the key vault and the storage account by performing the following steps:
    1. Obtain the Managed Service Identity for the Data Factory created earlier by select Properties from the left pane and copying the **Managed Identity Application ID** value.
    1. Add Access Policies to the Key Vault, Open the Key Vault created earlier.
        1. Select **Access policies** from the left pane.
        2. Select **+ Add access policy** and add your own account with the following options:
            1. **Configure from template: Key, Secret, & Certificate Management**
            1. **Select principal**
                1. Search for using your Id, select the result.
        3. Click **Add**.
        4. Click **Save**
1. Grant Storage Account permissions to the Data Factory Managed Service Identity.
    1. Open the Storage Account created earlier, Select Access Control (IAM).
    1. 



















