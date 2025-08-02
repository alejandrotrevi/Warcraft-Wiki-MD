# API C QuestLine.GetAvailableQuestLines

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_QuestLine|system=QuestLineUI}}
Returns available quest lines on a map.
 questLines = C_QuestLine.GetAvailableQuestLines(uiMapID)

==Arguments==
:;uiMapID:{{apitype|number}} : [[UiMapID]]

==Returns==
:;questLines:{{apitype|QuestLineInfo[]}}
{{:Struct QuestLineInfo|nocaption=1}}

==Patch changes==
* {{Patch 8.0.1|note=Added.<ref>{{ref FrameXML|Blizzard_SharedMapDataProviders/StorylineQuestDataProvider.lua|8.0.1|27101||20180716}}</ref>}}

==See also==
* {{api|C_TaskQuest.GetQuestsForPlayerByMapID}}()

==References==
```