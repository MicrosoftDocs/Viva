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


[test image](~/Images/WpA/Overview/architecture.png)
Workplace Analytics leverages Office 365 collaboration data to deliver powerful new insights for enterprise productivity. It provides a way for companies to understand the communication behaviors and collaboration patterns across their organization and how they influence productivity and corporate performance.

Workplace analytics analyzes header level metadata [see privacy page for more information around the data accessed](Privacy-And-Data-Access.md) from exchange online mailboxes and combines it with organizational data from line of business applications. Message Body and Attachment contents are never accessed. By combining these datasets, analysts are able to analyze a [Variety of organizational challenges](http://insights.office.com). Workplace Analytics provides a workbench to run custom analysis and pre developed aggregated dashboards.  All data is owned by the customer and stored within the O365 Compliance Boundary pursuant to the [Office 365 Compliance Framework](http://go.microsoft.com/fwlink/p/?LinkId=615657).

##Core Considerations
Workplace Analytics provide organizations with choice:
1.	Scope of mailboxes that are part of analysis.
2.	Who has access to de-identified datasets and aggregated visual dashboards
3.	Configurable options to exclude specific meeting and email metadata from analysis
Our [Privacy and data access document](Privacy-And-Data-Access.md) describes these considerations in greater detail.



[test image](~/Images/WpA/Overview/FLOW.png)  
## Data Inputs
**Collaboration Data**|**Organizational Data**
:-----:|:-----:
Header information from emails|PersonId,Organization,ManagerId,Layer,Timezone,Level,Location, EffectiveDate|
Header information from Meetings|At a minimum, the above data fields are required to be loaded for the population that are in scope for analysis. Most organizations provide this data for the entire company so analysts can understand what organizations the population in scope for analysis are For more information see our Organizational Data Documentation collaborating with.
Attachments and text in the body of emails and meetings are never used by Workplace Analytics.

## Data outputs

**Output type**|**SAMPLE**|**Role that has Access **
:-----:|:-----:|:-----:
De-Identified Row Level Data| |Analyst
Meeting Query Output| |Analyst
Meeting Query output with subject lines encrypted| |Analyst
Visual Dashboards with Minimum Aggregation Threshold | |Analyst

## Privacy Options
Privacy
Include Subject lines – Subject lines
Minimum group size
Exclusion
Private and meetings / Mails with Digital Rights Management are automatically excluded.

Customers can exclude specific metadata based on the following parameters –
Subject lines – provide keywords to exclude from analysis
Domains – exclude involving specific domains from the dataset
Email addresses - exclude content involving specific email addresses from the dataset

For More information see our Configuring Settings Page

## FAQ

### How does your Service handle data?
We are currently a Category A Office 365 service, Moving towards Category C. Please visit the [Office 365 Trust Center Top 10 security and privacy features] (https://products.office.com/en-us/business/office-365-trust-center-top-10-trust-tenets-cloud-security-and-privacy)

###Can you describe the de-identification process?
Data processed from o365 datasets will omit personal data and de-identify them when in a stored state. This process leverages a symmetric key process to ensure that supplemental organizational data can be added when needed. Keys are securely maintained by Microsoft only allowing programmatic access.

###Does Workplace Analytics Support GDPR?
Microsoft has made the commitment to be GDPR compliant. As such, Workplace Analytics has plans to implement GDPR protections in alignment with its worldwide introduction date of May 25th, 2018.

###Is WpA Compliant with Workers Councils?
There is no compliance certification for such workers councils.  Customers often have to work directly within each of their company's to ensure that Workers Councils are comfortable with the product and its use within the company.  We strongly suggest you work with your internal legal and HR teams to respectfully engage with your Workers Councils.
