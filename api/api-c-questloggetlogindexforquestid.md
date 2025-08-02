# API C QuestLog.GetLogIndexForQuestID

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_QuestLog|system=QuestLog}}
Returns the quest log index for a quest ID.
 questLogIndex = C_QuestLog.GetLogIndexForQuestID(questID)

==Arguments==
:;questID:{{apitype|number}}

==Returns==
:;questLogIndex:{{apitype|number?}}

==Details==
* Only returns a log index for actual quests, not headers.

==Patch changes==
* {{Patch 9.0.1|note=Moved to <code>C_QuestLog.GetLogIndexForQuestID()</code>}}
* {{Patch 4.0.1|note=Added as {{api|GetQuestLogIndexByID}}()}}
```