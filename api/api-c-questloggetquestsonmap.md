# API C QuestLog.GetQuestsOnMap

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_QuestLog|system=QuestLog}}
Needs summary.
 quests = C_QuestLog.GetQuestsOnMap(uiMapID)

==Arguments==
:;uiMapID:{{apitype|number}} : [[UiMapID]]

==Returns==
:;quests:{{apitype|QuestPOIMapInfo[]}}
{{:Struct QuestPOIMapInfo|nocaption=1}}

==Patch changes==
* {{Patch 11.0.5|note=Replaced <code>QuestOnMapInfo</code> return struct  with <code>QuestPOIMapInfo</code>, added <code>inProgress, numObjectives, mapID, isQuestStart, isDaily, isCombatAllyQuest, childDepth, questTagType, isMeta</code> fields, removed <code>type</code> field.}}
* {{Patch 8.1.0|note=Added <code>type, isMapIndicatorQuest</code> fields.}}
* {{Patch 8.0.1|note=Added.}}
```