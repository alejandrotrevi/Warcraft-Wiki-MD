# API C QuestLog.IsComplete

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_QuestLog|system=QuestLog}}
Returns whether the supplied quest in the quest log is complete.
 isComplete = C_QuestLog.IsComplete(questID)

==Arguments==
:;questID:{{apitype|number}}

==Returns==
:;isComplete:{{apitype|boolean}} - Whether the quest is both in the quest log and is complete

==Patch changes==
* {{Patch 9.0.1|note=Moved to <code>C_QuestLog.IsComplete()</code>}}
* {{Patch 6.0.2|note=Added as {{api|IsQuestComplete}}()}}
```