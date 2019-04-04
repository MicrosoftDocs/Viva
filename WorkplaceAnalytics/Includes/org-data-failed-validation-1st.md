---
# Metadata Sample
# required metadata

title: Options upon failed validation (first upload)
description: What you can do after your uploaded data has failed to validate.  
author: paul9955
ms.author: v-pascha
ms.date: 03/19/2019
ms.topic: article
localization_priority: normal 
ms.prod: wpa
---

<!-- Note: Options in subsequent uploads contain a) changing thresholds and b) Abandon option. Options for first upload do not.   -->

| Nature of errors | Recommended selection | Description |
| ----- | ----- | ----- |
| Minor errors, small in number | Select **Edit mapping** | This displays the **Field Mapping** page, on which you can change how you map source-file fields to Workplace Analytics attributes and then re-attempt validation. You can do this without changing and re-uploading the source file. This is best for minor errors such as having mapped the wrong column in the source file to a particular attribute. |
| Major errors | Select **Upload file** | This displays the first **File upload** page. Consider this option in the case of major errors in the originally uploaded data. First, edit the source-data file to fix those errors and then re-attempt the upload and validation process with the corrected file.|

> [!Note] 
> * Workplace Analytics does not modify or fill in data that is missing from HR uploads, even for EffectiveDate or TimeZone. The administrator is responsible for correcting such errors or omissions.
> * For more information about correcting data in an uploaded source file that is causing validation errors, see the [Use only valid values and formats](../setup/prepare-organizational-data.md#use-only-valid-values-and-formats) section of [Prepare organizational data](../setup/prepare-organizational-data.md).
