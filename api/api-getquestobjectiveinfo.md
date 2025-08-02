# API GetQuestObjectiveInfo

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns information about a quest objective.
 text, objectiveType, finished, fulfilled, required = GetQuestObjectiveInfo(questID, objectiveIndex, displayComplete)

==Arguments==
:;questID:{{apitype|number}} - [[QuestID]]
:;objectiveIndex:{{apitype|number}} - Index of the quest objective to query, ascending from 1 to {{api|GetNumQuestLeaderBoards}}(questIndex) or to numObjectives from {{api|GetTaskInfo}}(questID).
:;displayComplete:{{apitype|boolean}} - Pass 'true' to return as if the objective were complete. You want false generally

==Returns==
:;text:{{apitype|string}} - Text description of the objective, e.g. "0/3 Monsters slain"
:;objectiveType:{{apitype|string}} - A token describing objective type, one of "item", "object", "monster", "reputation", "log", "event", "player" or "progressbar".
:;finished:{{apitype|boolean}} - true if sub-objective is completed, false if incomplete.
:;fulfilled:{{apitype|number}} - quantity of the objectives completed
:;required:{{apitype|number}} - quantity of objectives needed to finish the quest.

==Details==
This function's usage is identical to {{api|GetQuestLogLeaderBoard}}, except it takes a QuestID instead of QuestLogIndex as an argument and returns amount of fulfilled and required items without need to parse objective text manually. Using the quest ID allows for getting information about a quest's objectives even if it's not currently in the player's log.

===Use with Tasks===
This function is useful when querying data for [[Quest#Bonus_Objectives|bonus objectives]].  Bonus objectives (known as Tasks in functions such as {{api|GetTaskInfo}}) are only in the quest log while the player is in the area and they are invisible in the quest log interface.  This function allows keeping track of Bonus objectives even when they are not in the quest log, and thus have no quest log index.

The quest IDs of tasks differ from normal quests.  They will return incorrect values if a task has not been encountered during the character's login session.  This function will begin returning accurate values upon entering the task area.  It's necessary to save quest objective progress to a file if accurate information about partially completed tasks is required before the player re-enters the area.

==Patch changes==
* {{Patch 6.0.2|note=Added.}}
```