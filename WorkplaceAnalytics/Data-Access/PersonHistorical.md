---

ROBOTS: NOINDEX,NOFOLLOW
title: Historical person metrics for Workplace Analytics Data export
description: One row for each person that has HR attribute changes
author: paul9955
ms.author: v-mideh
ms.topic: article
ms.prod: wpa
---

# PersonHistorical (.csv)

This file includes one row for each person that has HR attribute changes and for each HR change with the following metrics. A new row is created when a person's HR attributes change.
  
|Column name|Data type|Description|
|-----------------|---------------|-----------------|
|PersonHistoricalId|string|Unique value for every person for each HR change; primary key|
|EmailAddress|string|Masked value, unique for every email address|  
|StartDate|datetime|Effective start date of last HR change (does not apply for original hire date, or leave date)|
|EndDate|datetime|Effective end date of last HR change (does not apply for original hire date, or leave date)|
|PopulationType|string|Type of employee. See [PopulationType](#populationtype).|
|ManagerId|string|Unique value for each person's manager|
|HR Attribute 1|varies |HR values that have been added to the dataset; see [HR attributes](#hr-attributes).|
|   ...   |||
|HR Attribute n|varies |HR values that have been added to the dataset; see [HR attributes](#hr-attributes).|
|LevelDesignation|string|HR values for employee levels that represent an employee's experience, management level, or seniority within the organization.|
|Organization|string|HR values for the internal organization for which employees belong that's specific and identifiable by the organization's leaders.|
|IsInternal|boolean|True if PopulationType is either MeasuredEmployee or InternalCollaborator|
|ExternalCollaboratorId|string|Email address if PopulationType is ExternalCollaborator and the tenant is configured to include external email IDs in the report|

## PopulationType

The following describes possible values for the **PopulationType** column.

|Value|Description|
|------|------|
|MeasuredEmployee|An employee who has a Workplace Analytics license assigned|
|InternalCollaborator |A person within the company who does not have a Workplace Analytics license assigned|
|ExternalCollaborator |A person with a domain that does not match the default company domain|
|DistributionList |An Active Directory distribution list|
|MeetingRoom |A meeting room|

## HR attributes

The HR attributes represent organizational data your company has uploaded for use in Workplace Analytics. The attributes include a required set of attributes, optional attributes, and custom attributes. For more information about these attributes, see [Prepare organizational data](../setup/prepare-organizational-data.md#attribute-reference).

## Related topics

[Data export](./data-access.md)
