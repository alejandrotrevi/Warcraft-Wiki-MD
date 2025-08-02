# API C TaskQuest.GetQuestLocation

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_TaskQuest|system=QuestTaskInfo}}
Needs summary.
 locationX, locationY = C_TaskQuest.GetQuestLocation(questID, uiMapID)

==Arguments==
:;questID:{{apitype|number}}
:;uiMapID:{{apitype|number}} : [[UiMapID]]

==Returns==
:;locationX:{{apitype|number}}
:;locationY:{{apitype|number}}

==Patch changes==
* {{Patch 8.0.1|note=Replaced <code>mapID, parentMapID</code> arguments with <code>questID, uiMapID</code>}}
* {{Patch 7.0.3|note=Added.}}
```