# API GetAchievementNumCriteria

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns the number of criteria for an achievement.
 numCriteria = GetAchievementNumCriteria(achievementID)

==Arguments==
:;achievementID:{{apitype|number}} - Uniquely identifies each achievement

==Returns==
:;numCriteria:{{apitype|number}} - The number of criteria required for the given Achievement

==Details==
Used in conjunction with [[API_GetAchievementCriteriaInfo|GetAchievementCriteriaInfo]]

==Patch changes==
* {{Patch 3.0.2|note=Added.}}
```