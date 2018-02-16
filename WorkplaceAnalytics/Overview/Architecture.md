---
# Metadata Sample
# required metadata

title: Workplace Analytics - How it Works
description: This is a Checklist to introduce what is required to implement Workplace Analytics for your Organization
author: rodonahu
ms.author: rodonahu
ms.date: 1/19/2018
ms.topic: get-started-article
ms.prod: mya
---

# Architecture / How it Works
<CENTER>
![Architecture Diagram](~/Images/WpA/Overview/Architecture.png) </CENTER>
Workplace Analytics leverages Office 365 collaboration data to deliver powerful new insights for enterprise productivity. It provides a way for companies to understand the communication behaviors and collaboration patterns across their organization and how they influence productivity and corporate performance.

Workplace Analytics analyzes Office 365 Email and Calendar header level metadata [see privacy page for more information around the data accessed](Privacy-And-Data-Access.md) and combines it with organizational data from line of business applications.  By combining these datasets, analysts are able to provide a [Variety of organizational insights](http://insights.office.com). Workplace Analytics provides a workbench to run custom analysis and pre developed aggregated dashboards.  All data is owned by the customer and stored within the O365 Compliance Boundary pursuant to the [Office 365 Compliance Framework](http://go.microsoft.com/fwlink/p/?LinkId=615657).

##Core Considerations
By design, Workplace Analytics provide organizations with choice:
*	Our Customers Decide the Scope of mailboxes to analyze.
* Our Customers Decide who within their organization has access to de-identified datasets and aggregated visual dashboards
* Our Customers Configure options to exclude specific meeting and email metadata from analysis as directed by their Legal and HR teams

As Some

Our [Privacy and data access document](Privacy-And-Data-Access.md) describes these considerations in greater detail.



<CENTER>
![Workplace Analytics Data Flow](~/Images/WpA/Overview/Flow.png)
</CENTER>
## Data Inputs
**Collaboration Data**|**Organizational Data**
:-----:|:-----:
Header information from emails|PersonId,Organization,ManagerId, Layer,Timezone,Level,Location, EffectiveDate|
Header information from Meetings|At a minimum, the above data fields are required for the population scope that you are analyzing.

Most organizations provide this data for the entire company to understand how the mailboxes being analyzed collaborate across the entire organization

For more information see our Organizational Data Documentation

>[!Important]
>Attachments and text in the body of emails and meetings are never used by Workplace Analytics.

## Data outputs

**Output type**|**SAMPLE**|**Role that has Access**
:-----:|:-----:|:-----:
De-Identified Row Level Data|[Sample.csv](~/ExamplePersonQuery.csv)|Analyst
Meeting Query Output|[Sample.csv](~/ExampleMeetingQuery.csv)|Analyst
Meeting Query output with subject lines encrypted|[Sample.csv](~/ExampleMeetingHASHQuery.csv) |Analyst
Group Query|[Sample.csv](~/ExampleGroupQuery.csv) |Analyst
Visual Dashboards with Minimum Aggregation Threshold ||Analyst, Analyst (Limited)
Data Sources | | Administrator
## Privacy Options
* Include Subject lines – As part of a meeting query, an administrator can choose to have meeting subject lines encrypted
* Minimum group size - By default our aggregated dashboards default to a minimum group size of 5, this can be increased to a larger number as needed

### Exclusion
All exclusion occurs before metadata is processed within the Workplace Analytics Data Engine
>[!Important]
>Private and meetings / Mails with Digital Rights Management are automatically excluded.

Customers can exclude any meeting or mail metadata based on the following parameters, (which may have impact on analysis):
* Subject lines – provide keywords to exclude from analysis
* Domains – exclude involving specific domains from the dataset
* Email addresses - exclude content involving specific email addresses from the dataset

For More information see our Configuring Settings Page and Our [Privacy and data access document](Privacy-And-Data-Access.md)

## FAQ

### How does your Service handle data?
As part of the Office 365 offering, we are currently a Category A Office 365 service, Moving towards Category C. Please visit the [Office 365 Trust Center Top 10 security and privacy features] (https://products.office.com/en-us/business/office-365-trust-center-top-10-trust-tenets-cloud-security-and-privacy) and [Office 365 Compliance Framework](http://go.microsoft.com/fwlink/p/?LinkId=615657) for more information about our data handling standards.

### Can you describe the de-identification process?
Workplace Analytics processes metadata from o365 email and calendar. Email addresses are never shown in Workplace Analytics through dashboards or query results. The Workplace Data Engine de-identifies leveraging a symmetric hashing to ensure that supplemental organizational data can be added when needed. Encryption keys are securely maintained by Microsoft only allowing programmatic access.

### Does Workplace Analytics Support GDPR?
Microsoft has made the commitment to be GDPR compliant. As such, Workplace Analytics has plans to implement GDPR protections in alignment with its worldwide introduction date of May 25th, 2018.

### Is WpA Compliant with Workers Councils?
There is no compliance certification for such workers councils.  Customers often have to work directly within each of their company's to ensure that Workers Councils are comfortable with the product and its use within the company.  We strongly suggest you work with your internal legal and HR teams to respectfully engage with your Workers Councils.
