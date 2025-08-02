# API C QuestLog.GetDistanceSqToQuest

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_QuestLog|system=QuestLog}}
Returns the distance to a quest.
 distanceSq, onContinent = C_QuestLog.GetDistanceSqToQuest(questID)

==Arguments==
:;questID:{{apitype|number}}

==Returns==
:;distanceSq:{{apitype|number}}
:;onContinent:{{apitype|boolean}}

==Patch changes==
* {{Patch 9.0.1|note=Moved to <code>C_QuestLog.GetDistanceSqToQuest()</code>}}
* {{Patch 7.0.3|note=Added <code>C_TaskQuest.GetDistanceSqToQuest()</code>}}
* {{Patch 4.0.1|note=Added <code>GetDistanceSqToQuest()</code>}}
```