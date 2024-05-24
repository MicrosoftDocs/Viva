---
title: Configure 360 cycle settings
description: There are five areas to set up in a new 360 cycle. Follow this guidance.
ms.author: JudithWeiner
author: JudyWeiner
manager: MelissaBarry
audience: admin
f1.keywords: NOCSH
keywords: 
ms.collection:  
- m365initiative-viva
- selfserve 
search.appverid: MET150 
ms.topic: article
ms.service: viva-glint
ms.localizationpriority: high
ms.date: 5/23/2024
ROBOTS: NOINDEX, NOFOLLOW
---

# Configure 360 cycle settings

Although *Manage Subjects* appears first on the cycle page, we recommend setting up **Cycle Settings** first. There are five areas to set up. As you move through them, a filled blue circle confirms their completion.

:::image type="content" source="../../media/glint/setup/360-settings-do-first.png" alt-text="Screenshot of the five sections to configure in Cycle Settings.":::

## Setup

There are three sections to configure:
- The Basics
- Feedback provider category settings and confidentiality
- Feedback provider response information

Select **Save** when you are done configuring the page.

### The Basics
:::image type="content" source="../../media/glint/setup/360-the-basics.png" alt-text="Screenshot of the first section to configure in Cycle Settings.":::

### Feedback provider category settings and confidentiality

:::image type="content" source="../../media/glint/setup/360-categories-confidentiality.png" alt-text="Screenshot of the second section to configure in Cycle Settings.":::

Select up to six feedback provider categories. 
- Standard categories automatically prepopulate feedback providers based on Manager Hierarchy.
- Remove the Direct Reports category for individual contributor (IC) subjects,
- **Or** ask IC subjects to skip adding feedback providers for the Direct Reports category for  cycles with both managers and ICs.

>[!TIP]
>Choose at least three feedback provider categories (in addition to Self) to ensure a true 360 view.

|Feedback provider category|Minimum confidentiality threshold|Can subject or admin edit prepopulated feedback providers?|How assigned|
|----------|:-------------:|:-------------:|-------------|
|Self| 1|No|Required - All 360 subjects require a subject self assessment|
|Manager|1|Yes|Prepopulates with the subject's direct manager|
|Skip Manager|1|Yes|Prepopulates with the subject's direct manager|
|Direct reports|3*|Yes|Prepopulatees with the subject's direct reports|
|Peers|3*|Yes|Prepopulates with people who have the same direct manager as the subject|
|Custom|1|N/A|Not commonly used, but could by used for a *dotted line manager* or *mentor* feedback|
|Custom|3*|N/A|Commonly used for *Collaborators*|

> [!IMPORTANT]
> *At least three feedback providers must respond at the *survey level* to show feedback in a subject's report. Note that this requirement is not for *question* level.

### Edit a feedback provider category

**Hover over and choose a category** eo open the Edit window for that category, which looks like this (for example):

:::image type="content" source="../../media/glint/setup/360-edit-provider-category.png" alt-text="Screenshot of an example of a window that opens to edit a feedback provider category.":::

Edit each field as you’d like. When editing in another language that is available in the dropdown menu, that language saves so you can come back to it later if further edits are needed. 
Confidentiality Statements

>[!CAUTION]
>You can increase the confidentiality threshold for some feedback provider categories but you can’t information about confidentiality follows.

Dependent on the provider category, provider response information settings, and whether your organization included a privacy policy link in General Settings, the 360 confidentiality statement users see varies. [Learn more about Viva Glint 360 privacy and confidentiality](https://go.microsoft.com/fwlink/?linkid=2230922).

### Feedback provider response information

This setting can’t be edited once a cycle is live. Choose between:
- **On** (default): Subjects see feedback providers and if they've responded. In reporting, subjects see which feedback providers responded per category, but responses are not tied to individual names.
- **Off**: Subjects see feedback providers but can’t see whether they've responded. In reporting, they see only the number of feedback providers who responded.

:::image type="content" source="../../media/glint/setup/360-provider-response-info.png" alt-text="Screenshot of the Feedback Provider Response Information window.":::



