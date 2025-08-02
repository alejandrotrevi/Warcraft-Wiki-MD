# API C QuestLog.GetQuestObjectives

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns info for the objectives of a quest.
 objectives = C_QuestLog.GetQuestObjectives(questID)

==Arguments==
:;questID:{{apitype|number}} - Unique [[QuestID]] for the quest to be queried. Requires the quest to be in your quest log.

==Returns==
:;objectives:{{apitype|QuestObjectiveInfo[]}} - can be an empty table for quests without objectives
{| class="sortable darktable zebra" style="margin-left: 3.9em"
! Field !! Type !! Description
|-
| {{apiname|text}} || {{apitype|string}} || The text displayed in the quest log and the quest tracker
|-
| {{apiname|type}} || {{apitype|string}} || "monster", "item", etc.
|-
| {{apiname|finished}} || {{apitype|boolean}} || true if the objective has been completed
|-
| {{apiname|numFulfilled}} || {{apitype|number}} || number of partial objectives fulfilled
|-
| {{apiname|numRequired}} || {{apitype|number}} || number of partial objectives required
|-
| {{apiname|objectiveType}} || {{apitype|QuestObjectiveType?}} || 
|}

==Details==
For example, calling this function for the quest [[Colonel Kurzen (quest)]] returns a table with three subtables (with keys 1, 2, and 3), two with the type "monster" and one with the type "item".


Quests that have been encountered before (i.e. cached) are able to be queried instantly, however if the function is supplied a quest ID of a quest that isn't cached yet, it will not return anything until called again. Sometimes three calls are needed to fully cache everything (such as text).



It returns an empty table for some quests without any objectives, for example [[A Threat Within]].

==Patch changes==
* {{Patch 8.0.1|note=Added.}}
```