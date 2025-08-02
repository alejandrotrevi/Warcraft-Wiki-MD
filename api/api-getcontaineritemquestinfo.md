# API GetContainerItemQuestInfo

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns info for a quest item in a container slot.
 isQuestItem, questId, isActive = GetContainerItemQuestInfo(bag, slot)

==Arguments==
:;bag:{{apitype|number}} ([[BagID]]) - Index of the bag to query.
:;slot:{{apitype|number}} - Index of the slot within the bag (ascending from 1) to query.

==Returns==
:;isQuestItem:{{apitype|boolean}} - true if the item is a quest item, nil otherwise.
:;questId:{{apitype|number}} - Quest ID of the quest this item starts, no value if it does not start a quest.
:;isActive:{{apitype|boolean}} - 1 if the quest this item starts has been accepted by the player, nil otherwise.

==History==
* Added in [[Patch 3.3.3]].
```