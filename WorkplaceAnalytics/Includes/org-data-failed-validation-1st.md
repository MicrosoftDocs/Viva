---
# Metadata Sample
# required metadata

title: Options upon failed validation (first upload)
description: What you can do after your uploaded data has failed to validate.  
author: paul9955
ms.author: v-pausch
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

### Guidelines for correcting errors in data

This section contains help for correcting data in an uploaded source file that is causing validation errors.

When any data row or column has an invalid value for any attribute, the entire upload will fail until the source file is fixed (or the mapping changes the validation type of the attribute in a way that makes the value valid). 

[!INCLUDE [Valid values and formats](../includes/org-data-upload-tips.md)]