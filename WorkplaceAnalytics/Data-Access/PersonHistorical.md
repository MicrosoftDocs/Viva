---
# Metadata Sample
# required metadata

ROBOTS: NOINDEX,FOLLOW
title: PersonHistorical table (WPA Data Access)
description: One row for each person for each HR change
author: gbowerman
ms.author: guybo
ms.date: 05/11/2018
ms.topic: language-reference
ms.prod: wpa
---

# PersonHistorical table (CSV)

This table contains one row for each person for each HR change. A new row is created when a person's HR attributes change.
  
|Column name|Data type|Description|
|-----------------|---------------|-----------------|
|**PersonHistoricalId**|**string**|Unique value for every person for each HR change. Primary key.|
|**EmailAddress**|**string**|Masked value, unique for every email address.|  
|**StartDate**|**datetime**|Effective start date of last HR change (does not apply for original hire date, or leave date).|
|**EndDate**|**datetime**|Effective end date of last HR change (does not apply for original hire date, or leave date).|
|**PopulationType**|**string**|Type of employee. See [PopulationType](#populationtype).|
|**IsInternal**|**boolean**|True if employee type is either MeasureEmployee or InternalCollaborator.|
|**ManagerId**|**string**|Unique value for each person's manager.|
|**HR Attribute 1**||HR values that have been added to the data set. See [HR Attributes](#hr-attributes).|
|   ...   |||
|**HR Attribute n**||HR values that have been added to the data set. See [HR Attributes](#hr-attributes).|

## Remarks

### PopulationType
The following table describes the possible values for the **PopulationType** column. 

|Value|Description|
|------|------|
|MeasuredEmployee|An employee who has a Workplace Analytics license assigned.|
|InternalCollaborator |A person within the company who does not have a WPA license assigned.|
|ExternalCollaborator |A person with a domain that does not match the default company domain.|
|DistributionList |An Active Directory distribution list.|
|MeetingRoom |A meeting room.|

### HR Attributes
The HR attributes represent organizational data your company has uploaded for use in Workplace Analytics. The attributes include a requires set of attributes, optional attributes, and custom attributes. For more information about these attributes refer to [Prepare and upload organizational data](../setup/prepare-and-upload-organizational-data.md#step-three--export-data).
