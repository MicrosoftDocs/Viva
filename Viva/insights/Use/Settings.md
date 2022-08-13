---

title: Advanced insights Controls
description: Learn about the settings in the Controls section of the advanced insights app with Microsoft Viva Insights, such as data sources, data uploads, system defaults, privacy rules, and other data analyst settings
author: madehmer
ms.author: helayne
ms.topic: article
ms.localizationpriority: medium 
ms.collection: viva-insights-advanced 
ms.service: viva 
ms.subservice: viva-insights 
search.appverid: 
- MET150 
manager: helayne
audience: Admin
---

# Controls in Advanced insights

Depending on the role you're assigned in the advanced insights app, you can use the following to configure settings about your organization in the Controls section of Advanced insights. These control settings are required for viewing and using the advanced insights app and in Microsoft Teams:

* [Data sources](#data-sources) – Admins and Analysts use these to verify that Microsoft 365 and organizational data is correctly uploaded into the advanced insights app. And Admins have access to **Upload** in Organizational data and CRM data, so they can prepare and upload organizational and customer data.
* [Leader & manager settings](#leader-and-manager-settings) – Only Admins have access and can set privacy settings and [manager settings](/viva/insights/use/manager-settings?toc=/viva/insights/use/toc.json&bc=/viva/insights/breadcrumb/toc.json) required to maintain minimum-group settings and to specify which managers and leaders get access to team insights in Microsoft Teams and in the advanced insights app.
* [Analyst settings](#analyst-settings) - Admins can access and configure [system defaults](/viva/insights/use/system-defaults?toc=/viva/insights/use/toc.json&bc=/viva/insights/breadcrumb/toc.json) and [privacy settings](/viva/insights/use/privacy-settings?toc=/viva/insights/use/toc.json&bc=/viva/insights/breadcrumb/toc.json). Analysts can access and customize meeting and attendee exclusion rules that help ensure data accuracy.

Access to one or more of the following Controls depends on what role you're assigned.

| Controls | Admin | Analyst | Analyst (Limited Access) |  
|---|---|---|---|
| Data sources | Full access| Read-only access excluding Upload | Read-only access excluding Upload |
| Leader & manager settings  | Full access | No access | No access |
| Analyst settings | Access to system defaults and privacy settings | Access to exclusions | Read-only access to exclusions|

For more details about roles, see [Assign roles](../Setup/Assign-roles-to-wpa-admins.md).

## Data sources

**Owners** – Viva Insights Admins and Advanced insights analysts, and limited analysts can view Data sources and only Admins can access Upload

* In **Data sources**, as an owner, you can see what Microsoft 365 collaboration data and organizational data was most recently uploaded into the advanced insights app. You can view average weekly meeting and email activity and measured-employee characteristics to ensure sufficient data coverage. You can also see high-level CRM data if it is uploaded and processed in Viva Insights. For details, see [Data sources](/viva/insights/use/data-sourcesv2?toc=/viva/insights/use/toc.json&bc=/viva/insights/breadcrumb/toc.json).
* In **Upload**, admins can upload the following types of data files in .csv format, UTF-8 encoded:

  * **Organizational data** - Contextual information about employees (such as, job title, level, location) from an HR or other information systems that admins upload as a data file into the advanced insights app. For details on preparing this upload file, see [Prepare organizational data](/viva/insights/setup/prepare-organizational-data?toc=/viva/insights/use/toc.json&bc=/viva/insights/breadcrumb/toc.json).
  * **CRM data** - Customer relationship management data from Microsoft Dynamics or Salesforce, which typically includes customer account information, sales records, purchasing history, service history, customer requests, and product inquiries. For details, see [CRM data in Advanced insights](/viva/insights/setup/crm-data-upload?toc=/viva/insights/use/toc.json&bc=/viva/insights/breadcrumb/toc.json).

## Leader and manager settings

**Owner** – Viva Insights admins have full access to these settings

In **Leader & manager settings**, Admins can configure the [system defaults](/viva/insights/use/system-defaults?toc=/viva/insights/use/toc.json&bc=/viva/insights/breadcrumb/toc.json), [privacy settings](/viva/insights/use/privacy-settings?toc=/viva/insights/use/toc.json&bc=/viva/insights/breadcrumb/toc.json), and [manager settings](/viva/insights/use/manager-settings?toc=/viva/insights/use/toc.json&bc=/viva/insights/breadcrumb/toc.json). For details, see [Leader & manager settings](/viva/insights/use/admin-settings?toc=/viva/insights/use/toc.json&bc=/viva/insights/breadcrumb/toc.json).

## Analyst settings

**Owners** – Viva Insights admins have full access to these settings and Analysts have full access and limited Analysts have read-only access to the exclusion settings

In **Analyst settings**, Admins can configure [system defaults](/viva/insights/use/system-defaults?toc=/viva/insights/use/toc.json&bc=/viva/insights/breadcrumb/toc.json), [privacy settings](/viva/insights/use/privacy-settings?toc=/viva/insights/use/toc.json&bc=/viva/insights/breadcrumb/toc.json), and default exclusion rules for meetings and attendees. Analysts can create and customize meeting and attendee exclusion rules that exclude meetings or attendees from analysis, such as appointments that are unrelated to work. Limited Analysts have read-only access to exclusion rules. For details, see Exclusion rules

## Related topics

* [Set up Advanced insights](/viva/insights/setup/set-up-workplace-analytics?toc=/viva/insights/use/toc.json&bc=/viva/insights/breadcrumb/toc.json)
* [Plans in Advanced insights](/viva/insights/tutorials/solutionsv2-intro?toc=/viva/insights/use/toc.json&bc=/viva/insights/breadcrumb/toc.json)
