# API C LFGList.GetAvailableActivityGroups

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_LFGList|system=LFGList}}
Returns a list of available LFG groups.
 activityIDs = C_LFGList.GetAvailableActivityGroups(categoryID [, filter])

==Arguments==
:;categoryID:{{apitype|number}} - The categoryID of the category you want to get available groups of. Use [[API_C_LFGList.GetAvailableCategories|C_LFGList.GetAvailableCategories]]() to get a list of all available categoryIDs.
:;filter:{{apitype|number?|default=0}} - Bit mask to filter the results. See [[API_C_LFGList.GetActivityInfo#Filters|C_LFGList.GetActivityInfo]] for more information.

==Returns==
:;activityIDs:{{apitype|number[]}} - A table containing the requested groupIDs (not in order).
```