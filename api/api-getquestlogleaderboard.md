# API GetQuestLogLeaderBoard

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns info for a quest objective in the quest log.
 description, objectiveType, isCompleted = GetQuestLogLeaderBoard(objIndex [, questIndex])

==Arguments==
:;objIndex:{{apitype|number}} - Index of the quest objective to query, ascending from 1 to {{api|GetNumQuestLeaderBoards}}(questIndex).
:;questIndex:{{apitype|number?}} - Index of the quest log entry to query, ascending from 1 to {{api|GetNumQuestLogEntries}}. If not provided or invalid, defaults to the currently selected quest (via {{api|SelectQuestLogEntry}})

==Returns==
:;description:{{apitype|string}} - Text description of the objective, e.g. "0/3 Monsters slain"
:;objectiveType:{{apitype|string}} - A token describing objective type, one of "item", "object", "monster", "reputation", "log", "event", "player", or "progressbar".
:;isCompleted:{{apitype|boolean}} - true if sub-objective is completed, false otherwise

==Example==
The following function attempts to parse the description message to figure out exact progress towards the objective:
 function GetLeaderBoardDetails (boardIndex,questIndex)
   local description, objectiveType, isCompleted = GetQuestLogLeaderBoard (boardIndex,questIndex);
   local itemName, numItems, numNeeded = description:match("(.*):%s*([%d]+)%s*/%s*([%d]+)");
   return objectiveType, itemName, numItems, numNeeded, isCompleted;
 end -- returns eg. "monster", "Young Nightsaber slain", 1, 7, nil

==Details==
* The type "player" was added in WotLK, which is used by [[No Mercy!]] and probably other quests.
* The type "log" was added sometime around patch 3.3.0, and seems to have replaced many instances of "event".
* Only ever found one quest, [[The Thandol Span (3)]] that had an "object" objective.
* The <code>description</code> return value can be incomplete under some circumstances, with localized item or NPC names missing from the text.

==See also==
* {{api|GetQuestObjectiveInfo}} - A function with identical returns, but takes a [[QuestID]] argument instead of QuestLogIndex.
```