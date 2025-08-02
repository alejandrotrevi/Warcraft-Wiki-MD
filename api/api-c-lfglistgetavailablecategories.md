# API C LFGList.GetAvailableCategories

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}} __NOTOC__
Returns a list of available LFG categories.
 categories = C_LFGList.GetAvailableCategories([filter])

==Arguments==
:;filter:{{apitype|number?}} - Bit mask to filter the results. If omitted the function returns all categories. See [[API_C_LFGList.GetActivityInfo#Filters|C_LFGList.GetActivityInfo]] for more information.

==Returns==
:;categories:{{apitype|table}} - A table containing the requested categoryIDs (not in order).
```