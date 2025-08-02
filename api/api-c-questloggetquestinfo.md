# API C QuestLog.GetQuestInfo

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_QuestLog|system=QuestLog}}
Returns the name for a Quest ID.
 title = C_QuestLog.GetQuestInfo(questID)

==Arguments==
:;questID:{{apitype|number}}

==Returns==
:;title:{{apitype|string}} - name of the quest

==Details==
* This API does not require the quest to be in your quest log.
* If the name is still an empty string (after having queried it from the server once) then the quest is assumed to have been removed.

==Patch changes==
* {{Patch 9.0.1|note=Changed to <code>C_QuestLog.GetTitleForQuestID()</code>}}
* {{Patch 8.0.1|note=Added as <code>C_QuestLog.GetQuestInfo()</code>}}

==See also==
* [[API_C_QuestLog.GetTitleForQuestID#Example|QuestEventListener]]
```