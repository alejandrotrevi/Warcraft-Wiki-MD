# API GetContainerItemID

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns the item ID in a container slot.
 itemId = GetContainerItemID(bag, slot)

==Arguments==
:;bag:{{apitype|number}} ([[BagID]]) - Index of the bag to query.
:;slot:{{apitype|number}} - Index of the slot within the bag to query; ascending from 1.

==Returns==
:;itemId:{{apitype|number}} - item ID of the item held in the container slot, nil if there is no item in the container slot.
```