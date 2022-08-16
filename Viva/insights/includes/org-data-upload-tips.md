---

title: Tips for uploading organizational data
description: Tips when uploading organizational data for personal insights
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
#### Rules for field headers

All field header or column names must:

* Begin with a letter (not a number)
* Only contain alphanumeric characters (letters and numbers, for example Date1)
* Have at least one lower-case letter (Hrbp); all uppercase won’t work (HRBP)
* Match exactly as listed for the Required and Reserved optional attributes, including for case sensitivity, such as PersonId and HireDate
* Have no leading or trailing blank spaces or special characters (non-alphanumeric, such as @, #, %, &); if spaces or special characters are included, which will be removed from the name

#### Rules for field values

The field values in data rows must comply with the following formatting rules:

* The required EffectiveDate and HireDate field values must be in the MM/DD/YYYY format
* The required PersonId and ManagerId field values must be a valid email address (for example, gc@contoso.com)
* The TimeZone field values must be in a supported Windows format
* The Layer field values must contain numbers only
* The HourlyRate field values must contain numbers only, which the app assumes is in US dollars for calculations and data analysis

>[!Note]
>The app does not currently perform currency conversions for HourlyRate data. All calculations and data analysis assumes the data to be in US dollars.

#### Rules for characters in field values

The following field rules apply to characters in field values:

* Double-byte characters, such as Japanese characters, _are_ permitted in the field values
* Limit the character length of field values in rows to a maximum of 128 KB, which is about 1024 x 128 characters
* The following characters are _not_ permitted in field values:

  * tilde (~)
  * "new line" (\n)
  * Double quotes (" ")
  * Single quotes (' ')

<!-- FORMERLY HERE: 
* No accent marks (á)
* No short or long dashes (-, --)
* No commas (,)  -->
