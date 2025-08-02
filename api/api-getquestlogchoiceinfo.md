# API GetQuestLogChoiceInfo

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns a bunch of data about a quest reward choice from the quest log.
 itemName, itemTexture, quantity, quality, isUsable, itemID = GetQuestLogChoiceInfo(index [, questID])

==Arguments==
:;index:{{apitype|number}} - Index of a quest reward choice (between 1 and {{api|GetNumQuestLogChoices}})
:;questID:{{apitype|number?}}

==Returns==
:;itemName:{{apitype|string}} - The name of the quest item
:;itemTexture:{{apitype|fileID}} - The texture of the quest item
:;quantity:{{apitype|number}} - How many of the quest item
:;quality:{{apitype|Enum.ItemQuality}} - Quality of the quest item
:;isUsable:{{apitype|boolean}} - If the quest item is usable by the current player
:;itemID:{{apitype|number}}
```