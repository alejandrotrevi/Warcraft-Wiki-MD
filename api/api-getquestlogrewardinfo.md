# API GetQuestLogRewardInfo

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|Quest}}
Returns info for an unconditional quest reward item in the quest log.
 itemName, itemTexture, numItems, quality, isUsable, itemID, itemLevel = GetQuestLogRewardInfo(itemIndex[, questID])

==Arguments==
:;itemIndex:{{apitype|number}} - Index of the item reward to query, up to [[API_GetNumQuestLogRewards|GetNumQuestLogRewards]]
:;[[questID]]:{{apitype|number?}} - Unique identifier for a quest.

==Returns==
:;itemName:{{apitype|string}} - The name of the quest item
:;itemTexture:{{apitype|string}}  - The texture of the quest item
:;numItems:{{apitype|number}}  - How many of the quest item
:;quality:{{apitype|number}} - Quality of the quest item
:;isUsable:{{apitype|boolean}} - If the quest item is usable by the current player
:;itemID:{{apitype|number}} - Unique identifier for the item
:;itemLevel:{{apitype|number}} - Scaled item level of the reward, based on the character's item level

==Description==

*This function is used for quest reward items that are rewarded unconditionally (mandatory) upon completion of a quest.  For information about reward items a player can choose from, use [[API_GetQuestLogChoiceInfo|GetQuestLogChoiceInfo]] instead.
*This function appears to get info for the currently viewed quest completion dialog if called without a questID. Otherwise, it returns information about the supplied questID.
```