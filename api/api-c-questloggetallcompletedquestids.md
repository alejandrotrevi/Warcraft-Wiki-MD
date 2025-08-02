# API C QuestLog.GetAllCompletedQuestIDs

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_QuestLog|system=QuestLog}}
Returns all completed quests for the character.
 quests = C_QuestLog.GetAllCompletedQuestIDs()

==Returns==
:;quests:{{apitype|number[]}} - The sorted quest IDs

==Details==
* A quest appears in the list only after it has been completed and turned in, not while it is in your log.
* Completing certain quests can cause other quests (alternate versions, etc.) to appear completed also.
* Some quests are invisible.  These quests are not offered to players but suddenly become "completed" due to some other in-game occurrence.
* [[Daily quest]]s and [[World quest]]s appear completed only if they have been completed that day.
* [[Pet_Battle_System|Pet Battle]] quests are account-wide and will be returned from this API across all characters. They can be discerned with {{api|GetQuestTagInfo}}() tagID 102.

==Example==
For a fresh toon who only completed the first three starter quests: [[:Warming Up]] ([https://www.wowhead.com/quest=56775/warming-up 56775]), [[:Stand Your Ground]] ([https://www.wowhead.com/quest=58209/stand-your-ground 58209]) and [[:Brace for Impact]] ([https://www.wowhead.com/quest=58208/brace-for-impact 58208])
 /dump C_QuestLog.GetAllCompletedQuestIDs()

<syntaxhighlight lang="lua">
{
	[1] = 56775, -- "Warming Up"
	[2] = 58208, -- "Brace for Impact"
	[3] = 58209, -- "Stand Your Ground"
}
</syntaxhighlight>

Prints completed questIds and their names.
* Quest data might have to be cached first, from after the initial query or with [[API_C_QuestLog.GetTitleForQuestID#Example|QuestEventListener]].
* Some quests returned from this don't seem to exist or have a name.
<syntaxhighlight lang="lua">
for _, id in pairs(C_QuestLog.GetAllCompletedQuestIDs()) do
	local name = C_QuestLog.GetTitleForQuestID(id)
	print(id, name)
end
</syntaxhighlight>

==Patch changes==
* {{Patch 9.0.1|note=Moved to <code>C_QuestLog.GetAllCompletedQuestIDs()</code> and returns quest IDs in a sorted array (<code>{ QuestID1, QuestID2, ... }</code>)}}
* {{Patch 3.3.0|note=Added as {{api|GetQuestsCompleted}}()}}
```