# API C QuestLog.IsUnitOnQuest

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_QuestLog|system=QuestLog}}
Returns true if the unit is on the specified quest.
 isOnQuest = C_QuestLog.IsUnitOnQuest(unit, questID)

==Arguments==
:;unit:{{apitype|string}} : [[UnitId]]
:;questID:{{apitype|number}}

==Returns==
:;isOnQuest:{{apitype|boolean}}

==Patch changes==
* {{Patch 9.0.1|note=Moved to <code>C_QuestLog.IsUnitOnQuest()</code>}}
* {{Patch 6.0.2|note=Added <code>IsUnitOnQuestByQuestID()</code>}}
* {{Patch 1.3.0|note=Added {{api|IsUnitOnQuest}}()}}
```