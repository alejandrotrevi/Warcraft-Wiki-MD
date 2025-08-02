# API GetQuestID

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns the ID of the displayed quest at a quest giver.
 questID = GetQuestID()

==Returns==
:;questID:{{apitype|number}} - quest ID of the offered/discussed quest.

==Details==
* Only returns proper (non-zero) values:
:: after {{api|t=e|QUEST_DETAIL}} for offered quests and {{api|t=e|QUEST_PROGRESS}} / {{api|t=e|QUEST_COMPLETE}} for accepted quests.
:: before {{api|t=e|QUEST_FINISHED}}.
* This function is not related to your quest log.
```