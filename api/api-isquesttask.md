# API IsQuestTask

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns whether a given quest is a task (also known as [[Quest#Bonus_Objectives|bonus objectives]]).
 isTask = IsQuestTask(questID)

== Arguments ==
; questID : Number - Unique identifier of the quest.

==Return values==
; isTask : Boolean - True if the quest is a task.  False if not, or player has not entered task area this login session.

== Details ==
[[QuestID]]s for tasks are unusable in all functions that take a QuestID until the player receives that quest in their log.  This function returns false for known tasks, if the task has not been encountered this session.  Logging out of the character makes the QuestID unusable again.

== Patch changes ==
* {{Patch 6.0.2|note=Added.}}
```