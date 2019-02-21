---
# Metadata Sample
# required metadata

title: Options upon failed validation
description: What you can do after your uploaded data has failed to validate.  
author: paul9955
ms.author: v-pascha
ms.date: 2/21/2019
ms.topic: article
localization_priority: normal 
ms.prod: wpa
---

* **Abandon** restarts the upload-map-validate process with new data rather than retrying the process with the current data. Select **Abandon** (at the upper right of the page). This option does not retain any of the field mappings.
* **Fix** has two options:
  * **Fix the source data** is recommended because it fixes the data in your source .csv file and increases the quality of the data.
  * **Change the mappings** enables you to change an incorrect data type, to lower the threshold. However, changing the threshold might negatively affect future data analysis. Select **Edit mapping** to set new mapping values, after which you can retry to validate your data file.
* **Upload file** retains your field mappings, which is different than the Abandon option. After you select this option, follow the steps in [File upload](#file-upload).