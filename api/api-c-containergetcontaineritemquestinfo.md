# API C Container.GetContainerItemQuestInfo

**Contributor:** Gsnerf

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_Container|system=Container}}
Needs summary.
 questInfo = C_Container.GetContainerItemQuestInfo(containerIndex, slotIndex)

==Arguments==
:;containerIndex:{{apitype|number}} ([[BagID]]) - Index of the bag to query.
:;slotIndex:{{apitype|number}} - Index of the slot within the bag (ascending from 1) to query.

==Returns==
:;questInfo:{{apitype|ItemQuestInfo}}
{| class="sortable darktable zebra" style="margin-left: 3.9em"
! Field !! Type !! Description
|-
| isQuestItem || {{apitype|boolean}} || <code>true</code> if the item is a quest item, <code>nil</code> otherwise. Items starting quests are apparently not considered to be quest items.
|-
| questID || {{apitype|number?}} ||Quest ID of the quest this item starts, no value if it does not start a quest or if the call refers to a bank bag/slot when the bank is not being visited.
|-
| isActive || {{apitype|boolean}} || <code>true</code> if the quest this item starts has been accepted by the player, <code>false</code> otherwise
|}
```