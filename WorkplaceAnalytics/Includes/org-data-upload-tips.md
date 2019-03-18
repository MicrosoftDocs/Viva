---
# Metadata Sample
# required metadata

title: Tips for uploading org data
description: Tips when uploading org data to MyAnalytics. 
author: paul9955
ms.author: v-pascha
ms.date: 03/18/2019
ms.topic: article
localization_priority: normal
ms.prod: mya
---

### Invalid values or formats

When any data row or column has an invalid value for any attribute, the entire upload will fail until the source file is fixed (or the mapping changes the validation type of the attribute in a way that makes the value valid). Lowering a threshold does not ignore or skip an invalid value.

All field header or column names must:

* Begin with a letter (not a number)
* Only contain alphanumeric characters (letters and numbers, for example Date1)
* Have at least one lower-case letter (Hrbp); all uppercase won’t work (HRBP)
* Have no spaces (Date1)
* Have no special characters (non-alphanumeric, such as @, #, %, &, *)
* Match exactly as listed for Workplace Analytics’ Required and Reserved optional attributes, including for case sensitivity (for example PersonId and HireDate)

The field values in the data row must comply with the following formatting rules:

* The required EffectiveDate and HireDate field values must be in the MM/DD/YYYY format
* The required PersonId and ManagerId field values must be a valid email address (for example, gc@contoso.com). 
* The required TimeZone field values must be in a supported Windows format.
* The required Layer field values must contain numbers only.
* The required HourlyRate field values must contain numbers only, which Workplace Analytics assumes is in US dollars for calculations and data analysis.

>[!Note]
> Workplace Analytics does not currently perform currency conversions for HourlyRate data. All calculations and data analysis in Workplace Analytics assume the data to be in US dollars.

The field values also cannot contain any of the following:

* No accent marks (á)
* No tildes (~)
* No short or long dashes (-, --)
* No commas (,)
* No "new line" characters (\n)
* No double (" ") or single quotes (‘ ‘)
* Limit character length of field values in rows to a maximum of 128 KB, which is about 1024 x 128 characters

### Addition of missing data

Workplace Analytics does not modify or fill in data that is missing from HR uploads, even for EffectiveDate or TimeZone. The administrator is responsible for correcting such errors or omissions.

### Addition of a new data column

Let's say that you've already uploaded at least 13 months of snapshot data, which contained the five required columns (PersonId, EffectiveDate, LevelDesignation, ManagerId, Organization) for all employees. Now, you want to upload one new column of data – for example, an engagement score value for each employee – and you want it to apply to all of the historical data. When you upload to append the new "EngagementScore" data column, remember to reupload all five of the minimum required fields along with the new field. 

### Set Validity threshold for custom fields

The threshold depends on the intended use of the custom field. If you intend to use this data in much of your analysis, consider setting it to a high percentage. You can set a lower threshold for data that applies, for example, to only a small subset of people in your organization.

#### Set a high value

Generally, you should set the Validity threshold to a high value. This is especially important if your analysis will focus on that field.

For example, you might include a "SupervisorIndicator" attribute. At first, you might not think that you're analyzing manager behavior and you might be tempted to omit this attribute. But the organization hierarchy is used implicitly by many Workplace Analytics analyses – for differentiating different work groups, for determining high- and low-quality meetings based on how many levels attend, and more.

#### Set a lower value

The goal of your analysis might be to determine sales effectiveness. Your data might include an attribute for sales attainment that only makes sense for members of your sales force, who constitute about 10% of the company. This number doesn't apply to engineers or program managers, but it is critical for high-performers in sales.  