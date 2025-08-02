# API C LFGList.GetActivityInfoExpensive

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}} __NOTOC__
Returns the zone associated with an activity.
 currentArea = C_LFGList.GetActivityInfoExpensive(activityID)

==Arguments==
:;activityID:{{apitype|number}} - The activityID for which information are requested, as returned by [[API_C_LFGList.GetAvailableActivities|C_LFGList.GetAvailableActivities]]().

==Returns==
:;currentArea:{{apitype|boolean}} - True if you are in the zone of the activity, false otherwise.
```