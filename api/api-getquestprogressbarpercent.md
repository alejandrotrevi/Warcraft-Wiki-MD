# API GetQuestProgressBarPercent

**Contributor:** Rowaasr13

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns a quest's objective completion percentage.
 percent = GetQuestProgressBarPercent(questID)

==Arguments==
:;questID:{{apitype|number}} - [[QuestID]]

==Returns==
:;percent:{{apitype|number}} - Percentage of quest progress towards completion, from 0 to 100.

==Details==
Used for quest that can be progressed in a variety of ways. These quests have a progress bar for one of objectives and killing monsters, interacting with objects, using special abilities, etc. can all advance the quest towards completion. Such quests will have objectiveType "progressbar" returned from [[API_GetQuestObjectiveInfo|GetQuestObjectiveInfo]] for that one of the objectives.

==Example quests==
*[[We'll Make an Aspirant Out of You]] (more than one objective)
*[[The Netherstar]] (one-time quest)
*[[Patterns Within Patterns]] (weekly)
*[[Trashing the Camp]] (world quest)
```