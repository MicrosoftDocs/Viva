---
ms.date: 02/13/2024
title: Query results in Viva Insights FAQs
description: Get answers to common questions about advanced insights query results
author: zachminers
ms.author: v-zachminers
ms.topic: article
ms.localizationpriority: medium 
ms.collection: viva-insights-advanced 
ms.service: viva 
ms.subservice: viva-insights 
search.appverid: 
- MET150 
manager: anirudhbajaj
audience: Admin
---

# Query results FAQs

We've compiled answers for some questions you might run across while viewing your query results. 

## Meeting queries

### Q1. Why is a meeting's Attendee count lower than expected? Or, why are metric values listed as 0?

A1. You might notice that more people accepted a meeting than attended it. This can happen for a few reasons:

* Some invitees accepted the meeting but then attended another meeting without changing their response. Or, some invitees were deemed to be attending a conflicting meeting.
* Some attendees are external or unmeasured, meaning they're not assigned a Viva Insights license, and thus aren't included in the metric calculation.
* The query was run in a partition and the meeting had participants who aren't in the partition, and thus aren't included in the metric calculation.

### Q2. Why are meetings missing from my results?

A2. The query might not have had any attendees. If no one attended a meeting, Viva Insights removes that meeting from query results by default. 

### Q3. Why is data about the meeting organizer missing?

A3. This can happen for a few reasons:

* The organizer doesn't have a license.

* The organizer opted out of Viva Insights. Learn more about opting out in [Opt out of Viva Insights](../../personal/use/opt-out-of-mya.md).
* The organizer isn't part of the partition.
* The organizer's HR data hasn't been uploaded.


### Q4. Why is the Subject column empty for a meeting?

A4. Your admin might have suppressed certain sensitive keywords. If a meeting title contained one of those keywords, then query results don't show that meeting title.

### Q5. Why isn't a user showing up in query results?

Licensing might be a factor. For a user to appear in query results, that user needs to have a license at the time the query is run.

If you have questions about user licensing, contact your Microsoft 365 admin and your Insights Administrator.