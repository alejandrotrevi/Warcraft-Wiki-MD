# API GetTrackedAchievements

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns the currently tracked achievements.
 id1, id2, ..., idn = GetTrackedAchievements()

==Returns==
:;id1, id2, ..., idn:{{apitype|number}} - achievementId(s) of achievements you are currently tracking.

==Details==
* Returns up to 10 tracked achievements.

==Patch changes==
* {{Patch 3.1.0|note=Renamed from GetTrackedAchievement to GetTrackedAchievements.}}
* {{Patch 3.0.2|note=Added.}}

==See also==
* {{api|AddTrackedAchievement}}
* {{api|GetNumTrackedAchievements}}
* {{api|RemoveTrackedAchievement}}
```