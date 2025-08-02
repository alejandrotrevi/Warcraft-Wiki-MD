# API C QuestLog.SetSelectedQuest

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_QuestLog|system=QuestLog}}
Selects a quest in the quest log.
 C_QuestLog.SetSelectedQuest(questID)

==Arguments==
:;questID:{{apitype|number}}

==Details==
* This function is called whenever the user clicks on a quest name in the quest log.
* It is necessary to call this function to allow other API functions that do not take a questIndex argument to return information about specific quests.

==Patch changes==
* {{Patch 9.0.1|note=Moved to <code>C_QuestLog.SetSelectedQuest()</code>}}
* {{Patch 1.0.0|note=Added as {{api|SelectQuestLogEntry}}()}}
```