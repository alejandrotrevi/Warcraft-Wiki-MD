# API C LFGList.GetAvailableActivities

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}} __NOTOC__
Returns a list of available LFG activities.
 activities = C_LFGList.GetAvailableActivities([categoryID [, groupID [, filter]]])

==Arguments==
:;categoryID:{{apitype|number?}} - Use to only get activityIDs associated with a specific category. Use [[API_C_LFGList.GetAvailableCategories|C_LFGList.GetAvailableCategories]]() to get a list of all available categoryIDs. If omitted the function returns activities of all categories.
:;groupID:{{apitype|number?}} - Use to only get activityIDs associated with a specific group. See [[API_C_LFGList.GetActivityGroupInfo|C_LFGList.GetActivityGroupInfo]] for more information. If omitted the function returns activities of all groups.
:;filter:{{apitype|number?}} - Bit mask to filter the results. See [[API_C_LFGList.GetActivityInfo#Filters|C_LFGList.GetActivityInfo]] for more information.

==Returns==
:;activities:{{apitype|table}} - A table containing the requested activityIDs (not in order).
```