---
title: Import organizational data (subsequent import)
description: Learn how to refresh your data in the Viva Insights advanced insights app through a connection
author: lilyolason
ms.author: v-lilyolason
ms.topic: article
ms.localizationpriority: medium
ms.collection: viva-insights-advanced
ms.service: viva 
ms.subservice: viva-insights
manager: anirudhbajaj
audience: Admin
---

# Import organizational data (subsequent import)

This article talks about refreshing data that's already been imported to Viva Insights.

>[!Important]
>Only use the following steps if this is ***not*** the first time you’re importing organizational data. If this is your first import, refer to [Import organizational data (first import)](import-org-data-subsequent.md) to set up a connection and import data to Viva Insights.

## Full refresh

When you perform a full refresh, you’re replacing all your organization’s data in Viva Insights. During a full refresh, you send *every* value for *every* field to Viva Insights—that is, you’re removing and replacing all the data that currently lives in Viva Insights, except perhaps fields you want to delete. We talk about deleting data in the next section.

### Deleting fields with full refreshes

You can use a full refresh to delete fields. To do so, refresh your data and select all fields except the fields you want to delete. Because a full refresh replaces existing data, you’ll end up with every field except the ones you left out during the import.

## Incremental refresh

Perform an incremental refresh when you only want to add some new information to organizational data that already lives in Viva Insights. Here’s what you can do with an incremental refresh:

* Add new employees
* Add new attributes for existing employees
* Add new attributes for new employees
* Edit existing employees’ attributes

Let’s use a couple of examples:

Say you wanted to add five new hires to your organizational data. During the import, you’d only select those five rows that contained new data. After the import finishes, the only change you’d notice is five new rows and their values.

Or maybe you want to add a new attribute, **DeskNumber**, for all existing employees. When you go to import your data, you’d only select the **DeskNumber** field. After the import finishes, you’d find the same data that was there before, with the exception of a new column for each employee, **DeskNumber**.
