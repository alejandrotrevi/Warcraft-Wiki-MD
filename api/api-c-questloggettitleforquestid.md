# API C QuestLog.GetTitleForQuestID

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_QuestLog|system=QuestLog}}
Returns the name for a Quest ID.
 title = C_QuestLog.GetTitleForQuestID(questID)

==Arguments==
:;questID:{{apitype|number}}

==Returns==
:;title:{{apitype|string?}}

==Details==
* This API does not require the quest to be in your quest log.
* Only returns a valid title for quests, header titles cannot be discovered using this.
* Data might not be readily available from the server, query this asynchronously with {{api|C_QuestLog.RequestLoadQuestByID}}() and {{api|t=e|QUEST_DATA_LOAD_RESULT}}

==Example==
Queries the quest name with [https://www.townlong-yak.com/framexml/9.0.2/ObjectAPI/AsyncCallbackSystem.lua#17 QuestEventListener]
<syntaxhighlight lang="lua">
local questID = 29950 -- Li Li's Day Off

QuestEventListener:AddCallback(questID, function()
	local name = C_QuestLog.GetTitleForQuestID(questID)
	print(name)
end)
</syntaxhighlight>

==Patch changes==
* {{Patch 9.0.1|note=Moved to <code>C_QuestLog.GetTitleForQuestID()</code>}}
* {{Patch 8.0.1|note=Added as {{api|C_QuestLog.GetQuestInfo}}()}}

==See also==
* {{api|HaveQuestData}}()
```