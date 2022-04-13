---

title: Options upon failed validation (subsequent uploads)
description: What you can do after your uploaded data has failed to validate  
author: madehmer
ms.author: helayne
ms.topic: article
ms.localizationpriority: medium 
ms.collection: m365initiative-viva-insights 
ms.service: viva 
ms.subservice: viva-insights 
search.appverid: 
- MET150 
---
<!-- Note: Options in subsequent uploads contain a) changing (or even mentioning) thresholds and b) Abandon option. Options for first upload do not.   -->
| Nature of errors | Recommended selection | Description |
| ----- | ----- | ----- |
| Minor errors, small in number | Select **Edit mapping** | This displays the **Field Mapping** page, on which you can change how you map source-file fields to app attributes, optionally change validation thresholds, and then re-attempt validation. You can do these things without changing and re-uploading the source file. This is best for minor errors such as having mapped the wrong column in the source file or assigned a too-high validation threshold to a particular attribute. |
| Major errors | Select **Upload file** | This displays the first **File upload** page. Consider this option in the case of major errors in the originally uploaded data. First, edit the source-data file to fix those errors and then re-attempt the upload and validation process with the corrected file.|

There is also an option to select **Abandon**, a button on the top right of the page. Select this to cancel the current upload. You can abandon your upload for any reason, related or unrelated to errors in the upload file.

>[!Note]
>
>* The app does not modify or fill in data that is missing from HR uploads, such as for TimeZone. The administrator is responsible for correcting such errors or omissions.
>* When any data row or column has an invalid value for any attribute, the entire upload will fail until the source file is fixed (or the mapping changes the validation type of the attribute in a way that makes the value valid). Lowering a threshold does not ignore or skip an invalid value.

The following can help correct data in an uploaded source file that might be causing the validation errors.

When any data row or column has an invalid value for any attribute, the entire upload will fail until the source file is fixed (or the mapping changes the validation type of the attribute in a way that makes the value valid). Lowering a threshold does not ignore or skip an invalid value.

[!INCLUDE [Valid values and formats](../includes/org-data-upload-tips.md)]
