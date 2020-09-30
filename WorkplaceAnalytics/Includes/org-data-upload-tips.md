---
# Metadata Sample
# required metadata

title: Tips for uploading org data
description: Tips when uploading org data to MyAnalytics. 
author: paul9955
ms.author: v-mideh
ms.topic: article
localization_priority: normal
ms.prod: wpa
---

All field header or column names must:

* Begin with a letter (not a number)
* Only contain alphanumeric characters (letters and numbers, for example Date1)
* Have at least one lower-case letter (Hrbp); all uppercase won’t work (HRBP)
* Match exactly as listed for Workplace Analytics’ Required and Reserved optional attributes, including for case sensitivity (for example PersonId and HireDate)
* Have no leading or trailing blank spaces or special characters (non-alphanumeric, such as @, #, %, &); if spaces or special characters are included, Workplace Analytics will remove them from the name

The field values in the data row must comply with the following formatting rules:

* The required EffectiveDate and HireDate field values must be in the MM/DD/YYYY format
* The required PersonId and ManagerId field values must be a valid email address (for example, gc@contoso.com)
* The required TimeZone field values must be in a supported Windows format
* The required Layer field values must contain numbers only
* The required HourlyRate field values must contain numbers only, which Workplace Analytics assumes is in US dollars for calculations and data analysis
 * Double-byte characters, such as Japanese characters, are permitted in the data values.

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
