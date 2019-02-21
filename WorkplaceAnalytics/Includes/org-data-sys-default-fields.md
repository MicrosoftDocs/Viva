---
# Metadata Sample
# required metadata

title: System default fields table
description: Tables that are used for mapping the system default fields.   
author: paul9955
ms.author: v-pascha
ms.date: 2/21/2019
ms.topic: article
localization_priority: normal 
ms.prod: wpa
---

System default fields represent attributes that are known by Workplace Analytics and are used in specific calculations beyond grouping and filtering. A system field can be either required or optional.

* **Required fields** are identified in two ways. Their rows have dark shading and show as “Required" under the Source column header. These rows represent data that was found in the uploaded file. For the upload to succeed, you must map the required fields with a column in your .csv file that is the correct data type and meets the validity threshold.

   >[!Important]
   >Every required field must have a valid, non-null value in every row. This means that, even if the names of these attributes are not present in the uploaded .csv file, other columns must be present in the .csv file that are mapped to these attributes.

* **Optional fields** appear below the required fields in rows that have lighter shading. These rows are commonly encountered system fields that Workplace Analytics suggests for use. You don't need to map these fields if your organization doesn't have data for them.