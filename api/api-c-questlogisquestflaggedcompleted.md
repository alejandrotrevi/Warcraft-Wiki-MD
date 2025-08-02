# API C QuestLog.IsQuestFlaggedCompleted

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_QuestLog|system=QuestLog}}
Returns if a quest has been completed.
 isCompleted = C_QuestLog.IsQuestFlaggedCompleted(questID)

==Arguments==
:;questID:{{apitype|number}}

==Returns==
:;isCompleted:{{apitype|boolean}} - Returns true if completed; returns false if not completed or if the questID is invalid.

==Example==
Returns if [https://www.wowhead.com/quest=176/wanted-hogger WANTED: "Hogger"] has been completed.
 /dump C_QuestLog.IsQuestFlaggedCompleted(176)

==Patch changes==
* {{Patch 8.2.5|note=Moved to {{api|C_QuestLog.IsQuestFlaggedCompleted}}(). The previous alias is deprecated. [https://www.townlong-yak.com/framexml/8.2.5/Blizzard_Deprecated/Deprecated_8_2_5.lua#52]}}
* {{Patch 6.0.2|note=Now returns a boolean true or false}}
* {{Patch 5.0.4|note=Added as {{api|IsQuestFlaggedCompleted}}()}}

==See also==
* {{api|C_QuestLog.GetAllCompletedQuestIDs}}()
```