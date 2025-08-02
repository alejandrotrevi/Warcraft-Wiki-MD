# API GetAchievementCategory

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns the category number the requested achievement belongs to.
 categoryID = GetAchievementCategory(achievementID)

==Arguments==
:;[[achievementID]]:{{apitype|number}} - ID of the achievement to retrieve information for.

==Returns==
:;categoryID:{{apitype|number}} - ID of the achievement's category.

==Patch changes==
* {{Patch 3.0.2|note=Added.}}

==See also==
* {{api|GetAchievementComparisonInfo}}
* {{api|SetAchievementComparisonUnit}}
* {{api|GetNumComparisonCompletedAchievements}}
```