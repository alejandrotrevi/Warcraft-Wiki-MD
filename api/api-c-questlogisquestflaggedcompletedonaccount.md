# API C QuestLog.IsQuestFlaggedCompletedOnAccount

**Contributor:** Hariel

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_QuestLog|system=QuestLog}}
Returns if a quest has been completed by any character on an account.
 isCompletedOnAccount = C_QuestLog.IsQuestFlaggedCompletedOnAccount(questID)

==Arguments==
:;questID:{{apitype|number}}

==Returns==
:;isCompletedOnAccount:{{apitype|boolean}} - Returns true if completed; returns false if not completed or if the questID is invalid.

==Example==
Returns if [https://www.wowhead.com/quest=44285/the-emerald-nightmare-piercing-the-veil The Emerald Nightmare: Piercing the Veil] has been completed by any character on the account.
 /dump C_QuestLog.IsQuestFlaggedCompletedOnAccount(44285)

==Notes==
Will return true if any character on the account has completed the quest, whether the quest is an account-wide quest or not.

==See also==
* {{api|C_QuestLog.IsAccountQuest}}()
* {{api|C_QuestLog.IsQuestFlaggedCompleted}}()
```