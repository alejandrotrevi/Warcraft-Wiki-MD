# API C QuestLog.RemoveQuestWatch

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_QuestLog|system=QuestLog}}
Untracks a quest.
 wasRemoved = C_QuestLog.RemoveQuestWatch(questID)

==Arguments==
:;questID:{{apitype|number}}

==Returns==
:;wasRemoved:{{apitype|boolean}}

==Patch changes==
* {{Patch 9.0.1|note=Moved to <code>C_QuestLog.RemoveQuestWatch()</code>}}
* {{Patch 8.2.5|note=Added <code>RemoveQuestWatchForQuestID()</code>}}
* {{Patch 1.3.0|note=Added {{api|RemoveQuestWatch}}()}}
```