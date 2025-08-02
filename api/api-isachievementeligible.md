# API IsAchievementEligible

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Indicates whether the specified achievement is eligible to be completed.
 eligible = IsAchievementEligible(achievementID)

==Arguments==
:;achievementID:{{apitype|number}} - ID of the achievement to query.

==Returns==
:;eligible:{{apitype|boolean}}

==Details==
* This function is used in the watch frame to determine whether a tracked achievement should be shown in red text (not eligible) or normal colors (eligible).

==Patch changes==
* {{Patch 4.0.1|note=Added.}}
```