# API GetNumComparisonCompletedAchievements

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns the number of completed achievements for the comparison player.
 total, completed = GetNumComparisonCompletedAchievements(achievementID)

==Arguments==
:;achievementID:{{apitype|number}} - ID of the achievement to retrieve information for.

==Returns==
:;total:{{apitype|number}} - Total number of achievements currently in the game.
:;completed:{{apitype|number}} - Number of achievements completed by the comparison unit.

==Details==
* Does not include [[Feats of Strength]]
* Only accurate after the after [[SetAchievementComparisonUnit]] is called and the [[INSPECT_ACHIEVEMENT_READY]] event has fired.
* Inaccurate after [[ClearAchievementComparisonUnit]] has been called.

==Patch changes==
* {{Patch 3.0.2|note=Added.}}

==See also==
* {{api|SetAchievementComparisonUnit}} - to select a target before using this function
* {{api|ClearAchievementComparisonUnit}} - to clear the selection after using this function
* {{api|GetNumCompletedAchievements}} - for details about the player's own progress
```