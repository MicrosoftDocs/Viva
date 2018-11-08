---
# Metadata Sample
# required metadata

title: Tips for uploading org data
description: Tips when uploading org data to MyAnalytics. 
author: paul9955
ms.author: v-pascha
ms.date: 11/05/2018
ms.topic: get-started-article
localization_priority: normal 
ms.prod: mya
---

### Invalid values

When any row has an invalid value for any attribute, the entire upload will fail until the source file is fixed (or the mapping changes the validation type of the attribute in a way that makes the value valid). Lowering a threshold does not ignore or skip an invalid value.

### Adding missing data

Workplace Analytics does not modify or fill in data that is missing from HR uploads, even for EffectiveDate or TimeZone. The administrator is responsible for correcting such errors or omissions.

### Set Validity threshold for custom fields

The threshold depends on the intended use of the custom field. If you intend to use this data in much of your analysis, consider setting it to a high percentage. You can set a lower threshold for data that applies, for example, to only a small subset of people in your organization.

#### Set a high value

Generally, you should set the Validity threshold to a high value. This is especially important if your analysis will focus on that field.

For example, you might include a "ManagerID" attribute. At first, you might not think that you're analyzing manager behavior and you might be tempted to omit this attribute. But the organization hierarchy is used implicitly by many Workplace Analytics analyses – for differentiating different work groups, for determining high- and low-quality meetings based on how many levels attend, and more.

#### Set a lower value

The goal of your analysis might be to determine sales effectiveness. Your data might include an attribute for sales attainment that only makes sense for members of your sales force, who constitute about 10% of the company. This number doesn't apply to engineers or program managers, but it is critical for high-performers in sales.  