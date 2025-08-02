# API C QuestLog.AddWorldQuestWatch

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_QuestLog|system=QuestLog}}
Tracks a world quest.
 wasWatched = C_QuestLog.AddWorldQuestWatch(questID [, watchType])

==Arguments==
:;questID:{{apitype|number}}
:;watchType:{{apitype|Enum.QuestWatchType?}}
{{:Enum.QuestWatchType|nocaption=1}}

==Returns==
:;wasWatched:{{apitype|boolean}}

==Patch changes==
* {{Patch 9.0.1|note=Added.}}
```