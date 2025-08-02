# API C TaskQuest.GetQuestInfoByQuestID

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_TaskQuest|system=QuestTaskInfo}}
Needs summary.
 questTitle, factionID, capped, displayAsObjective = C_TaskQuest.GetQuestInfoByQuestID(questID)

==Arguments==
:;questID:{{apitype|number}}

==Returns==
:;questTitle:{{apitype|string}}
:;factionID:{{apitype|number?}} : [[FactionID]]
:;capped:{{apitype|boolean?}}
:;displayAsObjective:{{apitype|boolean?}}

==Patch changes==
* {{Patch 8.3.0|note=Added <code>displayAsObjective</code> return.}}
* {{Patch 7.0.3|note=Added.}}
```