# API C QuestLog.IsPushableQuest

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_QuestLog|system=QuestLog}}
Returns true if the quest can be shared with other players.
 isPushable = C_QuestLog.IsPushableQuest(questID)

==Arguments==
:;questID:{{apitype|number}}

==Returns==
:;isPushable:{{apitype|boolean}}

==Patch changes==
* {{Patch 9.0.1|note=Moved to <code>C_QuestLog.IsPushableQuest()</code>}}
* {{Patch 1.0.0|note=Added as {{api|GetQuestLogPushable}}()}}
```