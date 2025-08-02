# API UnitQuestTrivialLevelRange

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|system=Unit}}
Returns the difference between the units' current level and the level at which fixed-level quests are of trivial difficulty.
 levelRange = UnitQuestTrivialLevelRange(unit)

==Arguments==
:;unit:{{apitype|string}} : [[UnitId]]

==Returns==
:;levelRange:{{apitype|number}}

==Patch changes==
* {{Patch 9.0.1|note=Changed to <code>UnitQuestTrivialLevelRange()</code>}}
* {{Patch 1.0.0|note=Added as {{api|GetQuestGreenRange}}()}}
```