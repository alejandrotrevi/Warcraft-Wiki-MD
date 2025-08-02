# API C QuestLog.GetNumWorldQuestWatches

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_QuestLog|system=QuestLog}}
Replaces `GetNumWorldQuestWatches`.
 numQuestWatches = C_QuestLog.GetNumWorldQuestWatches()

==Returns==
:;numQuestWatches:{{apitype|number}}

==Example==
Returns the number of World Quests that the player is tracking.

 /run local count = 0 for i = 1, C_QuestLog.GetNumWorldQuestWatches() do if C_QuestLog.GetQuestIDForWorldQuestWatchIndex(i) then count = count + 1 end end print("Tracking " .. count .. " World Quests")

==Patch changes==
* {{Patch 9.0.1|note=Added.}}
```