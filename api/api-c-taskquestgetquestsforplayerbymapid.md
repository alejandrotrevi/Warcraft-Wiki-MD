# API C TaskQuest.GetQuestsForPlayerByMapID

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_TaskQuest|system=QuestTaskInfo}} {{deprecatedapi|patch=11.0.5}}
Locates world quests, follower quests and bonus objectives on a map.
 taskPOIs = C_TaskQuest.GetQuestsForPlayerByMapID(uiMapID)

==Arguments==
:;uiMapID:{{apitype|number}} : [[UiMapID]]

==Returns==
:;taskPOIs:{{apitype|QuestPOIMapInfo[]}}
{| class="sortable darktable zebra" style="margin-left: 3.9em"
! Field !! Type !! Description
|-
| questID || {{apitype|number}} || 
|-
| x || {{apitype|number}} || 
|-
| y || {{apitype|number}} || 
|-
| inProgress || {{apitype|boolean}} || 
|-
| numObjectives || {{apitype|number}} || 
|-
| mapID || {{apitype|number}} || 
|-
| isQuestStart || {{apitype|boolean}} || 
|-
| isDaily || {{apitype|boolean}} || 
|-
| isCombatAllyQuest || {{apitype|boolean}} || 
|-
| childDepth || {{apitype|number?}} || 
|-
| questTagType || {{apitype|questTagType?}} || 
|-
| isMeta || {{apitype|boolean}} || 
|-
| isMapIndicatorQuest || {{apitype|boolean}} || 
|}

==Patch changes==
* {{Patch 11.0.5|note=Replaced <code>TaskPOIData</code> return struct with <code>QuestPOIMapInfo</code>, Added <code>questTagType, isMeta, isMapIndicatorQuest</code> fields, Replaced <code>questId</code> with <code>questID</code>}}
* {{Patch 8.2.0|note=Added <code>isQuestStart, isDaily, isCombatAllyQuest</code> fields.}}
* {{Patch 8.1.0|note=Added <code>childDepth</code> field.}}
* {{Patch 8.0.1|note=Replaced <code>mapID, parentMapID</code> arguments with <code>uiMapID</code>}}
* {{Patch 6.0.2|note=Added.}}

==See also==
* {{api|C_QuestLine.GetAvailableQuestLines}}()
```