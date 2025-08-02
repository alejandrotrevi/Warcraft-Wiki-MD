# API C QuestLog.GetQuestIDForWorldQuestWatchIndex

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_QuestLog|system=QuestLog}}
Returns the quest ID represented by the given quest watch index.
 questID = C_QuestLog.GetQuestIDForWorldQuestWatchIndex(questWatchIndex)

==Arguments==
:;questWatchIndex:{{apitype|number}}

==Returns==
:;questID:{{apitype|number?}}

==Example==
Returns the Quest ID of any World Quests player is tracking.

 /run for i=1, C_QuestLog.GetNumWorldQuestWatches() do local qID = C_QuestLog.GetQuestIDForWorldQuestWatchIndex(i) if qID then print("WQ "..i..": ID "..qID) end end

==Patch changes==
* {{Patch 9.0.1|note=Added.}}
```