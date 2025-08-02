# API C AchievementInfo.GetSupercedingAchievements

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_AchievementInfo|system=AchievementInfo}}
Returns the next achievement in a series.
 supercedingAchievements = C_AchievementInfo.GetSupercedingAchievements(achievementID)

==Arguments==
:;achievementID:{{apitype|number}} : [[AchievementID]]

==Returns==
:;supercedingAchievements:{{apitype|number[]}} - Only returns the next ID in a series even though it's in a table.

==Example==
After [[Level 90 (Legacy)|Level 90]] (6193) comes [[Level 100 (Legacy)|Level 100]] (9060)
 /dump C_AchievementInfo.GetSupercedingAchievements(6193)

 > {9060}

==Patch changes==
* {{Patch 8.1.0|note=Added.}}
```