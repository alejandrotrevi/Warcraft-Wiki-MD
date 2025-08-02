# API C QuestLog.GetQuestIDForQuestWatchIndex

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_QuestLog|system=QuestLog}}
Returns the quest ID represented by the given quest watch index.
 questID = C_QuestLog.GetQuestIDForQuestWatchIndex(questWatchIndex)

==Arguments==
:;questWatchIndex:{{apitype|number}}

==Returns==
:;questID:{{apitype|number?}}

==Example==
Returns the Quest ID of any non-world quests player is tracking.

 /run for i=1, C_QuestLog.GetNumQuestWatches() do local qID = C_QuestLog.GetQuestIDForQuestWatchIndex(i) if qID then print("# "..i..": ID "..qID) end end

==Patch changes==
* {{Patch 9.0.1|note=Added.}}
```