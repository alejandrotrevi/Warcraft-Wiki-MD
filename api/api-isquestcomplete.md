# API IsQuestComplete

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns whether the supplied quest in the quest log is complete.
 isComplete = IsQuestComplete(questID)

==Arguments==
:;questID:{{apitype|number}} - The ID of the quest.

==Returns==
:;isComplete:{{apitype|boolean}} - true if the quest is both in the quest log and is complete, false otherwise.

==Details==
* This function will only return true if the questID corresponds to a quest in the player's log.  If the player has already completed the quest, this will return false.
* This can return true even when the "isComplete" return of {{api|GetQuestLogTitle}} returns false, if the quest in question has no objectives to complete.

==See also==
* {{api|GetQuestLogTitle}}
* {{api|IsQuestFlaggedCompleted}}
```