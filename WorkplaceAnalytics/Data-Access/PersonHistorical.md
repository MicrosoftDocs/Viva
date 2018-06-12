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


  Contains one row for each person for each HR change. A new row is created when a person's HR attributes change.
  
|Column name|Data type|Description|
|-----------------|---------------|-----------------|
|**PersonHistoricalId**|**string**|Unique value for every person for each HR change. Primary key.|
|**EmailAddress**|**string**|Masked value, unique for every email address.|  
|**StartDate**|**datetime**|Effective start date of last HR change (does not apply for original hire date, or leave date).|
|**EndDate**|**datetime**|Effective end date of last HR change (does not apply for original hire date, or leave date).|
|**PopulationType**|**string**|Type of employee. See Remarks.|
|**IsInternal**|**boolean**|True if employee type is either MeasureEmployee or InternalCollaborator.|
|**ManagerId**|**string**|Unique value for each person's manager.|
|**HR Attribute 1**||HR values that have been added to the data set. See Remarks.|
|   ...   |||
|**HR Attribute n**||HR values which have been added to the data set. See Remarks.|

## Remarks

### PopulationType
The following table describes the possible values for the **PopulationType** column. 

|Value|Description|
|------|------|
|MeasuredEmployee|Employee who has a WPA license assigned.|
|InternalCollaborator |Person within the company who does not have a WPA license assigned.|
|ExternalCollaborator |Person with an domain that does not match the default company domain.|
|DistributionList |An Active Directory distribution list.|
|MeetingRoom |A meeting room.|

### HR Attributes
The HR attributes represent organizational data your company has uploaded for use in Workplace Analytics. The attributes include a requires set of attributes, optional attributes, and custom attributes. For more information about these attributes refer to [Prepare and upload organizational data](https://docs.microsoft.com/workplace-analytics/setup/prepare-and-upload-organizational-data#step-three--export-data).
