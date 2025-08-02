# API C QuestLog.IsQuestTask

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_QuestLog|system=QuestLog}}
Returns whether a given quest is a task (also known as bonus objectives or world quest).
 isTask = C_QuestLog.IsQuestTask(questID)

==Arguments==
:;questID:{{apitype|number}}

==Returns==
:;isTask:{{apitype|boolean}}

==Details==
* [[QuestID]]s for tasks are unusable in all functions that take a QuestID until the player receives that quest in their log.  This function returns false for known tasks, if the task has not been encountered this session.  Logging out of the character makes the QuestID unusable again.

==Patch changes==
* {{Patch 9.0.1|note=Moved to <code>C_QuestLog.IsQuestTask()</code>}}
* {{Patch 6.0.2|note=Added as <code>IsQuestTask()</code>}}
```