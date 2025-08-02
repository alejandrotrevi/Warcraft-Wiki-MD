# API GetNumCompletedAchievements

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns the total and completed number of achievements.
 total, completed = GetNumCompletedAchievements()

==Returns==
:total, completed <!-- remove this line if it's just one value -->

:;total:{{apitype|number}} - total number of available achievements
:;completed:{{apitype|number}} - total number of completed achievements

==Details==

: Unknown whether this takes Feats of Strength into account.

==Patch changes==
* {{Patch 3.0.2|note=Added.}}

==See also==
{{api|GetNumComparisonCompletedAchievements}} - To get information about another player's progress
```