---

title: System fields table
description: Tables that are used for mapping the system fields.   
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

<!-- NOTE: "System default fields" is the proper term. We are temporarily using "system fields" in the subsequent uploads topic because that's what the UI has on the mapping screens for subsequent uploads. 
This UI will change soon (probably spring 2019). After that happens, use not this include file but the sibling one for "system fields" wherever this info is needed. After that, this include file can be deleted. 
-->

System fields represent attributes that are known by the app and are used in specific calculations beyond grouping and filtering. A system field can be either required or optional. However, the validity threshold cannot be changed when editing existing data.

* **Required fields** are identified in two ways. Their rows have dark shading and show as "Required" under the Source column header. These rows represent data that was found in the uploaded file. For the upload to succeed, you must map the required fields with a column in your .csv file that is the correct data type and meets the validity threshold.

   >[!Important]
   >Every required field must have a valid, non-null value in every row. This means that, even if the names of these attributes are not present in the uploaded .csv file, other columns must be present in the .csv file that are mapped to these attributes.

* **Optional fields** appear below the required fields in rows that have lighter shading. These rows are commonly encountered system fields that are suggested for use. You don't need to map these fields if your organization doesn't have data for them.