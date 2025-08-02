# API GetAchievementComparisonInfo

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns information about the comparison unit's achievements.
 completed, month, day, year = GetAchievementComparisonInfo(achievementID)

==Arguments==
:;achievementID:{{apitype|number}} - ID of the achievement to retrieve information for.

==Returns==
:;completed:{{apitype|boolean}} - Returns true/false depending on whether the unit has completed the achievement or not.
:;month:{{apitype|number}} - Month in which the unit has completed the achievement. Returns nil if completed is false.
:;day:{{apitype|number}} - Day of the month in which the unit has completed the achievement. Returns nil if completed is false.
:;year:{{apitype|number}} - Year (two digits, 21st century is assumed) in which the unit has completed the achievement. Returns nil if completed is false.

==Details==
* Only accurate after the after [[SetAchievementComparisonUnit]] is called and the [[INSPECT_ACHIEVEMENT_READY]] event has fired.
* Inaccurate after [[ClearAchievementComparisonUnit]] has been called.

==Patch changes==
* {{Patch 3.0.2|note=Added.}}

==See also==
* {{api|ClearAchievementComparisonUnit}}
* {{api|SetAchievementComparisonUnit}}
* {{api|GetNumComparisonCompletedAchievements}}
```