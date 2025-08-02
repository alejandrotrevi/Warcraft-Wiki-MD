# API C QuestLog.GetNumQuestLogEntries

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_QuestLog|system=QuestLog}}
Returns the number of entries in the quest log.
 numShownEntries, numQuests = C_QuestLog.GetNumQuestLogEntries()

==Returns==
:;numShownEntries:{{apitype|number}} - Number of entries, including headers and invisible content.
:;numQuests:{{apitype|number}} - Number of actual quests.

==Patch changes==
* {{Patch 9.0.1|note=Moved to <code>C_QuestLog.GetNumQuestLogEntries()</code>}}
* {{Patch 1.0.0|note=Added as {{api|GetNumQuestLogEntries}}()}}
```