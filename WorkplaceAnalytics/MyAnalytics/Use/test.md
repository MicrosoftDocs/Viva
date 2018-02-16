

**Parameter**|**Required**|**Description**
:-----:|:-----:|:-----:
Identity|Yes|User ID for the current user as stored in Azure Active Directory (AAD).
PrivacyMode|Yes|Excluded: MyAnalytics will not use the current user’s data to compute derived statistics for other users. The current user will not be able to change this from the Feature settings menu in MyAnalytics, but will still be able to see personalized statistics in their MyAnalytics dashboards. * Opt-out: MyAnalytics will not use the current user’s data to compute derived statistics for other users. The current user will not see statistics in MyAnalytics, but can change this from the Feature settings menu and choose to opt-in. * Opt-in: MyAnalytics will use the current user’s data to compute derived statistics for other users. The current user will see statistics in MyAnalytics, and can change this from the Feature settings menu to opt out.
