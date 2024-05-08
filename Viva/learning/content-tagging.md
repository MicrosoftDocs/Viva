---
title: Content tagging and content metadata export  
ms.author: bhaswatic
author: bhaswatic
manager: elizapo
ms.reviewer: chrisarnoldmsft
ms.date: 12/08/2023
audience: admin
ms.topic: article
ms.service: viva-learning
search.appverid: MET150
ms.collection:
  - enabler-strategic
  - m365initiative-viva-learning
  - Tier1
ms.localizationpriority: medium
description: Learn how you can enrich content metadata with interests to provide better content recommendations and search relevance for learners.
---

# Content tagging and content metadata export

Use content tagging and content metadata export in Viva Learning to enable:  

- Tagging content with interests - admins and content owners (permissions set through Microsoft 365
groups) can manually tag content with interests.
- Exporting content metadata - admins and content owners can export content metadata in
a csv file for offline review and analysis of interest tags. Users can export metadata for the entire
content catalog or for a filtered set of content.
- Viewing interest tags - Learners can see interest tags associated with content on the content details page.

## Permissions

The following roles can export content metadata and edit content tags by accessing **Manage Content Metadata**:

- Knowledge admin
- Knowledge manager  
- Global Administrator
- Feature access management - access delegation through Microsoft 365 group.

## Exporting content metadata

This section outlines admin actions and steps to export content metadata.

### Admin actions

Admins and content owners (access set through Microsoft 365 groups) can export content metadata to a CSV file and share it with content owners for offline review and analysis of interest tags. They can then update the tags for content, which don't have tags or have inapplicable tags using the Viva Learning deep link in the exported file or by searching for the content in Viva Learning.

Admins and content owners can export content metadata in Viva Learning Admin by navigating to **Manage Content Metadata** and selecting **Bulk Export**.

### How to export content metadata

Admins can export content metadata for the entire course catalog or can make a custom selection to export content metadata for a specific set of content.

1. Select the following options:

    - Filter by Language
    - Filter by Provider
    - Filter by Content Type
    - Filter by tagged/untagged status for interests
    - Filter by interests

2. Select **Confirm** to export content metadata.

Users are notified that the content metadata export data has started.

Processing time is dependent on data export volume and can take up to an hour.

Users are notified that the content metadata export data is complete and can download the exported content metadata.

The exported csv file has the following metadata:

- Content ID
- Content Title
- Content Description
- Content Language
- Content Type
- Provider
- Author
- Source tags: Displays the tags coming from source (LMS or content provider). These tags can't be edited in Viva Learning.
- Curated tags: Tags that are manually curated by admins or content owners in Viva Learning. Admins and content owners can edit tags on content on Viva Learning through the content details page of the specific content.
- External ID:  The unique ID of the learning content from the external provider.- Provider ID: The unique ID of a provider when registered with Viva Learning.
- VL deep-link: Admins and content owners can select on this link for a specific content to go to the Viva Learning content details to update the irrelevant or unavailable tags for specific content.

## Curating tags on content

Only admins and content owners (who were given access through the delegation flow) can edit tags for content on the content details page. Interests coming from source (LMS or content provider) and interests curated by admins or content owners are visible here. 

Existing interests on the content are also visible as "Interests" under the content description on the content details page.

> [!NOTE]
> For source tags, only the tags coming from source which are part of the interest inventory (curated through the "Manage Interests" flow) are visible on the content details page. Interest from source tags that are not part of the curated interest inventory aren't displayed on content details page.

To edit tags for content, select **Edit**. An "Edit Interest tags" window opens, in which tags coming from source (if any) are displayed, source tags which are not part of the curated interest inventory are differentiated with an 'i' icon. You can't edit the incoming source tags. 

Admins and content owners can search and select up to three interests from the list of curated interests to tag the content. These manually added tags can be deselected to select more relevant interest applicable for the content.

The tags appear on the content details page after you save it.

> [!NOTE]
> Tagging learning collections with interests isn't currently supported. Currently, source tags from SuccessFactors is not supported as SuccessFactors package does not support tags on content.
## Learner view of interest tags

Learner can view an interest's tags (source tags that are part of the interest inventory and curated tags) in a read only mode.
They're able to view this information and search for more content for an appropriate interest as applicable.
