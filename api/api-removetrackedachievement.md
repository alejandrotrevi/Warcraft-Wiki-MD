# API RemoveTrackedAchievement

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Untracks an achievement from the WatchFrame.
 RemoveTrackedAchievement(achievementId)

==Arguments==
:;[[achievementID]]:{{apitype|number}} - ID of the achievement to add to tracking.

==Triggers events==
* {{api|t=e|TRACKED_ACHIEVEMENT_UPDATE}}

==Details==
* A maximum of WATCHFRAME_MAXACHIEVEMENTS (10 as of 5.4.8) tracked achievements can be displayed by the WatchFrame at a time. 
* You may need to manually updated the AchievementUI and WatchFrame after calling this function.

==Patch changes==
* {{Patch 3.1.0|note=Added.}}

==See also==
* {{api|AddTrackedAchievement}}
* {{api|GetTrackedAchievements}}
* {{api|GetNumTrackedAchievements}}
```