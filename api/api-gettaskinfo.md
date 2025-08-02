# API GetTaskInfo

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns information about a [[Quest#Bonus_Objectives|bonus objective]].
 isInArea, isOnMap, numObjectives = GetTaskInfo(questID)

==Arguments==
:;questID:{{apitype|number}} - Unique identifier for the quest.

==Returns==
''All returns are nil if [[API IsQuestTask|IsQuestTask()]] returns false for the quest.''
:;isInArea:{{apitype|boolean}} - True if player is in the location where the task activates.
:;isOnMap:{{apitype|boolean}} - True if task is active and visible on the player's map.
:;numObjectives:{{apitype|number}} - Number of objectives for the task.

==Details==
The bonus objectives system allows players to progress quests that are activated based on location, rather than a quest-giving NPC.  While these player is in the appropriate area and these quests are active, they are invisible entries the quest log. After the player leaves the area, the quest is removed from the quest log and thus has no longer has a usable quest index.  Bonus objectives (known in the API as "tasks") have a quest ID and information about them can be queried by all functions that accept a quest ID.

Until the player enters the task area for the first time per session, all tasks return false with <code>IsQuestTask()</code> (and thus return nil values with <code>GetTaskInfo()</code>).  Quest IDs for tasks will become unusable again if the player logs out.

==See also==
* {{api|GetQuestObjectiveInfo}}
* [[QUESTTASK_UPDATE]]

==Patch changes==
* {{Patch 6.0.2|note=Added.}}
```