# API SetAchievementComparisonUnit

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Sets the unit to be compared to.
 success = SetAchievementComparisonUnit(unit)

==Arguments==
:;unit:{{apitype|string}} : [[UnitId]]

==Returns==
:;success:{{apitype|boolean}} - Returns true/false depending on whether the unit is valid.

==Triggers events==
* {{api|t=e|INSPECT_ACHIEVEMENT_READY}}, when your query has finished processing on the server and new information is available

==See also==
* {{api|ClearAchievementComparisonUnit}}
* {{api|GetAchievementComparisonInfo}}
* {{api|GetNumComparisonCompletedAchievements}}
```